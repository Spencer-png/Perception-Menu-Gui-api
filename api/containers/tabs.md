# Tabs

## Horizontal tabs
```lua
if imgui.BeginTabBar(id) then
  local activeA = imgui.BeginTabItem('Tab A')
  if activeA then
    -- content for A
    imgui.EndTabItem()
  end
  local activeB = imgui.BeginTabItem('Tab B')
  if activeB then
    imgui.EndTabItem()
  end
  imgui.EndTabBar()
end
```
- Reorder by dragging a tab
- Close button per tab (marks it hidden)

## SideTabBar
Icon-first vertical bar (used in the ProDemo):
```lua
local current = imgui.SideTabBar('side', {
  { bitmap = my_icon, w = 24, h = 24 },
  { bitmap = 'A' }, -- fallback text icon
}, 50)
```
Returns the 1-based active index. 