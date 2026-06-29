# Active Workspace Indicator

Adds a visible indicator around the currently active workspace button in Zen's sidebar, so you always know at a glance which workspace you're in.

## Options

| Setting | Description | Default |
|---|---|---|
| **Indicator style** | `Outline` / `Border` / `Background tint` / `Glow` | Outline |
| **Indicator color** | Any valid CSS color (`#fff`, `oklch(…)`, `cornflowerblue`, etc.) | `currentColor` (follows your workspace theme) |
| **Opacity** | A CSS percentage controlling indicator intensity | `100%` |
| **Corner radius** | Border radius of the indicator | `6px` |

## Style guide

- **Outline** — drawn *outside* the element box, so it never shifts the sidebar layout. Fully opaque by default.
- **Border** — drawn *inside* the element box with `box-sizing: border-box` to prevent size shifts. Similar to outline but renders slightly inward.
- **Background tint** — fills behind the workspace icon. Works best with a low opacity (20–30%); 100% gives a fully solid fill.
- **Glow** — a soft `box-shadow` emanating outward. Does not affect layout.

## Notes

- `currentColor` as the color value automatically follows whichever color your active workspace theme sets.
- The opacity preference uses `color-mix()` to blend the indicator color toward transparent, so the workspace icon itself is never affected.
- Outline and Glow are the most layout-safe choices on compact sidebars.
