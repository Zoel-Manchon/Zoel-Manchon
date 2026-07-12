<div align="center">

<img src="https://komarev.com/ghpvc/?username=Zoel-Manchon&style=for-the-badge&color=3fb950"/>
&nbsp;
<a href="mailto:zroot1001@proton.me">
<img src="https://img.shields.io/badge/Email-ProtonMail-6D4AFF?style=for-the-badge&logo=protonmail&logoColor=white"/>
</a>
&nbsp;
<a href="https://github.com/Zoel-Manchon">
<img src="https://img.shields.io/badge/GitHub-Zoel--Manchon-181717?style=for-the-badge&logo=github"/>
</a>

</br>
</br>
<img src="https://raw.githubusercontent.com/Zoel-Manchon/Zoel-Manchon/main/assets/pipeline.svg" width="100%" alt="Animated terminal panel: data flowing through Zoel's pipeline — edge sensors, link, backend, store, telemetry — with a security layer scanning across every stage." />
<br/>
</div>

<br/>

## `$ whoami`

<div align="center">

<img src="https://raw.githubusercontent.com/Zoel-Manchon/Zoel-Manchon/main/assets/whoami.svg" width="100%" alt="System spec card — role, focus, editor, languages, APIs, data, infrastructure and edge stack." />

</div>

I learn by building real systems end to end — edge sensors, secured services, real-time backends, and analytical tools. The pipeline above isn't a metaphor; it's the shape of most things in here.

<br/>

## `$ tree ~/projects`

```bash
~/projects
├── cybersecurity/   # secrets vault, zero-trust auth, scanners, hardening
├── iot/             # esp32, lora, edge-ml, telemetry pipelines
├── quant/           # backtesting engines, trading analytics
├── backend/         # real-time services
└── games/           # because why not
```

### `~/cybersecurity`

<table>
<tr>
<td width="50%" valign="top">

#### AegisVault — Encrypted Secrets Vault (Python + Rust)

Local-first, zero-knowledge secrets manager built on DDD + hexagonal architecture: a Python domain core with a native **Rust crypto engine** (Argon2id + XChaCha20-Poly1305 + zeroize via PyO3). Envelope encryption with **Shamir K-of-N recovery**, master-password rotation, TOTP/2FA, a **tamper-evident hash-chained audit ledger** with SIEM export (CEF/syslog/JSON), HIBP breach checks via k-anonymity, X25519 public-key team sharing with revocation, secret injection for DevOps (`run -- <cmd>`), an auto-locking agent daemon, and a PySide6 desktop GUI with its own design system. 96 tests across two swappable crypto backends.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/PyO3-0B7261?style=flat-square"/>
<img src="https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white"/>
<img src="https://img.shields.io/badge/XChaCha20--Poly1305-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/aegisvault)

</td>
<td width="50%" valign="top">

#### Aegis — Zero-Trust Auth Lab & Attack Range

Ground-up zero-trust identity provider in Rust/Axum with a built-in Security Operations Console. RS256 JWTs with refresh rotation & JTI replay detection, mandatory TOTP MFA for admins, a per-request risk engine with GeoIP impossible-travel detection, RBAC, and a hash-chained (tamper-evident) audit trail. A React SOC console streams events live (SSE) with WebSocket alert popups and a geo-map, plus a built-in attack range — 10 scenarios + storm — to launch attacks and watch detections fire.

<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/Axum-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/Vault-FFEC6E?style=flat-square&logo=vault&logoColor=black"/>

[**→ repository**](https://github.com/Zoel-Manchon/aegis-zero-trust)

</td>
</tr>

<tr>
<td width="50%" valign="top">

#### Auth-Lab — Zero-Trust Authentication

Zero-trust auth backend: JWT access/refresh with rotation & replay (JTI) protection, mandatory TOTP MFA for admins, a per-request risk engine with GeoIP impossible-travel detection, RBAC and a security-event audit trail. Fronted by an Astro SOC dashboard behind a Caddy TLS proxy, with a defensive attack simulator that CI-verifies the defenses. Optional HashiCorp Vault layer for secrets & dynamic DB credentials.

<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Vault-FFEC6E?style=flat-square&logo=vault&logoColor=black"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/auth-lab)

</td>
<td width="50%" valign="top">

#### Pyscan — Modular Port & OT Scanner

A tiny modular network scanner in Python: async TCP connect scanning, banner grabbing, service/version fingerprinting, CIDR host discovery, JSON/table output, and read-only OT protocol identification for Modbus/TCP lab environments. Built on a clean hexagonal architecture so new scan strategies, discovery methods, and output formats drop in without touching the core engine.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/AsyncIO-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/Typer-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/Modbus-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/OT_Security-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>

[**→ repository**](https://github.com/Zoel-Manchon/pyscan)

</td>
</tr>

<tr>
<td width="50%" valign="top">

#### Arch Linux Hardened Server

Security-focused Arch Linux setup: system hardening, reduced attack surface, and production-ready configuration practices, documented end to end.

<img src="https://img.shields.io/badge/Arch_Linux-1793D1?style=flat-square&logo=archlinux&logoColor=white"/>
<img src="https://img.shields.io/badge/Hardening-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/Infrastructure-3FB950?style=flat-square"/>

[**→ repository**](https://github.com/Zoel-Manchon/arch-linux-hardened-server)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

### `~/iot`

> **Simulation-first IoT.** I build these pipelines against coherent *virtual
> worlds* before the hardware arrives — so the full edge→broker→TSDB→dashboard
> path is testable on day one, and the ESP32/LoRa integration stays isolated to
> adapter swaps. Hexagonal cores, MicroPython-ready, enforced by architecture
> fitness tests.

<table>
<tr>
<td width="50%" valign="top">

#### 🛡️ Sentinel Node — Multi-Sensor Edge Sentinel

Space-monitoring node fusing **air quality (BME680)**, **mmWave human presence
(LD2410)**, and **on-device ML** for acoustic events (INMP441 + TinyML) and
vision (ESP32-CAM). Its hexagonal core models two kinds of observation on
purpose — scalar `Measurement`s and discrete `Event`s from edge models — so
**raw audio and images never enter the telemetry frame**: the classifier runs
on-device and only the verdict is published (camera JPEGs saved out-of-band,
served via a Node-RED gallery). A coherent simulated space drives every channel
from one occupancy schedule; MQTT → Node-RED → InfluxDB → Grafana. 45 tests
incl. architecture fitness functions. Roadmap: real sensors, TLS/mTLS,
signed frames.

<img src="https://img.shields.io/badge/ESP32--S3-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/Edge_ML-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/mmWave_LD2410-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/Architecture-Hexagonal-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/sentinel-node)

</td>
<td width="50%" valign="top">

#### ☀️ Solar Weather Station — Simulation-First IoT

Solar-powered weather-station architecture developed **simulation first**. A
coherent virtual weather world drives simulated BME280, BH1750, PMS5003 and
rain sensors, reproducing daylight cycles, pressure fronts, rainfall, humidity
changes, particulate scrubbing, solar charging and battery behavior. Telemetry
flows over MQTT through Node-RED into InfluxDB and Grafana, while the hexagonal,
MicroPython-ready core keeps the future ESP32 + LoRa hardware integration
isolated to adapter changes.

<img src="https://img.shields.io/badge/Status-Simulation_Ready-3FB950?style=flat-square"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Architecture-Hexagonal-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/solar-weather-station)

</td>
</tr>
</table>

<details>
<summary><b>▸ Sentinel Node — live dashboard & camera gallery</b></summary>
<br/>
<div align="center">
<img src="https://raw.githubusercontent.com/Zoel-Manchon/sentinel-node/main/docs/screenshots/demo.gif" width="100%" alt="Sentinel Node live: a simulated day of occupancy, air quality and a scripted acoustic anomaly streaming into Grafana."/>
</div>
</details>

<table>
<tr>
<td width="50%" valign="top">

#### API IoT

End-to-end temperature & humidity monitor: ESP32 + DHT22 firmware publishing
over MQTT to a Node.js/Express backend and a real-time React dashboard.

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>

[**→ repository**](https://github.com/Zoel-Manchon/api_iot)

</td>
<td width="50%" valign="top">

#### Eastron LoRaWAN Energy Monitoring

Energy monitoring over LoRaWAN: collecting, processing, and visualizing
electrical consumption data through an InfluxDB + Grafana telemetry stack.

<img src="https://img.shields.io/badge/LoRaWAN-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>
<img src="https://img.shields.io/badge/Telemetry-3FB950?style=flat-square"/>

[**→ repository**](https://github.com/Zoel-Manchon/eastron-lorawan-energy-monitoring)

</td>
</tr>

<tr>
<td width="50%" valign="top">

#### SmartWatch LoRaWAN

Wearable IoT project using LoRaWAN, embedded sensors, and remote monitoring.

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/LoRaWAN-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/Embedded-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/Wearable_IoT-3FB950?style=flat-square"/>

[**→ repository**](https://github.com/Zoel-Manchon/Proyecto_IoT_J3_SmartWatch_LoRaWAN)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

### `~/quant`

<table>
<tr>
<td width="50%" valign="top">

#### QuantLab — Backtesting Engine

Python trading backtesting engine built with DDD + hexagonal architecture: a rich domain core with `Portfolio` invariants for cash, margin and position crossing, `Order` entities for MARKET/LIMIT/STOP execution, automatic stop-loss / take-profit groups with OCO behavior, short selling support, walk-forward analysis, SQLite persistence, and performance analytics such as Sharpe, Sortino, profit factor and expectancy. One core exposed through CLI, Textual TUI and PySide6 desktop GUI, with CI checks using ruff, mypy and pytest.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/DDD-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/Textual-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white"/>
<img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white"/>
<img src="https://img.shields.io/badge/Backtesting-3FB950?style=flat-square"/>

[**→ repository**](https://github.com/Zoel-Manchon/quantlab)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

### `~/backend`

<table>
<tr>
<td width="50%" valign="top">

#### Crypto·Watch Dashboard

Real-time cryptocurrency terminal: a Rust/Axum backend streaming live prices over WebSockets to an Astro + React dashboard, with PostgreSQL persistence and a full Docker stack.

<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/Axum-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/Astro-FF5D01?style=flat-square&logo=astro&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/crypto-dashboard)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

### `~/games`

<table>
<tr>
<td width="50%" valign="top">

#### Snake HD

A Nokia-era classic rebuilt as a polished arcade game: HD rendering, custom pixel-art sprites, combo multiplier, power-ups, sound, screen shake, and a SHA-256 tamper-evident leaderboard backed by a Rust/Axum service.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Pygame-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/Axum-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/Game_Dev-3FB950?style=flat-square"/>

[**→ repository**](https://github.com/Zoel-Manchon/snake-hd)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

<br/>

```text
$ cat ~/.principles
> build small systems, not isolated scripts
> measure what you build
> keep security in mind from line one
> ship something that actually works
```

<div align="center">

**From edge devices to secured data — still learning, still building.**

</div>
