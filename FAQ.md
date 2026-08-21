# Frequently asked questions

## Which Windows version is targeted?

Windows 11 is OmniShade's primary supported, development and release-
qualification target. Windows 10 may continue to run, but new compatibility
claims and release testing no longer target it, so it is best-effort and not
guaranteed.

## What is OmniShade?

OmniShade is the runtime and per-game installer layer for real-time post-processing. It detects the selected game's architecture and renderer, deploys the matching runtime, hosts compatible effects and presets, and provides the in-game player interface.

## Is OmniShade free?

Yes. OmniShade is free donationware: payment is not required, there are no ads, and Patreon or Ko-fi support is optional.

## Is OmniShade a shader pack?

Not primarily. It includes a small core effect set and can install selected shader packages, but OmniShade is the host runtime. The complete OmniVisuals suite is a separate, optional shader-only product.

## Where is the installer?

Not on GitHub. Contact [omnivex@theomnigrid.biz](mailto:omnivex@theomnigrid.biz) for the current official distribution or use the official Patreon/Ko-fi pages. No payment is required.

## Is the source code on GitHub?

No. This repository contains documentation, approved screenshots, support information, and marketing artwork only. It intentionally contains no application source, installer, DLL, shader payload, preset archive, or GitHub Release.

## Does it work in every game?

No universal injector can promise that. Compatibility depends on the graphics API, engine, executable architecture, anti-cheat policy, overlays, wrapper chain, driver, and the buffers the game exposes.

## Which graphics APIs are supported?

OmniShade has routes for Direct3D 9, Direct3D 10/11/12, DirectDraw, OpenGL, and Vulkan, including common DXVK and RTX Remix arrangements. OpenXR-aware variants are available where the title and runtime path support them.

## Does OmniShade improve frame rate?

It is a post-processing runtime, not a universal performance booster. Some effects cost GPU time; Performance Mode and lighter presets can reduce OmniShade's own overhead, but results remain game-, effect-, resolution-, and hardware-specific.

## Is OmniVisuals included?

No. OmniVisuals is installed separately, remains shader-only, and requires a genuine OmniShade host. OmniShade never treats OmniVisuals as a replacement runtime.

## Is OmniToggler another required download?

No. OmniToggler behavior is integrated into OmniShade. The normal consumer package does not require a separate OmniToggler add-on DLL.

## Does OmniShade collect telemetry?

OmniShade does not send gameplay or performance telemetry to an OmniVex service. Setup may contact named third-party HTTPS endpoints for optional package or compatibility metadata. The distributed product includes the full privacy notice.

## Is online or competitive use safe?

Do not assume so. Check the game's rules and anti-cheat documentation first. If injection or visual modification is prohibited, do not use OmniShade in that game or mode.

## Can I redistribute the installer?

Do not mirror the installer, runtime, private delivery URL, or complete OmniVex package. Share this repository or the official Patreon/Ko-fi pages instead. Rights in third-party portions remain governed by their original licenses and notices.

## How do I repair or uninstall it?

Run the same Setup, choose the exact game executable, verify the detected renderer, and select **Verify and repair OmniShade** or **Uninstall OmniShade and effects**. Repair preserves personal presets and settings where the operation says it will.

## Which languages are available?

English, German, Spanish, French, and Romanian.

## Where do I report a problem?

Use [GitHub Issues](https://github.com/TheOmniGrid/OmniShade/issues) for ordinary bugs and feature requests. Read [SUPPORT.md](SUPPORT.md) first. Send security-sensitive reports privately as described in [SECURITY.md](SECURITY.md).
