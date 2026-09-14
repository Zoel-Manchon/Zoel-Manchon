<div align="center">

# Zoel Arias Manchón

### IoT/OT Security · Secure Systems · Rust / Python / Java · AppSec / DevSecOps

I build security-focused systems end to end: embedded telemetry, hardened Linux,
zero-trust identity, cryptographic evidence, defensive attack simulations,
real-time backends and native tools.

[Portfolio](https://zoel-manchon.github.io/) ·
[LinkedIn](https://www.linkedin.com/in/zoel-arias-manchon) ·
[Email](mailto:zroot1001@proton.me)

**Core stack:** `Rust` · `Python` · `Java` · `TypeScript` · `Linux` · `Docker` · `PostgreSQL` · `TimescaleDB` · `MQTT`

</div>

---

## Featured work at a glance

| Project | What it is | Stack | Demo |
|---|---|---|---|
| **[Emberwall](https://github.com/Zoel-Manchon/emberwall)** | Hardened Linux built from source for IoT/OT edge | `Buildroot` `Rust` `nftables` | [▶](#emberwall) |
| **[Psychron](https://github.com/Zoel-Manchon/psychron)** | Secure ESP32 telemetry that survives outages | `ESP32` `FastAPI` `MQTT/mTLS` | [▶](#psychron) |
| **[Aegis](https://github.com/Zoel-Manchon/aegis-zero-trust)** | Zero-trust identity provider with a live SOC | `Rust` `Axum` `React` | [▶](#aegis) |
| **[HoneyTrap](https://github.com/Zoel-Manchon/honeytrap)** | MQTT/CoAP honeypot that refuses to amplify | `Python` `asyncio` `InfluxDB` | [▶](#honeytrap) |
| **[Keystone](https://github.com/Zoel-Manchon/keystone-control-plane)** | Device identity and OTA plane with its own CA | `Java 25` `Spring Boot` `PostgreSQL` | [▶](#keystone) |
| **[Prorata](https://github.com/Zoel-Manchon/prorata)** | Tamper-evident submetering a tenant can verify | `Python` `FastAPI` `Angular` | [▶](#prorata) |
| **[Ferrogate](https://github.com/Zoel-Manchon/ferrogate)** | Multi-tenant telemetry isolated in the engine | `Python` `MQTT/mTLS` `InfluxDB` | [▶](#ferrogate) |
| **[AgriSentinel](https://github.com/Zoel-Manchon/agrisentinel)** | Rural IoT lab whose gateway trusts no frame | `Python` `MQTT/mTLS` `Grafana` | [▶](#agrisentinel) |
| **[Sentinel Node](https://github.com/Zoel-Manchon/sentinel-node)** | Edge sentinel where raw audio and video never leave | `ESP32-S3` `TinyML` `MQTT` | [▶](#sentinel-node) |
| **[Solar Weather Station](https://github.com/Zoel-Manchon/solar-weather-station)** | Solar ESP32 station whose core runs on MicroPython | `Python` `LoRa` `InfluxDB` | [▶](#solar-weather-station) |
| **[Pyscan](https://github.com/Zoel-Manchon/pyscan)** | OT scanner and ICS intrusion detector on one core | `Python` `asyncio` `Modbus/S7` | [▶](#pyscan) |

---

## Profile

My work sits between **software engineering, cybersecurity and connected devices**.
I am especially interested in systems where security is part of the architecture,
not an additional layer added at the end.

I focus on:

- **IoT/OT security:** secure telemetry, edge gateways, MQTT, LoRaWAN and anomaly detection.
- **Systems security:** Rust, hardened Linux, integrity controls and applied cryptography.
- **Cryptographic evidence:** hash chains, Merkle transparency logs and proofs a third party can recheck.
- **Application security:** zero-trust authentication, MFA, passkeys, RBAC and auditability.
- **Delivery:** reproducible Docker environments, automated tests, CI and technical documentation.

> **From the sensor to the SOC: build the complete system, define the trust boundaries,
> observe its behaviour and prove that the controls work.**

---

# Featured engineering work

## 1. <a id="emberwall"></a>[Emberwall — Hardened IoT/OT Security Linux](https://github.com/Zoel-Manchon/emberwall)

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

## 2. <a id="psychron"></a>[Psychron — Secure Environmental Telemetry](https://github.com/Zoel-Manchon/psychron)

**An ESP32 measures a room and produces a trustworthy record even through outages, reboots and an unavailable wall clock.**

Psychron secures the full telemetry path: the node authenticates with its own client
certificate, buffers readings locally when connectivity disappears, and a Python
ingest service reconstructs event time without flattening an outage into a false
period of calm. A React panel exposes both the environmental measurements and the
integrity of the record.

**Engineering evidence**

- MQTT 5 over mutual TLS, with broker ACLs bound to certificate identity and no plaintext listener.
- LittleFS ring buffer and oldest-first replay preserve readings while the network is unavailable.
- Boot anchors reconstruct timestamps from device uptime when the ESP32 has no valid wall clock.
- Idempotent identity through `(device, boot, seq)`, so replayed telemetry cannot become duplicate measurements.
- Explicit quality bits retain doubtful readings with provenance instead of silently discarding them.
- TimescaleDB hypertable and continuous aggregates keep queries bounded across long time ranges.
- Verified OTA digests, invitation-only panel enrolment, Argon2id, TOTP and hardened session cookies.
- 82 tests across the Python domain, the C++ payload builder and live mTLS transport assertions.

**Technology:** `ESP32 WROOM-32` · `Arduino C++` · `Python 3.12` · `FastAPI` · `React 19` · `PostgreSQL 17` · `TimescaleDB` · `MQTT/mTLS`

[Repository](https://github.com/Zoel-Manchon/psychron) ·
[Wire contract](https://github.com/Zoel-Manchon/psychron/blob/main/docs/CONTRACT.md)

https://github.com/user-attachments/assets/7cd61433-e8dd-42be-8adb-ff7d193a1d83

---

## 3. <a id="aegis"></a>[Aegis — Zero-Trust Identity & Defensive Attack Range](https://github.com/Zoel-Manchon/aegis-zero-trust)

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
[Walkthrough](https://github.com/Zoel-Manchon/aegis-zero-trust/blob/main/README.md)

https://github.com/user-attachments/assets/db154dab-3684-4ee1-919d-70c0405ac1c4

---

## 4. <a id="honeytrap"></a>[HoneyTrap — MQTT/CoAP Honeypot That Refuses to Amplify](https://github.com/Zoel-Manchon/honeytrap)

**A low-interaction IoT honeypot whose hardest requirement was not capturing attacks, but never becoming one.**

Over UDP the source address is never verified, so a CoAP service that answers every
request is a reflector waiting to be aimed at someone else. HoneyTrap emulates
believable IoT devices, classifies the hostile traffic they attract, and decides per
datagram whether replying is safe.

**Engineering evidence**

- Anti-amplification by design: a response-size ceiling, a per-source token bucket bounded in memory, and `Proxy-Uri` never honoured. The attempt is always recorded; only the reply is withheld.
- MQTT 3.1/3.1.1/5.0 and CoAP codecs as pure functions over `bytes`, fuzzed with 5,000 random inputs each — no exception but a malformed-packet error may escape.
- Spec violations are captured, not rejected: a strict parser would discard exactly the traffic worth studying.
- Every listener limit is a security control with a test: byte budgets, idle and session timeouts, per-IP connection caps.
- Attacker-controlled values never become InfluxDB tags — `client_id` as a tag is a cardinality DoS against your own database.
- Newlines are stripped rather than escaped: neither line protocol nor CEF can escape them, so one would inject a forged record.
- The attack simulator is a separate package importing nothing from the honeypot, and every scenario doubles as a CI regression test.
- CEF output on the same Emberwall schema as `phosphor` and `maat`, so a hostile session and a file-integrity alert correlate in one pane.
- Zero runtime dependencies, hash-pinned toolchain, 105 tests, `mypy --strict`, `bandit` and `ruff` clean.

**Technology:** `Python` · `asyncio` · `Hexagonal architecture` · `MQTT` · `CoAP` · `InfluxDB` · `Grafana` · `Docker`

[Repository](https://github.com/Zoel-Manchon/honeytrap) ·
[Architecture](https://github.com/Zoel-Manchon/honeytrap/blob/main/docs/ARCHITECTURE.md)

https://github.com/user-attachments/assets/23ed7417-6421-4fc8-b83d-7f227bf84f72

---

## 5. <a id="keystone"></a>[Keystone — Device Identity & OTA Control Plane](https://github.com/Zoel-Manchon/keystone-control-plane)

**A control plane that decides who a device is and what firmware it is allowed to run.**

Keystone collects no telemetry. It runs its own two-tier X.509 CA, enrols devices with
single-use tokens, signs firmware artifacts and rolls updates out by cohort with
rollback. The layers are separate **Maven modules**, so the direction of dependencies is
guaranteed by the compiler rather than by discipline.

**Engineering evidence**

- Root + issuing CA hierarchy on EC P-256, with CSR proof-of-possession; the subject and extensions are set by the CA and never copied from the request.
- Enrolment tokens are spent by an atomic compare-and-set in PostgreSQL, so exactly one of N concurrent requests can win before any certificate is signed.
- Certificate rotation demands an ECDSA signature from the **current** private key over the canonical DER of the new CSR — a fingerprint is public information, not a secret.
- Real mTLS against Mosquitto: server certificate issued by the CA, `require_certificate`, CRL refreshed every 5 minutes and per-device-id ACLs.
- Firmware signed with Ed25519; the device id lives inside the signed manifest, so a manifest cannot be replayed onto another device.
- Cohort membership is computed, not stored: a rollout over a hundred thousand devices costs the same as one over ten.
- Hash-chained audit log with an append-only trigger in PostgreSQL, so an `UPDATE` is rejected by the engine.
- 78 tests: 30 domain, 5 application, 6 ArchUnit contracts and 37 integration tests against a real PostgreSQL via Testcontainers.

**Technology:** `Java 25` · `Spring Boot 4` · `PostgreSQL` · `Bouncy Castle` · `MQTT/mTLS` · `Testcontainers` · `ArchUnit`

[Repository](https://github.com/Zoel-Manchon/keystone-control-plane)

https://github.com/user-attachments/assets/4ba67ffe-b369-4bb9-b658-b71dc7ed7610

---

## 6. <a id="prorata"></a>[Prorata — Tamper-Evident Submetering](https://github.com/Zoel-Manchon/prorata)

**Split a building's shared consumption, and let the tenant recompute the evidence behind their bill.**

A meter reading only means something if you know who measured it, so the signature is
produced **on the device** before anything touches the network. Every settlement interval
is sealed with a Merkle root, and a tenant disputing a line recomputes it **in their own
browser** — a proof checked by the server that issued the invoice would prove nothing.

**Engineering evidence**

- On-device Ed25519 signing over a canonical payload, verified against the certificate enrolled at commissioning; enrolment is a deliberate operator action, never a self-service endpoint.
- RFC 6962 append-only log: inclusion proofs say a reading is in *some* tree, so consistency proofs show nothing was rewritten between two heads.
- Each head is co-signed by an independent witness running outside the operator's control, and optionally anchored on chain.
- The common-area split uses largest remainder, because rounding must not create or destroy kWh.
- MySQL triggers reject `UPDATE`/`DELETE` on readings and sealed intervals: application-level append-only is not enough.
- Erasure without destroying evidence — readings are encrypted per tenant, so destroying the key erases the data while every root and proof still verifies.
- Nothing is ever edited: a bad reading is superseded by a new signed frame carrying the original's timestamp, so the energy stays in its own tariff period.
- 261 tests, 134 of them running with no database and no I/O at all; Python and TypeScript assert the same protocol vectors so the two sides cannot drift.

**Technology:** `Python` · `FastAPI` · `Angular` · `MySQL` · `Ed25519` · `RFC 6962` · `Hexagonal architecture`

[Repository](https://github.com/Zoel-Manchon/prorata)

https://github.com/user-attachments/assets/e0dd7a3c-2e27-4de8-8d5b-c59b388dc889

---

## 7. <a id="ferrogate"></a>[Ferrogate — Multi-Tenant Industrial Telemetry](https://github.com/Zoel-Manchon/ferrogate)

**Edge gateways that speak Modbus and OPC-UA, publishing to a platform that isolates each customer in the engine, not in the code.**

The ingest service is an MQTT client: it never sees the certificate of the gateway that
published. So every envelope is signed at the edge and verified against the certificate
enrolled in PostgreSQL, which puts **the broker outside the trust base** — it can replay,
reorder or mix messages, but it cannot forge a valid one.

**Engineering evidence**

- Gateway identity lives in the certificate SAN and is the only source of truth; the topic is checked against the proven identity, never the reverse.
- Topic ownership is compared segment by segment, so `acme` never validates a topic belonging to `acme-corp`.
- Replay defence on two axes: a time window on `sent_at` and a monotonic per-gateway sequence persisted across restarts.
- Tenant isolation by PostgreSQL Row Level Security with `FORCE`, so the policy applies to the table owner too. The scope is transaction-local: with a connection pool, a session-level setting would leak the previous request's tenant.
- It fails closed — with no tenant set, `current_setting` returns NULL, and NULL matches nothing.
- Four bounded contexts that cannot import each other, enforced by `import-linter` as a build-breaking contract.
- Store-and-forward SQLite buffer at the edge, drained before anything new so an intermittent link does not deliver data out of order.
- 62 tests, 2 architecture contracts, `ruff`, `mypy --strict` and `bandit` clean.

**Technology:** `Python` · `DDD` · `Modbus` · `OPC-UA` · `MQTT/mTLS` · `PostgreSQL RLS` · `InfluxDB` · `Grafana`

[Repository](https://github.com/Zoel-Manchon/ferrogate)

https://github.com/user-attachments/assets/a6826689-530c-48cd-af2b-8a3253fda893

---

## 8. <a id="agrisentinel"></a>[AgriSentinel — Rural IoT Security Lab](https://github.com/Zoel-Manchon/agrisentinel)

**Crops, water and livestock telemetry behind a gateway that treats the sensor network itself as an attack surface.**

A spoofed soil probe triggers needless irrigation; a replayed "tank full" hides a dry tank.
Three field nodes sign every reading, and the gateway verifies, inspects and only then
forwards what it trusts — clean telemetry and security alerts on separate streams, so one
pipeline feeds both an agronomy dashboard and a SOC dashboard.

**Engineering evidence**

- Every frame carries an HMAC, a sequence number and a nonce; per-node keys are derived from one master, with rotation and revocation.
- Four independent checks at the gateway: bad signature, out-of-range value, replay (by sequence **and** by nonce), and stale or flooding traffic.
- Physics is the last line of defence: an attacker holding the key still cannot report 250% soil moisture without an alert.
- MQTT over mutual TLS, one client certificate per node (`CN = key_id`), individually revocable by CRL.
- Tamper-evident hash-chained log of security events; InfluxDB and Grafana behind a TLS proxy with a write-only token.
- A CI fitness test proves the core imports no adapters, I/O or crypto, so raw wire bytes never reach the domain and the core stays MicroPython-safe.
- Threat model with zones, conduits, STRIDE and IEC 62443 foundational requirements; 43 tests.

**Technology:** `Python` · `Hexagonal architecture` · `HMAC` · `MQTT/mTLS` · `Node-RED` · `InfluxDB` · `Grafana` · `Caddy`

[Repository](https://github.com/Zoel-Manchon/agrisentinel) ·
[Threat model](https://github.com/Zoel-Manchon/agrisentinel/blob/main/docs/THREAT_MODEL.md)

<a href="https://github.com/Zoel-Manchon/agrisentinel/blob/main/docs/demo-soc.gif">
  <img src="https://raw.githubusercontent.com/Zoel-Manchon/agrisentinel/main/docs/demo-soc.gif"
       alt="AgriSentinel security dashboard flipping to UNDER ATTACK as an injected spoof attack raises alerts"
       width="100%">
</a>

---

## 9. <a id="sentinel-node"></a>[Sentinel Node — Multi-Sensor Edge Sentinel](https://github.com/Zoel-Manchon/sentinel-node)

**Air quality, mmWave presence, acoustic TinyML and vision on one hexagonal core — and raw media never enters the pipeline.**

The audio node classifies on the device and publishes only the verdict; the camera writes
its JPEG out of band and puts a *path* in the event. A time-series database is not a blob
store, and a microphone that ships audio is a different product with different consent.

**Engineering evidence**

- Two kinds of observation: a `Measurement` is a scalar reading, an `Event` is a classification from an edge model — separate data and event planes in InfluxDB.
- Glass-break or person-count verdicts leave the device; audio samples and images do not.
- One coherent simulated space: a single occupancy schedule drives the radar, CO₂/VOC, room temperature, sound events and head count, so the channels agree because they share a cause.
- The hexagon is enforced by `tests/test_architecture.py`: the domain and use cases import no adapters and run unmodified on MicroPython.
- The move to hardware is per sensor and mechanical — one import line — and sensors not yet on the bench stay simulated.
- 55 tests, architecture fitness functions included.

**Technology:** `ESP32-S3` · `TinyML` · `ESP32-CAM` · `BME680` · `LD2410 mmWave` · `Python / MicroPython` · `MQTT` · `Node-RED` · `InfluxDB` · `Grafana`

[Repository](https://github.com/Zoel-Manchon/sentinel-node) ·
[Setup guide](https://github.com/Zoel-Manchon/sentinel-node/blob/main/docs/SETUP.md)

<a href="https://github.com/Zoel-Manchon/sentinel-node/blob/main/docs/screenshots/demo.gif">
  <img src="https://raw.githubusercontent.com/Zoel-Manchon/sentinel-node/main/docs/screenshots/demo.gif"
       alt="Sentinel Node Grafana dashboard: a simulated day of occupancy, air quality and a scripted acoustic anomaly"
       width="100%">
</a>

---

## 10. <a id="solar-weather-station"></a>[Solar Weather Station — Self-Powered ESP32 Telemetry](https://github.com/Zoel-Manchon/solar-weather-station)

**A solar ESP32 weather station whose core runs on the microcontroller unchanged — and a test that walks the AST to keep it that way.**

BME280, BH1750, PMS5003 and a rain sensor report from an 18650 cell and a small panel.
The whole pipeline runs today without hardware, against one coherent virtual weather world
rather than four random generators.

**Engineering evidence**

- The domain and use cases import no adapters, no third-party libraries and none of `typing`, `dataclasses`, `abc`, `enum` or `asyncio`; an AST-walking test fails CI if that breaks.
- One world, every channel: a storm saturates humidity, collapses illuminance and scrubs particulates on every panel at once, because it is the same event.
- Solar charging and 18650 battery state are modelled and reported as telemetry.
- The transport is a port: MQTT straight to the broker today, LoRa P2P at 868 MHz and a gateway slotting in ahead of it without touching the core.
- A demo director scripts the rain cues, so a full day replays in twelve minutes, reproducibly.
- 43 tests; next is a binary codec of 64 bytes or less, because JSON does not fit the LoRa payload budget.

**Technology:** `Python / MicroPython` · `ESP32` · `LoRa P2P` · `MQTT` · `Node-RED` · `InfluxDB` · `Grafana`

[Repository](https://github.com/Zoel-Manchon/solar-weather-station)

<a href="https://github.com/Zoel-Manchon/solar-weather-station/blob/main/docs/demo.gif">
  <img src="https://raw.githubusercontent.com/Zoel-Manchon/solar-weather-station/main/docs/demo.gif"
       alt="Solar Weather Station Grafana dashboard: a simulated day with a scripted rain event"
       width="100%">
</a>

---

## 11. <a id="pyscan"></a>[Pyscan — OT Scanner & ICS Intrusion Detector](https://github.com/Zoel-Manchon/pyscan)

**A port scanner, an OT protocol identifier, a packet sniffer and an ICS detection engine — all on one small hexagon.**

A scanner asks *what is this device?*; an intrusion detector asks *who is touching it?*.
Both need to know what a Modbus write is, so here they share one set of pure protocol
codecs instead of each keeping its own copy — fix a codec once and both products are fixed.

**Engineering evidence**

- Async TCP connect, SYN over IPv4 and IPv6, and UDP with protocol-aware payloads, plus banner and version fingerprinting and a CIDR sweep rate-limited across the whole sweep.
- Read-only OT identification: Modbus device ID, IEC 60870-5-104 keepalive and the S7comm module order number.
- `pyscan monitor` checks Modbus, IEC-104 and S7comm traffic against a baseline of who may drive the process, with alerts mapped to MITRE ATT&CK for ICS and the action a responder should take.
- Streaming pcap and pcapng reader of its own: the whole OT toolkit runs on the standard library.
- Two Textual TUIs, including an OT command centre with an evidence timeline and a one-keystroke incident report.
- A new technique is one file and one `@register` line; the domain knows nothing about sockets, files or the terminal.
- 255 tests, 89% coverage gated in CI, `mypy --strict`, `ruff`, `bandit`, CodeQL and `pip-audit` on Linux, macOS and Windows.

**Technology:** `Python` · `asyncio` · `Typer` · `Textual` · `Modbus` · `IEC-104` · `S7comm` · `MITRE ATT&CK for ICS`

[Repository](https://github.com/Zoel-Manchon/pyscan)

https://github.com/user-attachments/assets/ad3e4071-137c-411f-9e3b-ee4022adcc8b

---

# Security desktop tools

| [AegisVault — Local-First Encrypted Secrets Vault](https://github.com/Zoel-Manchon/aegisvault) | [Phosphor — Native File Integrity Monitor](https://github.com/Zoel-Manchon/phosphor) |
|---|---|
| <a href="https://github.com/Zoel-Manchon/aegisvault/blob/main/docs/demo.gif"><img src="https://raw.githubusercontent.com/Zoel-Manchon/aegisvault/main/docs/demo.gif" alt="AegisVault unlocking, secret management and audit ledger demo" width="100%"></a> | <a href="https://github.com/Zoel-Manchon/phosphor/blob/main/docs/demo.gif"><img src="https://raw.githubusercontent.com/Zoel-Manchon/phosphor/main/docs/demo.gif" alt="Phosphor baseline signing and real-time tamper detection demo" width="100%"></a> |
| Zero-knowledge vault with a Python domain core and Rust cryptography through PyO3: Argon2id, XChaCha20-Poly1305, envelope encryption, Shamir K-of-N recovery and a hash-chained audit ledger. | Signs a SHA-256 baseline with HMAC, verifies it in constant time and flags modified, added or deleted files in real time, with JSON and CEF export for a SIEM. |
| `Python` · `Rust` · `PyO3` · `PySide6` | `Rust` · `egui` · `HMAC` · `SIEM` |

---

# Additional selected projects

### Security and systems

- **[Maat](https://github.com/Zoel-Manchon/maat)** — Rust modal editor with SHA-256 integrity tracking, atomic saves, external-change detection and SIEM audit output. · [Demo](https://github.com/Zoel-Manchon/maat/blob/main/assets/maat-demo.gif)
- **[Auth-Lab](https://github.com/Zoel-Manchon/auth-lab)** — NestJS zero-trust authentication lab with MFA, replay defence, risk analysis and a controlled attack simulator. · [Demo](https://github.com/Zoel-Manchon/auth-lab/blob/main/docs/diagrams/demo/attack-simulator.gif)
- **[Arch Linux Hardened Server](https://github.com/Zoel-Manchon/arch-linux-hardened-server)** — documented Linux hardening and attack-surface reduction.

### Backend and data

- **[Toychain](https://github.com/Zoel-Manchon/toychain)** — Rails 8 tamper-evident blockchain with background proof-of-work, authenticated real-time updates and an independent Python verifier. · [Demo](https://github.com/Zoel-Manchon/toychain/blob/main/docs/demo.gif)
- **[Crypto·Watch](https://github.com/Zoel-Manchon/crypto-dashboard)** — Rust/Axum WebSocket backend, Astro/React frontend, PostgreSQL persistence and Docker delivery.
- **[QuantLab](https://github.com/Zoel-Manchon/quantlab)** — DDD and hexagonal backtesting engine with order execution, OCO controls, walk-forward analysis and performance metrics.
- **[Elitewear XI](https://github.com/Zoel-Manchon/elitewear-xi)** — Laravel 13 ecommerce with PayPal checkout and a versioned REST API, built with application security as the design constraint: IDOR prevention, row-level locking against stock and coupon oversell, strict CSP without inline scripts and a tamper-evident audit log. The test suite verifies that the attacks fail.

### Earlier hardware and telemetry work

- **[Eastron LoRaWAN Energy Monitoring](https://github.com/Zoel-Manchon/eastron-lorawan-energy-monitoring)** — electrical-energy telemetry with LoRaWAN, InfluxDB and Grafana.
- **[SmartWatch LoRaWAN](https://github.com/Zoel-Manchon/Proyecto_IoT_J3_SmartWatch_LoRaWAN)** — wearable sensing and remote monitoring over LoRaWAN.
- **[Snake HD](https://github.com/Zoel-Manchon/snake-hd)** — polished Pygame project with a tamper-evident leaderboard backed by Rust/Axum. · [Demo](https://github.com/Zoel-Manchon/snake-hd/blob/main/docs/screenshots/snake_hd.gif)

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
