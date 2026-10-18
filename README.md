<div align="center">

# Hi, I'm Miguel 👋

**Software Engineering student at UDC · A Coruña, Spain**



[![Website](https://img.shields.io/badge/migueltaibo.com-000000?style=flat&logo=cloudflare&logoColor=white)](https://migueltaibo.com)
[![Email](https://img.shields.io/badge/contact@migueltaibo.com-000000?style=flat&logo=icloud&logoColor=white)](mailto:contact@migueltaibo.com)

</div>

---

I've been programming since I was a kid. These days most of what I write lives on my own server: a Raspberry Pi that runs my home automation system, my cloud storage and the services around them, all self hosted and built from scratch.

## ☁️ TPCloud — my personal cloud

[**tpcloud**](https://github.com/mtaibo/tpcloud) is the gateway to everything I self host under `migueltaibo.com`. One Caddy gateway behind a Cloudflare Tunnel, one auth service with a single sign-on session across every subdomain, and a set of modules that plug into it.

<table>
<tr>
<td width="50%" valign="top">

#### 🔐 [`auth`](https://github.com/mtaibo/tpcloud/tree/main/auth) · [`login`](https://github.com/mtaibo/tpcloud/tree/main/login)
Authentication service with passkeys, password + TOTP, and sessions shared across all subdomains. Acts as an auth layer for every service.<br/>
<sub>Python · FastAPI · SQLModel · Vue 3</sub>

</td>
<td width="50%" valign="top">

#### 👤 [`accounts`](https://github.com/mtaibo/tpcloud/tree/main/accounts) · [`cloud`](https://github.com/mtaibo/tpcloud/tree/main/cloud)
Account management (profile, security, active sessions, admin) and the cloud dashboard that ties every module together.<br/>
<sub>Vue 3 · Tailwind </sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🗂️ [`tpstore`](https://github.com/mtaibo/tpstore)
My own storage and photo cloud: file browser, photo backup and share links.<br/>
<sub>Python · FastAPI · SQLite · Vue 3</sub>

</td>
<td width="50%" valign="top">

#### 📱 [`tpapp`](https://github.com/mtaibo/tpapp)
Native iOS and macOS app that replaces the web frontends: Store, Photos, Home.<br/>
<sub>Swift · SwiftUI</sub>

</td>
</tr>
<tr>
<td colspan="2" valign="top">

#### 🌐 [`gateway`](https://github.com/mtaibo/tpcloud/tree/main/gateway)
Caddy reverse proxy that routes each subdomain to its service on a shared Docker network, exposed only through Cloudflare Tunnel.<br/>
<sub>Caddy · Docker Compose · Cloudflare</sub>

</td>
</tr>
</table>

## 🏠 TPHome: home automation end to end system

[**tphome**](https://github.com/mtaibo/tphome) started because I was tired of needing a different app for every device in my house. So I replaced the factory firmware on commercial blind controllers and light switches with my own, and built the whole stack on top. It runs entirely on my local network.

| Layer | What it does | Stack |
|---|---|---|
| [`firmware`](https://github.com/mtaibo/tphome/tree/main/firmware) | Runs on the ESP8266 chips inside the switches: relays, motors, WiFi, binary MQTT protocol, OTA updates | C++ · Arduino |
| [`api`](https://github.com/mtaibo/tphome/tree/main/api) | Device management, state persistence, MQTT orchestration, real-time WebSocket events, OTA firmware serving | Python · FastAPI · Mosquitto · SQLite |
| [`frontend`](https://github.com/mtaibo/tphome/tree/main/frontend) | Interactive SVG floor plan to see and control every light and blind in real time | Vue 3 · Tailwind |

## 🏆 HackUDC 2026: Inditex challenge

[**hackUDC26_reto_inditex**](https://github.com/mtaibo/hackUDC26_reto_inditex) · Visual fashion search built with my team in one weekend. Upload a photo of a garment and get the most similar products in the catalogue, using a fine-tuned CLIP model for image embeddings and FAISS for nearest-neighbour search. Served by a FastAPI backend with a vanilla web frontend, all in Docker.

<sub>Python · PyTorch · OpenCLIP · FAISS · FastAPI · Docker</sub>

---

<div align="center">
<sub>Also see: <a href="https://github.com/mtaibo/dotfiles">dotfiles</a> (Nix flakes for my devices) · <a href="https://github.com/mtaibo/udc">udc</a> (university coursework) · <a href="https://github.com/mtaibo/portfolio">portfolio</a> (migueltaibo.com)</sub>
</div>
