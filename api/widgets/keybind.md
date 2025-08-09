# Keybind

```lua
local kb = imgui.Keybind(label, default_key?, default_mode?)
kb:get_key() -> keycode
kb:set_key(k)
kb:get_mode() -> mode
kb:set_mode(mode)
kb:is_active() -> bool
```
- Click the box to capture a key (ESC clears).
- Right-click the box to open a mode popup.

Modes (`imgui.key_mode`):
1. `onhotkey` – active while key is held
2. `offhotkey` – active while key is NOT held
3. `toggle` – toggles on key press
4. `singlepress` – active on the press frame
5. `always_on` – always active

Display uses `imgui._get_key_name(keycode)`. 