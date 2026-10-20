<p align="center"><img src="src/main/resources/assets/cinematiczoom/icon.png" width="128" alt="Cinematic Zoom Extended icon"></p>

<h1 align="center">Cinematic Zoom Extended</h1>

<p align="center">A smooth, configurable zoom with animated cinema bars.<br>Fabric &nbsp;|&nbsp; 1.20.1 – 26.3</p>

<p align="center">
<a href="https://modrinth.com/mod/cinematic-zoom-extended"><img src="https://img.shields.io/modrinth/dt/cinematic-zoom-extended?logo=modrinth&label=Modrinth&color=1bd96a" alt="Modrinth downloads"></a>
<a href="https://github.com/simply-sunny/CinematicZoom-Extended/releases"><img src="https://img.shields.io/github/v/release/simply-sunny/CinematicZoom-Extended?label=release&color=2ea44f" alt="Latest release"></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="MIT license"></a>
</p>

---

Hold a key and the view eases in while black bars slide across the screen, then eases back out when you let go. Cinematic Zoom Extended adds two independent profiles, six easing curves, ultra-wide zoom, snap targets and fine control over what the HUD hides.

> A fork of [Cinematic Zoom (Fabric)](https://modrinth.com/mod/cinematic-zoom-fabric) by [Mel1x](https://github.com/mel1x), based on the original [Cinematic Zoom](https://www.curseforge.com/minecraft/mc-mods/cinematic-zoom) by [KubePixel](https://www.curseforge.com/members/kubepixel/projects). Published with Mel1x's permission ([PR #8](https://github.com/mel1x/CinematicZoom/pull/8#issuecomment-6139411837)). Not affiliated with or endorsed by either author.

## Features

- **Two profiles.** Cinematic (with bars) and Regular (without), each with its own key, zoom, timing, curves, toggle mode, snap targets and HUD options.
- **Smooth motion.** Per-frame easing with six curves and separate in and out durations.
- **Framing.** Adjust the bars live with the arrow keys, zoom out to 0.5x with ultra-wide, step the wheel in fixed increments, and snap to targets like `2x` or `45fov`.
- **Camera and HUD.** Scale mouse sensitivity, remove view bobbing, and hide the HUD, crosshair and hands independently. F3 hides with the HUD.
- **Settings screen.** Cloth Config through Mod Menu, in English and Russian.
- **Easy switching.** Cinematic Zoom 1.3 configs migrate automatically, and Zoomify, Ok Zoomer, Just Zoom and similar mods are imported on first launch.

## Installation

1. Install Fabric Loader, Fabric API, [Cloth Config](https://modrinth.com/mod/cloth-config) and [Mod Menu](https://modrinth.com/mod/modmenu).
2. Put the jar for your Minecraft version in `mods`.
3. Remove any other Cinematic Zoom build; only one can be installed.

Client-side only. Servers do not need it.

## Supported versions

| Minecraft | Build target | Java | Cloth Config |
| --- | --- | --- | --- |
| 1.20.1 | `1.20.1` | 17+ | 11.1.136+ |
| 1.21.1 | `1.21.1` | 21+ | 15.0.140+ |
| 1.21.2–1.21.4 | `1.21.2` | 21+ | 16.0.143+ |
| 1.21.5–1.21.6 | `1.21.5` | 21+ | 18.0.145+ |
| 1.21.7–1.21.8 | `1.21.7` | 21+ | 19.0.147+ |
| 1.21.9–1.21.11 | `1.21.11` | 21+ | 20.0.149+ |
| 26.1–26.1.2 | `26.1` | 25+ | 26.1.154+ |
| 26.2–26.2.2 | `26.2` | 25+ | 26.2.155+ |
| 26.3 | `26.3` | 25+ | 26.3.159+ |

All targets build from `main` and share the same zoom logic.

## Requirements

| Requirement | Notes |
| --- | --- |
| **Fabric Loader** | Latest for your Minecraft version. |
| **Fabric API** | Matching your Minecraft version. |
| **Cloth Config** | **Required.** See the minimums above. |
| **Mod Menu** | **Required.** Adds the settings screen. |
| **Java** | 17 for 1.20.1, 21 for 1.21.x, 25 for 26.x. |

Client-side only; servers do not need it.

## Usage

| Action | Default key |
| --- | --- |
| Cinematic Zoom (hold or toggle) | `C` |
| Zoom without bars | Unbound — bind it in Controls |
| Increase bar size | `↑` |
| Decrease bar size | `↓` |

All keys are rebindable under **Options → Controls → Key Binds → Cinematic Zoom**.

- Hold the zoom key to zoom in; release to return smoothly. Enable **Toggle zoom** to press once on and once off.
- Use the mouse wheel while zooming to adjust magnification.
- With **Ultra-wide zoom** enabled, scroll back past 1× to reach 0.5×.
- Zoom and overlays are disabled while a GUI screen is open.

## Configuration

Open **Mod Menu → Cinematic Zoom Extended → Settings**. Every setting is there, including both profiles, curves, timings, HUD hiding, snap targets, and wheel behavior.

The settings screen writes to `config/cinematiczoom.json`:

- **Windows:** `%appdata%\.minecraft\config\cinematiczoom.json`
- **macOS:** `~/Library/Application Support/minecraft/config/cinematiczoom.json`
- **Linux:** `~/.minecraft/config/cinematiczoom.json`

Advanced JSON-only keys:

| Key | Default | Notes |
| --- | --- | --- |
| `wheelStep` | `0.05` | Continuous wheel sensitivity, 0.01–0.25. |
| `minZoomMultiplier` | `0.0333` (1/30) | Lower allows more zoom; maximum factor is `1 / value`. |

Edit those only if needed, then restart. Delete the file to reset to defaults.

### Importing from other zoom mods

If `cinematiczoom.json` is missing, Extended imports what it recognizes on first launch:

- **Zoomify** — `config/zoomify.json`
- **Ok Zoomer** — `config/ok_zoomer/config.toml` or legacy `okzoomer.json`
- **Just Zoom** — `config/justzoom/config.json`
- **Other zoom mods** — any JSON/TOML file with `zoom` in its path, matched by key name.

WI Zoom and Logical Zoom keep no config file. Existing `cinematiczoom.json` is never overwritten; delete it and relaunch to re-import.

## Migrating from Cinematic Zoom 1.3

1. Keep only one Cinematic Zoom build in `mods` — Extended replaces the original `cinematiczoom-*.jar`.
2. Install `cinematiczoom-extended-<minecraft>-1.0.0.jar`.
3. Leave `config/cinematiczoom.json` in place; legacy keys migrate on first launch.

Extended uses a new mod ID but keeps the same config filename. Migrated keys: `startingZoom`, `baseZoomMultiplier`, `barsPercent`, `smoothMs`, `hideHudDuringZoom`, `enableCinematicCamera`, `toggleMode`, `minZoomMultiplier`.

To start fresh, delete the file and relaunch.

## Compatibility

- **Client-side only.** No server component.
- **Not compatible with the original Cinematic Zoom.** Only one build can be installed.
- **Other zoom mods** may conflict with FOV handling. Don't run them together; import their settings instead.
- **Sodium, Iris, and shaders** have no known conflicts, but are not specifically tested in 1.0.0.
- **OptiFine** is unsupported; **Quilt** is untested.
- **Cloth Config and Mod Menu** are required.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| `requires cloth-config2` | Install Cloth Config for your Minecraft version. |
| `requires modmenu` | Install Mod Menu for your Minecraft version. |
| `incompatible with cinematiczoom` | Keep only one Cinematic Zoom jar in `mods`. |
| Crash on launch | Check Java: 17 / 21 / 25 depending on Minecraft. |
| Settings screen missing | Install both Mod Menu and Cloth Config. |
| Zoom key does nothing | Bind **Cinematic Zoom** under Controls. |
| Wheel does not zoom | Enable **Mouse wheel during zoom** and hold the zoom key. |
| Bars do not appear | Use the cinematic key and set the bar height above 0. |
| Broken config | Delete `config/cinematiczoom.json` and relaunch. |

Logs are in `.minecraft/logs/latest.log`. Include the log and your Minecraft, mod, and loader versions when reporting an issue.

## Building from source

Requires **JDK 25** (1.20.1 compiles with `--release 17`, 1.21.x with 21, 26.x with 25).

```bash
./gradlew clean test buildAll
```

This builds all nine targets and runs the 40-check regression suite. JARs land in `build/libs/`. Build one target with:

```bash
./gradlew :1.21.7:build
```

## Credits

- **KubePixel** — original Cinematic Zoom concept and Forge mod.
- **Mel1x** — upstream Fabric implementation and the 1.3 base.
- **simply-sunny** — Extended features, profiles, tests, and release.
- **ColoredChromium** — velvet curtain texture used in the icon ([CC BY 3.0](https://creativecommons.org/licenses/by/3.0/)).

## License

The mod code and original assets are MIT — see [LICENSE](LICENSE). Original work copyright © 2025 Melix; changes copyright © 2026 Saunak Karnati (simply-sunny).

The icon uses a velvet curtain texture by [ColoredChromium](https://www.deviantart.com/coloredchromium/art/Curtains-Red-Transparency-Light-424984584), licensed under [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). That texture remains CC BY 3.0. Minecraft is a trademark of Mojang Studios.
