# Silicon to Screen — The Computer System Engine

An interactive, single-file web simulation that teaches the complete computer-system
architecture pipeline — from raw human input and hardware digitization through CPU
logic execution to visual output rendering.

**Play it:** open `index.html` in any modern browser, or visit the GitHub Pages deployment.

## The 6 Modules

1. **Input & Signal Conversion** — compile-time source translation vs. runtime peripheral digitization + IRQs.
2. **Software Stack & Hardware Layer** — App → OS Kernel/Utilities → Device Drivers → Hardware Registers; system calls; driver vs. middleware.
3. **Motherboard & Tri-Bus Router** — PSU, cooling, PCH, PCIe, SATA, USB; Address / Data / Control bus dispatch.
4. **Memory Hierarchy & Cache Blitz** — ROM→RAM boot, storage media classification, L1/L2/L3 SRAM cache pyramid.
5. **Microarchitecture Machine Cycle** — transistors → gates → ALU/registers; step through Fetch → Decode → Execute.
6. **Output Display & Thermal Balancing** — GPU frame buffer rendering; CRT < LCD < OLED < micro-LED trade-offs.

## Tech

Single `index.html` — inline CSS, vanilla JavaScript, HTML5 Canvas and the Web Audio API.
No frameworks, no build step, no dependencies.

---

> "What a computer is to me is the most remarkable tool that we have ever come up with.
> It's the equivalent of a bicycle for our minds." — Steve Jobs
