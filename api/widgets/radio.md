# Radio Buttons

```lua
local clicked = imgui.RadioButton(label, is_active)
```
- Returns `true` when clicked; you manage the grouping/state.

Example:
```lua
local current = 1
if imgui.RadioButton('A', current == 1) then current = 1 end
imgui.SameLine(10)
if imgui.RadioButton('B', current == 2) then current = 2 end
``` 