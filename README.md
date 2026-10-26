# Knob Hub apps

Apps for [Knob Hub](https://github.com/Shyam-Sangeeth/KnobHub), the PC controller built on a round-screen knob. Each app runs on your PC inside Knob Hub and shows its screens on the knob.

## Installing an app

In Knob Hub, open **Add apps**: it lists the apps released here, with **Install** (or **Update** when a newer version is out). You can also download an app's `.knobapp` from [Releases](https://github.com/Shyam-Sangeeth/KnobHub-Apps/releases) and use **Install from file…**.

Apps run with Knob Hub's permissions on your PC: only install apps you trust.

## Apps

| App | What it does |
| --- | --- |
| AudioDesk | Channels, volume, Sonar and output devices of [AudioDesk](https://github.com/Shyam-Sangeeth/AudioDesk) (AudioDesk must be running) |
| Counter | A small example: counts up and down as you turn the knob |

## How releases are laid out

Each release is one version of one app, tagged `<app id>-v<version>` (for example `audiodesk-v1.0.0`), with two files:

- `<app id>.knobapp`: the app (a zip of its `app.json` and DLL)
- `<app id>.app.json`: its details (name, description, icon, colour, version, author), so Knob Hub can list apps without downloading them

Knob Hub offers the newest version of each app. The apps' source code is in the [Knob Hub repository](https://github.com/Shyam-Sangeeth/KnobHub/tree/main/hub/Plugins); `hub/Plugins/pack-release.ps1` there builds them and publishes new versions here.
