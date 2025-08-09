# Checkbox

```lua
local cb = imgui.Checkbox(label, default?)
cb:get() -> bool
cb:set(bool)
cb:set_active(bool)
```
- Uses internal state by ID. Call `:get()` each frame to read current value.

Example:
```lua
local show = imgui.Checkbox('Show overlay', true)
if show:get() then
  -- draw overlay
end
``` 