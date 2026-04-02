# Rollin' Green — Placeholder Page Prompt

Build a single-page maintenance / coming-soon placeholder for Rollin' Green. All copy is English (enUS). Follow the brand system (Deep Green #0F3D2E, Signal Red #E53935, white, modern sans-serif, rounded corners, soft shadows).

---

## Layout Overview

```
┌──────────────────────────────────────────────────────────────┐
│                      TOP BAR  (~100px)                       │
│   [LEFT TEXT]        [   LOGO   ]        [RIGHT TEXT]        │
│                     ↕ logo overflows ↕                       │
├──────────────────────────────────────────────────────────────┤
│                   DUTCHIE EMBED SECTION                      │
└──────────────────────────────────────────────────────────────┘
```

---

## 1 — Top Bar

- **Height:** ~100px, full-width, Deep Green background (#0F3D2E).
- **Three-column layout** (left, center, right), vertically centered.
- No heavy nav, no extra links — keep it clean.

### Center — Logo
- Use `rollingreen-logo-casino-rgb.svg`.
- Logo is **taller than the bar** (~140–160px), centered horizontally.
- It visually "floats" — the bottom of the logo bleeds over the bar's bottom edge into the section below, creating a layered effect.
- `position: relative; z-index: 10` so it sits on top of the boundary.
- No border, no background behind the logo.

### Left — Maintenance Copy
Short, clean, slightly subdued. Suggested copy:

> **We're under maintenance.**
> We'll be back shortly, better than ever.

- White text, small size (13–15px), left-aligned.
- Soft opacity on the subtitle (70–80%) to let it breathe.

### Right — Shop Copy
Warm, inviting, brand-voice forward. Suggested copy:

> **Until then, keep it green.**
> Shop Rollin' Green — where the red carpet is always rolled out for you.

- White text, same scale as left column, right-aligned.
- Optionally highlight "red carpet" in Signal Red (#E53935) for brand punch.

---

## 2 — Dutchie Embed Section

- Sits directly below the top bar, full-width, light background (#F5F5F5 or white).
- Add enough top padding (~80px) to clear the overflowing logo.
- Embed the Dutchie menu widget exactly:

```html
<div>
  <script async="" id="dutchie--embed__script"
    src="https://dutchie.com/api/v2/embedded-menu/68719be58385bb9c85de5f26.js">
  </script>
</div>
```

- No wrapper card, no extra chrome — let the embed fill the section naturally.

---

## Visual & UX Notes

- **Overflow trick:** The logo's `position: relative` + negative or zero bottom margin makes it appear to "bleed" into the embed section. The embed section's top padding compensates so no content is hidden behind it.
- **Depth:** The top bar can have a subtle bottom shadow (`box-shadow: 0 4px 24px rgba(0,0,0,0.18)`) to reinforce the floating logo illusion.
- **No busy backgrounds** — solid Deep Green bar, clean light embed section.
- **Responsive:** On mobile, stack left/right text above and below the logo; logo stays centered and prominent.
- **Font:** Inter or system sans-serif. Tight letter-spacing on headings.
