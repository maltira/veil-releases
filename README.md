# Veil

A minimal VPN client for Linux and Windows, powered by [Xray-core](https://github.com/XTLS/Xray-core).

This repository hosts the official builds of Veil and its issue tracker. The source code is closed.

## Download

Get the latest build from [Releases](https://github.com/maltira/veil-releases/releases/latest).

| Platform | Package |
| --- | --- |
| Linux | `.deb`, `.rpm`, `.AppImage` |
| Windows | `.exe` installer |

## Features

- Import servers and subscriptions from links: VLESS, VMess, Trojan, Shadowsocks, Xray JSON and `incy://` links
- Subscription details: traffic usage, expiry date and provider announcements
- Server latency checks and automatic selection of the fastest server
- System proxy or TUN mode
- Connection check, live speed and event log
- Tray icon, autostart and opening of proxy links (in installed builds)

## Notes

- **TUN on Linux** works in the `.deb` and `.rpm` packages only, not in the AppImage. On first use the system asks for the administrator password once.
- **TUN on Windows** needs administrator rights. Veil offers to restart itself as administrator.
- Windows support is in early testing.

## Feedback

Found a bug or have a suggestion? [Open an issue](https://github.com/maltira/veil-releases/issues). Please include the Veil version and system from the *About* page, and do not share subscription links or server keys.

## License

The source code is closed, all rights reserved. Veil includes [Xray-core](https://github.com/XTLS/Xray-core) (MPL-2.0), Electron and other open-source components under their own licenses.

Country flags are drawn with [Twemoji](https://github.com/twitter/twemoji) artwork (© Twitter, Inc. and other contributors), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
