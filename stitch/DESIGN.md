---
name: SignalPad Recovery Core
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#45464d'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#76777d'
  outline-variant: '#c6c6cd'
  surface-tint: '#565e74'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#131b2e'
  on-primary-container: '#7c839b'
  inverse-primary: '#bec6e0'
  secondary: '#505f76'
  on-secondary: '#ffffff'
  secondary-container: '#d0e1fb'
  on-secondary-container: '#54647a'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#271901'
  on-tertiary-container: '#98805d'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2fd'
  primary-fixed-dim: '#bec6e0'
  on-primary-fixed: '#131b2e'
  on-primary-fixed-variant: '#3f465c'
  secondary-fixed: '#d3e4fe'
  secondary-fixed-dim: '#b7c8e1'
  on-secondary-fixed: '#0b1c30'
  on-secondary-fixed-variant: '#38485d'
  tertiary-fixed: '#fcdeb5'
  tertiary-fixed-dim: '#dec29a'
  on-tertiary-fixed: '#271901'
  on-tertiary-fixed-variant: '#574425'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  display:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
  label-caps:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.05em
  data-mono:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  gutter: 12px
  margin: 16px
---

## Brand & Style
The design system is engineered for high-stakes operational environments where clarity and speed of data processing are paramount. The brand personality is clinical, reliable, and unobtrusive—positioning itself as a professional tool rather than a consumer app. 

The aesthetic follows a **Product-First Minimalism** approach. It rejects decorative elements like gradients or heavy shadows in favor of a structural hierarchy defined by precise borders, subtle surface shifts, and rigorous alignment. The goal is to minimize cognitive load during recovery operations by providing a calm, predictable interface that recedes into the background, allowing the data to take center page.

## Colors
The palette is rooted in a professional "Slate" spectrum. The primary action color is a deep Navy (#0F172A), providing high contrast against the light gray work surfaces. 

- **Surface Tiers:** Use `#FFFFFF` for the primary content area, `#F8FAFC` for the base background, and `#F1F5F9` for secondary UI elements like sidebars or header backgrounds.
- **Semantic Colors:** Status indicators use high-chroma, recognizable hues but are applied sparingly (e.g., small pips or thin borders) to avoid visual fatigue. 
- **Borders:** Use `#E2E8F0` for standard dividers and `#CBD5E1` for interactive element strokes.

## Typography
The system utilizes **Inter** for its exceptional legibility and comprehensive support for tabular OpenType features. 

- **Tabular Figures:** Always enable `tnum` (tabular numbers) and `lnum` (lining numbers) for data tables, counters, and recovery progress indicators to ensure vertical alignment of digits.
- **Scale:** The scale is intentionally compact. 14px is the standard for body text, while 13px is utilized for secondary data points and sidebars to increase information density.
- **Hierarchy:** Use font weight (600 for headings) and color (Slate 900 for primary text, Slate 500 for secondary text) rather than large size increases to differentiate information.

## Layout & Spacing
This design system employs a strict **4px/8px incremental grid**. To maximize functional utility on desktop viewports, margins and gutters are tighter than consumer-facing applications.

- **Grid Model:** Use a 12-column fluid grid for dashboard layouts. In data-heavy "Explorer" views, use a fixed sidebar (240px) with a fluid content area.
- **Density:** Components use "Compact" padding (e.g., 6px vertical padding on inputs and buttons) to allow more rows of data to be visible above the fold.
- **Mobile Reflow:** For tablet and mobile, the 12-column grid collapses to 4 columns. Information-dense tables should transition to a "List Card" format or horizontal scroll with pinned "ID" columns.

## Elevation & Depth
The system relies on **Tonal Layering** and **Low-Contrast Outlines** rather than physical shadows.

- **Stacking:** Surface height is communicated by background color shifts. A "raised" card is not shadowed; instead, it sits on a `#F8FAFC` background with a `#FFFFFF` fill and a 1px `#E2E8F0` border.
- **Interactions:** Hover states are indicated by a subtle shift to a darker gray background (e.g., Slate 50 to Slate 100) or a primary-colored border.
- **Focus:** Active input states use a 1px solid border of the Info/Blue color with a 2px semi-transparent "halo" (no blur) to maintain the crisp, geometric feel.

## Shapes
The shape language is **Soft (0.25rem)**. This provides a subtle modern touch that softens the "industrial" feel of a dense data tool without wasting the space required by large radii.

- **Elements:** Buttons, inputs, and small containers use a 4px (0.25rem) radius.
- **Large Containers:** Cards or modal windows use 8px (0.5rem).
- **Status Pips:** Indicator dots and small status tags (chips) may use a full-round (pill) radius to distinguish them from interactive buttons.

## Components
- **Data Tables:** The core of the recovery tool. Use 1px horizontal borders only (`#E2E8F0`). Header cells should have a subtle gray background (`#F1F5F9`) and `label-caps` typography. Row hover states are mandatory.
- **Buttons:** 
    - *Primary:* Solid Slate 900, white text. 
    - *Secondary:* White fill, 1px Slate 300 border. 
    - *Destructive:* Solid Error Red for final recovery actions. 
    - Padding should be 6px vertical, 12px horizontal.
- **Input Fields:** Use 1px borders. Labels sit above the field in `body-sm` (Bold). Validation states use the semantic colors for the bottom border and a small trailing icon.
- **Status Chips:** Small, low-saturation backgrounds with high-saturation text (e.g., Light Green background with Dark Green text) for non-interactive status labels.
- **Progress Bars:** Use a simple 4px height bar. The "track" is Slate 100; the "fill" is Info Blue. For critical errors, the fill shifts to Error Red.
- **Navigation:** Vertical sidebar using `body-sm` weight 500. Active states indicated by a 2px vertical "hit-mark" on the left edge of the menu item.