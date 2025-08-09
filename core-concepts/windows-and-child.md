# Windows & Child Regions

## Windows
```lua
if imgui.BeginWindow(id, title, x, y, w, h) then
  -- content
end
imgui.EndWindow()
```
- Draggable by title bar (first 28px)
- Collapsible via a small +/- button
- Inner content is clipped and vertically scrollable with mouse wheel

Helpers:
- `imgui.get_window_position(id) -> x, y`
- `imgui.is_window_open(id) -> bool`
- `imgui.set_window_open(id, is_open)`

## Child regions
```lua
if imgui.BeginChild(id, w, h, border) then
  -- content
end
imgui.EndChild()
```
- Independent clip rect and vertical scrolling
- Maintains per-child scroll in `imgui._state.child_states[id]` 