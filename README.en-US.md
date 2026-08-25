# eFootball Toolkit PRO

<p align="center">
  <strong>Match monitoring, in-game overlay, and network tools for eFootball on Windows and consoles.</strong>
</p>

<p align="center">
  <a href="README.md"><img src="docs/images/language-pt-br.svg" alt="Português (Brasil)" height="42"></a>
  <a href="README.en-US.md"><img src="docs/images/language-en-us.svg" alt="English (US)" height="42"></a>
  <a href="README.es-ES.md"><img src="docs/images/language-es-es.svg" alt="Español (España)" height="42"></a>
</p>

<p align="center">
  <a href="https://mixdev-br.github.io/eFootballToolkitPRO/?lang=en"><strong>Official website</strong></a>
  ·
  <a href="https://github.com/MixDev-br/eFootballToolkitPRO/releases/latest"><strong>Download PRO</strong></a>
  ·
  <a href="https://github.com/MixDev-br/eFootballToolkitPRO/releases/tag/trial-v2.1.1"><strong>Try it on Windows for 5 days</strong></a>
  ·
  <a href="OPENWRT_MOBILE_GUIDE.md"><strong>Mobile and OpenWrt guide (Portuguese)</strong></a>
</p>

<p align="center">
  <img alt="Version 2.1.1" src="https://img.shields.io/badge/version-2.1.1-22d3ee">
  <img alt="Windows 10 and 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-2563eb">
  <img alt="Compatible with Steam and Xbox PC" src="https://img.shields.io/badge/eFootball-Steam%20%7C%20Xbox%20PC-10b981">
  <img alt="Available languages" src="https://img.shields.io/badge/languages-PT%20%7C%20EN%20%7C%20ES-a855f7">
</p>

> This is the official distribution channel for eFootball Toolkit PRO. The repository contains ready-to-use packages, the update manifest, and public documentation.

## Overview

The Toolkit brings together information that is normally scattered or hidden while searching for matches:

- real-time session ping, region, distance, and endpoint;
- identification of P2P and server-hosted matches;
- compact in-game overlay;
- server center with country-based measurements;
- game modes and temporary firewall rules;
- match, opponent, and rematch history;
- Xbox and PlayStation controller diagnostics;
- support for eFootball on **Steam** and **Xbox PC**;
- PC, PlayStation, and Xbox monitoring through **OpenWrt**;
- Mobile app for monitoring matches and controlling X1 and COOP modes.

## Explore the application

### Match monitor

![Main match monitor screen](docs/images/01-monitor-principal.png)

The main screen concentrates capture status and session information. When a match is found, the panel displays:

- **connection type**, such as P2P or server;
- **destination and protocol** used by the match;
- **ping**, detected region, and approximate distance;
- important events in the **Activity** panel;
- connection, server, and opponent details in the **IP1, IP2, and IP3** fields;
- shortcuts to launch eFootball, control the monitor, switch game modes, and open the opponent center.

### Firewall and game modes

![Firewall screen](docs/images/02-firewall.png)

The Firewall area controls where the temporary rules for the selected mode are applied:

- **eFootball only:** restricts filters to the game executable;
- **Entire system:** applies the mode to the whole computer and is recommended for the Xbox PC edition;
- **No rules:** keeps the monitor running without requesting Toolkit filters.

The panel also shows the selected scope, detected platform, active mode, and number of active filters. Protections are temporary and are removed when the application session ends.

<details>
<summary><strong>Custom rule editor</strong></summary>

![Firewall rule editor](docs/images/03-editor-regras.png)

The editor lets users create, review, and restore custom rules. Only rules created by the user or found in Windows are shown on this screen; the Toolkit's internal definitions remain protected.

</details>

<details>
<summary><strong>Link existing Windows rules</strong></summary>

![Window for linking Windows rules](docs/images/04-vincular-regras.png)

This window lets Toolkit features reuse definitions that already exist in Windows Firewall. Name, direction, protocol, addresses, and ports are imported without enabling, disabling, or modifying the original rule.

</details>

### Server center

![Server center](docs/images/05-central-servidores.png)

The server center organizes known servers in a compact list with country, address, filter status, and measurement result. It allows users to:

- test every destination or choose a specific country;
- search by IP, measurement, or status;
- add a public IPv4 or IPv6 address;
- block, allow, edit, or test a single server;
- track how many destinations are allowed, blocked, and available.

Displayed results are real measurements. When a destination does not respond, the Toolkit keeps it marked as untested or unresponsive instead of fabricating a ping value.

<details>
<summary><strong>Regional selection</strong></summary>

![Country and server selection](docs/images/06-selecao-regional.png)

The regional selector helps prioritize countries during matchmaking. Users select preferred destinations while the Toolkit temporarily handles the other destinations during the search. Newly observed public IP addresses can be checked and cataloged locally.

This feature assists with selection, but it cannot guarantee that the match will be hosted in a specific region.

</details>

### Network and overlay

![Network and overlay customization](docs/images/07-rede-overlay.png)

On this screen, users select the network adapter used for capture and customize the floating panel:

- one-line or two-line layout;
- opacity level;
- visible information blocks;
- status, mode, distance, ping, and packet loss;
- FPS, controller polling, rematches, endpoint, region, and time;
- instant preview before returning to the game.

#### In-game overlay

![eFootball Toolkit overlay](docs/images/11-overlay-em-jogo.png)

The overlay keeps essential data visible without taking over the main screen. It follows the match in real time and can show only the fields selected by the user. When the session allows an opponent to be marked, the **Mark IP** button appears on the right.

### Opponent and match center

![Blocked opponents and matches center](docs/images/08-central-adversarios.png)

The center separates information into three lists:

- **Blocked now:** filters active in the current session;
- **Rematches:** opponents marked for future identification;
- **Matches:** history of protected sessions.

The columns include name, observed IP addresses, region, date, ping, and distance whenever that information is available. Automatic blocking is an auxiliary protection: IP changes, shared connections, or decisions made by the game's infrastructure may prevent a match from being canceled automatically.

### Controller tester

![Xbox controller tester](docs/images/09-testador-controle.png)

The diagnostic tool detects compatible controllers and displays an appropriate visual representation for Xbox or PlayStation. Buttons, triggers, and analog sticks react to input in real time.

When the device exposes the required information, the screen also displays:

- connection type;
- battery status;
- vibration support;
- polling rate and average interval;
- analog stick behavior and pressed inputs.

### Settings

![Application settings](docs/images/10-configuracoes-redigida.png)

Preferences are gathered on a single screen and restored the next time the Toolkit starts. Available options include:

- Portuguese, English, and Spanish;
- sound alert when a match is found;
- automatic monitor startup;
- automatic overlay opening;
- game mode and Xbox PC notices;
- application rule restoration;
- direct access to support.

The device code was hidden in the public screenshot for security.

## Trial and PRO

| Feature | Trial | PRO |
|---|:---:|:---:|
| Duration | 5 days | According to the plan |
| Match monitor | Full | Full |
| Overlay | Essential 1-line layout | Customizable |
| Game modes | X1 | X1, COOP, and custom modes |
| Server center | — | Full |
| History and opponents | — | Full |
| Firewall tools | Limited | Full |
| Key or card required to try | No | — |

## Download

- [Download eFootball Toolkit PRO 2.1.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/v2.1.1/eFootball-Toolkit-PRO-v2.1.1.zip)
- [Download eFootball Toolkit TRIAL 2.1.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/trial-v2.1.1/eFootball-Toolkit-TRIAL-v2.1.1.zip)
- [Download eFootball Toolkit Mobile 2.1.1](https://github.com/MixDev-br/eFootballToolkitPRO/releases/download/v2.1.1/eFootball-Toolkit-Mobile-v2.1.1.apk)
- [Set up Mobile and OpenWrt (Portuguese guide)](OPENWRT_MOBILE_GUIDE.md)
- [Browse all versions](https://github.com/MixDev-br/eFootballToolkitPRO/releases)

Each release includes the `.zip` package, a `.sha256` file for integrity verification, and update notes.

## Requirements

- Windows 10 or Windows 11;
- eFootball for Steam or Xbox PC;
- administrator privileges for temporary filters;
- [Npcap](https://npcap.com/#download) installed.

**Npcap** is the component used to observe the local network traffic required by the monitor's measurements. Download it only from the official website.

## Installation

1. Install the [official Npcap](https://npcap.com/#download).
2. Download the PRO or Trial edition from Releases.
3. Extract **the entire contents** of the ZIP file.
4. Keep the executable next to the `runtime` folder.
5. Run `eFootballToolkitPRO.exe`.

Do not move or run the `.exe` by itself.

## Updates and integrity

The application checks this repository's signed `update_manifest.json`. Packages are downloaded exclusively from Releases and accepted only after validating their signature, size, and SHA-256 hash.

To verify a download manually in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\eFootball-Toolkit-PRO-v2.1.1.zip
```

Compare the result with the `.sha256.txt` file published in the same Release.

## Support

- Website: [mixdev-br.github.io/eFootballToolkitPRO](https://mixdev-br.github.io/eFootballToolkitPRO/?lang=en#suporte)
- Email: [efootballtoolkitpro.suporte@gmail.com](mailto:efootballtoolkitpro.suporte@gmail.com)

When requesting help, include your Toolkit version, whether you use Steam or Xbox PC, and a description of the behavior you observed.

---

eFootball Toolkit PRO is an independent project and is not affiliated with KONAMI.
