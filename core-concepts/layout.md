# Layout

## Flow
Widgets advance a cursor; the library computes positions with padding and spacing.

- `imgui.SameLine(spacing?)`: place next widget on the same line
- `imgui.Indent(width?)` / `imgui.Unindent(width?)`: increase/decrease left offset
- `imgui.Spacing(h?)`: vertical gap
- `imgui.Separator()`: thin horizontal line

`imgui.NextWidget(w, h)` is an internal helper used by widgets; you generally won’t call it directly. 