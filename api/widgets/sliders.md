# Sliders

## Integer
```lua
local s = imgui.SliderInt(label, min, max, default)
s:get() -> int
s:set(int)
```
- Drag or click the bar to change value.

## Float
```lua
local s = imgui.SliderFloat(label, min, max, default)
s:get() -> number
s:set(number)
```
- Displays two decimal places.

Example:
```lua
local speed = imgui.SliderInt('Speed', 0, 100, 50)
local opacity = imgui.SliderFloat('Opacity', 0.0, 1.0, 0.75)
``` 