<div align="center">

# Collab-it Server

**Local-first BIM collaboration hub — runs entirely on your LAN**

[![Latest Release](https://img.shields.io/github/v/release/cr8-click/collab-it-server?label=latest&color=0ea5e9&style=flat-square)](https://github.com/cr8-click/collab-it-server/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11%2064--bit-blue?style=flat-square)](https://github.com/cr8-click/collab-it-server/releases/latest)
[![Publisher](https://img.shields.io/badge/publisher-cr8.click-6366f1?style=flat-square)](https://cr8.click)

**[⬇ Download latest installer](https://github.com/cr8-click/collab-it-server/releases/latest)**

</div>

---

## What is Collab-it Server?

Collab-it Server is the **on-premise hub** of the Collab-it platform. It runs on one designated machine inside your LAN and stores all of your team's BIM collaboration data — issues, comments, attachments, and user accounts — entirely **on your own hardware**.

No project data ever leaves your network.

```
Internet ←— license activation & admin identity only
    │
cr8.click Portal
    │
Collab-it Server  ←— all project data lives here (your machine, your LAN)
    │
Collab-it Clients × N  ←— each team member's machine
```

Team members install [Collab-it](https://github.com/cr8-click/collab-it-client) on their own machines and connect to the server address you share with them.

---

## System requirements

| | |
|---|---|
| **OS** | Windows 10 or Windows 11 (64-bit) |
| **RAM** | 2 GB minimum · 4 GB recommended |
| **Disk** | 500 MB for the application + storage for your project data |
| **Network** | A stable LAN connection reachable by all team members |
| **Internet** | Required only for initial license activation and admin sign-in |

---

## Installation

1. Download the latest `Collab-it-Server_x.x.x_x64-setup.exe` from the **[Releases](https://github.com/cr8-click/collab-it-server/releases/latest)** page.
2. Run the installer. Accept the UAC prompt — the installer automatically configures Windows Firewall rules for the server and the embedded database.
3. Launch **Collab-it Server** from the Start menu.
4. On first launch, claim your license using the serial key you received from [cr8.click](https://cr8.click), or sign in to import an existing license token from another LAN.
5. Copy the `http://<LAN-IP>:<port>` address shown on the dashboard and share it with your team. They enter it when first opening [Collab-it](https://github.com/cr8-click/collab-it-client).

---

## Licensing

Each Collab-it license is **per seat** and **active on one LAN at a time**. The built-in LAN-token mechanism enforces this automatically.

| Scenario | What to do |
|---|---|
| Fresh installation | Enter your serial key in the **Licenses** tab to claim the license for this LAN |
| Moving to a new server machine | Export the license token on the old server, then import it on the new one |
| Old server is gone (no access) | Sign in to [cr8.click](https://cr8.click) and use **Force release** to free the token |

Need a license? Visit [cr8.click](https://cr8.click).

---

## Data privacy

Collab-it Server is **local-first by design**:

- All issues, comments, attachments, and user records are stored in an embedded database **on your machine** — they never leave your LAN.
- The only information transmitted to cr8.click's cloud is administrator email addresses (for identity verification) and license-state events (for compliance auditing).
- No telemetry, analytics, or usage data are collected.

As the operator of this server you are the **data controller** for your organisation's project data. Backup, retention, encryption, and access control are your responsibility. See the full terms in the EULA bundled with the installer.

---

## Security

Collab-it Server installers are currently **not code-signed** with a certificate authority. Windows SmartScreen may display a blue "Windows protected your PC" warning on first install.

**This is expected.** To proceed:
1. Click **More info** in the SmartScreen dialog.
2. Click **Run anyway**.

Every installer published here is automatically scanned on VirusTotal immediately after it is built. The scan report for each release is linked in the release notes on this page. You can also verify any installer yourself by dropping the `.exe` file onto [virustotal.com](https://www.virustotal.com).

---

## Upgrading

Run the new installer over an existing installation. Your project database (`pb_data`) is preserved automatically — no manual migration needed.

---

## Support

| | |
|---|---|
| **General support** | support@cr8.click |
| **Legal & licensing** | legal@cr8.click |
| **Website** | [cr8.click](https://cr8.click) |

---

<div align="center">
<sub>Published by <a href="https://cr8.click">cr8.click</a> &nbsp;·&nbsp; Copyright © 2026 cr8.click. All rights reserved.</sub>
</div>
