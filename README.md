<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=28&duration=2500&pause=800&color=3FB950&center=true&vCenter=true&width=950&lines=root%40zr00t%3A~%24+whoami;Backend+%7C+IoT+%7C+Security;From+ESP32+sensors+to+Rust+APIs;Learning+by+building+real+projects;ESP32+%E2%86%92+APIs+%E2%86%92+Telemetry" />

<br><br>

<img src="https://komarev.com/ghpvc/?username=Zoel-Manchon&style=for-the-badge&color=3fb950"/>
&nbsp;
<a href="mailto:zroot1001@proton.me">
<img src="https://img.shields.io/badge/Email-ProtonMail-6D4AFF?style=for-the-badge&logo=protonmail&logoColor=white"/>
</a>
&nbsp;
<a href="https://github.com/Zoel-Manchon">
<img src="https://img.shields.io/badge/GitHub-Zoel--Manchon-181717?style=for-the-badge&logo=github"/>
</a>

</div>

---

## root@zr00t

```bash
$ whoami

Zoel Arias Manchón
├── Backend & Web Developer
├── IoT & embedded tinkerer
├── Security enthusiast
└── Building real connected projects to learn
```

```text
What I'm into:
Embedded Devices → Backend APIs → Databases → Telemetry → Security
```

---

## Tech I Work With

<div align="center">

<table>
  <tr>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rust/rust-original.svg" width="44" height="44" alt="Rust"/><br>Rust</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="44" height="44" alt="Python"/><br>Python</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="44" height="44" alt="TypeScript"/><br>TypeScript</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="44" height="44" alt="JavaScript"/><br>JavaScript</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" width="44" height="44" alt="PHP"/><br>PHP</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="44" height="44" alt="React"/><br>React</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/astro/astro-original.svg" width="44" height="44" alt="Astro"/><br>Astro</td>
  </tr>
  <tr>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" width="44" height="44" alt="Node.js"/><br>Node.js</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg" width="44" height="44" alt="Laravel"/><br>Laravel</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="44" height="44" alt="PostgreSQL"/><br>PostgreSQL</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="44" height="44" alt="MySQL"/><br>MySQL</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" width="44" height="44" alt="MongoDB"/><br>MongoDB</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" width="44" height="44" alt="Redis"/><br>Redis</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" width="44" height="44" alt="Bootstrap"/><br>Bootstrap</td>
  </tr>
  <tr>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="44" height="44" alt="Docker"/><br>Docker</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" width="44" height="44" alt="Nginx"/><br>Nginx</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="44" height="44" alt="Linux"/><br>Linux</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="44" height="44" alt="Git"/><br>Git</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/grafana/grafana-original.svg" width="44" height="44" alt="Grafana"/><br>Grafana</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/influxdb/influxdb-original.svg" width="44" height="44" alt="InfluxDB"/><br>InfluxDB</td>
    <td align="center" width="92"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/arduino/arduino-original.svg" width="44" height="44" alt="Arduino"/><br>Arduino</td>
  </tr>
</table>

</div>

---

## How My Projects Fit Together

Most of what I build is a slice of one bigger idea: getting data out of the physical world and into something I can store, watch, and secure. My projects line up along that path — sensors on one end, dashboards on the other.

```mermaid
flowchart LR
    A["Edge devices<br/>ESP32 · sensors"] --> B["Connectivity<br/>LoRaWAN · MQTT"]
    B --> C["Backend APIs<br/>Rust · Axum · Node"]
    C --> D["Data stores<br/>PostgreSQL · MongoDB · Redis"]
    D --> E["Telemetry<br/>InfluxDB · Grafana"]
```

---

## Projects

<table>
<tr>
<td width="50%" valign="top">

### Aegis — Zero-Trust Auth Lab & Attack Range

Ground-up zero-trust identity provider in Rust/Axum with a built-in Security Operations Console. JWT (RS256) with refresh rotation & replay (JTI) detection, mandatory TOTP MFA for admins, a per-request risk engine with GeoIP impossible-travel detection, RBAC, and a hash-chained (tamper-evident) audit trail. A React SOC console streams events live (SSE) with WebSocket alert popups and a geo-map, plus a built-in attack range (10 scenarios + storm) to launch attacks and watch the detections fire. Dockerized behind a Caddy single-origin proxy, with optional HashiCorp Vault dynamic DB credentials.

<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/Axum-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
<img src="https://img.shields.io/badge/HashiCorp_Vault-FFEC6E?style=flat-square&logo=vault&logoColor=black"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Security-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>

[**→ View repository**](https://github.com/Zoel-Manchon/aegis-zero-trust)

</td>
<td width="50%" valign="top">

### Auth-Lab — Zero-Trust Authentication

Zero-trust auth backend: JWT access/refresh with rotation & replay (JTI) protection, mandatory TOTP MFA for admins, a per-request risk engine with GeoIP impossible-travel detection, RBAC and a security-event audit trail. Fronted by an Astro SOC dashboard behind a Caddy TLS proxy, with a defensive attack simulator that CI-verifies the defenses. Optional HashiCorp Vault layer for secrets & dynamic DB credentials.

<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/HashiCorp_Vault-FFEC6E?style=flat-square&logo=vault&logoColor=black"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Security-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>

[**→ View repository**](https://github.com/Zoel-Manchon/auth-lab)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### Crypto·Watch Dashboard

Real-time cryptocurrency terminal: a Rust/Axum backend streaming live prices over WebSockets to an Astro + React dashboard, with PostgreSQL persistence and a full Docker stack.

<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white"/>
<img src="https://img.shields.io/badge/Astro-FF5D01?style=flat-square&logo=astro&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>

[**→ View repository**](https://github.com/Zoel-Manchon/crypto-dashboard)

</td>
<td width="50%" valign="top">

### API IoT

End-to-end IoT temperature & humidity monitor: ESP32 + DHT22 firmware publishing over MQTT to a Node.js/Express backend and a real-time React dashboard.

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/Arduino_(.ino)-00979D?style=flat-square&logo=arduino&logoColor=white"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>

[**→ View repository**](https://github.com/Zoel-Manchon/api_iot)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### Eastron LoRaWAN Energy Monitoring

Energy monitoring over LoRaWAN: collecting, processing, and visualizing electrical consumption data.

<img src="https://img.shields.io/badge/LoRaWAN-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>
<img src="https://img.shields.io/badge/Telemetry-3FB950?style=flat-square"/>

[**→ View repository**](https://github.com/Zoel-Manchon/eastron-lorawan-energy-monitoring)

</td>
<td width="50%" valign="top">

### SmartWatch LoRaWAN

Wearable IoT project using LoRaWAN, embedded sensors, and remote monitoring.

<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/LoRaWAN-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/Embedded-111111?style=flat-square"/>
<img src="https://img.shields.io/badge/Wearable_IoT-3FB950?style=flat-square"/>

[**→ View repository**](https://github.com/Zoel-Manchon/Proyecto_IoT_J3_SmartWatch_LoRaWAN)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### Arch Linux Hardened Server

Security-focused Arch Linux setup: system hardening, reduced attack surface, and production-ready configuration practices.

<img src="https://img.shields.io/badge/Arch_Linux-1793D1?style=flat-square&logo=archlinux&logoColor=white"/>
<img src="https://img.shields.io/badge/Security-111111?style=flat-square&logo=hackthebox&logoColor=9FEF00"/>
<img src="https://img.shields.io/badge/Infrastructure-3FB950?style=flat-square"/>

[**→ View repository**](https://github.com/Zoel-Manchon/arch-linux-hardened-server)

</td>
<td width="50%" valign="top">

### Snake HD

Modern Snake game built around game logic, rendering, and desktop interaction.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Pygame-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/Game_Dev-3FB950?style=flat-square"/>

[**→ View repository**](https://github.com/Zoel-Manchon/snake-hd)

</td>
</tr>
</table>

---

## Currently Building

> Work in progress — repo and link will go live once it ships.

<table>
<tr>
<td width="50%" valign="top">

### Solar Weather Station — LoRa

Self-powered ESP32 weather station: BME280, BH1750, PMS5003 (PM1.0/2.5/10) and a rain sensor reporting over LoRa P2P to an ESP32 gateway, then MQTT → Home Assistant / Node-RED → InfluxDB → Grafana. Runs on an 18650 cell with a small solar panel.

<img src="https://img.shields.io/badge/Status-In_Progress-FFA500?style=flat-square"/>
<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square"/>
<img src="https://img.shields.io/badge/LoRa-0055FF?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

---

## What I'm Learning Right Now

```rust
struct Developer {
    name: &'static str,
    focus: [&'static str; 4],
    currently_building: &'static str,
    coffee_dependency: bool,
}

let zoel = Developer {
    name: "Zoel Arias Manchón",
    focus: [
        "Rust & Axum for backend APIs",
        "IoT with ESP32 & LoRaWAN",
        "Linux & security fundamentals",
        "Databases & telemetry pipelines",
    ],
    currently_building: "connected systems, end to end",
    coffee_dependency: true,
};
```

## How I Like to Work

```text
Build small projects, not just isolated scripts.
Measure what I build.
Automate the boring stuff.
Keep security in mind from the start.
Ship something that actually works.
```

<div align="center">

### From embedded devices to web apps — still learning, still building.

</div>
