# Columns

Simple fixed-width columns with row advance.

```lua
imgui.BeginColumns('cols', 3)
imgui.Text('A1'); imgui.NextColumn(); imgui.Text('B1'); imgui.NextColumn(); imgui.Text('C1')
imgui.NextColumn()
imgui.Text('A2'); imgui.NextColumn(); imgui.Text('B2'); imgui.NextColumn(); imgui.Text('C2')
imgui.EndColumns()
``` 