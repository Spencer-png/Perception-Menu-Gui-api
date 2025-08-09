# ImGui (Lua) – Menu Library for PerceptionAPI

A lightweight, immediate-mode GUI library implemented in pure Lua, designed for PerceptionAPI environments that provide `render`, `input`, and optional `time`/`winapi` globals.

- **Version**: 2.5.5 (see `imgui._version`)
- **Paradigm**: Immediate-mode UI
- **Runtime**: Lua + PerceptionAPI
- **Key Features**:
  - Windows, child regions, clipping and scrolling
  - Layout utilities: `SameLine`, `Indent`, `Unindent`, `Spacing`, `Separator`
  - Widgets: `Text`, `Button`, `Checkbox`, `RadioButton`, `SliderInt/Float`, `DragInt/Float`, `InputText`/`InputTextEx`
  - Selectors: `SingleSelect`, `MultiSelect`, `InputListSingle/Multi`
  - Color utilities: `ColorPicker`, `CheckboxWithColorPicker`
  - Key handling: `Keybind` (+ five modes)
  - Containers: `BeginPopup/EndPopup`, `OpenPopup`, `BeginTabBar/BeginTabItem/EndTabBar`, `BeginColumns/NextColumn/EndColumns`
  - Theming: `imgui.style` colors, rounding, spacing
  - Built-in demo windows

## What this is not
- Not the C++ Dear ImGui. This is a self-contained Lua reimplementation targeting PerceptionAPI’s drawing/input primitives.

## Requirements
- A host providing:
  - `render.*` (draw_text, draw_rectangle, draw_circle, draw_triangle, draw_bitmap, measure_text, clip_start/clip_end)
  - `input.*` (get_mouse_position, is_key_down, get_scroll_delta, get_clipboard, set_clipboard)
  - Optional: `time.unix_ms()` or `winapi.get_tickcount64()` for blinking carets

## Include
```lua
-- Option A
local imgui = dofile('imgui.lua')

-- Option B (if your environment supports require/package.path)
local imgui = require('imgui')
```

## Frame lifecycle
Always wrap UI each frame:
```lua
imgui.BeginFrame()
if imgui.BeginWindow('main', 'My Menu', 100, 100, 600, 400) then
  imgui.Text('Hello world')
  if imgui.Button('Click Me', {0, 28}) then
    -- handle click
  end
  imgui.EndChild() -- when used
end
imgui.EndWindow()
imgui.EndFrame()
```

## Demos
You can explore features via built-in demos:
```lua
imgui.ProDemoWindow()
imgui.BasicDemoWindow()
imgui.WidgetsDemoWindow()
imgui.PopupsDemoWindow()
imgui.StyleDemoWindow()
```

## Next steps
- Read the Quickstart
- Learn Core Concepts (state/input, windows/child, layout)
- Browse API reference for widgets and containers
- Customize look & feel via Styling & Theming 