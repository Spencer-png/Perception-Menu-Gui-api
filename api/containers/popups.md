# Popups & Menus

```lua
imgui.OpenPopup(id)
if imgui.BeginPopup(id) then
  -- draw popup content
  imgui.EndPopup()
end
imgui.CloseCurrentPopup() -- closes topmost popup
```
- Popup position anchors to current mouse position when opened.
- Click outside to close.

Implementation detail: a render proxy captures drawing calls inside the popup and replays them after the frame to keep z-ordering consistent. 