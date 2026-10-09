# WhatsApp web (click-to-chat page): design tokens

Pulled from the compiled CSS on api.whatsapp.com/send on 2026-10-09. Class names are hashed, so these are usage counts and not official token names.

## Color
| Role | Value |
|---|---|
| Brand green (accent, hover, underline) | `#25d366` |
| Primary button bg | `#43cd66` |
| Text on green button | `#103928` |
| Primary text / dark ink | `#111b21` |
| Secondary dark text | `#1c1e21` |
| Muted text | `#5e5e5e`, `#606770` |
| Borders / dividers | `#cdd0d5`, `#c4d0d4`, `#dadde1`, `#ebedf0` |
| Light surface | `#f0f4f9`, `#f8f9fa` |
| Background | `#fff` |
| Legacy teal | `#128c7e`, `#075e54` |
| Link blue | `#027eb5` |

```css
:root {
  --green: #25d366;
  --button: #43cd66;
  --on-button: #103928;
  --ink: #111b21;
  --ink-2: #1c1e21;
  --muted: #5e5e5e;
  --border: #cdd0d5;
  --surface: #f0f4f9;
  --bg: #fff;
  --link: #027eb5;
}
```

## Type
- Family: `"WhatsApp Sans Var", sans-serif` (proprietary; Helvetica/Arial fallback)
- Sizes (px): 12 · 13 · 14 · **16 (body)** · 18 · 24 · 28 · 32 · 40 · 48
- Weights: 400 body · **500 UI (most used)** · 700 headings

## Shape
- Pill buttons: `border-radius: 100px` (also 25px / 50px), `min-height: 34px`, `padding: 5px 15px`, `gap: 8px`
- Cards: radius 24–32px; small controls 4–8px; avatars 50%

## Elevation
- `0 10px 50px #0000000d` (soft card)
- `0 10px 30px #0003, 0 4px 6px #0000001a` (raised)

## Breakpoints
`767px` (mobile) · `768–1095px` (tablet) · `1096px+` (desktop)
