# Sing-Box & Sing-Box-Extended for OpenWrt (ARM64 Cortex-A53)

[English](README.md) | [Русский](README_RU.md)

[![Sync Upstream](https://github.com/mrvokintos/sing-box-clean/actions/workflows/sync-upstream.yml/badge.svg)](https://github.com/mrvokintos/sing-box-clean/actions/workflows/sync-upstream.yml)
[![OpenWrt A53 Build](https://github.com/mrvokintos/sing-box-clean/actions/workflows/openwrt-a53.yml/badge.svg)](https://github.com/mrvokintos/sing-box-clean/actions/workflows/openwrt-a53.yml)
[![Latest Release](https://img.shields.io/github/v/release/mrvokintos/sing-box-clean?label=release)](https://github.com/mrvokintos/sing-box-clean/releases/latest)

Automated builds of **sing-box** (Official) and **sing-box-extended** for **OpenWrt ARM64 Cortex-A53** (`aarch64_cortex-a53`) with daily upstream synchronization.

---

## Direct Download Links (Latest)

| Core | IPK Package | APK Package |
| :--- | :--- | :--- |
| **Official sing-box** | [sing-box.ipk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box.ipk) | [sing-box.apk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box.apk) |
| **sing-box-extended** | [sing-box-extended.ipk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box-extended.ipk) | [sing-box-extended.apk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box-extended.apk) |

---

## Build Features and Protocols

### 1. Official sing-box (`testing` branch)
* **Upstream:** [sagernet/sing-box](https://github.com/sagernet/sing-box)
* **Build Tags:** `with_quic,with_naive_outbound,badlinkname,tfogo_checklinkname0,with_musl`
* **Protocols:** NaiveProxy, Hysteria 2 / QUIC, VLESS, ShadowTLS, WireGuard, etc.

### 2. sing-box-extended (`extended` branch)
* **Upstream:** [Shtorm-7/sing-box-extended](https://github.com/Shtorm-7/sing-box-extended)
* **Build Tags:** `with_quic,with_utls,with_naive_outbound,badlinkname,tfogo_checklinkname0,with_musl`
* **Protocols & Features:**
  - NaiveProxy (`with_naive_outbound`)
  - Hysteria 2 / QUIC (`with_quic`)
  - Full VLESS with **REALITY** and **uTLS** support (`with_utls`)
  - **XHTTP** (SplitHTTP — natively supported)

---

## Repository Structure

* `clean` (**Default branch**) — orchestrator branch containing build scripts, synchronization workflows, and documentation.
* `testing` — 1:1 pure mirror of upstream `sagernet/sing-box:testing`.
* `extended` — 1:1 pure mirror of upstream `Shtorm-7/sing-box-extended:extended`.
