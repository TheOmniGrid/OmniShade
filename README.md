<p align="center">
  <img src="media/banner-animated.gif" width="100%" alt="OmniShade — precision post-processing for games">
</p>

<p align="center">
  <img alt="Version 1.0.0" src="https://img.shields.io/badge/version-1.0.0-8468FF?style=flat-square">
  <img alt="Windows" src="https://img.shields.io/badge/platform-Windows-54D6FF?style=flat-square">
  <img alt="Free donationware" src="https://img.shields.io/badge/donationware-free-32D99B?style=flat-square">
  <img alt="No ads" src="https://img.shields.io/badge/ads-none-202733?style=flat-square">
  <img alt="No gameplay telemetry" src="https://img.shields.io/badge/gameplay%20telemetry-none-202733?style=flat-square">
</p>

<!-- Quick navigation. Each chip jumps to a README section or maintained
     document. Keep the fragment links aligned with GitHub's heading slugs. -->
<p align="center">
  <a href="#getting-omnishade"><img alt="Get OmniShade" src="https://img.shields.io/badge/%E2%86%93%20Get%20OmniShade-8468FF?style=for-the-badge"></a>
  <a href="#why-omnishade"><img alt="Overview" src="https://img.shields.io/badge/Overview-25213B?style=for-the-badge"></a>
  <a href="FEATURES.md"><img alt="Features" src="https://img.shields.io/badge/Features-25213B?style=for-the-badge"></a>
  <a href="#how-it-fits-together"><img alt="How it works" src="https://img.shields.io/badge/How%20it%20works-25213B?style=for-the-badge"></a>
  <a href="#see-it"><img alt="Screenshots" src="https://img.shields.io/badge/Screenshots-25213B?style=for-the-badge"></a>
  <a href="#requirements-and-compatibility"><img alt="Compatibility" src="https://img.shields.io/badge/Compatibility-25213B?style=for-the-badge"></a>
  <a href="FAQ.md"><img alt="FAQ" src="https://img.shields.io/badge/FAQ-25213B?style=for-the-badge"></a>
  <a href="SUPPORT.md"><img alt="Support" src="https://img.shields.io/badge/Support-25213B?style=for-the-badge"></a>
  <a href="CHANGELOG.md"><img alt="Changelog" src="https://img.shields.io/badge/Changelog-25213B?style=for-the-badge"></a>
</p>

> [!IMPORTANT]
> This is OmniShade's **documentation and support repository**. It intentionally contains no source code, installer, runtime DLL, shader payload, preset archive, or GitHub Release. Official builds are distributed outside GitHub.

## Why OmniShade

OmniShade is a game-first, ReShade-derived post-processing runtime. It brings renderer-aware setup, dependable per-title recovery, a focused in-game interface, and a modern effects foundation together in one package—without turning ordinary play into a developer workflow.

![Abstract optical illustration of the OmniShade image pipeline](media/omnishade-pipeline-art.png)

| Game-aware | Reversible | Player-focused |
|---|---|---|
| Select the real game executable. Setup reads its architecture and renderer evidence without launching it. | Install, update, repair, and uninstall stay scoped to the selected title, with backup and recovery data. | Home, Game Profiles, Settings, Performance, Troubleshooting, and About—no capture lab or developer console in consumer builds. |

### One runtime, broad renderer coverage

OmniShade routes the correct native x86 or x64 runtime for Direct3D 9, Direct3D 10/11/12, DirectDraw, OpenGL, and Vulkan. Common DXVK and RTX Remix arrangements are recognized, and OpenXR-aware variants are available where the title and runtime path support them.

### Built for the image pipeline

The runtime provides ReShade FX compatibility, color and depth access, depth-input controls, cache-aware effect loading, HDR/color coordination, motion and temporal services for compatible effects, and integrated OmniToggler behavior without a separate consumer add-on DLL.

### Honest by design

OmniShade does not promise universal compatibility, guaranteed frame-rate gains, hardware ray tracing, or anti-cheat safety. The game, engine, graphics API, driver, wrapper chain, and exposed buffers still decide what is possible.

## How it fits together

![Diagram showing a game flowing through its graphics API into OmniShade and compatible effects](media/omnishade-runtime-flow.svg)

**OmniShade is the runtime.** **OmniVisuals is the optional shader suite.** OmniVisuals remains shader-only, installs separately, and requires a genuine OmniShade installation. OmniToggler remains integrated into OmniShade.

## See it

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="media/omnishade-installer-target-v2.jpg" alt="OmniShade Setup target selection with locally detected games"><br>
      <sub><strong>Choose the game.</strong> Search detected titles or browse directly to the actual executable.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="media/omnishade-installer-renderer.jpg" alt="OmniShade Setup renderer detection showing DirectX and 64-bit evidence"><br>
      <sub><strong>Verify the renderer.</strong> Architecture, API, import evidence, and wrapper conflicts are visible before deployment.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <img src="media/omnishade-installer-operation.jpg" width="70%" alt="OmniShade Setup update, repair, and uninstall choices"><br>
      <sub><strong>Stay in control.</strong> Update only the runtime, modify effects, verify and repair, or remove OmniShade-managed files.</sub>
    </td>
  </tr>
</table>

## Feature highlights

- **Automatic architecture selection:** native 32-bit and 64-bit payloads chosen from the executable—not from a filename guess.
- **Renderer-aware deployment:** clear routing for modern DirectX, D3D9, DirectDraw, OpenGL, Vulkan, DXVK, RTX Remix, and optional OpenXR paths.
- **Wrapper-chain awareness:** existing proxy candidates are reported instead of silently overwritten or assumed compatible.
- **Depth Buffer 2.0 foundation:** depth-candidate management plus standard far-plane, upside-down, reversed, and logarithmic controls.
- **Modern effect runtime:** transactional reload, cache validation, bounded startup work, HDR/color metadata, and compatible temporal/motion coordination.
- **Integrated OmniToggler:** suppress selected game effects through the host runtime without shipping another consumer DLL.
- **Movable, resizable overlay:** a compact Omni Night interface that remembers bounded placement and keeps player tasks together.
- **Five complete languages:** English, Deutsch, Español, Français, and Română across Setup and the consumer runtime.
- **Gaming-only package:** no developer, capture, telemetry, calibration, or shader-analysis surfaces in normal builds.
- **No ads or required account:** local per-game operation with no OmniVex-operated gameplay telemetry service.

[Explore the complete consumer feature overview →](FEATURES.md)

## Requirements and compatibility

| Area | Requirement |
|---|---|
| OS | Windows 10 or Windows 11 |
| Architecture | x86 or x64 game executable |
| Graphics | A supported Direct3D, DirectDraw, OpenGL, or Vulkan path |
| Permissions | Write access to the selected game folder; some locations may require elevation |
| Online games | Check the publisher's modding and anti-cheat rules first; when injection is prohibited, do not use OmniShade |

Compatibility is game-specific. A supported API does not prove that every effect, depth path, overlay, or third-party wrapper will work in every title. See the [FAQ](FAQ.md) before assuming support.

## Getting OmniShade

OmniShade is **free donationware**: payment is not required, there are no ads, and support through Patreon or Ko-fi is entirely optional. GitHub intentionally hosts documentation and screenshots only—not the installer or source.

For the current build, distribution help, or a no-payment copy, contact **[omnivex@theomnigrid.biz](mailto:omnivex@theomnigrid.biz)**. If OmniShade is useful to you and you want to fund continued work, use either official page:

<p align="center">
  <a href="https://www.patreon.com/TheOmniGrid"><img src="media/support-patreon.svg" height="64" alt="Support OmniShade on Patreon"></a>
  &nbsp;&nbsp;
  <a href="https://ko-fi.com/theomnigrid"><img src="media/support-kofi.svg" height="64" alt="Support OmniShade on Ko-fi"></a>
</p>

No payment is required. Please do not mirror the installer, runtime, or private delivery links; share this repository or the official support pages instead.

## Documentation

| Guide | What it covers |
|---|---|
| [Features](FEATURES.md) | Complete consumer-facing capability list and boundaries |
| [FAQ](FAQ.md) | Installation, compatibility, privacy, redistribution, and uninstall answers |
| [Support](SUPPORT.md) | Reproduction details, logs, privacy, and contact channels |
| [Security](SECURITY.md) | Private vulnerability reporting and safe disclosure |
| [Changelog](CHANGELOG.md) | OmniShade 1.0.0 highlights |
| [Repository notice](REPOSITORY_NOTICE.md) | Why this public repository contains documentation only |
| [Documentation license](LICENSE.md) | Rights applying to this public documentation and artwork |

## Support and feedback

Bug reports and feature requests are welcome through [GitHub Issues](https://github.com/TheOmniGrid/OmniShade/issues). Please remove usernames, local paths, account identifiers, and other personal information from logs or screenshots before posting. Security reports belong in private email, not a public issue.

## Independence and credits

OmniShade is an independent ReShade-derived distribution. ReShade is developed by its respective authors. OmniShade is not endorsed by or affiliated with ReShade, game publishers, GPU vendors, Patreon, or Ko-fi. Third-party licenses and required notices are included with authorized product distributions.

---

<p align="center">
  <img src="media/omnishade-symbol.png" width="54" alt="OmniShade fx symbol"><br>
  <sub>Built by <strong>OmniVex</strong> · Free donationware · No ads · No gameplay telemetry</sub>
</p>
