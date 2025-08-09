# Styling & Theming

Customize through `imgui.style`:

## Metrics
- `WindowPadding = {x, y}`
- `FramePadding = {x, y}`
- `ItemSpacing = {x, y}`
- `ItemInnerSpacing = {x, y}`
- `WindowRounding`, `FrameRounding`, `ChildRounding`

## Colors (RGBA)
- `window_bg`, `window_title_bg`, `window_border`
- `child_bg`, `panel_bg`
- `widget_bg`, `widget_hot`, `widget_active`
- `text`, `text_disabled`
- `button_bg`, `button_hot`, `button_active`
- `slider_bg`, `slider_fill`
- `checkbox_bg`, `checkbox_tick`, `radio_off`, `radio_on`
- `input_bg`
- `menu_bg`, `menu_hot`
- `separator`
- `tab_bg`, `tab_active`, `tab_hot`

## Live editing
Use `imgui.StyleDemoWindow()` to tweak values at runtime.

Example:
```lua
imgui.style.WindowRounding = 8
imgui.style.text = {255, 255, 255, 255}
``` 