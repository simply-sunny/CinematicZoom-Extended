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
| Icon | `src/main/resources/assets/cinematiczoom/icon.png` — final 512×512 PNG (velvet stage, spyglass, clapperboard, `++`) |
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

Modrinth accepts gallery files up to **5 MiB** each. Use PNG or JPEG screenshots.

| Order | Asset | Caption |
| --- | --- | --- |
| 1 | Hero screenshot, 1280×720 | Cinematic zoom with animated black bars |
| 2 | Screenshot of settings screen | Two independent profiles: Cinematic and Regular |
| 3 | Ultrawide/snap screenshot | Ultra-wide zoom and snap targets |
| 4 | HUD comparison | Hide the HUD, crosshair, and hands independently |
| 5 | Cinematic camera screenshot | Smooth per-frame zoom and bar animation |

Alt text should repeat the caption.

---

# Cinematic Zoom Extended

Smooth, cinematic zoom for **Fabric 1.20.1–26.3** — now with two independent zoom profiles, custom easing, ultra-wide zoom, snap targets, and granular HUD control.

Cinematic Zoom Extended is a client-side mod and a feature-rich fork of [Cinematic Zoom (Fabric)](https://modrinth.com/mod/cinematic-zoom-fabric) by [Mel1x](https://github.com/mel1x), published as a separate project with permission. The original zoom concept comes from [Cinematic Zoom](https://www.curseforge.com/minecraft/mc-mods/cinematic-zoom) by [KubePixel](https://www.curseforge.com/members/kubepixel/projects). This project is not affiliated with or endorsed by KubePixel or Mel1x.

## Why Extended?

The 1.3 release gave you cinematic zoom with bars. Extended turns it into a complete camera toolkit:

- A separate **Regular Zoom** profile for smooth zoom without bars.
- Independent timing, curves, starting zoom, and HUD settings for each profile.
- Live black-bar adjustment and optional persistence.
- Ultra-wide zoom, discrete wheel stepping, and snap/magnetize targets.
- Mouse-sensitivity scaling and view-bobbing removal.
- Independent hiding of the HUD, crosshair, and first-person hands.
- A config screen in Mod Menu via Cloth Config (both required).

## Features

### Two zoom profiles

- **Cinematic Zoom** — animated black bars, optional cinematic camera, and live bar controls.
- **Regular Zoom** — the same per-frame smoothing without bars.
- Each profile has its own keybind, starting zoom, zoom-in/out duration, easing curves, toggle mode, magnetize/snap settings, and HUD options.

### Smooth motion

- Per-frame easing instead of 20 TPS stepping.
- Six curves: exponential, cubic ease-out, cubic ease-in, cubic ease-in-out, linear, and sine.
- Separate zoom-in and zoom-out durations, from instant to five seconds.

### Framing controls

- **Animated black bars** with adjustable height (0–50% of the screen per bar).
- **Arrow-key bar adjustment** while zoomed, with custom step size and smoothing.
- **Ultra-wide zoom** — scroll below 1× down to 0.5×.
- **Discrete mouse-wheel zoom** — fixed increments per notch.
- **Snap/magnetize targets** — accept zoom factors (`2x`) or FOV values (`45fov`, `60°`).

### HUD and camera

- Hide the HUD, crosshair, and first-person hands independently.
- Hide the F3 debug overlay while the HUD is hidden during zoom.
- Optional cinematic camera and view-bobbing removal.
- Mouse sensitivity scales with the zoom level.

### Quality of life

- Hold-to-zoom or toggle mode, per profile.
- Client-side only — no server installation.
- English and Russian translations.
- Automatic config migration from Cinematic Zoom 1.3.
- First-run import of settings from Zoomify, Ok Zoomer, Just Zoom, and other zoom-mod configs.

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
- **Cloth Config** — **required**; see the minimum versions above.
- **Mod Menu** — **required**; adds the in-game settings screen.
- **Java** — 17 for 1.20.1, 21 for 1.21.x, 25 for 26.x.

## Installation

1. Install Fabric Loader, Fabric API, Cloth Config, and Mod Menu for your Minecraft version.
2. Put the matching `cinematiczoom-extended-<minecraft>-1.0.0.jar` in `mods`.
3. Keep only one Cinematic Zoom build in `mods`: Extended replaces the original, and the two cannot run together.
4. Launch the game.

## Usage

| Action | Default key |
| --- | --- |
| Cinematic Zoom | `C` |
| Zoom without bars | Unbound — set it in Controls |
| Increase bar size | `↑` |
| Decrease bar size | `↓` |

All keys are rebindable under **Options → Controls → Key Binds → Cinematic Zoom**.

- Hold the zoom key to zoom in; release to return smoothly. Enable **Toggle zoom** to press once on and once off.
- The regular zoom key is unbound by default so it does not clash with the cinematic key.
- Use the mouse wheel while zooming to adjust magnification.
- With **Ultra-wide zoom** enabled, keep scrolling back past 1× to reach 0.5×.
- Zoom and overlays are disabled while a GUI screen is open.

## Configuration

Open **Mod Menu → Cinematic Zoom Extended → Settings**, or edit `config/cinematiczoom.json`:

- **Windows:** `%appdata%\.minecraft\config\cinematiczoom.json`
- **macOS:** `~/Library/Application Support/minecraft/config/cinematiczoom.json`
- **Linux:** `~/.minecraft/config/cinematiczoom.json`

The full option reference, defaults, ranges, and snap-target syntax are in the [GitHub README](https://github.com/simply-sunny/CinematicZoom-Extended#configuration).

### Importing settings from other zoom mods

On first launch, if `cinematiczoom.json` does not exist, Extended scans the `config` folder for zoom-mod configs and imports what it recognizes:

- **Zoomify** — `config/zoomify.json`: zoom amount, in/out times and curves, toggle mode, sensitivity, view bobbing, cinematic camera, scroll zoom, and secondary zoom.
- **Ok Zoomer** — `config/ok_zoomer/config.toml` or a legacy `okzoomer.json`: transition times and curves, crosshair, view bobbing, sensitivity, cinematic camera, zoom mode, and scroll zoom.
- **Just Zoom** — `config/justzoom/config.json`: base zoom, animation durations, sensitivity, smooth camera, hands, and HUD visibility.
- **Any other zoom config** — any JSON or TOML file whose path contains `zoom`, matched by key name.
- **WI Zoom / Logical Zoom** — store no config file; their zoom is built in, so there is nothing to import.

Existing `cinematiczoom.json` files are never overwritten. To re-run the import, delete `config/cinematiczoom.json` and relaunch.

### Snap target examples

```text
2x, 4x, 8x
30fov, 45fov, 60fov
5, 10, 20      (values below 20 are zoom factors)
30, 45, 60     (values of 20 or above are FOV degrees)
```

Enable **Magnetize zoom targets** to step strictly between the parsed values with the mouse wheel.

## Migrating from Cinematic Zoom 1.3

1. Keep only one Cinematic Zoom build in `mods` — Extended replaces the original `cinematiczoom-*.jar`.
2. Install the matching Extended JAR.
3. Keep `config/cinematiczoom.json` — it is migrated automatically.

Extended uses a new mod ID and declares the original mod incompatible, so installing both produces a clear loader error instead of double zoom. The config file name is deliberately unchanged for a seamless upgrade.

## Compatibility

- Client-side only; servers do not need the mod.
- **Do not install the original Cinematic Zoom alongside Extended.**
- Do not combine with other zoom/FOV mods (Zoomify, Ok Zoomer, Just Zoom, Logical Zoom, etc.); Extended can import their settings on first launch instead.
- Sodium, Iris, and shader packs have no known conflicts, but are not specifically tested in 1.0.0; report version-specific issues.
- OptiFine is not supported.
- Quilt is not officially tested; use the Fabric build at your own risk.
- Cloth Config and Mod Menu are required.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| Missing `cloth-config2` | Install Cloth Config for your Minecraft version. |
| Missing `modmenu` | Install Mod Menu for your Minecraft version. |
| Incompatible with `cinematiczoom` | Keep only one Cinematic Zoom jar in `mods`. |
| Game crashes on launch | Check your Java version: 17 / 21 / 25 depending on Minecraft. |
| Zoom key does nothing | Bind **Cinematic Zoom** (and **Zoom (no bars)**) under Controls. |
| Mouse wheel does not zoom | Enable **Mouse wheel during zoom** and hold the zoom key. |
| Bars do not appear | Use the cinematic key and set the bar height above 0. |
| F3 overlay disappears | Disable **Hide HUD**; the debug overlay follows the HUD setting. |
| Settings screen missing | Install both Mod Menu and Cloth Config. |
| Broken config | Delete `config/cinematiczoom.json` and relaunch. |

When reporting an issue, include `logs/latest.log`, your Minecraft version, the mod version, and the Fabric Loader version.

## Credits

- **KubePixel** — original Cinematic Zoom concept and Forge mod.
- **Mel1x** — upstream Fabric implementation and the 1.3 base.
- **simply-sunny** — Extended features, tests, and this release.
- **ColoredChromium** — velvet curtain texture used in the icon ([CC BY 3.0](https://creativecommons.org/licenses/by/3.0/)).

Published with Mel1x's permission: [PR #8](https://github.com/mel1x/CinematicZoom/pull/8#issuecomment-6139411837). Not affiliated with or endorsed by KubePixel, Mel1x, Mojang Studios, or Microsoft.

## License

The mod code and original assets are MIT. Original work copyright © 2025 Melix; changes copyright © 2026 Saunak Karnati (simply-sunny). See the [LICENSE](https://github.com/simply-sunny/CinematicZoom-Extended/blob/main/LICENSE).

The project icon incorporates a velvet curtain texture by [ColoredChromium](https://www.deviantart.com/coloredchromium/art/Curtains-Red-Transparency-Light-424984584), licensed under [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). That texture remains under CC BY 3.0; the icon may be reused under the same terms. Minecraft is a trademark of Mojang Studios.
