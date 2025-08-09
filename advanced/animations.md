# Widget Animations

Most interactive widgets keep a small animation state in `imgui._state.widget_anim[id]` with fields like `hot_t` and `active_t`.
- Updated each `BeginFrame()` via `_lerp` toward 0/1
- Used to blend colors (`_lerp_color`) for hover/active feedback

You can read it for custom effects, but the API is internal and may change. 