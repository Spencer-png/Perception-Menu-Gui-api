# Input Text

Two variants: `InputText` (simple) and `InputTextEx` (selection/drag selection).

## InputText
```lua
local it = imgui.InputText(label, default)
it:get() -> string
it:set(str)
it:set_active(bool)
```
- Supports typing, caret, copy/cut/paste, undo/redo, word-nav with Ctrl.

## InputTextEx
```lua
local it = imgui.InputTextEx(label, default)
```
- Adds mouse-drag selection and precise caret placement.

Common shortcuts:
- Ctrl+A/C/X/V, Ctrl+Z/Y
- Ctrl+Backspace/Delete to delete words
- Home/End, Shift+arrows for selection 