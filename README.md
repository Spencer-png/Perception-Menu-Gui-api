# Overview

A lightweight, immediate-mode GUI library implemented in pure Lua, designed for PerceptionAPI environments that provide `render`, `input`, and optional `time`/`winapi` globals.

* **Version**: 2.5.5&#x20;
* **Paradigm**: Immediate-mode UI
* **Runtime**: Lua + Perception Lua API
* **Key Features**:
  * Windows, child regions, clipping and scrolling
  * Layout utilities: `SameLine`, `Indent`, `Unindent`, `Spacing`, `Separator`
  * Widgets: `Text`, `Button`, `Checkbox`, `RadioButton`, `SliderInt/Float`, `DragInt/Float`, `InputText`/`InputTextEx`
  * Selectors: `SingleSelect`, `MultiSelect`, `InputListSingle/Multi`
  * Color utilities: `ColorPicker`, `CheckboxWithColorPicker`
  * Key handling: `Keybind` (+ five modes)
  * Containers: `BeginPopup/EndPopup`, `OpenPopup`, `BeginTabBar/BeginTabItem/EndTabBar`, `BeginColumns/NextColumn/EndColumns`
  * Theming: `imgui.style` colors, rounding, spacing
  * Built-in demo windows

## What this is not

* Not the C++ Dear ImGui. This is a self-contained Lua reimplementation targeting PerceptionAPI’s drawing/input primitives.

## Requirements

* A host providing:
  * `render.*` (draw\_text, draw\_rectangle, draw\_circle, draw\_triangle, draw\_bitmap, measure\_text, clip\_start/clip\_end)
  * `input.*` (get\_mouse\_position, is\_key\_down, get\_scroll\_delta, get\_clipboard, set\_clipboard)
  * Optional: `time.unix_ms()` or `winapi.get_tickcount64()` for blinking carets

## Require

```lua
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

* Read the Quickstart
* Learn Core Concepts (state/input, windows/child, layout)
* Browse API reference for widgets and containers
* Customize look & feel via Styling & Theming
