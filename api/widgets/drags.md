# Drag Controls

Horizontal mouse drag to adjust numeric values.

## DragInt
```lua
local v = imgui.DragInt(label, default, speed?, min?, max?) -- returns int
```
- Click in the box and drag horizontally. `speed` defaults ~0.1.

## DragFloat
```lua
local v = imgui.DragFloat(label, default, speed?, min?, max?, decimals?) -- returns number
```
- `decimals` is for display only.

Example:
```lua
local max_players = imgui.DragInt('Max Players', 16, 0.2, 1, 64)
local fov = imgui.DragFloat('FOV', 90.0, 0.05, 30.0, 179.0, 1)
``` 