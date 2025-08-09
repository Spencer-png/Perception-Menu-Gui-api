# Selectors

## SingleSelect
```lua
local s = imgui.SingleSelect(label, items, default_index)
s:get() -> index
s:set(index)
```
Opens a popup with choices.

## MultiSelect
```lua
local m = imgui.MultiSelect(label, items, default_selected)
m:get(i) -> bool
m:set(i, bool)
```
Shows a comma-joined preview; opens a popup of checkboxes.

## InputListSingle
Scrollable list with radio behavior.
```lua
local s = imgui.InputListSingle(label, items, default_index, height?)
```

## InputListMulti
Scrollable list with checkboxes.
```lua
local m = imgui.InputListMulti(label, items, default_selected, height?)
``` 