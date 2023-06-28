![wellum-description-english](./images/wellum-description-english.jpg)

# Wellum — 36-keys callum-styled keyboard layout

## Details
- Hold <kbd>SYM</kbd> to activate the symbols layer.
- Hold <kbd>NAV</kbd> to activate the navigation layer.
- Hold <kbd>SYM</kbd> and <kbd>NAV</kbd> together to activate the numbers layer.

## Terms
- Modifiers: <kbd>Shift</kbd>, <kbd>Ctrl</kbd>, <kbd>Alt</kbd> or <kbd>Gui</kbd>
- Layer keys: <kbd>SYM</kbd> or <kbd>NAV</kbd>

## How One-shot Sticky Modifiers work

When you hold layer key, modifiers will be added to a queue and remain pressed until some non-modifier key or layer key is pressed.

For example, to press the Windows <kbd>Gui</kbd> key without any combinations, you need to:
- hold down the layer key
- press the <kbd>Gui</kbd> modifier
- release the layer key and press it again.

And if you need, for example, to press the Ctrl+Shift+T combination, you have several options:

1. The first one:
    - Hold down the <kbd>SYM</kbd> layer key.
    - Type the <kbd>K (Ctrl)</kbd> and <kbd>J (Shift)</kbd> modifiers in any sequence.
    - Release the <kbd>SYM</kbd> layer key.
    - Type <kbd>T</kbd>.
2. The second one:
    - Hold down the <kbd>NAV</kbd> layer key.
    - Type the <kbd>D (Ctrl)</kbd> and <kbd>F (Shift)</kbd> modifiers in any sequence.
    - Release the <kbd>NAV</kbd> layer key.
    - Type <kbd>T</kbd>.

As soon as the T key is pressed, the queue of modifiers will be activated, cleared, and the <kbd>Ctrl+Shift+T</kbd> combination will be entered.

Moreover, if you hold down the modifier keys but release the layer key, the modifiers will remain held down, allowing you to use them in combinations with keys from the other half of the keyboard.

## How Swapper and Tabber work

The Swapper key <kbd>NAV+W</kbd> and the Tabber key <kbd>NAV+Q</kbd> are macros for <kbd>Alt+Tab</kbd> and <kbd>Ctrl+Tab</kbd>, respectively. When pressed, they leave the Alt or Ctrl modifiers held down. 
Thus, by pressing <kbd>W</kbd> and <kbd>Q</kbd> again, you can switch between windows in Windows, tabs in a Web Browser, or Terminal.

// TODO: not implemented
These keys are compatible with the <kbd>Shift</kbd> modifier, which allows you to reverse the direction of window/tab switching.