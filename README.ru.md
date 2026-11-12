# Hauflo Cards

[English](README.md) · **Русский**

Карточки панелей Home Assistant в стиле Hauflo «Ателье»: комнаты, свет, шторы, климат, охрана, медиа и датчики, светлая и тёмная тема, телефон и настенный планшет. Один файл, ничего не грузится из интернета.

[![Marketplace / HACS custom](https://img.shields.io/badge/Marketplace%20%2F%20HACS-plugin-41BDF5)](#установка) [![Home Assistant 2026.9+](https://img.shields.io/badge/Home%20Assistant-2026.9%2B-18BCF2)](#установка) [![Release](https://img.shields.io/github/v/release/Hauflo/hauflo-cards)](https://github.com/Hauflo/hauflo-cards/releases)

<img src="https://raw.githubusercontent.com/Hauflo/hauflo-agent/main/docs/images/family.ru.webp" width="840" alt="Три экрана телефона в демо-доме: комната со светом, сценами и шторами; кондиционер; аварии — карточки Hauflo, светлая и тёмная тема.">

## Карточки

| | Группа | Карточки (`custom:…`) |
|---|---|---|
| `mdi:home-outline` | Дом, свет, шторы | `hauflo-hero` `hauflo-room` `hauflo-scenes` `hauflo-sliders` `hauflo-lights` `hauflo-covers` |
| `mdi:thermostat` | Климат и воздух | `hauflo-climate` `hauflo-air` `hauflo-acs` |
| `mdi:shield-home-outline` | Безопасность и видео | `hauflo-alert` `hauflo-security` `hauflo-camera` `hauflo-leaks` |
| `mdi:play-circle-outline` | Медиа и погода | `hauflo-media` `hauflo-weather` |
| `mdi:chart-line` | Датчики и автоматизации | `hauflo-graph` `hauflo-auto` `hauflo-status` `hauflo-entity` `hauflo-devices` `hauflo-area` `hauflo-title` |

Для совместимости (оставлены для панелей, собранных вручную; сам Hauflo ставит рекомендованные): `hauflo-entity` → берите `hauflo-lights` / `hauflo-devices`; `hauflo-auto` → берите `hauflo-automations`. Все остальные карточки — рекомендуемые.

Все карточки — в выборе карточек Home Assistant, с превью и визуальным редактором; тексты — на языке пользователя (русский, английский). Иконки: `mdi:*` и свой набор Hauflo `hauflo:*`.

## Установка

1. Настройки → **Marketplace** → ⋮ → **Add from link** → `https://github.com/Hauflo/hauflo-cards` (тип **Dashboard**). На Home Assistant до 2026.11 — HACS → ⋮ → **Custom repositories**.
2. Скачайте **Hauflo Cards** и обновите страницу браузера. Ресурс панелей Marketplace/HACS добавит сам.
3. Тема (по желанию): скопируйте `themes/hauflo-atelier.yaml` в `/config/themes` (при `frontend: themes: !include_dir_merge_named themes`), затем Инструменты разработчика → Действия → `frontend.reload_themes`.

## Вместе с агентом Hauflo

[Агент Hauflo](https://github.com/Hauflo/hauflo-agent) несёт те же карточки и добавляет то, что без него невозможно: колокольчики аварий на плитках, список защищённых устройств для «Точно?», порядок и названия комнат, которые переживают выкатку, семейные сцены и страницу автоматизаций. Если стоят оба, работает одна копия: этот плагин, когда он новее карточек агента, иначе — карточки агента, а Настройки → Ремонт подскажут, что обновить. Тему агент добавляет сам.

## Версии

Версия 1.0.9. В каждом выпуске указан минимальный агент (`agent_min`); настройка карточки, которая работала, работает и в следующих версиях.

Лицензия: [LICENSE](LICENSE). Шрифт: Onest, SIL Open Font License 1.1.
