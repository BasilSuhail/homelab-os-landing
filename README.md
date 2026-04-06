# Homelab Operating System

> One dashboard. One login. Zero cloud dependency. Encryption-first homelab OS.

**Live preview:** [View the landing page →](https://basilsuhail.github.io/ProjectS-HomeForge/)

----



![Dashboard Preview](screenshot.png)

## Architecture at a glance

```mermaid
flowchart TD
    User[("🖥️ You (Browser)")] --> Dashboard["Homelab Dashboard<br/>:3069"]
    Dashboard --> Nginx["Nginx Reverse Proxy"]
    
    Nginx --> Nextcloud["Nextcloud + Collabora<br/>Files & Office"]
    Nginx --> Jellyfin["Jellyfin<br/>Media"]
    Nginx --> Matrix["Matrix Synapse + Element<br/>Chat"]
    Nginx --> Vaultwarden["Vaultwarden<br/>Passwords"]
    Nginx --> Theia["Eclipse Theia<br/>Browser IDE"]
    Nginx --> Kiwix["Kiwix<br/>Offline Wikipedia"]
    Nginx --> OpenWebUI["Open‑WebUI + Ollama<br/>Local AI"]
    Nginx --> OpenVPN["OpenVPN<br/>Secure remote access"]

    style Dashboard fill:#d4e157,stroke:#333,stroke-width:2px,color:#000
    style Nginx fill:#22d3ee,stroke:#333,stroke-width:2px
    style User fill:#a855f7,stroke:#333,stroke-width:2px,color:#fff
```

## Security flow (encryption‑first)

```mermaid
flowchart LR
    Mouse["🖱️ Mouse movement entropy"] --> SHA["SHA‑512"]
    SHA --> Entropy["128‑char entropy key"]
    Entropy --> HKDF["HKDF‑SHA512"]
    
    HKDF --> Session["Session secret"]
    HKDF --> WS["WebSocket ticket secret"]
    HKDF --> DB["Database key (AES‑256‑GCM)"]
    
    DB --> SQLCipher["SQLCipher encrypted DB"]
    Session --> Iron["iron‑session cookie"]
    WS --> Terminal["Secure terminal access"]
    
    style Mouse fill:#facc15,stroke:#333
    style Entropy fill:#ef4444,stroke:#333,color:#fff
    style DB fill:#22c55e,stroke:#333
```

## What we're building (roadmap)

```mermaid
timeline
    title Project progress
    section Phase 1 ✅
        Research & tool selection : Complete
        Core Docker orchestration : Complete
    section Phase 2 ✅
        Security & auth : Complete
        Entropy key + SQLCipher : Complete
    section Phase 3 🔨
        Dashboard UI : 11 themes, live charts
        Integrated services : Jellyfin, Nextcloud, Matrix, Vaultwarden...
    section Phase 4 📅
        Backups & one‑click store : Planned
        Mobile app : Planned
    section Phase 5 🔮
        Smart home & automation : Future
```

---

## Status

**Pre‑alpha / Private Development** – The source code is not yet public. We are building in private and will share more as we progress.

---

## What is it?

This project bundles the best open‑source tools into a single, encrypted dashboard. Install on a Raspberry Pi, an old PC, or a VPS. Own your data. No cloud subscriptions. No telemetry.

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
- One‑command install on Linux / macOS
- Security layer: Argon2id, AES‑256‑GCM, rate‑limited auth
- All core services integrated and functional

## What’s not yet ready

- Automated backups (planned)
- One‑click module store (planned)
- Mobile companion app (planned)

---

## Get early access

We are looking for early testers who run a homelab and want to try the pre‑alpha build.

👉 **[Request early access – fill out this 2-minute form](https://forms.gle/LNhX4XaBUQvshBqHA)**

(Only email is required. The rest is optional research to help us build what you actually need.)

---

## Team

- **Basil Suhail** – [LinkedIn](https://linkedin.com/in/basilsuhail) | [GitHub](https://github.com/BasilSuhail)
- **Saad Shafique** – [LinkedIn](https://www.linkedin.com/in/saad-shafique-60115934b/) | [GitHub](https://github.com/saadsh15)

---

*This is a public landing page for a pre-alpha project. The source code is currently private.*
