# State & Input

The library maintains a global state in `imgui._state`.

## State highlights
- `windows`: window registry and per-window positions, sizes, scroll
- `mouse`: x, y, down, pressed, released, scroll
- `keys`: current key states; `keys_pressed`: edge-triggered press
- `hot` / `active`: hot/pressed widget IDs
- `widget_states`: persistent per-widget data (values, open flags, etc.)
- `popup_stack` and `popup_render_queue`
- `tab_bars`, `columns_stack`, `tree_stack`
- `style_stack` (reserved)

## Input update
Each frame, call `imgui.BeginFrame()` (which calls `imgui.UpdateInput()`):
- Polls mouse and keyboard
- Updates `keys_pressed`
- Synchronizes clipboard
- Drives text input subsystem if an `InputText` is active

## Key names and modes
- `imgui._key_names`: lookup for display strings
- `imgui.key_mode`: enum for `Keybind` widget
  - `onhotkey`, `offhotkey`, `toggle`, `singlepress`, `always_on`

## IDs
Widgets derive an ID from the current window + label via `imgui._gen_id`. Use `##suffix` to disambiguate labels that share visible text. 