<div align="center">

<img src="https://raw.githubusercontent.com/cloudcord-mod/release-hub/main/assets/cloudcord-logo.png" width="250" alt="CloudCord logo">

# CloudCord macOS

**Native preview installers for Apple Silicon and Intel Macs.**

[**Downloads**](https://getcloudcord.com/#download) · [**Release Hub**](https://github.com/cloudcord-mod/release-hub) · [**Builds**](https://github.com/cloudcord-mod/macos/actions) · [**Status**](https://getcloudcord.com/status)

</div>

---

## Install

Open **About This Mac** to check your processor, then download the matching preview disk image.

| Mac | Download |
| --- | --- |
| Apple Silicon | [ARM64 DMG](https://getcloudcord.com/download/mac/arm64) |
| Intel | [x64 DMG](https://getcloudcord.com/download/mac/x64) |

Open the DMG and follow the installer prompts. For launch or install issues, include your macOS version, processor, Discord build, and the exact error in your [bug report](https://github.com/cloudcord-mod/release-hub/issues).

## Build locally

The [macOS workflow](.github/workflows/build.yml) builds the standalone CX runtime from a pinned Release Hub commit and packages it for both architectures. To reproduce the packaging locally, run these steps in their respective checkouts.

1. In `desktop/client` in the Release Hub checkout, run `pnpm install --frozen-lockfile` and `pnpm buildStandalone`.
2. From this macOS checkout, run the packaging script with the standalone ASAR you built.

```sh
bash desktop/client/scripts/build-mac.sh /path/to/desktop.asar
```

GitHub Actions uploads preview artifacts. The official downloads are available through Release Hub.

[Source and history before the repository split](https://github.com/cloudcord-mod/release-hub/commit/56f21964c42ff1c4c115195d6e51e4efaf8bd2e1).

## Credits and license

CloudCord is maintained by [Xohus](https://xohus.lol/). The DMGs bundle the CloudCord desktop runtime, which builds on Sincord, Vencord, and their contributors. [Desktop credits](desktop/client/CREDITS.md) · [Runtime license](https://github.com/cloudcord-mod/release-hub/blob/main/desktop/client/LICENSE) · [CloudCord license](https://github.com/cloudcord-mod/release-hub/blob/main/license)
