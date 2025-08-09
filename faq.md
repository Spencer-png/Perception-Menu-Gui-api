# FAQ

## Nothing draws
- Ensure you call `imgui.BeginFrame()` before any UI and `imgui.EndFrame()` after
- Verify your host provides the required `render` and `input` functions

## Text caret not blinking
- Provide `time.unix_ms()` or `winapi.get_tickcount64()` for timing

## My popup is behind other content
- Always draw popups via `BeginPopup/EndPopup` and avoid manual layering

## Why do some labels start with `##`?
- `##` hides the text but keeps it as a unique ID suffix, useful for paired controls like color previews

## How do I persist values?
- The library already persists in `widget_states` by widget ID. To save externally, read values and write your own config. 