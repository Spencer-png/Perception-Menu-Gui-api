# Button

```lua
local pressed = imgui.Button(label, size?)
```
- `label`: string
- `size`: `{w, h}`; use `{0, h}` or omit for auto width
- Returns `true` on the frame it’s clicked

Example:
```lua
if imgui.Button('Save', {120, 28}) then
  save()
end
``` 