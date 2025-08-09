# Quickstart

## Minimal window
```lua
imgui.BeginFrame()
if imgui.BeginWindow('main', 'My Menu', 100, 100, 600, 400) then
  imgui.Text('Welcome!')
  if imgui.Button('Click Me', {0, 28}) then
    -- handle click
  end
end
imgui.EndWindow()
imgui.EndFrame()
```

## Child regions and layout
```lua
if imgui.BeginChild('left', 260, 320, true) then
  imgui.Text('Left')
  imgui.Separator()
  imgui.Checkbox('Enable', true)
  imgui.EndChild()
end
imgui.SameLine(10)
if imgui.BeginChild('right', 0, 320, true) then
  imgui.Text('Right')
  imgui.SliderInt('Value', 0, 100, 50)
  imgui.EndChild()
end
```

## Popups
```lua
if imgui.Button('Open Popup', {140, 28}) then
  imgui.OpenPopup('my_popup')
end
if imgui.BeginPopup('my_popup') then
  imgui.Text('Menu')
  imgui.Separator()
  if imgui.Button('Close', {0, 22}) then
    imgui.CloseCurrentPopup()
  end
  imgui.EndPopup()
end
``` 