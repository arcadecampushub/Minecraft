# Minecraft

Eaglercraft (browser Minecraft) builds served for Arcade Campus Hub
(https://www.arcadecampushub.online/).

| Version | Path | Notes |
| --- | --- | --- |
| EaglercraftX 1.8.8 | `/1.8.8/index.html` | Single-file build: everything it needs is in one HTML file. |
| Eaglercraft 26.1.2 | `/26.1.2/index.html` | The source zip routes `assets.epk` through Git LFS, so this zip holds only the 134-byte LFS pointer, not the real 369 MB asset pack. The build fetches `assets.epk` at startup. |

Worlds are kept in the browser's IndexedDB, one store per version; they do not
carry between builds. `save-bridge.html` at the repo root lets the hub back a
world up to a signed-in account.
