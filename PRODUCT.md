# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Primary users are **ICT students** studying how a computer system works end-to-end. They use the schematic for self-directed study — stepping through stages, dragging controls, and re-running signals at their own pace to build intuition for abstract hardware and software concepts.

A secondary audience is the **teacher/instructor who grades the work**, evaluating whether it teaches correctly and holds up as a finished piece.

## Product Purpose

"Silicon to Screen — The Computer System Engine" is a single-file interactive schematic of the complete computer-system pipeline: raw hardware input, through software abstraction and system buses, into memory, across the CPU machine cycle, and out to display pixels. It exists so a learner can *see and steer* live signals through that pipeline instead of only reading about it.

Success means: a student finishes the tour with a working mental model of how signals move through a computer, and the work reads as a polished, credible artifact to a grading teacher.

## Positioning

**Full-stack pipeline in one continuous canvas.** Where neighboring explainers isolate one subsystem (just the CPU, just memory), this covers input → software → motherboard → memory → CPU → display as one global, camera-panned schematic with live animated signal flow. It is deliberately *not* a quiz: no scores, no right answers — pure manipulable visualization.

## Operating Context

- Opened directly in any browser, or via the GitHub Pages deployment.
- Self-study sessions on a laptop/desktop; also plausibly presented on a shared screen by a teacher.
- An auto-scrolling tour dwells ~11s per stage and can be paused; users can also jump freely between stages and drive each stage's controls.
- Ambient Web Audio (drone + ticks) begins only after the first user interaction.
- Concepts are drawn from an **ICT** computer-systems curriculum (input/output devices, systems software, system bus, memory hierarchy, machine cycle, display technologies).

## Capabilities and Constraints

- **Single-file, zero-dependency:** one `index.html` with inline CSS, vanilla JavaScript, HTML5 Canvas, and the Web Audio API. No frameworks, no build step, no dependencies. This is a binding constraint — the deliverable must remain a self-contained file deployable to GitHub Pages (`.nojekyll` present).
- **Fixed content set (binding):** the **6 visual stages**, the **14 ICT concepts** depicted, the **four-color signal legend**, and the **Steve Jobs closing quote** are the fixed curriculum and must be preserved by future work.
- Four signal accents encode meaning: Electric Cyan (address/control), Amber Gold (data/registers), Emerald Glow (logic/ALU), Deep Magenta (interrupts/IRQ).
- Performance techniques in place: layered rendering, delta-time `requestAnimationFrame`, eased camera, pooled particle system.

## Brand Commitments

- Product name: **"Silicon to Screen"**; subtitle/tagline: **"The Computer System Engine."**
- The four-color signal language and its meanings are an identity commitment, not decoration.
- Closing note is the attributed Steve Jobs quote ("…the equivalent of a bicycle for our minds."), credited by name.

## Evidence on Hand

The only real content is the live schematic itself plus the README's description. There are **no** testimonials, customers, benchmarks, press, pricing, or analytics. Future work must not fabricate any.

## Product Principles

1. **Show, don't test.** The value is a manipulable schematic with live signals — never a quiz or score.
2. **One continuous system, not isolated parts.** Every stage is a segment of a single pipeline the visitor can traverse.
3. **Accuracy is the teaching.** The 14 ICT concepts must be depicted correctly; credibility with a grading teacher depends on it.
4. **Aesthetic immersion is part of the lesson.** The visual/audio craft is a teaching device — it makes abstractions feel physical.
5. **Ship as one file.** No frameworks, no build, no dependencies — deployable straight to GitHub Pages.
