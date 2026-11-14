---
name: Obsidian Pulse
colors:
  surface: '#131314'
  surface-dim: '#131314'
  surface-bright: '#3a393a'
  surface-container-lowest: '#0e0e0f'
  surface-container-low: '#1c1b1c'
  surface-container: '#201f20'
  surface-container-high: '#2a2a2b'
  surface-container-highest: '#353436'
  on-surface: '#e5e2e3'
  on-surface-variant: '#c6c4d8'
  inverse-surface: '#e5e2e3'
  inverse-on-surface: '#313031'
  outline: '#908fa1'
  outline-variant: '#464555'
  surface-tint: '#c1c1ff'
  primary: '#c1c1ff'
  on-primary: '#1400a8'
  primary-container: '#5d5dff'
  on-primary-container: '#fefaff'
  inverse-primary: '#4644e9'
  secondary: '#c8c5ca'
  on-secondary: '#303033'
  secondary-container: '#47464a'
  on-secondary-container: '#b7b4b8'
  tertiary: '#ffb690'
  on-tertiary: '#542100'
  tertiary-container: '#bf5400'
  on-tertiary-container: '#fffbfa'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e1dfff'
  primary-fixed-dim: '#c1c1ff'
  on-primary-fixed: '#09006b'
  on-primary-fixed-variant: '#2a21d2'
  secondary-fixed: '#e4e1e6'
  secondary-fixed-dim: '#c8c5ca'
  on-secondary-fixed: '#1b1b1e'
  on-secondary-fixed-variant: '#47464a'
  tertiary-fixed: '#ffdbca'
  tertiary-fixed-dim: '#ffb690'
  on-tertiary-fixed: '#331100'
  on-tertiary-fixed-variant: '#783200'
  background: '#131314'
  on-background: '#e5e2e3'
  surface-variant: '#353436'
  surface-glass: rgba(15, 15, 18, 0.6)
  border-glow: rgba(255, 255, 255, 0.08)
  accent-glow: rgba(93, 93, 255, 0.15)
  text-dim: '#8E8E93'
typography:
  display-lg:
    fontFamily: Geist
    fontSize: 48px
    fontWeight: '600'
    lineHeight: '1.1'
    letterSpacing: -0.04em
  headline-lg:
    fontFamily: Geist
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Geist
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Geist
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Geist
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-md:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: 0.02em
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.4'
    letterSpacing: 0.05em
  headline-lg-mobile:
    fontFamily: Geist
    fontSize: 28px
    fontWeight: '600'
    lineHeight: '1.2'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  gutter: 16px
  margin-mobile: 16px
  margin-desktop: 32px
  bento-gap: 12px
---

## Brand & Style

The design system is built on the philosophy of **Invisible Complexity**. It masks high-powered orchestration behind a calm, ethereal facade that feels both professional and technical. The target audience consists of power users and professionals who demand high information density without the associated cognitive fatigue.

The aesthetic is a fusion of **Glassmorphism** and **Bento Grid** architecture, emphasizing depth over raw contrast. By simulating physical properties like light refraction, inner glows, and multi-layered backdrop blurs (15px–40px), the UI creates a spatial hierarchy that feels tactile yet digital. The atmosphere is premium and forward-leaning, prioritizing hardware-software synergy through OLED-optimized surfaces and haptic-responsive interactions.

## Colors

The palette is anchored by `#0A0A0B`, a deep charcoal base chosen to eliminate OLED smearing while maintaining the depth of a dark interface. Pure black is explicitly avoided to reduce visual harshness.

**Electric Indigo (#5D5DFF)** serves as the sole chromatic accent, used for high-intent actions, glowing states, and focus indicators. 

The system relies heavily on **Alpha Channels** for its layering strategy. Surface colors are rarely opaque; instead, they use varying levels of transparency combined with backdrop filters to create the "multi-layered glass" effect. Inner glows on borders simulate light hitting the edges of glass panels, providing definition without the need for high-contrast strokes.

## Typography

Typography is clean and technical, utilizing **Geist** for its precision and modernist appeal. For metadata and technical indicators, **JetBrains Mono** is used to reinforce the "technical" personality of the system.

The system features toggleable density modes:
- **Airy Mode:** Increases line-height and letter spacing for long-form reading and focused tasks.
- **Compact Mode:** Tightens vertical rhythm for data-heavy dashboards and complex monitoring.

All display and headline styles utilize negative letter-spacing to maintain a "tight" professional feel, while labels utilize increased tracking for legibility at small scales.

## Layout & Spacing

This design system employs a **Bento Grid** layout model, using CSS Subgrid to maintain perfect alignment across nested components. The layout is modular, with content organized into distinct tiles that reflow based on viewport size.

- **Desktop:** A 12-column grid with flexible tile spans. Large margins (32px) create a focused "island" feel for the content.
- **Tablet:** An 8-column grid with reduced gutters.
- **Mobile:** A single-column vertical stack with a fixed "Chat Input" container at the bottom (0px margin from bottom edge) to mimic native OS-level interfaces.

The spacing rhythm is strictly based on a 4px scale, ensuring all elements align to a predictable baseline and horizontal grid.

## Elevation & Depth

Hierarchy is established through **Backdrop Refraction** rather than traditional drop shadows.

1.  **Base Layer:** The `#0A0A0B` background.
2.  **Bento Tiles:** Surfaces with `surface-glass` (60% opacity) and a `15px` backdrop-blur. Borders use an `inner-glow` (subtle white at 8% opacity).
3.  **Command Center (Floating):** The highest elevation tier. It uses a `40px` backdrop-blur and a subtle `accent-glow` shadow to suggest it is floating high above the dashboard. When active, a heavy `overlay` dims the layers below.
4.  **Interactive Elements:** Buttons and active inputs utilize a subtle "Electric Indigo" outer glow to signify focus and energy.

## Shapes

The shape language is consistently **Rounded**, using a 0.5rem (8px) base radius. This strikes a balance between the precision of a technical tool and the approachability of a premium consumer product.

- **Bento Tiles:** Use `rounded-lg` (16px) to clearly define content boundaries.
- **Command Center:** Uses `rounded-xl` (24px) to emphasize its distinct, "floating" nature.
- **Small Components:** Chips and buttons follow the base 8px radius.

## Components

### Buttons & Chips
Buttons are semi-transparent with an inner border glow. The "Primary" state uses a solid Electric Indigo fill with a soft glow transition on hover. Chips are minimalist, using `label-sm` typography and a high-blur background.

### Bento Tiles (Cards)
The foundational container. Every tile must have a `1px` border with the `border-glow` color. Content inside tiles should follow the adaptive density rules (Airy vs. Compact).

### Command Center
A global floating modal (triggered by `Cmd+K`). It should feel like a search-first OS interface. It is the only component allowed to use the maximum `40px` blur.

### Input Fields
Inputs are "ghost" style—no solid background, only a bottom border that illuminates with an indigo glow when focused.

### Chat Input
A fixed-position container at the bottom of the screen. It features a high-density layout to handle "Streaming" AI responses (`st.write_stream` patterns) gracefully, ensuring the text is readable as it generates.