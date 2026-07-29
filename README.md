<div align="center">

# Zoel Arias Manchón

### IoT/OT Security · Secure Systems · Rust / Python · AppSec / DevSecOps

I build security-focused systems end to end: embedded telemetry, hardened Linux,
zero-trust identity, defensive attack simulations, real-time backends and native tools.

[Portfolio](https://zoel-manchon.github.io/) ·
[LinkedIn](https://www.linkedin.com/in/zoel-arias-manchon) ·
[Email](mailto:zroot1001@proton.me)

**Core stack:** `Rust` · `Python` · `Linux` · `Docker` · `PostgreSQL` · `MQTT` · `Grafana`

</div>

---

## Profile

My work sits between **software engineering, cybersecurity and connected devices**.
I am especially interested in systems where security is part of the architecture,
not an additional layer added at the end.

I focus on:

- **IoT/OT security:** secure telemetry, edge gateways, MQTT, LoRaWAN and anomaly detection.
- **Systems security:** Rust, hardened Linux, integrity controls and applied cryptography.
- **Application security:** zero-trust authentication, MFA, passkeys, RBAC and auditability.
- **Delivery:** reproducible Docker environments, automated tests, CI and technical documentation.

> **From the sensor to the SOC: build the complete system, define the trust boundaries,
> observe its behaviour and prove that the controls work.**

---

# Featured engineering work

## 1. [Emberwall — Hardened IoT/OT Security Linux](https://github.com/Zoel-Manchon/emberwall)

**A minimal Linux distribution built from source for secure IoT/OT edge deployments.**

Emberwall uses **Buildroot** to produce its own cross-toolchain, hardened kernel and
small immutable userland. It includes `sentinel`, a native Rust binary that combines
OT/IoT-aware TCP and UDP scanning with an Argon2id + XChaCha20-Poly1305 secrets vault.

**Engineering evidence**

- Hardened toolchain and kernel configuration: PIE, RELRO, SSP, FORTIFY, KASLR and LSM controls.
- Default-deny `nftables` policy and reduced runtime attack surface.
- OT/ICS and IoT recognition for Modbus, S7comm, IEC-104, CoAP, MQTT and LoRaWAN.
- Live ISO, workstation and locked-appliance variants for x86-64 and ARM64.
- Reproducible Buildroot packaging with vendored Rust dependencies.

**Technology:** `Buildroot` · `Linux` · `Rust` · `C` · `nftables` · `MQTT` · `OT/ICS`

[Repository](https://github.com/Zoel-Manchon/emberwall) ·
[Demo in GitHub viewer](https://github.com/Zoel-Manchon/emberwall/blob/main/docs/demo.gif) ·
[Build documentation](https://github.com/Zoel-Manchon/emberwall/blob/main/docs/BUILD.md)

<a href="https://github.com/Zoel-Manchon/emberwall/blob/main/docs/demo.gif">
  <img src="https://raw.githubusercontent.com/Zoel-Manchon/emberwall/main/docs/demo.gif"
       alt="Emberwall boot, sentinel scanner, encrypted vault and MQTT gateway demo"
       width="100%">
</a>

---

## 2. [Aegis — Zero-Trust Identity & Defensive Attack Range](https://github.com/Zoel-Manchon/aegis-zero-trust)

**A Rust identity provider connected to a real-time Security Operations Console.**

Aegis authenticates users, evaluates risk on every request and records security events
in a tamper-evident audit chain. Its React SOC console streams events live and includes
a controlled attack range for demonstrating detection and response.

**Engineering evidence**

- RS256 access tokens, rotating refresh tokens and JTI replay detection.
- Mandatory TOTP MFA for administrators and WebAuthn/passkey authentication.
- Per-request risk scoring and GeoIP impossible-travel detection.
- Hash-chained audit events stored in PostgreSQL.
- Real-time SOC feed through PostgreSQL `LISTEN/NOTIFY`, SSE and WebSocket alerts.
- Ten defensive attack scenarios, run-all and storm modes.
- Docker Compose delivery behind a single-origin Caddy reverse proxy.
- Optional HashiCorp Vault dynamic database credentials.

**Technology:** `Rust` · `Axum` · `React` · `PostgreSQL` · `Redis` · `Caddy` · `Vault`

[Repository](https://github.com/Zoel-Manchon/aegis-zero-trust) ·
[Attack-range demo in GitHub viewer](https://github.com/Zoel-Manchon/aegis-zero-trust/blob/main/docs/attack_simulator.gif) ·
[Walkthrough](https://github.com/Zoel-Manchon/aegis-zero-trust/blob/main/DEMO.md)

<a href="https://github.com/Zoel-Manchon/aegis-zero-trust/blob/main/docs/attack_simulator.gif">
  <img src="https://raw.githubusercontent.com/Zoel-Manchon/aegis-zero-trust/main/docs/attack_simulator.gif"
       alt="Aegis SOC attack range launching controlled attacks and displaying live detections"
       width="100%">
</a>

---

## 3. [AegisVault — Local-First Encrypted Secrets Vault](https://github.com/Zoel-Manchon/aegisvault)

**A zero-knowledge secrets manager with a Python domain core and native Rust cryptography.**

The project applies domain-driven and hexagonal architecture to a security-sensitive
desktop application, keeping cryptographic operations isolated behind swappable ports.

**Engineering evidence**

- Argon2id key derivation and XChaCha20-Poly1305 authenticated encryption.
- Rust crypto engine integrated into Python through PyO3.
- Envelope encryption and Shamir K-of-N recovery.
- TOTP, password rotation and X25519 public-key sharing with revocation.
- Tamper-evident hash-chained audit ledger with JSON, CEF and syslog export.
- Secret injection for development workflows and an auto-locking local agent.
- PySide6 desktop interface and automated tests across crypto backends.

**Technology:** `Python` · `Rust` · `PyO3` · `PySide6` · `SQLite` · `Applied cryptography`

[Repository](https://github.com/Zoel-Manchon/aegisvault)

---

## 4. [Phosphor — Native File Integrity Monitor](https://github.com/Zoel-Manchon/phosphor)

**A cross-platform Rust desktop tool for detecting filesystem tampering in real time.**

Phosphor anchors a signed baseline for a directory, watches changes through native
filesystem notifications and exposes modified, added or deleted files immediately.

**Engineering evidence**

- SHA-256 file baselines protected by HMAC-SHA256 signatures.
- Constant-time signature verification.
- Real-time filesystem monitoring and native desktop alerts.
- Gitignore-style exclusion rules and controlled re-baselining.
- JSON and CEF export for SIEM ingestion.
- Unit-tested core with no UI dependencies.

**Technology:** `Rust` · `egui` · `SHA-256` · `HMAC` · `SIEM`

[Repository](https://github.com/Zoel-Manchon/phosphor) ·
[Demo in GitHub viewer](https://github.com/Zoel-Manchon/phosphor/blob/main/docs/demo.gif)

---

# IoT and edge-security systems

## [AgriSentinel](https://github.com/Zoel-Manchon/agrisentinel)

A simulation-first rural IoT security lab spanning crops, water and livestock.
Each node signs telemetry with HMAC, sequence numbers and nonces. The gateway detects
replay, stale, rate and physically impossible readings before trusted data reaches
MQTT, InfluxDB and Grafana.

`Python` · `Hexagonal architecture` · `MQTT` · `InfluxDB` · `Grafana` · `HMAC`

[Repository](https://github.com/Zoel-Manchon/agrisentinel) ·
[SOC demo](https://github.com/Zoel-Manchon/agrisentinel/blob/main/docs/demo-soc.gif)

## [Sentinel Node](https://github.com/Zoel-Manchon/sentinel-node)

A multi-sensor edge architecture combining air quality, mmWave presence, acoustic
TinyML and vision. Raw audio and images remain at the edge; only classifications and
trusted observations enter the telemetry pipeline.

`ESP32-S3` · `Edge ML` · `Python` · `MQTT` · `Node-RED` · `Grafana`

[Repository](https://github.com/Zoel-Manchon/sentinel-node) ·
[Dashboard demo](https://github.com/Zoel-Manchon/sentinel-node/blob/main/docs/screenshots/demo.gif)

## [Solar Weather Station](https://github.com/Zoel-Manchon/solar-weather-station)

A simulation-first, solar-powered weather station with coherent virtual sensors,
battery behaviour and environmental events. Its hexagonal core is prepared for a
future ESP32 and LoRa hardware adapter without rewriting the domain model.

`Python` · `ESP32-ready` · `LoRa` · `MQTT` · `Node-RED` · `InfluxDB` · `Grafana`

[Repository](https://github.com/Zoel-Manchon/solar-weather-station) ·
[Demo](https://github.com/Zoel-Manchon/solar-weather-station/blob/main/docs/demo.gif)

---

# Additional selected projects

### Security and systems

- **[Maat](https://github.com/Zoel-Manchon/maat)** — Rust modal editor with SHA-256 integrity tracking, atomic saves, external-change detection and SIEM audit output.
- **[Pyscan](https://github.com/Zoel-Manchon/pyscan)** — asynchronous network and OT-protocol scanner with host discovery, fingerprinting and structured output.
- **[Auth-Lab](https://github.com/Zoel-Manchon/auth-lab)** — NestJS zero-trust authentication lab with MFA, replay defence, risk analysis and a controlled attack simulator.
- **[Arch Linux Hardened Server](https://github.com/Zoel-Manchon/arch-linux-hardened-server)** — documented Linux hardening and attack-surface reduction.

### Backend and data

- **[Toychain](https://github.com/Zoel-Manchon/toychain)** — Rails 8 tamper-evident blockchain with background proof-of-work, authenticated real-time updates and an independent Python verifier.
- **[Crypto·Watch](https://github.com/Zoel-Manchon/crypto-dashboard)** — Rust/Axum WebSocket backend, Astro/React frontend, PostgreSQL persistence and Docker delivery.
- **[QuantLab](https://github.com/Zoel-Manchon/quantlab)** — DDD and hexagonal backtesting engine with order execution, OCO controls, walk-forward analysis and performance metrics.

### Earlier hardware and telemetry work

- **[API IoT](https://github.com/Zoel-Manchon/api_iot)** — ESP32 and DHT22 telemetry over MQTT to a Node.js backend and React dashboard.
- **[Eastron LoRaWAN Energy Monitoring](https://github.com/Zoel-Manchon/eastron-lorawan-energy-monitoring)** — electrical-energy telemetry with LoRaWAN, InfluxDB and Grafana.
- **[SmartWatch LoRaWAN](https://github.com/Zoel-Manchon/Proyecto_IoT_J3_SmartWatch_LoRaWAN)** — wearable sensing and remote monitoring over LoRaWAN.
- **[Snake HD](https://github.com/Zoel-Manchon/snake-hd)** — polished Pygame project with a tamper-evident leaderboard backed by Rust/Axum.

---

# Engineering principles

```text
Build complete systems, not disconnected scripts.
Treat security as an architectural requirement.
Keep the domain independent from infrastructure.
Make behaviour observable.
Test the trust boundaries.
Document how another engineer can run the project.
Ship a working demonstration.
```

---

<div align="center">

### Open to junior opportunities in IoT/OT security, backend and systems engineering

[View my portfolio](https://zoel-manchon.github.io/) ·
[Connect on LinkedIn](https://www.linkedin.com/in/zoel-arias-manchon) ·
[Send an email](mailto:zroot1001@proton.me)

**From edge devices to secured data.**

</div>
