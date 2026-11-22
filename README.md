# Krodin

Krodin is a native client for [Krunker.io](https://krunker.io), with OpenGL and Vulkan renderers. It plays in live Krunker lobbies (public, custom and ranked) and on Krodin's own servers.

This repository only hosts Krodin's releases. The source code is private.

## Download

Get the latest build from [Releases](../../releases). Pick one:

- **Installer:** run `Krodin-Setup-<version>.exe`. It installs for your user only, needs no admin rights and adds a Start menu shortcut. It isn't code-signed yet, so Windows SmartScreen will warn you the first time: choose "More info", then "Run anyway".
- **Zip:** unzip it into a new folder and run `Krodin.exe`. `README-TESTERS.txt` inside the zip covers first-time setup.

Your settings, logs and mods are kept in `%LOCALAPPDATA%\Krodin`, so updating doesn't touch them.

## Changes

See [CHANGELOG.md](CHANGELOG.md).

## Reporting problems

Open an issue and include:
- `krunker-network.log` from your logs folder (Settings → Gameplay → Diagnostics → Open logs folder, or `%LOCALAPPDATA%\Krodin\logs`);
- your GPU, CPU and driver version;
- what you were doing when it happened.

The log never contains your Krunker login token.
