# How to Adapt the Layout for My Keyboard?

The instruction is given for QMK / Vial firmware.

In this instruction, the [Corne](https://github.com/foostan/crkbd) is taken as an example.

First, we need a QMK/Vial repository with ready-made settings for your keyboard. In our example, we clone the [qmk](https://github.com/qmk/qmk_firmware) repository.

The layout itself is in `keyboards/crkbd/keymaps`. We take the one called `default` as a basis. Simply duplicate this folder and work in it. The layout consists of several files, the main one being `keymap.c`. Our task is to adapt this standard layout to Wellum. Specifically, we need to change the number, names, and composition of layers, add connections to files with additional functions, etc.

Layer names by default are declared in some header file, but each custom layout usually uses its own names. Therefore, we copy the block with `enum layers { ... }` into the `keymap.c` file.

Next, custom keycodes (custom names for key combinations): they are also declared somewhere by default, so we can move them to `keymap.c` if we want to use them. Also, we transfer these custom codes from the firmware (they go before the declaration `enum layers { ... }`).

**Important**: they must go before the definition of the layer contents `const uint16_t PROGMEM keymaps[][MATRIX_ROWS][MATRIX_COLS] = { ... }`

We copy the contents of this section from the Wellum layout, there will be seven sections (`_DEF, _GAM, _GFN, _SYM, _NAV, _NUM _CMD`). The problem is that they are oriented towards a 36-key layout, but ours may (and most likely will) be different. For example, Corne has 42 keys.

We need to observe the dimensions and put `KC_NO` in the missing keys — empty key. For example, for Corne, you may need to adjust the layout to match the 42-key matrix.

The remaining firmware code (after the `keymaps` section) we just insert after this section. Then there is OLED code that displays the name of the active layer. It needs to be adjusted to our new layer names (`_DEF, _GAM, ...`).

We've finished with the layout, now we need to connect additional functionality (`oneshot.c/h`, `swapper.c/h`). Simply copy these files from the Wellum layout repository and create `rules.mk` with this content:

```c
SRC += ./oneshot.c
SRC += ./swapper.c
```

And that's it, you can build. For this, Docker is needed.

In the root of the repository, call `util/docker_build.sh crkbd:wellum`. The format is like this: `<keyboard folder>:<layout folder>`. Docker will pull all necessary dependencies and try to build the firmware. If there are errors, they will be output to the console. For example, I had an error with the missing file. It lies in some user folder, but the build command for some reason doesn't pick it up. Here you need to check the build instructions for your keyboard... But I just ignored this file, commented out its import in `keymap.c`.

After a successful build, a firmware file will appear in the `.build` folder — `crkbd_wellum.uf2`. We flash it onto both halves and rejoice?
