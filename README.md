# MONO-HMI

Version 1.5.0 · Author: knvbepr · Default panel port: 51737.

The standalone UI design language and specimen for **PANELINK**: a pure-black,
hairline, zero-radius industrial HMI.

This repository holds the design tokens, the original UI specification, and the visual
specimens. The implementation lives in the PANELINK Android project.

## Design rules

- Pure black `#000000`; only white hairlines for structure.
- No rounded corners, no ripple, no shadows, no third-party chart widgets.
- Digits use DSEG7; Latin labels use JetBrains Mono; Chinese uses **WenQuanYi Bitmap
  Song 16px** at integer pixel multiples (16/32/48).
- Status colours: OK `#00C853`, caution `#FFB000`, fault `#FF1744`.
- Temperature warning uses amber `#FFB000`; alarm uses red `#FF1744`; both thresholds
  are adjustable. Fault state blinks continuously with a 0.5 s phase.
- Numeric columns are fixed and right-aligned so changing digit count never shifts
  neighbouring controls.

## Files

| file | content |
|---|---|
| `UI_SPEC.md` | full original design brief |
| `tokens.css` / `tokens.json` | colours, type, geometry, motion |
| `index.html` | browsable token + specimen sheet |
| `docs/` | Android 13 / settings / fault captures |

## Specimens

- `docs/remote-panel.png` — remote PC telemetry (multi-GPU, multi-disk, battery)
- `docs/remote-a13.png` — local panel on Android 13
- `docs/960x540.png` — 960x540 layout check
- `docs/settings-large.png` — two-column settings with large touch targets
- `docs/fault-solid.png` / `docs/fault-dim.png` — fault blink phases
