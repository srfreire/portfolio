# Design System

> Direction: Luxury — refined, elegant, Apple/Inditex-inspired
> Framework: React (Vite)
> CSS: Tailwind CSS 4
> Created: 2026-04-20
> Last updated: 2026-04-20

## Direction

Premium minimalism inspired by Apple product pages and Inditex's editorial web presence. Typography-driven, extreme whitespace, content reveals through scroll. Depth comes from spacing, not shadows. Color is almost absent — the work speaks for itself.

## Tokens

### Colors

#### Light Mode
| Token | Value | Usage |
|-------|-------|-------|
| `--color-background` | `#FFFFFF` | Page background |
| `--color-surface` | `#F5F2EF` | Alternate section background (warm off-white) |
| `--color-surface-hover` | `#EDEAE6` | Hovered surface |
| `--color-border` | `#E5E1DC` | Borders and dividers |
| `--color-text-primary` | `#1A1A1A` | Primary text |
| `--color-text-secondary` | `#6B7280` | Secondary/muted text |
| `--color-text-tertiary` | `#9CA3AF` | Placeholder, disabled |
| `--color-primary` | `#1A1A1A` | Primary actions, links (same as text — monochrome) |
| `--color-primary-hover` | `#404040` | Hovered primary |
| `--color-accent` | `#8B7355` | Warm bronze accent — subtle, editorial |
| `--color-destructive` | `#DC2626` | Error states |
| `--color-success` | `#16A34A` | Success states |
| `--color-warning` | `#D97706` | Warning states |

### Typography

| Token | Value | Usage |
|-------|-------|-------|
| `--font-sans` | `'Inter', system-ui, sans-serif` | Body text |
| `--font-display` | `'Inter', system-ui, sans-serif` | Headings (same family, different weight) |
| `--text-xs` | `0.75rem` | Labels, captions |
| `--text-sm` | `0.875rem` | Secondary text, tags |
| `--text-base` | `1rem` | Body |
| `--text-lg` | `1.125rem` | Subheadings |
| `--text-xl` | `1.25rem` | Section subtitles |
| `--text-2xl` | `1.5rem` | Section headers |
| `--text-3xl` | `2rem` | Page titles |
| `--text-4xl` | `3rem` | Display (project names) |
| `--text-5xl` | `4.5rem` | Hero name (desktop) |
| `--text-6xl` | `6rem` | Hero name (large desktop) |
| `--leading-tight` | `1.1` | Hero, large headings |
| `--leading-snug` | `1.3` | Section headings |
| `--leading-normal` | `1.65` | Body text |
| `--tracking-tight` | `-0.02em` | Large headings |
| `--tracking-normal` | `0em` | Body |
| `--tracking-wide` | `0.12em` | Uppercase labels, tagline |
| `--weight-normal` | `400` | Body |
| `--weight-medium` | `500` | Emphasis |
| `--weight-semibold` | `600` | Headings |
| `--weight-bold` | `700` | Hero name |

### Spacing

| Token | Value |
|-------|-------|
| `--space-1` | `4px` |
| `--space-2` | `8px` |
| `--space-3` | `12px` |
| `--space-4` | `16px` |
| `--space-6` | `24px` |
| `--space-8` | `32px` |
| `--space-12` | `48px` |
| `--space-16` | `64px` |
| `--space-24` | `96px` |
| `--space-32` | `128px` |
| `--space-48` | `192px` |

### Shape

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | `4px` | Tags, badges |
| `--radius-md` | `6px` | Buttons |
| `--radius-lg` | `8px` | Cards |
| `--radius-full` | `9999px` | Pills |

### Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `--shadow-sm` | `0 1px 2px rgba(0,0,0,0.04)` | Barely there — subtle lift |
| `--shadow-md` | `0 2px 8px rgba(0,0,0,0.06)` | Cards on hover |

### Animation

| Token | Value | Usage |
|-------|-------|-------|
| `--duration-fast` | `150ms` | Button feedback, hovers |
| `--duration-normal` | `300ms` | Transitions |
| `--duration-slow` | `600ms` | Section reveals |
| `--duration-reveal` | `800ms` | Hero entrance |
| `--ease-out` | `cubic-bezier(0.23, 1, 0.32, 1)` | Content entries |
| `--ease-in-out` | `cubic-bezier(0.77, 0, 0.175, 1)` | Smooth movement |

## Component Patterns

### Button
- Single variant: text-style link with arrow (`View project ->`)
- No background, no border — just text + subtle hover underline
- Uses `--color-primary`, transitions to `--color-primary-hover`
- Font: `--text-sm`, `--weight-medium`, `--tracking-wide`, uppercase

### Badge (Tech Tag)
- Pill shape with thin border
- Background: transparent, border: `--color-border`
- Font: `--text-xs`, `--weight-medium`, `--tracking-wide`, uppercase
- Padding: `--space-2` horizontal, `--space-1` vertical
- Radius: `--radius-full`

### Card (Project)
- No visible card chrome — separation through spacing only
- Project name: `--text-4xl`, `--weight-bold`, `--leading-tight`
- Subtitle: `--text-lg`, `--color-text-secondary`
- Description: `--text-base`, `--leading-normal`, max-width 640px
- Tags row below description with `--space-2` gap
- Link at bottom

### Section
- Full-width, min-height 100vh for hero, auto for others
- Content centered in narrow column: max-width 800px
- Vertical padding: `--space-32` top and bottom
- Alternating backgrounds: `--color-background` / `--color-surface`

### Link (Contact)
- Inline text, `--color-text-primary`
- Underline on hover with `--duration-fast` transition
- Font: `--text-base`, `--weight-normal`
- Separated by ` · ` delimiter

### Divider
- 1px height, `--color-border`
- Max-width same as content column
- Margin: `--space-16` vertical
