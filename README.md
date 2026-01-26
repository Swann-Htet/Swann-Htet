# ⚡ sh.skillfusion.tech

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue?style=for-the-badge&logo=none)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge&logo=github-actions)
![License](https://img.shields.io/badge/license-MIT-orange?style=for-the-badge)
![Uptime](https://img.shields.io/badge/uptime-99.9%25-success?style=for-the-badge)

**The high-performance, internal URL shortening & redirection engine for the SkillFusion ecosystem.**

[**Visit Dashboard**](https://sh.skillfusion.tech) · [**Report Bug**](https://github.com/skillfusion/sh/issues) · [**Request Feature**](https://github.com/skillfusion/sh/issues)

</div>

---

## 🚀 About The Project

**SkillFusion SH** (`sh.skillfusion.tech`) is a robust microservice designed to handle link compression, click tracking, and dynamic redirection for SkillFusion's learning platform. It ensures that shared links are concise, branded, and trackable.

### Why we built this
* **Branding:** Replace generic short links (bit.ly) with our own trusted domain.
* **Analytics:** Gain granular insights into student engagement and course click-through rates.
* **Reliability:** A dedicated service decoupled from the main monolith for high availability.

---

## ✨ Key Features

* 🔗 **Instant Shortening:** Compresses long course URLs into `sh.skillfusion.tech/xyz`.
* 📊 **Real-time Analytics:** Tracks clicks, geographic location, and referrer data.
* 🛡️ **Link Expiry:** Set automatic expiration dates for temporary promotional links.
* 📱 **QR Code Generation:** Auto-generates QR codes for offline marketing.
* ⚡ **Redis Caching:** Sub-millisecond redirection latency.

---

## 🛠️ Tech Stack

This project is built using a modern, scalable architecture.

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Runtime** | ![NodeJS](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) | Core application logic |
| **Framework** | ![Express](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white) | REST API framework |
| **Database** | ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) | Persistent storage for link metadata |
| **Caching** | ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) | High-speed caching for redirects |
| **Container** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) | Containerization & Orchestration |

---

## 🔌 API Reference

The service exposes a RESTful API for programmatic access.

### Shorten a Link
```http
POST /api/v1/shorten
