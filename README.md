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

OPhishGuard is an offline analyzer for phishing emails. It parses raw .eml/RFC 5322 messages to reconstruct the Received chain, evaluate SPF/DKIM/DMARC authentication, inspect URLs and attachments, and detect lookalike sender domains. Attachments are never executed, opened or written.

---

## ✨ Features

- Raw .eml/RFC 5322 parsing with header decoding and attachment metadata (name, type, size, SHA-256)
- Received-chain reconstruction with per-hop timing and originating-IP analysis
- SPF/DKIM/DMARC and ARC verdicts with identifier-alignment checks
- Offline lookalike detection via homoglyph, edit-distance and punycode/IDN analysis
- URL analysis for anchor/href mismatch, shorteners and IP literals
- Directory scanning, multiple output formats and a CI fail-on gate

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPhishGuard --eml suspicious.eml --urls --attachments
./OPhishGuard --dir ./mailbox --format json -o report.json
./OPhishGuard --check-domain paypa1.com
./OPhishGuard --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
