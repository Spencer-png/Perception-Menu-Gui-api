# Popup Render Proxy

When drawing inside `BeginPopup`/`EndPopup`, the library swaps `_G.render` with a proxy that records calls in `_state.popup_draw_list`. After closing, it replays them via the original renderer.

Why:
- Ensures popups draw on top, regardless of normal draw order
- Avoids deep renderer state juggling inside widgets

Caveats:
- Do not rely on side effects of `render` during capture beyond drawing
- `render.measure_text` is forwarded live to original API for layout 