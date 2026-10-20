# Changelog

All notable changes to Cinematic Zoom Extended are documented here. This project follows [Semantic Versioning](https://semver.org/).

## 1.0.0 — 2026-10-20

First release of Cinematic Zoom Extended, based on Cinematic Zoom 1.3 by Mel1x.

### Added

- Separate **Cinematic** (black bars) and **Regular** (no bars) zoom profiles.
- Per-profile keybinds, starting zoom, zoom-in/out durations, and easing curves.
- Six easing curves: exponential, cubic ease-out, cubic ease-in, cubic ease-in-out, linear, and sine.
- Mouse sensitivity scaling based on the current zoom level.
- Optional view-bobbing removal while zooming.
- Live black-bar adjustment with the arrow keys, including custom step size, smoothing, and persistence.
- Ultra-wide zoom: scroll below 1× down to 0.5×.
- Discrete mouse-wheel zoom stepping.
- Magnetize/snap targets accepting zoom factors (`2x`) or FOV values (`45fov`, `60°`).
- Independent hiding of the HUD, crosshair, and first-person hands.
- Debug (F3) overlay hiding while the HUD is hidden during zoom.
- New 512×512 Extended icon: velvet curtain stage, Minecraft spyglass, pixel-art clapperboard, and `++` mark.
- First-run import of settings from Zoomify, Ok Zoomer, Just Zoom, and any other zoom-named config. WI Zoom and Logical Zoom keep no config file.
- Config migration from Cinematic Zoom 1.3.
- 40 headless regression checks covering zoom state, config migration, external config import, wheel behavior, snapping, bar adjustment, and HUD contracts.

### Changed

- New mod ID `cinematiczoom_extended` and project name **Cinematic Zoom Extended**.
- The original `cinematiczoom` mod is declared incompatible so the loader reports a clear conflict.
- Cloth Config and Mod Menu are now required on every supported version.
- Added the missing Fabric API and Cloth Config declarations to the 26.x metadata.
- Single source of truth for the mod version in `gradle.properties`.
- Release JARs are now named `cinematiczoom-extended-<minecraft>-<version>.jar`.
- Updated metadata, links, translations, and credits for the Extended project.

### Fixed

- Zoom state is preserved when switching between cinematic and regular profiles.
- Hands, crosshair, and HUD hiding now work independently.
- The 26.x builds no longer rely on undeclared runtime dependencies.
- Unix `gradlew` wrapper is executable.
