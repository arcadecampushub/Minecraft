# Minecraft

Eaglercraft (browser Minecraft) builds served for Arcade Campus Hub
(https://www.arcadecampushub.online/).

| Version | Path | Notes |
| --- | --- | --- |
| EaglercraftX 1.8.8 | `/1.8.8/index.html` | Single-file build: everything it needs is in one HTML file. |
| Eaglercraft 26.1.2 | `/26.1.2/index.html` | The 369 MB asset pack lives in the [assets-26.1.2 release](https://github.com/arcadecampushub/Minecraft/releases/tag/assets-26.1.2) and is served CORS-clean through `https://mc.arcadecampushub.online/assets.epk` (Cloudflare Worker). PatentSMP is baked into the client's server list via `wss://mc.arcadecampushub.online/`. |

Worlds are kept in the browser's IndexedDB, one store per version; they do not
carry between builds. `save-bridge.html` at the repo root lets the hub back a
world up to a signed-in account.

The 26.1.2 gateway (Velocity + the EaglercraftXVelocity plugin, WS on
127.0.0.1:25560) runs on the PatentSMP machine and is exposed at
`wss://mc.arcadecampushub.online` through a Cloudflare Tunnel.
