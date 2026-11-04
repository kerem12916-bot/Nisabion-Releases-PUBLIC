# Paqnora Nisabion

Professional PDF and document editing studio for Windows — local, offline-first, privacy-respecting.

Nisabion is a native Windows x64 application for viewing, editing, and managing PDF documents and `.bion` project files. All document processing happens locally on your machine; no account, cloud service, or telemetry is required.

## Download

Get the latest build from the [Releases page](https://github.com/kerem12916-bot/Nisabion-Releases-PUBLIC/releases).

- **Nisabion-Setup-x64.exe** — per-user installer (no administrator rights required)
- **Nisabion-Portable-x64.zip** — portable package, runs without installation

Current release: `v0.9.0-beta.3` (beta — not a stable release)

## Features

- **PDF viewing and editing** — open, view, and edit existing PDF content, including in-place editing of existing text objects
- **Interactive AcroForm support** — fill text fields, checkboxes, radio groups, combo boxes, and list boxes directly in the document, with undo/redo and persistence
- **BION project format** — a container format (ZIP + protobuf) that preserves your editing session as a project; PDF source files are never modified in place
- **PDF utilities** — image-to-PDF, page organization, printing, and document export
- **Secure updates** — updates are delivered through a dedicated updater process and are authenticated with Ed25519 signatures; unsigned or tampered updates are refused

## Privacy and security

- Offline-first: the application and the PDF engine do not access the network
- Network access is restricted to the updater component only
- No telemetry, analytics, or online registration; documents and personal data never leave your device
- PDF parsing runs in an isolated worker process, separate from the main application

## System requirements

- Windows 10 version 1809 or later, or Windows 11 (64-bit)
- Approximately 4 GB RAM

## Beta status and known limitations

- This is a beta release — expect rough edges and please report issues.
- **No Windows Authenticode signature yet.** The installer and executables are unsigned; Windows SmartScreen may show an "unknown publisher" warning. This is expected and does not affect update authenticity (updates are verified separately with Ed25519). Code signing is planned for a future release.
- Form filling is locked on PDFs that carry digital signature fields or XFA content (fail-closed by design).
- Clean-OS installation testing was not performed for this beta; installation was validated on a real Windows 11 machine.

## Links

- [Releases and downloads](https://github.com/kerem12916-bot/Nisabion-Releases-PUBLIC/releases)
- [Project website](https://kerem12916-bot.github.io/Nisabion-Releases-PUBLIC/)

---

*Paqnora Nisabion is closed-source software distributed via this releases repository; the source code is not publicly available.*
