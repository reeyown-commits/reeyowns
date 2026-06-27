# Rian Joseph Durmiendo — Portfolio Design Tokens

> Professional dark theme with subtle RPG hints. Colors are defined in `src/styles.css` using OKLCH.

---

## Background Colors

| Token | OKLCH | Hex | Notes |
|-------|-------|-----|-------|
| `--background` | `oklch(0.18 0.018 265)` | `#0E121B` | Main page background |
| `--surface` | `oklch(0.225 0.02 265)` | `#161B26` | Cards, panels |
| `--surface-2` | `oklch(0.27 0.024 265)` | `#1E2431` | Elevated surfaces, inputs |
| `--surface-3` | `oklch(0.32 0.028 265)` | `#262D3C` | Progress track, icon backgrounds |

---

## Text Colors

| Token | OKLCH | Hex | Notes |
|-------|-------|-----|-------|
| `--foreground` | `oklch(0.96 0.008 250)` | `#F5F6F7` | Headings, primary text |
| `--muted-foreground` | `oklch(0.68 0.02 260)` | `#9FA3AD` | Body, secondary text |
| `--primary-foreground` | `oklch(0.18 0.018 265)` | `#0E121B` | Text on primary buttons |
| `--destructive-foreground` | `oklch(0.98 0.003 250)` | `#FAFAFB` | Text on destructive buttons |

---

## Accent Colors

| Token | OKLCH | Hex | Notes |
|-------|-------|-----|-------|
| `--primary` | `oklch(0.78 0.13 78)` | `#F3B03A` | Warm gold — main accent |
| `--primary-glow` | `oklch(0.86 0.14 85)` | `#FAD06A` | Lighter gold for gradients/glows |
| `--accent-2` | `oklch(0.78 0.11 175)` | `#3EE6C4` | Emerald/teal — secondary accent |
| `--destructive` | `oklch(0.62 0.22 25)` | `#E9425E` | Errors, warnings |

---

## Border & Utility Colors

| Token | OKLCH | Hex | Notes |
|-------|-------|-----|-------|
| `--border` | `oklch(0.35 0.025 265)` | `#3A4254` | Default borders |
| `--border-strong` | `oklch(0.5 0.04 265)` | `#5E6880` | Stronger borders, outlines |
| `--input` | `oklch(0.32 0.025 265)` | `#262D3C` | Form input backgrounds |
| `--ring` | `var(--primary)` | `#F3B03A` | Focus rings |

---

## Chart Colors

| Token | OKLCH | Hex |
|-------|-------|-----|
| `--chart-1` | `var(--primary)` | `#F3B03A` |
| `--chart-2` | `var(--accent-2)` | `#3EE6C4` |
| `--chart-3` | `oklch(0.65 0.18 30)` | `#E8704E` |
| `--chart-4` | `oklch(0.7 0.15 300)` | `#C98CE6` |
| `--chart-5` | `oklch(0.7 0.15 220)` | `#7AA7F5` |

---

## Typography

| Token | Font | Usage |
|-------|------|-------|
| `--font-display` | Space Grotesk | Headings, hero name, stat labels |
| `--font-sans` | Inter | Body text, paragraphs, buttons |
| `--font-mono` | JetBrains Mono | Code, stats, badges, technical labels |

---

## Gradients

```css
--gradient-primary: linear-gradient(135deg, var(--primary), var(--primary-glow));
--gradient-surface: linear-gradient(180deg, var(--surface), var(--surface-2));
--gradient-radial: radial-gradient(1200px circle at 20% -10%, color-mix(in oklab, var(--primary) 14%, transparent), transparent 60%),
                   radial-gradient(900px circle at 100% 0%, color-mix(in oklab, var(--accent-2) 10%, transparent), transparent 55%);
```

---

## Shadows

```css
--shadow-elegant: 0 20px 50px -20px color-mix(in oklab, var(--primary) 25%, transparent);
--shadow-card: 0 1px 0 0 color-mix(in oklab, var(--foreground) 6%, transparent) inset,
               0 18px 40px -24px rgb(0 0 0 / 0.6);
--shadow-glow: 0 0 0 1px color-mix(in oklab, var(--primary) 40%, transparent),
               0 0 36px -8px color-mix(in oklab, var(--primary) 50%, transparent);
```

---

## Radius

| Token | Value |
|-------|-------|
| `--radius` | `0.5rem` |
| `--radius-sm` | `0.5rem - 4px` |
| `--radius-md` | `0.5rem - 2px` |
| `--radius-lg` | `0.5rem` |
| `--radius-xl` | `0.5rem + 4px` |
| `--radius-2xl` | `0.5rem + 8px` |
| `--radius-3xl` | `0.5rem + 12px` |
| `--radius-4xl` | `0.5rem + 16px` |

---

## Theme File

These tokens are defined in `src/styles.css` and registered as Tailwind utilities via `@theme inline`.

The palette is dark-first by default; there is no separate `.dark` override because the `:root` block itself is already the dark theme.
