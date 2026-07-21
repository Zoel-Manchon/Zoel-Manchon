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

<br/>
<br/>
<img src="https://raw.githubusercontent.com/Zoel-Manchon/Zoel-Manchon/main/assets/pipeline.svg" width="100%" alt="Animated terminal panel: data flowing through Zoel's pipeline — edge sensors, link, backend, store, telemetry — with a security layer scanning across every stage." />
<br/>
</div>

<br/>

## `$ whoami`

<div align="center">

<img src="https://raw.githubusercontent.com/Zoel-Manchon/Zoel-Manchon/main/assets/whoami.svg" width="100%" alt="System spec card — role, focus, editor, languages, APIs, data, infrastructure and edge stack." />

</div>

I learn by building real systems end to end — edge sensors, secured services, real-time backends, and analytical tools. The pipeline above isn't a metaphor; it's the shape of most things in here.

<div align="center">

`AppSec` · `DevSecOps` · `IoT / OT security` — **secure by design, from the sensor to the dashboard.**

</div>

<br/>

<div align="center">

<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/Ruby-CC342D?style=flat-square&logo=ruby&logoColor=white"/>
<img src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-000000?style=flat-square&logo=linux&logoColor=white"/>
<img src="https://img.shields.io/badge/Buildroot-2E3B4E?style=flat-square"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>
<img src="https://img.shields.io/badge/Hardening-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>

</div>

<br/>

## `$ tree ~/projects`

```bash
~/projects
├── os/              # emberwall — hardened IoT/OT linux distro (buildroot + rust)
├── cybersecurity/   # secrets vault, zero-trust auth, scanners, hardening
├── desktop/         # native rust gui tools — file integrity monitor
├── iot/             # esp32, lora, edge-ml, secured telemetry pipelines
├── quant/           # backtesting engines, trading analytics
├── backend/         # real-time services, tamper-evident blockchain
└── games/           # because why not
```

<br/>

## `~/os` &nbsp;·&nbsp; ⭐ featured

<div align="center">

### 🔥 Emberwall — Hardened IoT/OT Security Linux

<em>A whole Linux distribution, built from source — where my scanner and my vault become one native Rust binary.</em>

</div>

A **from-scratch Linux distribution** built with **Buildroot** — its own cross-toolchain, a hardened kernel, and a few-MB immutable userland: no package manager, `PIE` / `RELRO` / `SSP` / `FORTIFY`, KASLR, `lockdown` + `yama` LSMs, and an `nftables` default-deny firewall. It ships **`sentinel`**, a native **Rust** tool that unifies my [`pyscan`](https://github.com/Zoel-Manchon/pyscan) scanner and the [`AegisVault`](https://github.com/Zoel-Manchon/aegisvault) crypto core into a single static binary: concurrent **TCP/UDP scanning** with OT/ICS + IoT recognition (Modbus, S7comm, IEC-104, CoAP, LoRaWAN) plus an **argon2id + XChaCha20-Poly1305** secrets vault. Designed to run as the **secure MQTT edge gateway** feeding the IoT pipelines below. Live ISO, workstation and locked-appliance variants for **x86-64 and ARM64**.

<div align="center">

<img src="https://img.shields.io/badge/Buildroot-2E3B4E?style=flat-square"/>
<img src="https://img.shields.io/badge/Linux-000000?style=flat-square&logo=linux&logoColor=white"/>
<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white"/>
<img src="https://img.shields.io/badge/Hardening-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/OT_Security-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/QEMU_/_ISO-3FB950?style=flat-square"/>

<br/><br/>

<img src="https://raw.githubusercontent.com/Zoel-Manchon/emberwall/main/docs/demo.gif" width="100%" alt="Emberwall live demo: silent boot, sentinel TCP/UDP/Modbus scan, secrets vault, and MQTT gateway."/>

<br/>

[**→ repository**](https://github.com/Zoel-Manchon/emberwall)

</div>

<br/>

## `~/cybersecurity`

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

> 🔥 Its Rust crypto core lives on as a native binary in [**Emberwall**](https://github.com/Zoel-Manchon/emberwall).

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

> 🔥 Ported to a native Rust `sentinel scan` inside [**Emberwall**](https://github.com/Zoel-Manchon/emberwall).

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

<details>
<summary><b>▸ Live demos — attack ranges catching attacks in real time</b></summary>
<br/>
<div align="center">

**Emberwall** — the hardened distro booting, `sentinel` scanning & the vault, all live
<img src="https://raw.githubusercontent.com/Zoel-Manchon/emberwall/main/docs/demo.gif" width="100%" alt="Emberwall live demo: silent boot, sentinel TCP/UDP/Modbus scan, secrets vault, and MQTT gateway."/>
<br/><br/>

**Aegis** — launch an attack from the SOC console and watch the detections fire
<img src="https://raw.githubusercontent.com/Zoel-Manchon/aegis-zero-trust/main/docs/attack_simulator.gif" width="100%" alt="Aegis zero-trust attack range: attacks launched, detections firing live in the SOC console."/>
<br/><br/>

**Auth-Lab** — the attack simulator driving scripted scenarios against the defenses
<img src="https://raw.githubusercontent.com/Zoel-Manchon/auth-lab/main/docs/diagrams/demo/attack-simulator.gif" width="100%" alt="Auth-Lab attack simulator running scripted attack scenarios with PASS/FAIL verdicts."/>
<br/><br/>

**Pyscan** — the modular OT/port scanner in action
<img src="https://raw.githubusercontent.com/Zoel-Manchon/pyscan/main/docs/demo.gif" width="100%" alt="Pyscan modular port and OT-protocol scanner demo."/>

</div>
</details>

## `~/desktop`

#### ◆ phosphor — File Integrity Monitor (Rust GUI)

A native desktop **file integrity monitor** (a mini Tripwire/AIDE) written in
Rust with an **egui** amber-CRT interface. Anchor a **SHA-256 baseline** of a
folder, then watch it in real time: a background `notify` thread streams
filesystem events down an `mpsc` channel and any modification, addition or
deletion surfaces the instant it happens — with a native desktop alert while
minimized. The baseline itself is **HMAC-SHA256 signed** (constant-time verify),
so an attacker who edits a file *and* rewrites `.phosphor.json` still can't forge
a valid signature without the key — *quis custodiet ipsos custodes*. Gitignore-style
ignore rules, re-baseline, and **JSON/CEF export** for SIEM ingestion. Pure,
unit-tested core with zero UI dependencies; cross-platform (inotify / FSEvents /
Win32).

<p>
<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/egui-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/SHA--256-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/HMAC_Signed-A32D2D?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/SIEM_JSON_/_CEF-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
</p>

> 🔥 Designed to fold into [**Emberwall**](https://github.com/Zoel-Manchon/emberwall) as an endpoint-integrity component.

[**→ repository**](https://github.com/Zoel-Manchon/phosphor)

<img src="https://raw.githubusercontent.com/Zoel-Manchon/phosphor/main/docs/demo.gif" width="100%" alt="phosphor — amber-CRT file integrity monitor: anchoring a signed baseline, live tamper detection with modified/added/deleted findings, desktop alert, and a rejected forged baseline."/>

## `~/iot`

> **Simulation-first IoT.** I build each pipeline against a coherent *virtual world*
> before any hardware exists — so the full **edge → broker → TSDB → dashboard** path
> is testable on day one, and the ESP32/LoRa integration stays isolated to adapter
> swaps. Hexagonal cores, MicroPython-ready, enforced by architecture fitness tests.
> Three end-to-end pipelines so far, **123 tests** between them, security built in.
>
> 🔥 They all ingest through **[Emberwall](https://github.com/Zoel-Manchon/emberwall)** — my hardened MQTT edge gateway.

<div align="center">

| Pipeline | Domain | Security | Tests | Status |
|:---|:---|:---|:---:|:---:|
| **🌾 agrisentinel** | crops · water · livestock | HMAC + anti-replay + anomaly detection | `33` | sim-ready |
| **🛡️ sentinel-node** | air · presence · edge ML | on-device ML, raw media never leaves | `45` | sim-ready |
| **☀️ solar-weather-station** | weather · solar power | self-powered edge, LoRa link | `43` | sim-ready |

</div>

<table>
<tr>
<td width="50%" valign="top">

#### 🌾 agrisentinel — Secured Rural IoT Lab

Smart-farm lab across **three domains at once** — crops, water and livestock —
where the sensor network itself is treated as an attack surface. Every field node
signs its telemetry with **HMAC + sequence + nonce**; a gateway verifies each frame
and runs four independent anomaly checks (out-of-range, replay, stale, rate) before
forwarding only what it trusts. Clean telemetry and security alerts travel on
separate MQTT streams, feeding **two Grafana dashboards from one pipeline** — an
agronomy view and a SOC-style security view. Inject a spoof/replay/forged attack
from the CLI and watch the SOC light up live. Physics is the last line of defence:
even a stolen key can't report soil moisture at 250%.

<img src="https://img.shields.io/badge/Security-HMAC_+_Anomaly-A32D2D?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Architecture-Hexagonal-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/agrisentinel)

</td>
<td width="50%" valign="top">

#### 🛡️ sentinel-node — Multi-Sensor Edge Sentinel

Space-monitoring node fusing **air quality (BME680)**, **mmWave human presence
(LD2410)**, and **on-device ML** for acoustic events (INMP441 + TinyML) and vision
(ESP32-CAM). Its hexagonal core models two kinds of observation on purpose — scalar
`Measurement`s and discrete `Event`s from edge models — so **raw audio and images
never enter the telemetry frame**: the classifier runs on-device and only the
verdict is published (camera JPEGs saved out-of-band, served via a Node-RED
gallery). A coherent simulated space drives every channel from one occupancy
schedule; MQTT → Node-RED → InfluxDB → Grafana.

<img src="https://img.shields.io/badge/ESP32--S3-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/Edge_ML-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/mmWave_LD2410-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/Architecture-Hexagonal-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/sentinel-node)

</td>
</tr>
</table>

<table>
<tr>
<td width="50%" valign="top">

#### ☀️ solar-weather-station — Self-Powered Weather IoT

Solar-powered weather-station architecture developed **simulation first**. A
coherent virtual weather world drives simulated BME280, BH1750, PMS5003 and rain
sensors, reproducing daylight cycles, pressure fronts, rainfall, humidity changes,
particulate scrubbing, solar charging and battery behavior. Telemetry flows over
MQTT through Node-RED into InfluxDB and Grafana, while the hexagonal,
MicroPython-ready core keeps the future ESP32 + LoRa hardware integration isolated
to adapter changes. Ingest is handled by my
[**Emberwall**](https://github.com/Zoel-Manchon/emberwall) MQTT edge gateway.

<img src="https://img.shields.io/badge/Status-Simulation_Ready-3FB950?style=flat-square"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Architecture-Hexagonal-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/LoRa-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/solar-weather-station)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

> **Why simulation-first?** Building against a virtual world means the whole pipeline — sensors, broker, storage, dashboards, and the security layer — is verified in CI before a single wire is soldered. The domain and application layers are MicroPython-safe, so the move to real ESP32 hardware is a mechanical adapter swap, not a rewrite. Same discipline I apply to backend work: test the contract, isolate the I/O.

<details>
<summary><b>▸ Live demos — dashboards & a security layer catching an attack</b></summary>
<br/>
<div align="center">

**sentinel-node** — occupancy, air quality & a scripted acoustic anomaly
<img src="https://raw.githubusercontent.com/Zoel-Manchon/sentinel-node/main/docs/screenshots/demo.gif" width="100%" alt="Sentinel Node live dashboard."/>
<br/><br/>

**agrisentinel** — a spoof attack lighting up the SOC dashboard in real time
<img src="https://raw.githubusercontent.com/Zoel-Manchon/agrisentinel/main/docs/demo-soc.gif" width="100%" alt="AgriSentinel security dashboard reacting to an injected attack."/>
<br/><br/>

**solar-weather-station** — a simulated day with a scripted rain event, streamed live
<img src="https://raw.githubusercontent.com/Zoel-Manchon/solar-weather-station/main/docs/demo.gif" width="100%" alt="Solar weather station: a simulated day with a scripted rain event streaming into Grafana."/>

</div>
</details>

<br/>

<details>
<summary><b>▸ More IoT — earlier hardware & LoRaWAN projects</b></summary>
<br/>
<table>
<tr>
<td width="50%" valign="top">

#### API IoT

End-to-end temperature & humidity monitor: ESP32 + DHT22 firmware publishing over
MQTT to a Node.js/Express backend and a real-time React dashboard.

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>

[**→ repository**](https://github.com/Zoel-Manchon/api_iot)

</td>
<td width="50%" valign="top">

#### Eastron LoRaWAN Energy Monitoring

Energy monitoring over LoRaWAN: collecting, processing, and visualizing electrical
consumption data through an InfluxDB + Grafana telemetry stack.

<img src="https://img.shields.io/badge/LoRaWAN-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

[**→ repository**](https://github.com/Zoel-Manchon/eastron-lorawan-energy-monitoring)

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### SmartWatch LoRaWAN

Wearable IoT project using LoRaWAN, embedded sensors, and remote monitoring.

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/LoRaWAN-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/Wearable_IoT-3FB950?style=flat-square"/>

[**→ repository**](https://github.com/Zoel-Manchon/Proyecto_IoT_J3_SmartWatch_LoRaWAN)

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>
</details>

## `~/quant`

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

## `~/backend`

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

#### ⛓ toychain — Tamper-Evident Blockchain (Rails)

An educational blockchain in Ruby on Rails built to make integrity *visible* —
and attributable. SHA-256 proof-of-work mined in **background jobs** (Solid
Queue) with a live progress bar streamed to every browser via Turbo Streams
over Solid Cable — a DB-backed realtime layer, **authenticated at the
WebSocket**. Every block records its mining operator; tampering is signed into
the data; a three-check validator (link · integrity · declared work) breaks
the chain in cascade. **Bearer-token JSON API** (only SHA-256 digests stored)
consumed by a dependency-free **Python verifier** that re-validates the whole
chain independently — don't trust, verify. Brakeman + RuboCop + ~40 tests in CI.

<img src="https://img.shields.io/badge/Rails_8-CC0000?style=flat-square&logo=rubyonrails&logoColor=white"/>
<img src="https://img.shields.io/badge/Ruby-CC342D?style=flat-square&logo=ruby&logoColor=white"/>
<img src="https://img.shields.io/badge/Solid_Queue_·_Cable-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/Hotwire-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/SHA--256_PoW-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/Bearer_API_+_Py_verifier-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>

[**→ repository**](https://github.com/Zoel-Manchon/toychain)

</td>
</tr>
</table>

<details>
<summary><b>▸ Live demos — real-time terminal & a chain breaking in cascade</b></summary>
<br/>
<div align="center">

**Crypto·Watch** — live prices, charts, and market analytics
<img src="https://raw.githubusercontent.com/Zoel-Manchon/crypto-dashboard/main/docs/screenshots/terminal.gif" width="100%" alt="Crypto·Watch real-time terminal: live prices, charts, and market analytics."/>
<br/><br/>

**toychain** — mine live, tamper with attribution, and verify the chain externally
<img src="https://raw.githubusercontent.com/Zoel-Manchon/toychain/main/docs/demo.gif" width="100%" alt="toychain: live proof-of-work mining with progress bar, attributed tamper breaking the chain in cascade, and independent verification from a Python script."/>

</div>
</details>

## `~/games`

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

<details>
<summary><b>▸ Live demo — Snake HD</b></summary>
<br/>
<div align="center">
<img src="https://raw.githubusercontent.com/Zoel-Manchon/snake-hd/main/docs/screenshots/snake_hd.gif" width="100%" alt="Snake HD: pixel-art arcade snake with combos, power-ups, and screen shake."/>
</div>
</details>

<br/>

## `$ cat ~/.principles`

```text
> build small systems, not isolated scripts
> measure what you build
> keep security in mind from line one
> ship something that actually works
```

<br/>


<div align="center">

**From edge devices to secured data — still learning, still building.**

</div>
