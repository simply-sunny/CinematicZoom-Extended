# Modrinth release sheet

This file is the source of truth for the Modrinth project settings, version metadata, and listing body. The listing body starts after the horizontal rule.

## Project settings

| Field | Value |
| --- | --- |
| Title | **Cinematic Zoom Extended** |
| Slug | `cinematic-zoom-extended` |
| Project type | Mod |
| Summary | Feature-rich fork of Cinematic Zoom with dual zoom profiles, custom easing, ultra-wide, snap zoom, and granular HUD control. Fabric 1.20.1–26.3, client-side. |
| License | MIT |
| Environment | Client-side only (`client_only`) |
| Featured categories | `fabric`, `utility`, `game-mechanics` |
| Additional categories | `decoration` |
| Source | https://github.com/simply-sunny/CinematicZoom-Extended |
| Issues | https://github.com/simply-sunny/CinematicZoom-Extended/issues |
| Wiki / docs | https://github.com/simply-sunny/CinematicZoom-Extended#configuration |
| Discord | *(none)* |
| Donation links | *(none)* |
| Icon | `src/main/resources/assets/cinematiczoom/icon.png` — 512×512 PNG |
| Featured gallery image | 1280×720 screenshot |

## Version metadata

Upload one Modrinth version per JAR, all with version number `1.0.0`, channel `release`, loader `fabric`, and the same changelog.

| JAR | Modrinth `game_versions` |
| --- | --- |
| `cinematiczoom-extended-1.20.1-1.0.0.jar` | `1.20.1` |
| `cinematiczoom-extended-1.21.1-1.0.0.jar` | `1.21.1` |
| `cinematiczoom-extended-1.21.2-1.21.4-1.0.0.jar` | `1.21.2`, `1.21.3`, `1.21.4` |
| `cinematiczoom-extended-1.21.5-1.21.6-1.0.0.jar` | `1.21.5`, `1.21.6` |
| `cinematiczoom-extended-1.21.7-1.21.8-1.0.0.jar` | `1.21.7`, `1.21.8` |
| `cinematiczoom-extended-1.21.9-1.21.11-1.0.0.jar` | `1.21.9`, `1.21.10`, `1.21.11` |
| `cinematiczoom-extended-26.1-1.0.0.jar` | `26.1`, `26.1.1`, `26.1.2` |
| `cinematiczoom-extended-26.2-1.0.0.jar` | `26.2` (Modrinth has no `26.2.1`/`26.2.2` tags yet) |
| `cinematiczoom-extended-26.3-1.0.0.jar` | `26.3` |

Version name format: `Cinematic Zoom Extended 1.0.0 (1.20.1)` or `Cinematic Zoom Extended 1.0.0 (1.21.2–1.21.4)`.

### Dependencies

| Project | ID | Type |
| --- | --- | --- |
| Fabric API | `P7dR8mSH` | Required |
| Cloth Config API | `9s6osm5g` | Required |
| Mod Menu | `mOgUt4GM` | Required |
| Cinematic Zoom (Fabric) | `LBKcRJTu` | Incompatible |

## Gallery plan

Gallery files must be under **5 MiB** each. Use PNG or JPEG screenshots.

| Order | Asset | Caption |
| --- | --- | --- |
| 1 | Hero screenshot, 1280×720 | Cinematic zoom with animated black bars |
| 2 | Settings screen | Two independent profiles: Cinematic and Regular |
| 3 | Ultra-wide/snap screenshot | Ultra-wide zoom and snap targets |
| 4 | HUD comparison | Hide the HUD, crosshair, and hands independently |

Alt text should repeat the caption.

---

# Cinematic Zoom Extended

Smooth, cinematic zoom for **Fabric 1.20.1–26.3**: animated black bars, per-frame easing, two independent zoom profiles, ultra-wide zoom, snap targets, and granular HUD control.

A client-side fork of [Cinematic Zoom (Fabric)](https://modrinth.com/mod/cinematic-zoom-fabric) by [Mel1x](https://github.com/mel1x), based on the original [Cinematic Zoom](https://www.curseforge.com/minecraft/mc-mods/cinematic-zoom) concept by [KubePixel](https://www.curseforge.com/members/kubepixel/projects). Published with permission. Not affiliated with or endorsed by KubePixel or Mel1x.

## Features

- **Two profiles** — Cinematic (bars) and Regular (no bars), each with its own key, zoom, timing, curves, toggle mode, snap targets, and HUD options.
- **Smooth motion** — per-frame easing with six curves and separate in/out durations.
- **Framing** — live arrow-key bar adjustment, ultra-wide zoom (0.5×), discrete wheel steps, and snap/magnetize targets (`2x`, `45fov`).
- **Camera and HUD** — sensitivity scaling, view-bobbing removal, independent HUD/crosshair/hands hiding, and F3 hidden with the HUD.
- **In-game settings** — Cloth Config screen via Mod Menu, with English and Russian translations.
- **Migration and import** — 1.3 configs migrate; Zoomify, Ok Zoomer, Just Zoom, and other zoom configs are imported on first launch.

## Supported versions

| Minecraft | Java | Cloth Config |
| --- | --- | --- |
| 1.20.1 | 17+ | 11.1.136+ |
| 1.21.1 | 21+ | 15.0.140+ |
| 1.21.2–1.21.4 | 21+ | 16.0.143+ |
| 1.21.5–1.21.6 | 21+ | 18.0.145+ |
| 1.21.7–1.21.8 | 21+ | 19.0.147+ |
| 1.21.9–1.21.11 | 21+ | 20.0.149+ |
| 26.1–26.1.2 | 25+ | 26.1.154+ |
| 26.2–26.2.2 | 25+ | 26.2.155+ |
| 26.3 | 25+ | 26.3.159+ |

## Requirements

- **Fabric Loader** — latest for your Minecraft version.
- **Fabric API** — matching your Minecraft version.
- **Cloth Config** — required; see the minimums above.
- **Mod Menu** — required; adds the settings screen.
- **Java** — 17 for 1.20.1, 21 for 1.21.x, 25 for 26.x.

## Installation

1. Install Fabric Loader, Fabric API, Cloth Config, and Mod Menu.
2. Put the matching `cinematiczoom-extended-<minecraft>-1.0.0.jar` in `mods`.
3. Keep only one Cinematic Zoom build in `mods`; the two cannot run together.
4. Launch the game.

## Usage

| Action | Default key |
| --- | --- |
| Cinematic Zoom | `C` |
| Zoom without bars | Unbound — set it in Controls |
| Increase bar size | `↑` |
| Decrease bar size | `↓` |

- Hold the zoom key to zoom in; release to return smoothly. Enable **Toggle zoom** to press once on and once off.
- Use the mouse wheel while zooming to adjust magnification.
- With **Ultra-wide zoom** enabled, scroll back past 1× to reach 0.5×.
- Zoom and overlays are disabled while a GUI screen is open.

## Configuration

Open **Mod Menu → Cinematic Zoom Extended → Settings**. Every setting is there, including both profiles, curves, timings, HUD hiding, snap targets, and wheel behavior.

The screen writes to `config/cinematiczoom.json` (Windows `%appdata%\.minecraft\config\`, macOS `~/Library/Application Support/minecraft/config/`, Linux `~/.minecraft/config/`).

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
2. Install the matching Extended JAR.
3. Leave `config/cinematiczoom.json` in place; legacy keys migrate on first launch.

Extended uses a new mod ID but keeps the same config filename. To start fresh, delete the file and relaunch.

## Compatibility

- Client-side only; servers do not need the mod.
- **Do not install the original Cinematic Zoom alongside Extended.**
- Do not combine with other zoom/FOV mods; import their settings instead.
- Sodium, Iris, and shaders have no known conflicts, but are not specifically tested in 1.0.0.
- OptiFine is unsupported; Quilt is untested.
- Cloth Config and Mod Menu are required.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| Missing `cloth-config2` | Install Cloth Config for your Minecraft version. |
| Missing `modmenu` | Install Mod Menu for your Minecraft version. |
| Incompatible with `cinematiczoom` | Keep only one Cinematic Zoom jar in `mods`. |
| Crash on launch | Check Java: 17 / 21 / 25 depending on Minecraft. |
| Settings screen missing | Install both Mod Menu and Cloth Config. |
| Zoom key does nothing | Bind **Cinematic Zoom** under Controls. |
| Wheel does not zoom | Enable **Mouse wheel during zoom** and hold the zoom key. |
| Bars do not appear | Use the cinematic key and set the bar height above 0. |
| Broken config | Delete `config/cinematiczoom.json` and relaunch. |

Include `logs/latest.log`, your Minecraft version, the mod version, and the Fabric Loader version when reporting an issue.

## Credits

- **KubePixel** — original Cinematic Zoom concept and Forge mod.
- **Mel1x** — upstream Fabric implementation and the 1.3 base.
- **simply-sunny** — Extended features, profiles, tests, and release.
- **ColoredChromium** — velvet curtain texture used in the icon ([CC BY 3.0](https://creativecommons.org/licenses/by/3.0/)).

## License

The mod code and original assets are MIT. Original work copyright © 2025 Melix; changes copyright © 2026 Saunak Karnati (simply-sunny). See the [LICENSE](https://github.com/simply-sunny/CinematicZoom-Extended/blob/main/LICENSE).

The icon uses a velvet curtain texture by [ColoredChromium](https://www.deviantart.com/coloredchromium/art/Curtains-Red-Transparency-Light-424984584), licensed under [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). That texture remains CC BY 3.0. Minecraft is a trademark of Mojang Studios.
