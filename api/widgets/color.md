# Color

## ColorPicker
```lua
local cp = imgui.ColorPicker(label, {r, g, b, a})
cp:get() -> r, g, b, a
cp:set(r, g, b, a)
```
- Click preview to open popup with SV square, hue bar, alpha bar, hex display, copy/paste.

## CheckboxWithColorPicker
```lua
local w = imgui.CheckboxWithColorPicker(label, default_checked, {r, g, b, a})
w:get_checked() -> bool
w:set_checked(bool)
w:get_color() -> r, g, b, a
w:set_color(r, g, b, a)
```
- Shows color preview only when the checkbox is enabled. Clicking preview opens the same color popup. 