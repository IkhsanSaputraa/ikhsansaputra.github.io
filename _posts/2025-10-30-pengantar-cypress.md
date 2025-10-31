---
title : Pengantar Cypress
description: Pelajari konsep dasar Cypress, instalasi, perintah utama, serta keunggulannya dibanding Selenium. Disertai contoh study case login pada situs saucedemo.com untuk memahami praktik pengujian otomatis berbasis UI.
author: Ikhsan Saputra
date: 2025-10-30
categories: [Software Testing & Quality assurance, Pengantar Cypress]
Tag: [Software, Testing, Quality Assurance]
image:
    path: /assets/img/pengantar-cypress.png
    lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
    alt:
---

# 🌿 Pengenalan Cypress: Framework Modern untuk End-to-End Testing Aplikasi Web

**Cypress** adalah framework modern untuk **end-to-end (E2E) testing** aplikasi web berbasis JavaScript seperti **React, Vue, dan Angular**.  
Dengan Cypress, kita bisa **mensimulasikan perilaku pengguna** secara langsung di browser dan memverifikasi hasilnya secara real-time.

📂 **Akses Slide Asli:**  
[Pengenalan Cypress – Kelompok 8](https://drive.google.com/file/d/1lBwmTvmXF0iDxCIX0SbTfTBOQ7-eOLOx/view?usp=drive_link)

---

## 🧠 Apa Itu Cypress?

Cypress adalah framework **end-to-end testing** yang berjalan langsung di dalam browser dan terintegrasi erat dengan aplikasi yang diuji.

🔹 **Posisi Cypress dalam Tahapan Testing:**
| Jenis Testing | Penjelasan | Peran Cypress |
|----------------|-------------|---------------|
| **Unit Testing** | Menguji fungsi terkecil dari kode | Dapat digunakan |
| **Integration Testing** | Menguji interaksi antar modul | Dapat digunakan |
| **End-to-End Testing** | Menguji seluruh alur aplikasi dari UI hingga server | 🔥 **Utama** |

> Cypress berfokus pada *pengujian alur pengguna secara penuh*, mulai dari membuka halaman, login, hingga validasi hasil tampilan.

---

## ⚙️ Instalasi dan Setup Cypress

Sebelum menggunakan Cypress, pastikan sistem sudah memiliki **Node.js**.  
Berikut langkah instalasi lengkap:

```bash
# 1️⃣ Inisialisasi project Node.js
npm init -y

# 2️⃣ Instal Cypress sebagai dependensi pengujian
npm install cypress --save-dev

 