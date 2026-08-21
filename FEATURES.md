# OmniShade feature overview

OmniShade is the host runtime and per-game setup layer. This list describes the normal gaming build—not private authoring, capture, telemetry, calibration, or qualification tooling.

## Game-aware Setup

- Finds locally installed games while still allowing direct executable selection.
- Reads the selected executable's PE architecture and graphics imports without launching it.
- Selects the matching native 32-bit or 64-bit runtime.
- Shows the detected renderer, architecture, import evidence, and confidence before deployment.
- Reports existing proxy/wrapper candidates instead of silently overwriting or assuming compatibility.
- Supports install, runtime-only update, runtime-and-effects update, verify/repair, and uninstall workflows.
- Keeps operations scoped to the selected game and records backup/recovery information.
- Preserves personal presets and settings when the selected operation says it will.
- Explains uncertain or manually overridden choices in plain language.

## Renderer coverage

| Family | Routing |
|---|---|
| Direct3D 10 / 11 / 12 | DXGI proxy path |
| Direct3D 9 | Native D3D9 proxy path |
| DirectDraw / DirectX 1–7 | Legacy DirectDraw compatibility path |
| OpenGL | OpenGL proxy path |
| Vulkan | Native Vulkan layer path |
| DXVK | Recognized Vulkan-based arrangements where compatible |
| RTX Remix | Common wrapper arrangements where compatible |
| OpenXR | Optional companion variant for supported OpenXR titles |

A listed API is a supported route, not a promise that every game, driver, wrapper chain, or anti-cheat system will accept injection.

## Effect runtime and image pipeline

- ReShade FX language, preset, and effect-runtime compatibility.
- Color and depth resource access where the game exposes usable buffers.
- Depth-candidate management designed to handle changing frame conditions.
- Standard player-facing depth inputs for far-plane distance, upside-down depth, reversed depth, and logarithmic depth.
- Transactional effect reload: a working effect stays active until its replacement is ready.
- Validated effect cache behavior with recovery from invalid entries.
- Bounded startup compilation work, including a more conservative D3D12 startup path.
- HDR, color-space, and display-metadata coordination where the required information is available.
- Motion, temporal-history, and semantic coordination services for compatible effects.
- Integrated OmniToggler behavior for suppressing selected game effects without a separate consumer add-on DLL.
- Efficient no-work paths when no active effect or visible interface needs processing.

## Player overlay

- Compact **Omni Night** visual style shared with Setup.
- Movable and resizable floating window with bounded saved position and size.
- Task-focused pages: Home, Game Profiles, Settings, Performance, Troubleshooting, and About.
- One clear action rail for effect reload and Performance Mode.
- Contextual explanations for settings that materially affect compatibility or image behavior.
- Standard depth-input controls inside normal player settings.
- No source editor, render-graph capture, provider lab, calibration deck, or developer statistics page in consumer builds.

## Profiles, shaders, and OmniVisuals

- Balanced and Performance starting profiles.
- Package-level and per-effect shader selection during Setup.
- A small core effect set required by the host experience.
- Integrated OmniToggler support effects.
- Community shader packages can be selected where their own terms and compatibility allow.
- OmniVisuals is not bundled into OmniShade. It remains a separate, optional shader-only suite that requires a genuine OmniShade installation.

## Recovery and compatibility safeguards

- Backup-aware install, update, repair, and uninstall operations.
- Recovery journaling so interrupted operations can be diagnosed and rolled back.
- Architecture mismatch rejection instead of deploying a known-wrong DLL.
- Wrapper-chain warnings for existing proxy candidates.
- Startup recovery state and diagnostic logging for game-specific failures.
- Configuration writes are dirty-only and use safe replacement behavior.
- Repair restores OmniShade-managed files without claiming ownership of unrelated game files.

## Languages and accessibility

- English.
- Deutsch.
- Español.
- Français.
- Română.
- Keyboard focus is visible throughout Setup.
- Tooltips wrap and remain screen-aware.
- Motion is restrained and follows reduced-motion behavior where available.

## Privacy and distribution

- Free donationware: payment is not required.
- No advertising.
- No required OmniVex account.
- No OmniVex-operated gameplay or performance telemetry service.
- Official builds are distributed outside GitHub; this repository contains documentation and approved promotional images only.
- The installer may contact named third-party HTTPS services for optional package or compatibility information. The download includes the complete privacy notice.

## Important limits

- OmniShade is not guaranteed to work in every game.
- Injection may be prohibited by a game's publisher or anti-cheat policy.
- Screen-space effects only see the buffers and metadata the game exposes.
- HDR behavior depends on the game, swap-chain mode, display, driver, and effect.
- OmniShade does not turn screen-space shaders into engine-integrated hardware ray tracing.
- A newer runtime or more expensive preset is not automatically better for every title.
- Real compatibility and performance claims require testing on the specific game and hardware.

Return to the [OmniShade overview](README.md).
