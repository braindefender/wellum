![wellum-description-russian](./images/wellum-description-russian.jpg)

# Wellum — клавиатурная раскладка для 36 клавиш

[This article is also available in 🇬🇧 English language.](README.md)

![wellum-preview](./images/wellum-preview.jpg)

## Содержание

- [О прошивке](#о-прошивке)
- [Термины](#термины)
- [Клавиатурные слои](#клавиатурные-слои)
  - [Базовый слой](#базовый-слой)
  - [Символы](#символы)
  - [Навигация](#навигация)
  - [Цифры и F-клавиши](#цифры-и-f-клавиши)
  - [Специальные символы](#специальные-символы)
  - [Игровой слой](#игровой-слой)
- Дополнительно
  - [Как работают One-shot Sticky Modifiers](#как-работают-one-shot-sticky-modifiers)
  - [Как работает Swapper и Tabber](#как-работает-swapper-и-tabber)
- [Как установить?](#как-установить)
- [Как сделать LAYOUT\_split\_3x5\_3?](#как-сделать-layout_split_3x5_3)

## О прошивке

Прошивка/раскладка предназначена для использования с [Universal Layout](https://github.com/braindefender/universal-layout) — системной раскладкой для Windows, Linux и macOS. На странице проекта можно найти все необходимые инструкции по установке и модификации этой раскладки.

Прошивка/раскладка основана на [callum](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum) и работает на [QMK](https://docs.qmk.fm/), предназначенном для проводных клавиатур. Версия для беспроводных клавиатур, работающих на [ZMK](https://zmk.dev/docs) находится в разработке.

## Термины

- Модификатор: <kbd>Shift</kbd>, <kbd>Ctrl</kbd>, <kbd>Alt</kbd> или <kbd>Gui</kbd>
- Клавиши слоя: <kbd>SYM</kbd> или <kbd>NAV</kbd>

## Клавиатурные слои

- Удерживайте <kbd>SYM</kbd> чтобы активировать слой символов.
- Удерживайте <kbd>NAV</kbd> чтобы активировать слой навигации.
- Удерживайте <kbd>SYM</kbd> и <kbd>NAV</kbd> вместе, чтобы активировать слой с цифрами.
- Удерживайте <kbd>ALT</kbd> чтобы активировать виртуальный слой спец. символов.

## Базовый слой

![wellum-layer-base](./images/layers/wellum-layer-base.jpg)

> [!NOTE]
> Не волнуйтесь! Буквы `Ё`, `Ъ` и `Щ` находятся в [ALT слое](#специальные-символы).

## Символы

![wellum-layer-sym](./images/layers/wellum-layer-sym.jpg)

## Навигация

![wellum-layer-nav](./images/layers/wellum-layer-nav.jpg)

На левой половинке расположены <kbd>Game Layer</kbd>, <kbd>Print Screen</kbd> и различные макросы:

|                Клавиша | Макрос                                                                        |
| ---------------------: | ----------------------------------------------------------------------------- |
|      <kbd>SW TAB</kbd> | [Swapper](#как-работает-swapper-и-tabber) (для окон в Windows/Linux)          |
|      <kbd>SW WIN</kbd> | [Tabber](#как-работает-swapper-и-tabber) (для вкладок в браузере и терминале) |
|    <kbd>PREV TAB</kbd> | <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Tab</kbd>                           |
|    <kbd>NEXT TAB</kbd> | <kbd>Ctrl</kbd> + <kbd>Tab</kbd>                                              |
|  <kbd>SPACE LEFT</kbd> | <kbd>Ctrl</kbd> + <kbd>Gui</kbd> + <kbd>Left</kbd>                            |
| <kbd>SPACE RIGHT</kbd> | <kbd>Ctrl</kbd> + <kbd>Gui</kbd> + <kbd>Right</kbd>                           |

На правой половинке расположены vim-подобные стрелочки, Home/End (сверху) и Page Up/Down (снизу).

Клавиши <kbd>Escape</kbd>, <kbd>Enter</kbd> и <kbd>Tab</kbd> продублированы на обеих половинках, что удобно при в различных программах и редакторах, где только левая рука находится на клавиатуре, а правая держит мышь.

> Так как BIOS или система, на которой не установлена [Universal Layout](https://github.com/braindefender/universal-layout), сопоставляют клавиши и символы стандартным способом, то для совместимости, на слое [NAV](#навигация) расположена клавиша KC_QUOT, на которой обычно расположены одиночная и двойная кавычки. Это может пригодиться для RDP или, например, при правке конфигов в Live-USB режиме Linux.

## Цифры и F-клавиши

![wellum-layer-num](./images/layers/wellum-layer-num.jpg)

## Специальные символы

![wellum-layer-alt](./images/layers/wellum-layer-alt.jpg)

В слой вынесены русские буквы, которые не влезли в 2×15 сетку, а также различные символы, многие из которых расположены мнемонически:

|       Символ | Способ ввода                  |
| -----------: | ----------------------------- |
| <kbd>Ё</kbd> | <kbd>Alt</kbd> + <kbd>Е</kbd> |
| <kbd>Ъ</kbd> | <kbd>Alt</kbd> + <kbd>Ь</kbd> |
| <kbd>Щ</kbd> | <kbd>Alt</kbd> + <kbd>Ш</kbd> |
| <kbd>₽</kbd> | <kbd>Alt</kbd> + <kbd>Р</kbd> |

На месте **пробела** расположен символ **неразрывного пробела**, который заставляет делать перенос текста только вместе с соседними от него словами.

В ALT слое также доступны `<` `>` `«` `»` `[` `]` (доступные для обеих языков) и лигатура `=>`, удобная для разработчиков.

## Игровой слой

![wellum-layer-game](./images/layers/wellum-layer-game.jpg)
![wellum-layer-gfn](./images/layers/wellum-layer-gfn.jpg)

WASD смещён на одну колонку вправо, чтобы вместить <kbd>Tab</kbd>, <kbd>Shift</kbd> и <kbd>Ctrl</kbd> на почти привычных позициях. Для эргономичных клавиатур это также актуально из-за смещения клавиш по вертикали, где клавиша под средний палец находится выше всего.

Также, в слое с цифрами помещается два ряда цифр и часто используемые в играх клавиши:

|      Клавиша | Описание  |
| -----------: | --------- |
| <kbd>G</kbd> | Grenade   |
| <kbd>J</kbd> | Journal   |
| <kbd>I</kbd> | Inventory |
| <kbd>M</kbd> | Map       |
| <kbd>T</kbd> | Chat      |

## Как работают One-shot Sticky Modifiers

При зажатии клавиш слоя, нажатые модификаторы добавляются в очередь и остаются нажатыми, пока не будет нажата клавиша не-модификатор или клавиша слоя.

К примеру, чтобы нажать клавишу Windows <kbd>Gui</kbd> без каких-либо комбинаций, вам нужно:

- зажать клавишу слоя
- нажать модификатор <kbd>Gui</kbd>
- отпустить клавишу слоя и нажать её ещё раз.

А если вам нужно, к примеру, нажать комбинацию Ctrl+Shift+T, то для этого у вас есть несколько вариантов:

1. Первый:
   - Вы зажимаете клавишу слоя <kbd>SYM</kbd>
   - Набираете модификаторы <kbd>K (Ctrl)</kbd> and <kbd>J (Shift)</kbd> в любой последовательности
   - Отпускаете клавишу слоя <kbd>SYM</kbd>
   - Вводите <kbd>T</kbd>
2. Второй:
   - Вы зажимаете клавишу слоя <kbd>NAV</kbd>
   - Набираете модификаторы <kbd>D (Ctrl)</kbd> and <kbd>F (Shift)</kbd> в любой последовательности
   - Отпускаете клавишу слоя <kbd>NAV</kbd>
   - Вводите <kbd>T</kbd>

Как только будет нажата клавиша <kbd>T</kbd>, очередь из модификаторов сработает, очистится и введётся комбинация <kbd>Ctrl+Shift+T</kbd>.

Более того, зажав клавиши-модификаторы, но отпустив клавишу слоя, модификаторы останутся зажатыми, что позволит использовать их в комбинациях клавишами другой половинки.

## Как работает Swapper и Tabber

Клавиши Swapper <kbd>NAV+W</kbd> и Tabber <kbd>NAV+Q</kbd> – это специальные макросы для <kbd>Alt+Tab</kbd> и <kbd>Ctrl+Tab</kbd> соответственно. Однако при нажатии они оставляют зажатыми модификаторы <kbd>Alt</kbd> и <kbd>Ctrl</kbd> соответственно.

Таким образом, повторно нажимая W и Q можно переключаться по окнам в Windows, вкладкам в Веб-браузере или Терминале.

Эти клавиши совместимы с модификатором <kbd>Shift</kbd>, что позволяет инвертировать направление переключения по окнам/вкладкам.

## Как установить?

Здесь всё зависит от вашей клавиатуры. Если вы не знаете с чего начать, то изучите инструкцию о том, [как адаптировать раскладку под свою клавитуру?](./guides/как-адаптировать-раскладку-под-мою-клавиатуру.md)

Для некоторых клавиатур существуют билды прошивки (добавляются пользователями посредством Pull Request'ов). Можете поискать свою клавиатуру в папке `prebuilts`.

Для сборки прошивки понадобится актуальная версия [QMK](https://github.com/qmk/qmk_firmware/).

- Скопировать содержимое папки `firmware` в папку `<ваша_клавиатура>/keymaps/wellum`
- Сделать билд и прошивку стандартной командой сборки/прошивки под вашу клавиатуру, указав вариант `:wellum`.
- Если для вашей клавиатуры не определён `LAYOUT_split_3x5_3` в `info.json` вам нужно сделать его самим. Инструкция ниже.
- Установить [Universal Layout](https://github.com/braindefender/universal-layout) для вашей операционной системы.

## Как сделать LAYOUT_split_3x5_3?

Для сборки, `keymap.c` опирается на `LAYOUT_split_3x5_3`, но для большинства клавиатур он может быть не определён.
Для того, чтобы это исправить нужно продублировать ваш текущий `LAYOUT_split_***_*` и назвать его `LAYOUT_split_3x5_3`.
После этого, надо вычистить оттуда клавиши, не попадающие в новую сетку.
К примеру, для `LAYOUT_split_3x6_3` нужно убрать строки, соответствующие крайним левым и крайним правым столбцам.
Всего, в массиве `layout` должно остаться ровно **36 элементов**.

```jsonc
"LAYOUT_split_3x6_3": {
    "layout": [
        { "matrix": [0, 0], "x": 0, "y": 0.25 },  // крайний левый, удалить
        { "matrix": [0, 1], "x": 1, "y": 0.25 },
        { "matrix": [0, 2], "x": 2, "y": 0.125 },
        { "matrix": [0, 3], "x": 3, "y": 0 },
        { "matrix": [0, 4], "x": 4, "y": 0.125 },
        { "matrix": [0, 5], "x": 5, "y": 0.25 },
        { "matrix": [4, 0], "x": 8, "y": 0.25 },
        { "matrix": [4, 1], "x": 9, "y": 0.125 },
        { "matrix": [4, 2], "x": 10, "y": 0 },
        { "matrix": [4, 3], "x": 11, "y": 0.125 },
        { "matrix": [4, 4], "x": 12, "y": 0.25 },
        { "matrix": [4, 5], "x": 13, "y": 0.25 }, // крайний правый, удалить
        { "matrix": [1, 0], "x": 0, "y": 1.25 },  // крайний левый, удалить
        { "matrix": [1, 1], "x": 1, "y": 1.25 },
        { "matrix": [1, 2], "x": 2, "y": 1.125 },
        { "matrix": [1, 3], "x": 3, "y": 1 },
        { "matrix": [1, 4], "x": 4, "y": 1.125 },
        { "matrix": [1, 5], "x": 5, "y": 1.25 },
        { "matrix": [5, 0], "x": 8, "y": 1.25 },
        { "matrix": [5, 1], "x": 9, "y": 1.125 },
        { "matrix": [5, 2], "x": 10, "y": 1 },
        { "matrix": [5, 3], "x": 11, "y": 1.125 },
        { "matrix": [5, 4], "x": 12, "y": 1.25 },
        { "matrix": [5, 5], "x": 13, "y": 1.25 }, // крайний правый, удалить
        { "matrix": [2, 0], "x": 0, "y": 2.25 },  // крайний левый, удалить
        { "matrix": [2, 1], "x": 1, "y": 2.25 },
        { "matrix": [2, 2], "x": 2, "y": 2.125 },
        { "matrix": [2, 3], "x": 3, "y": 2 },
        { "matrix": [2, 4], "x": 4, "y": 2.125 },
        { "matrix": [2, 5], "x": 5, "y": 2.25 },
        { "matrix": [6, 0], "x": 8, "y": 2.25 },
        { "matrix": [6, 1], "x": 9, "y": 2.125 },
        { "matrix": [6, 2], "x": 10, "y": 2 },
        { "matrix": [6, 3], "x": 11, "y": 2.125 },
        { "matrix": [6, 4], "x": 12, "y": 2.25 },
        { "matrix": [6, 5], "x": 13, "y": 2.25 }, // крайний правый, удалить
        { "matrix": [3, 0], "x": 3.5, "y": 3.25 },
        { "matrix": [3, 1], "x": 4.5, "y": 3.5 },
        { "matrix": [3, 2], "x": 5.5, "y": 3.75 },
        { "matrix": [7, 0], "x": 7.5, "y": 3.75 },
        { "matrix": [7, 1], "x": 8.5, "y": 3.5 },
        { "matrix": [7, 2], "x": 9.5, "y": 3.25 }
    ]
}
```
