# Silicon to Screen — The Computer System Engine

A **stunning, minimalist visual immersion sandbox** — a single-file interactive schematic
that lets you steer live signals through the complete computer-system pipeline, from raw
hardware input, through software abstraction and system buses, into memory, across the CPU
machine cycle, and out to glowing display pixels.

Not a quiz. No scores. Just an aesthetic, fully manipulable schematic with a smooth
auto-scrolling tour.

**Play it:** open `index.html` in any browser, or visit the GitHub Pages deployment.

## Design language

- Deep charcoal backdrop, muted blueprint grid, crisp white typography.
- Four glowing signal accents: **Electric Cyan** (address / control), **Amber Gold**
  (data / registers), **Emerald Glow** (logic / ALU), **Deep Magenta** (interrupts).
- Fluid canvas particle simulations, eased camera pans, and subtle ambient synth hums
  with filtered ticks.

## The 6 visual stages

1. **Input — Live Digitization vs Static Compilation.** A code block collapses into
   binary (compile-time) beside live peripherals (keystroke waves, a draggable
   crosshair, OCR laser scan, microphone) digitizing straight onto the system bus.
2. **Software Abstraction & Register Mapping.** Glassmorphic layers — Applications →
   OS Kernel + Utilities → Driver Translators → Hardware Registers. Fire a *system call*
   and watch it descend as the driver writes register values. Middleware/DB APIs sit
   visibly apart — *not* a driver.
3. **Motherboard & Tri-Bus Flow.** PSU power grid, heat sinks with a thermal-throttle
   meter, PCH hub, PCIe (GPU, NIC), SATA, USB — feeding three bus rails: Address
   (unidirectional), Data (bidirectional), Control (strobes & IRQs).
4. **Memory Pyramid & Locality.** Drag *Data Access* and watch a request descend the
   hierarchy — Registers, L1/L2/L3 SRAM cache, DRAM/ROM — down to storage: magnetic tape
   (sequential), HDD, CD, non-volatile SSD. A live cycle meter proves locality of reference.
5. **Machine Cycle & Circuit Engine.** Single-step or auto-run Fetch → Decode → Execute
   across PC, MAR, MDR, CIR, CU, ALU, ACC. Zoom in to see NPN transistors → logic gates →
   combinational (adder/mux) and sequential (flip-flop/latch) circuits.
6. **Output Pipeline & Display Calibration.** The GPU renders a frame buffer to a panel you
   toggle between CRT / LCD / OLED / micro-LED — contrast ascending, power descending.

Closes on Steve Jobs: *"…the equivalent of a bicycle for our minds."*

## Tech

Single `index.html` — inline CSS, vanilla JavaScript, HTML5 Canvas, Web Audio API.
No frameworks, no build step, no dependencies. Layered rendering, delta-time
`requestAnimationFrame`, eased camera, and a pooled particle system keep it smooth.
