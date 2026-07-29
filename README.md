<h1 align="center">Zoel Arias Manchón</h1>

<p align="center">
  <strong>Junior IoT/OT Security · Rust & Python · Secure edge systems · AppSec · DevSecOps</strong>
</p>

<p align="center">
  <a href="https://zoel-manchon.github.io/">Portfolio</a>
  ·
  <a href="https://www.linkedin.com/in/zoel-arias-manchon/">LinkedIn</a>
  ·
  <a href="mailto:zroot1001@proton.me">Email</a>
</p>

<p align="center">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
  <img alt="Linux" src="https://img.shields.io/badge/Linux-111111?style=flat-square&logo=linux&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="MQTT" src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white">
  <img alt="Grafana" src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white">
</p>

---

## `$ whoami`

I build complete systems rather than isolated scripts: edge sensors, hardened Linux environments, secure backends, real-time telemetry, desktop security tools, and defensive attack simulations.

My main interests are **IoT/OT security**, **application security**, **zero-trust identity**, **Linux hardening**, and **secure systems programming with Rust**.

> **Secure by design — from the sensor to the dashboard.**

## `$ tree ~/projects`

```text
~/projects
├── os/              hardened IoT/OT Linux
├── cybersecurity/   zero-trust identity, vaults, scanners and hardening
├── desktop/         native Rust security tools
├── iot/             ESP32, LoRaWAN and secured telemetry pipelines
├── backend/         real-time services and tamper-evident systems
├── quant/           backtesting and trading analytics
└── games/           polished experimental projects
```

## Featured projects

### 🔥 [Emberwall — Hardened IoT/OT Security Linux](https://github.com/Zoel-Manchon/emberwall)

A Linux distribution built from source with **Buildroot**, a hardened kernel, an immutable minimal userland, and a default-deny `nftables` firewall. It includes `sentinel`, a native Rust binary combining concurrent TCP/UDP and OT/ICS scanning with an Argon2id + XChaCha20-Poly1305 secrets vault.

`Buildroot` · `Linux` · `Rust` · `C` · `nftables` · `MQTT` · `OT/ICS`

[Repository](https://github.com/Zoel-Manchon/emberwall) · [Open live demo](https://raw.githubusercontent.com/Zoel-Manchon/emberwall/main/docs/demo.gif)

### 🛡️ [Aegis — Zero-Trust Auth Lab & Attack Range](https://github.com/Zoel-Manchon/aegis-zero-trust)

A zero-trust identity provider written in **Rust/Axum**, with RS256 JWT rotation, JTI replay detection, mandatory administrator MFA, RBAC, GeoIP impossible-travel analysis, a tamper-evident audit trail, and a React Security Operations Console with a defensive attack range.

`Rust` · `Axum` · `React` · `PostgreSQL` · `Redis` · `Vault`

[Repository](https://github.com/Zoel-Manchon/aegis-zero-trust) · [Open attack-range demo](https://raw.githubusercontent.com/Zoel-Manchon/aegis-zero-trust/main/docs/attack_simulator.gif)

### 🔐 [AegisVault — Encrypted Secrets Vault](https://github.com/Zoel-Manchon/aegisvault)

A local-first, zero-knowledge secrets manager with a Python domain core and native Rust cryptography through PyO3. It implements envelope encryption, Argon2id, XChaCha20-Poly1305, Shamir recovery, TOTP, X25519 team sharing, revocation, a hash-chained audit ledger, SIEM export, and a PySide6 desktop interface.

`Python` · `Rust` · `PyO3` · `PySide6` · `SQLite` · `Applied cryptography`

[Repository](https://github.com/Zoel-Manchon/aegisvault)

### ◆ [Phosphor — File Integrity Monitor](https://github.com/Zoel-Manchon/phosphor)

A native Rust desktop file-integrity monitor with a signed SHA-256 baseline, real-time filesystem events, tamper detection, desktop alerts, ignore rules, re-baselining, and JSON/CEF export for SIEM ingestion.

`Rust` · `egui` · `SHA-256` · `HMAC` · `SIEM`

[Repository](https://github.com/Zoel-Manchon/phosphor) · [Open live demo](https://raw.githubusercontent.com/Zoel-Manchon/phosphor/main/docs/demo.gif)

### 🌾 [AgriSentinel — Secured Rural IoT Lab](https://github.com/Zoel-Manchon/agrisentinel)

A simulation-first smart-farm security lab covering crops, water, and livestock. Telemetry is signed with HMAC, sequence numbers, and nonces; the gateway detects replay, stale, rate, and physical-range anomalies before forwarding trusted data to MQTT, InfluxDB, and Grafana.

`Python` · `Hexagonal architecture` · `MQTT` · `InfluxDB` · `Grafana` · `HMAC`

[Repository](https://github.com/Zoel-Manchon/agrisentinel) · [Open SOC demo](https://raw.githubusercontent.com/Zoel-Manchon/agrisentinel/main/docs/demo-soc.gif)

### 🛰️ [Sentinel Node — Multi-Sensor Edge Sentinel](https://github.com/Zoel-Manchon/sentinel-node)

A multi-sensor ESP32-S3 architecture combining air quality, mmWave presence, acoustic TinyML, and computer vision. Raw audio and images remain at the edge; only classifications and trusted telemetry enter the MQTT pipeline.

`ESP32-S3` · `Edge ML` · `Python` · `MQTT` · `Node-RED` · `Grafana`

[Repository](https://github.com/Zoel-Manchon/sentinel-node) · [Open dashboard demo](https://raw.githubusercontent.com/Zoel-Manchon/sentinel-node/main/docs/screenshots/demo.gif)

## More security and systems work

- [Maat](https://github.com/Zoel-Manchon/maat) — modal Rust terminal editor with SHA-256 integrity tracking, atomic saves, conflict-aware writes, and SIEM audit output.
- [Pyscan](https://github.com/Zoel-Manchon/pyscan) — modular asynchronous TCP and OT protocol scanner with host discovery, fingerprinting, and structured output.
- [Auth-Lab](https://github.com/Zoel-Manchon/auth-lab) — NestJS zero-trust authentication lab with MFA, replay protection, risk analysis, Vault integration, and a defensive simulator.
- [Arch Linux Hardened Server](https://github.com/Zoel-Manchon/arch-linux-hardened-server) — documented server-hardening and attack-surface reduction practices.

## IoT and telemetry

- [Solar Weather Station](https://github.com/Zoel-Manchon/solar-weather-station) — simulation-first solar weather station with ESP32/LoRa-ready ports, MQTT, Node-RED, InfluxDB, and Grafana.
- [API IoT](https://github.com/Zoel-Manchon/api_iot) — ESP32 + DHT22 telemetry over MQTT to a Node.js backend and React dashboard.
- [Eastron LoRaWAN Energy Monitoring](https://github.com/Zoel-Manchon/eastron-lorawan-energy-monitoring) — electrical-energy monitoring with LoRaWAN, InfluxDB, and Grafana.
- [SmartWatch LoRaWAN](https://github.com/Zoel-Manchon/Proyecto_IoT_J3_SmartWatch_LoRaWAN) — wearable sensing and remote monitoring over LoRaWAN.

## Backend, data, and experimentation

- [Toychain](https://github.com/Zoel-Manchon/toychain) — tamper-evident educational blockchain with Rails 8, background proof-of-work, authenticated real-time updates, and an independent Python verifier.
- [Crypto·Watch](https://github.com/Zoel-Manchon/crypto-dashboard) — Rust/Axum WebSocket backend, Astro/React frontend, PostgreSQL persistence, and Docker deployment.
- [QuantLab](https://github.com/Zoel-Manchon/quantlab) — DDD and hexagonal backtesting engine with order execution, OCO risk controls, walk-forward analysis, and performance metrics.
- [Snake HD](https://github.com/Zoel-Manchon/snake-hd) — polished Pygame arcade project with a tamper-evident leaderboard backed by Rust/Axum.

## `$ cat ~/.principles`

```text
build complete systems, not disconnected scripts
measure and test what you build
keep security in mind from line one
ship something that actually works
```

---

<p align="center">
  <strong>From edge devices to secured data — still learning, still building.</strong>
</p>
