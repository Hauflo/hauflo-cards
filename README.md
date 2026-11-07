# Hauflo Cards

**English** · [Русский](README.ru.md)

Dashboard cards for Home Assistant in the Hauflo «Atelier» style: rooms, lights, blinds, climate, security, media and sensors, light and dark, phone and wall tablet. One file, nothing loaded from the internet.

[![Marketplace / HACS custom](https://img.shields.io/badge/Marketplace%20%2F%20HACS-plugin-41BDF5)](#install) [![Home Assistant 2026.9+](https://img.shields.io/badge/Home%20Assistant-2026.9%2B-18BCF2)](#install) [![Release](https://img.shields.io/github/v/release/Hauflo/hauflo-cards)](https://github.com/Hauflo/hauflo-cards/releases)

<img src="https://raw.githubusercontent.com/Hauflo/hauflo-agent/main/docs/images/family.webp" width="840" alt="Three phone screens of the demo home: a room with lights, scenes and blinds; the air conditioner; alarms — Hauflo cards, light and dark.">

## Cards

| | Group | Cards (`custom:…`) |
|---|---|---|
| `mdi:home-outline` | Home, lights, blinds | `hauflo-hero` `hauflo-room` `hauflo-scenes` `hauflo-sliders` `hauflo-lights` `hauflo-covers` |
| `mdi:thermostat` | Climate and air | `hauflo-climate` `hauflo-air` `hauflo-acs` |
| `mdi:shield-home-outline` | Security and video | `hauflo-alert` `hauflo-security` `hauflo-camera` `hauflo-leaks` |
| `mdi:play-circle-outline` | Media and weather | `hauflo-media` `hauflo-weather` |
| `mdi:chart-line` | Sensors and automations | `hauflo-graph` `hauflo-auto` `hauflo-status` `hauflo-entity` `hauflo-devices` `hauflo-area` `hauflo-title` |

Every card is in Home Assistant's card picker with a preview and a visual editor; texts follow the user's language (English, Russian). Icons: `mdi:*` and Hauflo's own `hauflo:*` set.

## Install

1. Settings → **Marketplace** → ⋮ → **Add from link** → `https://github.com/Hauflo/hauflo-cards` (type **Dashboard**). On Home Assistant before 2026.11 — HACS → ⋮ → **Custom repositories**.
2. Download **Hauflo Cards**, reload the browser page. The resource is added by Marketplace/HACS.
3. Optional theme: copy `themes/hauflo-atelier.yaml` into `/config/themes` (with `frontend: themes: !include_dir_merge_named themes`), then Developer tools → Actions → `frontend.reload_themes`.

## With the Hauflo agent

The [Hauflo agent](https://github.com/Hauflo/hauflo-agent) ships the same cards and adds what needs it: alarm bells on tiles, the «Sure?» list of protected devices, the room order and titles kept over deploys, family scenes and the automations page. With both installed only one copy is used: this plugin when it is newer than the agent's cards, otherwise the agent's — and Settings → Repairs says what to update. The agent adds the theme itself.

## Versions

Version 1.0.0. Each release says which agent it needs at least (`agent_min`); a card configuration that worked keeps working in later versions.

Licence: see [LICENSE](LICENSE). Font: Onest, SIL Open Font License 1.1.
