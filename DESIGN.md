---
name: Silicon to Screen — The Computer System Engine
description: A dark, blueprint-instrument schematic that animates live signals through the six stages of a computer system.
colors:
  void-charcoal: "#0d0f12"
  blueprint-line: "#1e232a"
  signal-white: "#f0f4f8"
  muted-grey: "#5a6472"
  deep-grey: "#39414d"
  address-cyan: "#00f0ff"
  data-amber: "#ffb700"
  logic-emerald: "#00ff88"
  interrupt-magenta: "#ff0055"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Helvetica, Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.14em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Helvetica, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.005em"
  statement:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Helvetica, Arial, sans-serif"
    fontSize: "clamp(20px, 3.2vw, 34px)"
    fontWeight: 300
    lineHeight: 1.5
    letterSpacing: "0em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, Helvetica, Arial, sans-serif"
    fontSize: "11.5px"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "0em"
  readout:
    fontFamily: "\"SFMono-Regular\", ui-monospace, \"JetBrains Mono\", Menlo, Consolas, monospace"
    fontSize: "10px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.24em"
  label:
    fontFamily: "\"SFMono-Regular\", ui-monospace, \"JetBrains Mono\", Menlo, Consolas, monospace"
    fontSize: "9px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.16em"
rounded:
  hairline: "2px"
  xs: "5px"
  sm: "8px"
  md: "10px"
  lg: "14px"
  pill: "50%"
spacing:
  hair: "3px"
  xs: "7px"
  sm: "9px"
  md: "14px"
  lg: "22px"
  xl: "26px"
components:
  control-chip:
    backgroundColor: "rgba(255,255,255,0.02)"
    textColor: "{colors.muted-grey}"
    rounded: "{rounded.xs}"
    padding: "8px 13px"
  control-chip-on:
    backgroundColor: "rgba(255,255,255,0.02)"
    textColor: "{colors.address-cyan}"
    rounded: "{rounded.xs}"
    padding: "8px 13px"
  icon-button:
    backgroundColor: "rgba(255,255,255,0.02)"
    textColor: "{colors.muted-grey}"
    rounded: "{rounded.pill}"
    size: "34px"
  control-cluster:
    backgroundColor: "rgba(16,19,24,0.72)"
    rounded: "{rounded.lg}"
    padding: "10px 16px"
  nav-dot:
    backgroundColor: "{colors.deep-grey}"
    rounded: "{rounded.pill}"
    size: "8px"
  nav-dot-active:
    backgroundColor: "{colors.address-cyan}"
    rounded: "{rounded.pill}"
    size: "8px"
  restart-button:
    backgroundColor: "transparent"
    textColor: "{colors.signal-white}"
    rounded: "{rounded.md}"
    padding: "11px 20px"
---

# Design System: Silicon to Screen — The Computer System Engine

## Overview

**Creative North Star: "The Blueprint Instrument"**

A drafting-table schematic that has come alive. The whole surface is a dark blueprint: a deep charcoal field ruled with a muted 44px grid, over which crisp white type and four glowing signal lines carry live traffic. Nothing is decorative — every mark on screen is a wire, a node, a readout, or a control. The vocabulary is that of a lab instrument, not a website: tracked monospace legends, hairline borders, and colored halos that stand in for motion and state.

The density is deliberately compact. Chrome type sits at 9–11.5px and never competes with the schematic it frames; the drawing itself — buses, registers, cache tiers, transistors — owns the center. Emphasis is achieved through glow, not weight: an active element gains a colored border and a soft halo of the same hue, while inactive elements recede to `--dim` and `--dim2`.

The mood is engineered calm: near-black and near-white, one accent per stage, and four signal colors that are strictly semantic. Motion is continuous but eased — a horizontally panning camera, particles travelling along Bézier paths, slow fades — so the instrument feels alive without ever feeling busy. There is no neutral drop-shadow language; depth comes from tonal panel fills and colored glow.

**Key Characteristics:**
- Dark blueprint field: charcoal ground, muted grid, near-white type.
- Four meaningful signal accents only — cyan, amber, emerald, magenta.
- Tracked uppercase monospace for all labels, readouts, and controls.
- 1px hairline borders; active state = accent border + matching halo.
- Depth via tonal panels and glow, never neutral elevation.
- Full-bleed canvas stage with a three-band HUD chrome around the edges.

## Colors

A near-monochrome blueprint lit by four semantic signal hues; each hue means exactly one thing and is used on a single stage as its accent.

### Primary
- **Address Cyan** (#00f0ff): The system's lead accent. Marks Address-bus traffic, control signals, the primary `on` state of controls, the stage progress bar, and the active navigation dot. The default "selected / active" color.
- **Data Amber** (#ffb700): Data-bus and register traffic — frame buffers, the memory-hierarchy accent, software-abstraction layer, and the `warm` chip state.
- **Logic Emerald** (#00ff88): Logic and ALU traffic — gates, the machine-cycle stage accent, cache tiers, and OK/hit status.
- **Interrupt Magenta** (#ff0055): Interrupts and alerts — IRQ signals, thermal throttling, latency misses, the output/display stage accent, and the `hot` chip state.

### Neutral
- **Signal White** (#f0f4f8): Primary text, node labels, values, and slider thumbs. Effectively the "on" text color.
- **Muted Grey** (#5a6472): Secondary text, descriptions, idle control labels, and dimmed legends.
- **Deep Grey** (#39414d): Tertiary markers — inactive nav dots, branch rules, the finale divider.
- **Blueprint Line** (#1e232a): Every border, grid rule, wire, and divider. The universal hairline.
- **Void Charcoal** (#0d0f12): The page and canvas ground; the base of every scrim and gradient.

### Named Rules
**The Four-Signal Rule.** Only cyan, amber, emerald, and magenta carry meaning. They encode bus/semantic roles and are never used as ornament; decorative warmth comes from glow on those same hues, not new ones.

**The One-Accent-Per-Stage Rule.** Each of the six stages declares a single accent hue (`accent`) that drives its caption bar, nav state, and title conditioning. Never introduce a second stage accent within one stage's drawing.

## Typography

**Display Font:** System sans (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif`)
**Body Font:** System sans (same stack)
**Label/Mono Font:** System monospace (`"SFMono-Regular", ui-monospace, "JetBrains Mono", Menlo, Consolas, monospace`)

**Character:** A precise pairing that splits duty by function. Monospace, always uppercase and letter-spaced, handles the instrument chrome — stage readouts, control labels, legends, kickers. Sans handles what a human reads as language — stage titles, descriptions, and the closing quote. The result reads like a device faceplate: engraved labels around a soft human panel.

### Hierarchy
- **Display** (600, 15px, 1.2, 0.14em uppercase): The brand wordmark "Silicon to Screen" only; paired with a 10px mono subtitle at 0.34em.
- **Statement** (300, clamp(20px–34px), 1.5): The finale blockquote; the only large, light-weight type in the system, reserved for the closing line.
- **Headline** (600, 17px, 1.2): The active stage title in the top-bar caption.
- **Body** (400, 11.5px, 1.6): Stage descriptions and supporting prose; sits under `--dim`.
- **Readout** (400, 10px, 0.24em uppercase, mono): Stage readouts, the Kicker line, and the counter (`Stage 01 / 06`).
- **Label** (400, 9px, 0.16em uppercase, mono): Control labels, nav-dot captions, legend rows, meta lines. The workhorse of the chrome.

### Named Rules
**The Tracked-Caps Rule.** Every mono label is uppercase and letter-spaced between 0.10em and 0.34em. Tracking increases as size decreases — the smaller the label, the wider it breathes.

**The Sans-Only-for-Sentences Rule.** If it is a word a person reads as language (title, description, quote), it is sans and sentence-cased. If it is a machine readout or a control name, it is uppercase mono. Never mix the two treatments on one string.

## Layout

A single full-viewport stage with no page scroll: two fixed canvases (`#bg` behind, `#scene` above) fill the window, and a pointer-transparent HUD grid (`22px 26px` padding, rows `auto 1fr auto`) floats the chrome on top.

The experience is **horizontally panned**, not scrolled: six stages each occupy one viewport width (`STAGE_W = window.innerWidth`), laid out left to right on one long canvas, with an eased camera (`exponential smoothing`) sliding between them. Only stages within `±W + 200` of the camera are drawn (horizontal culling).

The top bar is a three-column grid (`1fr / minmax(0, 680px) / 1fr`, gap 26px): brand left, centered stage caption (max 680px) in the middle, stage readout and play/pause right. The bottom band stacks the floating control cluster above the six navigation dots. A fixed legend sits lower-right; a 1px progress hairline is pinned to the very top edge.

Responsive (`max-width: 900px`): the top bar collapses to one column, the caption left-aligns, the legend hides, nav-dot captions hide, and the top-right cluster pins to the window corner. Controls wrap within `max-width: min(94vw, 1000px)`.

Spacing rhythm is tight and instrument-like: `26px` outer gutters, `22px` gaps between major chrome groups, `14–16px` inside the control cluster, and `7–9px` between label-and-value pairs. Nothing in the chrome exceeds ~70px tall.

## Elevation & Depth

This system is **tonal + glow, not shadow**. Depth is built from layered translucent fills over the charcoal ground (canvas panels at `rgba(20,24,30,0.55)`, the control cluster at `rgba(16,19,24,0.72)`) and from colored halos that stand in for state and motion. Neutral drop shadow appears in exactly one place — the control cluster — to detach it from the schematic beneath. The top bar is protected by a fixed vertical scrim (`rgba(13,15,18,.94)` fading to transparent at 190px) so its caption always reads over moving art.

### Shadow Vocabulary
- **Accent halo** (`box-shadow: 0 0 22px -6px var(--cyan)`): Hover on the circular icon button; the canonical "lit" state.
- **Chip halo** (`box-shadow: 0 0 20px -8px <accent>`): An engaged control chip, tinted to its accent (cyan / amber / magenta).
- **Focus ring** (`box-shadow: 0 0 0 4px rgba(0,240,255,.12), 0 0 16px var(--cyan)`): The active navigation dot — a soft dual-halo seat.
- **Cluster drop** (`box-shadow: 0 18px 50px -20px rgba(0,0,0,.9)`): The single structural shadow, under the floating control cluster.
- **Progress glow** (`box-shadow: 0 0 10px var(--cyan)`): Under the top progress hairline.

### Named Rules
**The Glow-Not-Shadow Rule.** Depth and emphasis are expressed as a colored halo on the element's own accent hue. Neutral elevation is reserved for the one floating control cluster; never add drop shadows to panels, nodes, or chips.

**The Scrim-Above-Art Rule.** Any chrome that sits over the moving canvas must carry its own translucent ground or gradient scrim. Text is never placed directly on moving art.

## Motion

**Creative intent: signal energy.** Motion here is never ambient decoration — it is the signal *arriving*. The continuous canvas motion (camera pan, Bézier particles, drifting grid) is the product itself; the HUD chrome's motion exists only to make a state change legible, and every entrance is the accent hue arriving on a conductor.

- **Timing.** Immediate feedback `100–150ms`; routine state change `150–300ms`; HUD reveals `450–550ms`; the finale `800ms`. Arrivals decelerate on `cubic-bezier(.16, 1, .3, 1)` (`--ease-out`); exits are faster than entrances. No bounce or elastic curves.
- **Boot ignition.** On load the chrome powers on as one sequence: brand, readout and controls rise (`hudRise`), nav dots pop in with a capped stagger (`dotPop`), and the progress hairline sweeps in (`energize`). Gated on the `.js` class, so a failed script leaves the HUD fully visible.
- **Stage change.** The one recurring authored moment: the caption comes into focus (`midFocus`, a bounded `blur` plus a short rise), its accent bar grows from center (`accentGrow`), the control cluster rises (`ctlIn`), and the newly active nav dot fires a single halo pulse (`dotGlow`). One material idea — accent arriving — carried across the chrome, never scattered effects.
- **Reduced motion.** `prefers-reduced-motion` removes spatial travel and blur: HUD entrances become opacity-only (`softIn`), the nav pulse is dropped, the camera settles almost instantly instead of gliding, ambient dust thins to roughly a third, and the auto-tour pauses (re-armed by the Play control). Signal flow inside the schematic is preserved — it carries the meaning.

### Named Rules
**The Signal-Energy Rule.** Animate the accent arriving, not the element: a sweep, a growth, a focus, a pulse. Reach for one authored moment per state change — never scattered effects, and never one identical entrance on every section.

**The No-Travel-Under-Reduced-Motion Rule.** When `prefers-reduced-motion` is set, drop translate, scale and blur and keep only opacity and color — but never remove feedback that confirms an action.

## Shapes

A soft-instrument geometry. Everything is a rounded rectangle with small radii — schematic panels use 8–16px, node boxes and chips 6–9px, the control cluster 14px — except circular elements (the icon button, nav dots, slider thumbs, and every particle/node in the canvas), which are perfect circles.

Borders are universally a 1px `--line` hairline. Active or highlighted elements keep the same 1px weight but swap the border color to the accent (paired with a halo); the system never thickens borders to signal emphasis. The blueprint grid — a 44px major grid with a 4× finer sub-grid at 0.4 opacity — is the recurring background form, drifting slowly with the camera to imply depth. Accent caption bars are short 26×2px rounded strokes.

## Components

### Buttons
- **Shape:** Control chips are gently rounded rectangles (~5px radius, from a 9px source radius on a 32px-tall control); icon buttons are perfect circles (50%).
- **Control chip (`button.cb`):** Uppercase 10.5px mono, 0.10em tracking; `8px 13px` padding on a `rgba(255,255,255,0.02)` ground with a 1px `--line` border; idle text is `--dim`.
- **Hover / Focus:** Text lightens to `--text` and the border warms to `--dim`.
- **On / active:** Border and text take the accent (`--cyan` by default; `--amber` for `.warm`; `--magenta` for `.hot`) plus a matching `0 0 20px -8px` halo. No fill change.
- **Icon button (`.icobtn`):** 34px circle, `--dim` glyph at 13px; hover turns border and glyph cyan with a `0 0 22px -6px` halo.
- **Restart button:** The finale's lone outline button — transparent ground, `--text` label, 10px radius; hover goes cyan with a halo.

### Navigation
- **Style:** A centered row of six dots (gap 22px), each an 8px circle with a caption beneath it. Dots idle at `--dim2`; visited (`done`) at `--dim`; hover brightens to `--dim`.
- **Active:** The active dot is `--cyan` with a dual halo (`0 0 0 4px rgba(0,240,255,.12), 0 0 16px`), and its caption rises to `--text`.
- **Mobile (≤900px):** Captions hide; gap tightens to 14px.

### Control Cluster
- **Shape:** A 14px-radius glass bar that groups the current stage's buttons and sliders.
- **Background:** `rgba(16,19,24,0.72)` with `backdrop-filter: blur(14px)` and a 1px `--line` border.
- **Shadow Strategy:** The system's only structural drop shadow (`0 18px 50px -20px rgba(0,0,0,.9)`).
- **Internal padding:** `10px 16px`, 14px gap, wrapping within `min(94vw, 1000px)`; stage-specific controls are swapped in with a `stagein` reveal on each stage change.
- **Dividers:** 1px × 22px vertical `--line` rules separate logical groups; each group is preceded by a 9px uppercase mono label.

### Inputs / Fields
- **Sliders (`input[type=range]`):** A 2px `--line` track (130px wide), 2px radius, with a 12px circular `--text` thumb carrying a soft `0 0 12px rgba(240,244,248,.6)` glow. Appearance is fully reset on both WebKit and Mozilla.
- **Focus:** The thumb is the only affordance; there is no visible outline ring on the track.

### Legend
- **Style:** A fixed lower-right stack of four rows, each a 16×2px rounded swatch in the signal hue beside a 9px uppercase mono caption. Pointer-events off; hidden on mobile.

### Canvas Panels (signature)
- **Corner Style:** Rounded rectangles, 6–16px radius depending on container size.
- **Background:** Translucent tonal fills over the void — glass layers at `rgba(24,28,34,0.5)`, schematic frames at `rgba(15,18,22,0.5)`, nodes at `rgba(255,255,255,0.02)`.
- **Border:** Always a 1px `--line` hairline; highlighted nodes swap to the accent border and gain a matching `shadowBlur` glow.
- **Text:** Drawn in-canvas via two helpers — `txt()` (mono/sans fill) and `track()` (manual letter-spaced labels) — matching the HUD hierarchy.

## Do's and Don'ts

### Do:
- **Do** keep a stage to one accent hue: drive its caption bar, nav state, and highlight color from `s.accent`.
- **Do** express state with an accent border plus a matching halo, keeping the 1px border weight.
- **Do** set all chrome labels as uppercase mono with 0.10–0.34em tracking, widening as the size drops.
- **Do** reserve the four signal hues for their meaning (cyan = address/control, amber = data/registers, emerald = logic/ALU, magenta = IRQ/alert).
- **Do** wrap any text over moving art in a translucent ground or the top-bar scrim.
- **Do** draw in-video labels through `txt()` / `track()` so canvas and HUD type share one scale.
- **Do** gate motion on delta time and clamp `dt` after tab switches, so the tour never jumps.

### Don't:
- **Don't** add a neutral drop shadow to panels, nodes, or chips — only the control cluster carries one.
- **Don't** invent a fifth accent hue; glow and tonal fills come from the existing four plus the neutrals.
- **Don't** thicken borders or fill buttons to show state; state is border-color + halo only.
- **Don't** set a stage title or description in mono, or a readout in sentence case.
- **Don't** place text directly on the canvas without a scrim behind it.
- **Don't** let the HUD chrome compete with the schematic — keep it inside the 9–17px band and off the center.
- **Don't** break the horizontal-pan model with vertical scroll or a second page.
