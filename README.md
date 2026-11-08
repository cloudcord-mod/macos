# CloudCord macOS

Native installer and DMG packaging for Apple Silicon and Intel.

- [Downloads](https://getcloudcord.com)
- [Release and integration repository](https://github.com/cloudcord-mod/release-hub)
- [Source and history before the split](https://github.com/cloudcord-mod/release-hub/commit/56f21964c42ff1c4c115195d6e51e4efaf8bd2e1)

The macOS workflow builds the CX runtime from a pinned release-hub commit and embeds it in both disk images. For a local build, run `pnpm buildStandalone` in the release-hub checkout’s `desktop/client` directory, then run `bash desktop/client/scripts/build-mac.sh /path/to/desktop.asar` in this checkout.

This repository's Actions builds upload artifacts. The integration repository continues to publish official releases.
