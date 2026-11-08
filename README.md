<div align="center">

# Discord Game Time Badge Spoofer — Docs

**Inoffizielle, zweisprachige Dokumentation · Unofficial bilingual documentation**

[![Deutsch](https://img.shields.io/badge/Anleitung-Deutsch-000000?style=for-the-badge&labelColor=DD0000)](README_DE.md)
[![English](https://img.shields.io/badge/Guide-English-012169?style=for-the-badge&labelColor=C8102E)](README_EN.md)
[![Original Gist](https://img.shields.io/badge/Original-nvckai%20Gist-24292f?style=for-the-badge&logo=github)](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5)

![Docs only](https://img.shields.io/badge/contains-docs%20only%2C%20no%20code-informational)
![Platform](https://img.shields.io/badge/Discord-desktop%20(PTB%2FCanary)-5865F2?logo=discord&logoColor=white)
[![License: CC BY 4.0](https://img.shields.io/badge/docs%20license-CC%20BY%204.0-lightgrey.svg)](LICENSE)

<img src="assets/images/banner.jpg" alt="MacBook mit einem illustrativen Discord-Bildschirm / MacBook showing an illustrative Discord screen" width="820">

<sub>KI-generiertes Konzeptbild, kein echter Screenshot · AI-generated concept image, not a real screenshot</sub>

</div>

---

> [!WARNING]
> **🇩🇪** Das dokumentierte Skript erzeugt künstliche Spielaktivitäts-Ereignisse und kann gegen die [Discord-Nutzungsbedingungen](https://discord.com/terms) verstoßen – dein Konto kann gefährdet sein. Führe niemals Konsolencode aus, den du nicht selbst geprüft hast.
>
> **🇬🇧** The documented script fabricates game-activity events and may violate [Discord's Terms of Service](https://discord.com/terms) – your account may be at risk. Never run console code you have not reviewed yourself.

## 🇩🇪 Worum geht es?

Dieses Repository erklärt Schritt für Schritt, was das [Konsolen-Snippet von **nvckai**](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5) für die Discord-Abzeichen **Game Time** und **Game Variety** tut, welche Einstellungen es hat und wie man es zunächst **nur im Testmodus (`dryRun: true`)** nachvollzieht.

**➡️ [Zur vollständigen deutschen Anleitung](README_DE.md)**

## 🇬🇧 What is this?

This repository explains, step by step, what the [console snippet by **nvckai**](https://gist.github.com/nvckai/b258c253fa00e4300888f5cb13a905b5) does for Discord's **Game Time** and **Game Variety** badges, what its settings mean, and how to inspect it in **dry-run mode (`dryRun: true`)** first.

**➡️ [Read the full English guide](README_EN.md)**

## Inhalt / Contents

| | 🇩🇪 Deutsch | 🇬🇧 English |
|---|---|---|
| Überblick / Overview | [Was ist das?](README_DE.md#was-ist-das) | [What is this?](README_EN.md#what-is-this) |
| Voraussetzungen / Requirements | [Voraussetzungen](README_DE.md#voraussetzungen) | [Requirements](README_EN.md#requirements) |
| Anleitung / Guide | [Schritt-für-Schritt](README_DE.md#schritt-für-schritt-anleitung) | [Step-by-step](README_EN.md#step-by-step-guide) |
| Einstellungen / Settings | [Einstellungen erklärt](README_DE.md#einstellungen-erklärt) | [Configuration reference](README_EN.md#configuration-reference) |
| Stoppen / Stopping | [Konsolenausgabe & Stoppen](README_DE.md#konsolenausgabe-stoppen-und-kontrolle) | [Console output & stopping](README_EN.md#console-output-stopping-and-checking) |
| FAQ | [Häufige Fragen & Fehler](README_DE.md#häufige-fragen--fehler) | [FAQ & troubleshooting](README_EN.md#faq-and-troubleshooting) |
| Quellen / Sources | [Quellen & Lizenz](README_DE.md#quellen-sicherheit-und-lizenz) | [Sources & licensing](README_EN.md#sources-safety-and-licensing) |

## Auf einen Blick / At a glance

| | |
|---|---|
| **Enthalten / Included** | Anleitung DE + EN, schematische Abbildungen, [`config.example.json`](config.example.json) (nur Referenz / reference only) |
| **Nicht enthalten / Not included** | Der Originalcode – siehe [`SOURCE.md`](SOURCE.md) · The original code – see [`SOURCE.md`](SOURCE.md) |
| **Plattform / Platform** | Discord-Desktop-App (Konsole laut Discord in PTB/Canary) · Discord desktop app (console per Discord in PTB/Canary) |
| **Nicht unterstützt / Not supported** | Browser, Mobile, Streaming-Abzeichen, Quests |
| **Stand / Reviewed** | 2026-11-08 – der Gist kann sich seitdem geändert haben · the Gist may have changed since |

## Repository-Struktur / Repository layout

```text
.
├── README.md              # Diese Startseite / this landing page
├── README_DE.md           # Vollständige Anleitung (Deutsch)
├── README_EN.md           # Full guide (English)
├── config.example.json    # Beispielwerte, wird vom Skript NICHT gelesen / sample values, NOT read by the script
├── SOURCE.md              # Herkunft & Prüfdatum / provenance & review date
├── LICENSE                # CC BY 4.0 für Text & Bilder / for text & images
├── LICENSE-NOTICE.md      # Hinweise zu Drittcode & Marken / third-party code & trademarks
├── CONTRIBUTING.md        # Mitwirken / contributing
├── SECURITY.md            # Sicherheit & Tokens / security & tokens
└── assets/images/         # Illustrationen / illustrations
```

## Mitwirken / Contributing

Korrekturen, Übersetzungsverbesserungen und Hinweise auf veraltete Schritte sind willkommen – siehe [`CONTRIBUTING.md`](CONTRIBUTING.md).
Fixes, translation improvements and reports of outdated steps are welcome – see [`CONTRIBUTING.md`](CONTRIBUTING.md).

> [!CAUTION]
> **Niemals Tokens, Passwörter oder Konsolen-Logs mit persönlichen Daten in Issues posten.** · **Never post tokens, passwords or console logs containing personal data in issues.** – [`SECURITY.md`](SECURITY.md)

## Rechtliches / Legal

Die Dokumentation (Text und eigene Abbildungen) steht unter [CC BY 4.0](LICENSE). Der Originalcode von nvckai ist **nicht** enthalten und fällt nicht unter diese Lizenz – siehe [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md).
The documentation (text and original illustrations) is licensed under [CC BY 4.0](LICENSE). nvckai's original code is **not** included and is not covered by this license – see [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md).

Dieses Projekt steht in keiner Verbindung zu Discord Inc. oder dem Originalautor. · This project is not affiliated with Discord Inc. or the original author.
