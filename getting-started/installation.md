# Installation

## 1) Load the module
```lua
local imgui = require('imgui')
```

## 2) Fonts
The library creates a default font via:
```lua
imgui.font = render.create_font('verdana.ttf', 15)
```
Adjust as needed:
```lua
imgui.font = render.create_font('Smallest Pixel.ttf', 16)
```

## 3) Environment prerequisites
- `render`: draw_text, draw_rectangle, draw_circle, draw_triangle, draw_bitmap, measure_text, clip_start, clip_end
- `input`: get_mouse_position, is_key_down, get_scroll_delta, get_clipboard, set_clipboard
- Optional: `time.unix_ms()` or `winapi.get_tickcount64()` for caret blink

## 4) First run
Render at least one frame per tick:
```lua
imgui.BeginFrame()
if imgui.BeginWindow('hello', 'Hello', 100, 100, 300, 200) then
  imgui.Text('It works!')
end
imgui.EndWindow()
imgui.EndFrame()

``` 

