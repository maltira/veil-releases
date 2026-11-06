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

## Your data and uninstalling

Veil keeps everything locally: subscriptions, settings and a random device ID. Nothing is sent anywhere except to your subscription provider.

| System | Data folder |
| --- | --- |
| Linux | `~/.config/veil` |
| Windows | `%APPDATA%\veil` |

To erase all subscriptions and settings, close Veil and delete that folder. The next launch starts from scratch.

Before uninstalling, turn off **Launch at login** and **Open links in Veil** in *Settings → System*. Removing the package cannot clean files in your own profile, so if you forget, a few harmless leftovers stay behind:

- `~/.config/autostart/veil.desktop` (autostart, Linux)
- lines `x-scheme-handler/…=veil.desktop` for `incy`, `vless`, `vmess`, `trojan`, `ss` in `~/.config/mimeapps.list` (Linux)
- `~/.local/share/applications/veil.desktop` and `~/.local/share/icons/veil-custom.png`, only if you changed the app icon (Linux)
- the *Veil* entry in *Task Manager → Startup apps* (Windows)

Veil restores your system proxy when it disconnects or quits. The TUN permission on Linux belongs to the installed program file and goes away when you remove the package.

## Feedback

Found a bug or have a suggestion? [Open an issue](https://github.com/maltira/veil-releases/issues). Please include the Veil version and system from the *About* page, and do not share subscription links or server keys.

## License

The source code is closed, all rights reserved. Veil includes [Xray-core](https://github.com/XTLS/Xray-core) (MPL-2.0), Electron and other open-source components under their own licenses.

Country flags are drawn with [Twemoji](https://github.com/twitter/twemoji) artwork (© Twitter, Inc. and other contributors), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
