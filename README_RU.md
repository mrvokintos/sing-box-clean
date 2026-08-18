# Sing-Box и Sing-Box-Extended для OpenWrt (ARM64 Cortex-A53)

[English](README.md) | [Русский](README_RU.md)

[![Sync Upstream](https://github.com/mrvokintos/sing-box-clean/actions/workflows/sync-upstream.yml/badge.svg)](https://github.com/mrvokintos/sing-box-clean/actions/workflows/sync-upstream.yml)
[![OpenWrt A53 Build](https://github.com/mrvokintos/sing-box-clean/actions/workflows/openwrt-a53.yml/badge.svg)](https://github.com/mrvokintos/sing-box-clean/actions/workflows/openwrt-a53.yml)
[![Latest Release](https://img.shields.io/github/v/release/mrvokintos/sing-box-clean?label=release)](https://github.com/mrvokintos/sing-box-clean/releases/latest)

Автоматическая сборка ядер **sing-box** (Official) и **sing-box-extended** под архитектуру **OpenWrt ARM64 Cortex-A53** (`aarch64_cortex-a53`) с ежедневной синхронизацией с апстримами.

---

## Прямые ссылки на скачивание (Latest)

| Ядро | Пакет IPK | Пакет APK |
| :--- | :--- | :--- |
| **Official sing-box** | [sing-box.ipk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box.ipk) | [sing-box.apk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box.apk) |
| **sing-box-extended** | [sing-box-extended.ipk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box-extended.ipk) | [sing-box-extended.apk](https://github.com/mrvokintos/sing-box-clean/releases/download/latest/sing-box-extended.apk) |

---

## Состав протоколов и тегов сборки

### 1. Official sing-box (ветка `testing`)
* **Апстрим:** [sagernet/sing-box](https://github.com/sagernet/sing-box)
* **Теги сборки:** `with_quic,with_naive_outbound,badlinkname,tfogo_checklinkname0,with_musl`
* **Протоколы:** NaiveProxy, Hysteria 2 / QUIC, VLESS, ShadowTLS, WireGuard и др.

### 2. sing-box-extended (ветка `extended`)
* **Апстрим:** [Shtorm-7/sing-box-extended](https://github.com/Shtorm-7/sing-box-extended)
* **Теги сборки:** `with_quic,with_utls,with_naive_outbound,badlinkname,tfogo_checklinkname0,with_musl`
* **Протоколы и возможности:**
  - NaiveProxy (`with_naive_outbound`)
  - Hysteria 2 / QUIC (`with_quic`)
  - Полноценный VLESS с поддержкой **REALITY** и **uTLS** (`with_utls`)
  - **XHTTP** (SplitHTTP — нативно включен в кодовую базу)

---

## Структура репозитория

* `clean` (**Основная ветка**) — управляющая ветка со скриптами сборки и автоматической синхронизации.
* `testing` — 100% чистый зеркальный трек официального репозитория `sagernet/sing-box:testing`.
* `extended` — 100% чистый зеркальный трек `Shtorm-7/sing-box-extended:extended`.
