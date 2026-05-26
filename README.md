# 🔍 ReconFlow

> A single-file pentest & CTF reconnaissance cheat sheet — offline, no dependencies, no install.

![HTML](https://img.shields.io/badge/HTML-single%20file-orange?style=flat-square&logo=html5)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![Tools](https://img.shields.io/badge/tools-28-brightgreen?style=flat-square)
![CMD Log](https://img.shields.io/badge/CMD_LOG-new-orange?style=flat-square)
![Language](https://img.shields.io/badge/lang-EN%20%2F%20TR-purple?style=flat-square)

---

## What is this?

ReconFlow is a **single HTML file** that acts as an interactive command reference during penetration tests and CTF competitions. Open it in any browser — no server, no install, no internet required.

It keeps your target IP in one place and injects it into every command automatically. Every command card has one-click copy, star favorites, and collapsible notes.

---

## Features

- **Target IP injection** — type the IP once, it fills into every command
- **One-click copy** — every command copies instantly
- **CMD LOG** — `+` button on every command logs it to a session activity page; add output/notes per entry, export as JSON
- **Favorites** — star any command to pin it at the top of the page
- **Notes** — collapsible note field on every command card
- **Custom commands** — add your own commands to any tool page
- **Session tracking** — check off services as you enumerate them
- **Info panels** — bilingual (EN/TR) summary, what to look for, common vulns, tips
- **Platform badges** — WIN / LIN labels on every tool info panel (indicates target platform)
- **Related tool badges** — AD and Linux pages show clickable tool shortcuts
- **Fully offline** — zero dependencies, works without internet
- **Persistent state** — everything saves to localStorage automatically

---

## Tools Covered (28)

### 🔵 Windows / Active Directory
| Tool | Description |
|------|-------------|
| crackmapexec | SMB/LDAP/WinRM Swiss army knife |
| enum4linux | SMB/NetBIOS enumerator |
| impacket | Windows/AD attack suite |
| xfreerdp | RDP client |
| evil-winrm | WinRM shell |
| responder | LLMNR/NBT-NS poisoner |
| kerbrute | Kerberos user enum & brute |

### 🟡 Cross-Platform
| Tool | Description |
|------|-------------|
| nmap | Network mapper |
| gobuster | Dir/DNS/VHost brute-forcer |
| ffuf | Web fuzzer |
| nikto | Web server scanner |
| hydra | Network login cracker |
| nuclei | Template-based vulnerability scanner |
| sqlmap | SQL injection automation |
| hashcat / john | Password crackers |
| searchsploit | ExploitDB CLI |
| msfvenom | Payload generator |
| chisel / ligolo-ng | Tunneling & pivoting |
| wpscan | WordPress scanner |

### 🟢 Linux
| Tool | Description |
|------|-------------|
| linPEAS / winPEAS | Privilege escalation scripts |
| pspy | Unprivileged process spy |
| pwncat-cs | Advanced Linux shell handler |
| linux-exploit-suggester | Kernel LPE finder |
| pwntools | Binary exploit framework |
| gdb + pwndbg | Binary debugger |
| socat | Socket Swiss army knife |
| strace / ltrace | Syscall tracer |
| binwalk | Firmware analyzer |

### 📋 Cheat Sheets
- **Active Directory** — domain enumeration, BloodHound, Kerberoasting, DCSync, ACL abuse
- **Linux Post-Exploitation** — privesc paths, SUID, cron, capabilities, kernel exploits

---

## Usage

```bash
# Just open it
xdg-open recon.html        # Linux
open recon.html            # macOS
start recon.html           # Windows
```

Or double-click `recon.html` in your file manager.

### Workflow

1. Enter target IP in the top bar
2. Click **+** next to discovered services to add them to your session
3. Select a tool from the sidebar
4. Click **ℹ INFO** for a summary of what to look for
5. Run commands — they auto-fill with your target IP
6. Star important commands, add notes, track your progress
7. Click **+** on any command card to log it → go to **CMD LOG** to add output/notes and export JSON

---

## Screenshot

> Services sidebar → tool page → commands with auto-injected IP → info panel with platform badges

```
┌─────────────────┬──────────────────────────────────────────┐
│  RECON // flow  │  nmap   Network Mapper          ℹ INFO   │
│  TARGET: [IP]   ├──────────────────────────────────────────┤
│                 │  ⊞ WIN  🐧 LIN                           │
│  SERVICES  ▼   │  nmap is the industry-standard scanner... │
│  □ FTP  21      ├──────────────────────────────────────────┤
│  □ SSH  22      │  ★ FAVORITES                             │
│  □ HTTP 80      ├──────────────────────────────────────────┤
│                 │  HOST DISCOVERY                          │
│  TOOLS  ▼      │  ┌─────────────────────────────────────┐ │
│  nmap           │  │ nmap -sn TARGETIP/24  [+][COPY][☆] │ │
│  gobuster       │  │ Ping sweep — find live hosts        │ │
│  ffuf           │  └─────────────────────────────────────┘ │
│  cme            │                                          │
│  ...            │                                          │
│                 │                                          │
│  AD / LINUX ▼  │                                          │
│  Active Dir.    │                                          │
│  Linux          │                                          │
│                 │                                          │
│  ◎ CMD LOG      │                                          │
└─────────────────┴──────────────────────────────────────────┘
```

---

## State & Privacy

All data (IP, notes, favorites, session progress) is stored in **browser localStorage** only — nothing is sent anywhere. Clear with the `SIFIRLA / CLEAR STATE` button.

---

## License

MIT — use freely, modify freely.
