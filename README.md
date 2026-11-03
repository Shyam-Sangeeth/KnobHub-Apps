<h1 align="center">Knob Hub apps</h1>

<p align="center">
  Apps for <a href="https://github.com/Shyam-Sangeeth/KnobHub">Knob Hub</a>, the round-screen knob controller for your PC.<br />
  Each app runs on your PC inside Knob Hub and shows its screens on the knob.
</p>

<p align="center">
  <img src="docs/audiodesk/home-audiodesk.png" width="160" alt="AudioDesk on the knob's Home ring" />
  <img src="docs/audiodesk/audiodesk-channels.png" width="160" alt="AudioDesk channels" />
  <img src="docs/audiodesk/audiodesk-channel-controls.png" width="160" alt="An AudioDesk channel" />
  <img src="docs/counter/home-counter.png" width="160" alt="Counter on the knob's Home ring" />
  <img src="docs/counter/counter-25.png" width="160" alt="Counter" />
  <img src="docs/displays/displays-main.png" width="160" alt="Displays, the main display" />
</p>

---

## Contents

- [Installing an app](#installing-an-app)
- [Apps](#apps)
  - [AudioDesk](#audiodesk)
  - [Counter](#counter)
  - [Displays](#displays)
- [Making your own app](#making-your-own-app)
- [How releases are laid out](#how-releases-are-laid-out)
- [Publishing an app](#publishing-an-app)

## Installing an app

In Knob Hub, go to the **Apps** page and click **Add apps**. It lists the apps released here as tiles: search for
one, then click **Install**, or **Update** when a newer version is out.

![Knob Hub's Add apps window](docs/knob-hub/hub-add-apps.png)

You can also download an app's `.knobapp` from [Releases](https://github.com/Shyam-Sangeeth/KnobHub-Apps/releases)
and use **Install from file...** in the same window.

Installed apps appear on the knob's Home ring and on Knob Hub's Apps page. There you can drag them into a different
order, turn them on or off the knob, change their settings, and remove them.

![Knob Hub's Apps page](docs/knob-hub/hub-apps.png)

> [!WARNING]
> Apps run on your PC with Knob Hub's permissions. Only install apps you trust; Knob Hub asks before installing
> anything.

## Apps

| App | Version | What it does |
|---|---|---|
| [AudioDesk](#audiodesk) | 1.0.2 | Channels, volume, Sonar and output devices of [AudioDesk](https://github.com/Shyam-Sangeeth/AudioDesk) |
| [Counter](#counter) | 1.0.0 | A small example: counts up and down as you turn the knob |
| [Displays](#displays) | 1.0.0 | Picks which display is the main one |

### AudioDesk

Controls [AudioDesk](https://github.com/Shyam-Sangeeth/AudioDesk)'s Game, Media and Aux channels from the knob: volume,
mute, whether each goes through SteelSeries Sonar, and where it plays.

<table>
  <tr>
    <td align="center"><img src="docs/audiodesk/audiodesk-channels.png" width="200" /><br />Channels</td>
    <td align="center"><img src="docs/audiodesk/audiodesk-channels-muted-switching.png" width="200" /><br />Game muted, Aux switching</td>
    <td align="center"><img src="docs/audiodesk/audiodesk-channel-controls.png" width="200" /><br />A channel</td>
  </tr>
  <tr>
    <td align="center"><img src="docs/audiodesk/audiodesk-channel-muted.png" width="200" /><br />Muted</td>
    <td align="center"><img src="docs/audiodesk/audiodesk-channel-no-sonar.png" width="200" /><br />Straight to the device</td>
    <td align="center"><img src="docs/audiodesk/audiodesk-not-running-start.png" width="200" /><br />AudioDesk isn't running</td>
  </tr>
</table>

- **Channels:** each channel is a ring in its colour, filled as far as its volume, with the device it plays on inside
  and a Sonar badge while it goes through Sonar. Muted channels are crossed out, and a spinning arc shows a device
  switch. Below are **Sonar** (every channel through Sonar) and **Headset | Home Theater**.
- **A channel** (press it): the volume, the channel's own Sonar on/off, and its output device. Press the knob to move
  between them and turn to change the selected one. Tap the icon or the volume %, or press twice quickly, to mute.
- **In step with AudioDesk:** changes on the knob show up in AudioDesk and the other way round. While a channel goes
  through Sonar, its volume is Sonar's own for that channel.
- **When AudioDesk isn't running,** the knob says so, with a **Start AudioDesk** button when it can find AudioDesk on
  the PC, and goes back to where you were once AudioDesk is running again.

**Needs:** [AudioDesk](https://github.com/Shyam-Sangeeth/AudioDesk/releases/latest) 1.0.0 or newer, running, with
**Knob support** on in AudioDesk's Settings tab (it's on by default).

**Settings** (on its row on Knob Hub's Apps page): **Volume step**, how much each click of the knob changes the volume
(1%, 2% by default, 5% or 10%).

### Counter

A small example app, and a starting point for writing your own. It opens at 0 and counts up by one for each click to
the right and down by one for each click to the left, never below 0. The number is drawn as big as fits in the middle
of a ring that fills once every 20 counts; each new lap fills in a new random bright colour.

<table>
  <tr>
    <td align="center"><img src="docs/counter/home-counter.png" width="200" /><br />On the Home ring</td>
    <td align="center"><img src="docs/counter/counter.png" width="200" /><br />Start</td>
    <td align="center"><img src="docs/counter/counter-25.png" width="200" /><br />25: the second lap</td>
  </tr>
</table>

### Displays

Picks the main display from the knob: the one with the Start menu and the taskbar's clock, where new windows open.

<table>
  <tr>
    <td align="center"><img src="docs/displays/home-displays.png" width="200" /><br />On the Home ring</td>
    <td align="center"><img src="docs/displays/displays-main.png" width="200" /><br />The main display</td>
    <td align="center"><img src="docs/displays/displays-other.png" width="200" /><br />Another display</td>
  </tr>
</table>

- **Cards:** each display Windows shows the desktop on is a card with its monitor's name. The main display comes
  first, with a green tick, then the others left to right as they're arranged.
- **Switching:** turn the knob to go through the displays, and press it (or tap the card) to make the one on show the
  main display, like **Make this my main display** in Windows' Settings. The displays keep their places round it, and
  the new main display moves to the front with the knob still on it. Windows may black out the screens for a moment
  while it switches.
- **In step with Windows:** displays plugged in or out, or a main display chosen in Settings, show up while the app
  is open.

**Needs:** Knob Hub and Knob OS built from 3 November 2026 on ([3fa0cc7](https://github.com/Shyam-Sangeeth/KnobHub/commit/3fa0cc7)), which draw its cards.

## Making your own app

The [wiki](https://github.com/Shyam-Sangeeth/KnobHub-Apps/wiki) explains how to make a Knob Hub app, from setting up to publishing: a step-by-step
tutorial, how apps work, every screen the knob can show, icons, testing, design guidelines and troubleshooting. Its
[For AI agents](https://github.com/Shyam-Sangeeth/KnobHub-Apps/wiki/For-AI-agents) page has all of it on one page for an AI coding agent.

To suggest your app for this list, [open an issue](https://github.com/Shyam-Sangeeth/KnobHub-Apps/issues) with a link
to its source code; apps here are reviewed before they're released. You can also publish apps in a repository of
your own: see [Publishing](https://github.com/Shyam-Sangeeth/KnobHub-Apps/wiki/Publishing).

## How releases are laid out

Each app has one release, tagged with the app's id (for example `audiodesk`), that holds every version of it. Each
version is two files:

- `<app id>-<version>.knobapp`: the app (a zip of its `app.json` and DLL), for example `audiodesk-1.0.2.knobapp`.
- `<app id>-<version>.app.json`: its details (name, description, icon, colour, version, author), so Knob Hub can list
  apps without downloading them.

The **All apps** release lists every app. It holds no app files, so Knob Hub ignores it; it's there so GitHub's
"Latest" mark points at an overview instead of one app.

Knob Hub offers the newest version of each app and downloads only over HTTPS. Before installing, it checks that the
download is the app the list showed.

## Publishing an app

The apps' source code is in the [Knob Hub repository](https://github.com/Shyam-Sangeeth/KnobHub/tree/main/hub/Plugins),
and [the wiki](https://github.com/Shyam-Sangeeth/KnobHub-Apps/wiki) explains how to make one. To publish one of them:

1. Bump `version` in the app's `app.json`.
2. Run `hub/Plugins/pack-release.ps1` in the Knob Hub repository. It builds every app and adds each version not
   released yet to its app's release here, creating the release for a new app (it needs the
   [GitHub CLI](https://cli.github.com/), logged in).

Knob Hub users then see **Update** on the app's tile.
