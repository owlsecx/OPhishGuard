# 🦉 OPhishGuard

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPhishGuard** — Phishing Email Analyzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Defensive phishing email analyzer & header forensics

---

## ✨ Features

- Raw .eml / RFC 5322 parser (stdlib `email`) with header decoding, text/html body extraction and attachment metadata (name, type, size, SHA-256). Attachments are NEVER executed, opened or written.
- Header forensics — Received chain reconstruction, per-hop timing, originating IP, private/bogon hops, Return-Path / Reply-To / Sender mismatch, Message-ID sanity, Date anomalies (future, stale, bad TZ)
- Authentication — Authentication-Results, Received-SPF, DKIM-Signature, ARC-* parsing; SPF/DKIM/DMARC verdicts and identifier alignment (relaxed) checks
- Offline sender reputation — homoglyph skeletons, edit-distance brand lookalikes, punycode / IDN and mixed-script detection, display-name brand spoofing
- URL analysis — anchor-text vs href mismatch, shorteners, IP literals, userinfo '@', punycode, deep subdomains, suspicious TLDs, data:/javascript: URIs, odd ports. No network access, ever, unless you explicitly ask.
- Content heuristics — urgency & credential-harvest language, hidden text, mixed charsets, base64 blobs, external form posts, risky / double-extension files
- Weighted 0–100 phishing score + verdict with per-signal explanation
- Export TXT / MD / JSON / CSV, save chooser, clipboard
- Batch directory scan + full CLI (--eml, --dir, --fail-on)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPhishGuard
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
