# Project S / HomeForge

> One dashboard. One login. Zero cloud dependency. Encryption-first homelab OS.

![Dashboard Preview](screenshot.png)

---

## Status

**Pre‑alpha / Private Development** – The source code is not yet public. We are building in private and will open source when we reach a stable beta.

---

## What is it?

Project S bundles the best open‑source tools into a single, encrypted dashboard. Install on a Raspberry Pi, an old PC, or a VPS. Own your data. No cloud subscriptions. No telemetry.

**What’s inside:**
- **Media** – Jellyfin (movies, music, photos)
- **Productivity** – Nextcloud with Collabora Office
- **Chat** – Matrix Synapse + Element
- **Passwords** – Vaultwarden (Bitwarden compatible)
- **Code** – Eclipse Theia IDE
- **Offline knowledge** – Kiwix (Wikipedia, Stack Overflow, etc.)

**Unique feature:** Mouse‑entropy encryption key + SQLCipher at rest. Your data is encrypted with a key derived from your own mouse movements. We never see your key.

---

## What’s working (internal build)

- Dashboard with live resource charts (CPU, RAM, disk, network)
- 11 color themes + glassmorphism UI
- One‑command install on Linux / macOS (`./install.sh`)
- Security layer: Argon2id, AES‑256‑GCM, rate‑limited auth, iron‑session cookies
- All core services integrated and functional

## What’s not yet ready

- Automated backups (planned)
- One‑click module store (planned)
- Mobile companion app (planned)

---

## Get early access

We are looking for early testers who run a homelab and want to try the pre‑alpha build.

👉 **[Request early access](https://forms.google.com/your-link)** (no spam – just a notification when testing opens)

---

## License

| Layer | License |
|-------|---------|
| Core orchestrator | FSL‑1.1 / Apache 2.0 |
| Basic app store & UI | Free |
| Premium integrations | Paid tier (future) |

GPL/AGPL tools (ERPNext, n8n, Kiwix) are available as optional user‑deployed modules – not bundled – to respect their license terms.

---

## Team

- **Basil Suhail** – [LinkedIn](https://linkedin.com/in/basilsuhail) | [GitHub](https://github.com/BasilSuhail)
- **Saad Shafique** – [GitHub](https://github.com/saadsh15)

---

*This repo is a public landing page. The source code is private during pre‑alpha development.*
