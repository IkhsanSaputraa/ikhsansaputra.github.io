---
title : Pengantar Selenium WebDriver
description: Pelajari dasar Selenium WebDriver untuk automasi pengujian aplikasi web. Artikel ini menjelaskan konsep, alasan penggunaan, instalasi, serta contoh test scenario dan test case menggunakan Python dan Selenium.
author: Kevin Ardhana
date: 2025-10-29
categories: [Software Testing & Quality assurance, Pengantar Selenium]
Tag: [Software, Testing, Quality Assurance]
image:
    path: /assets/img/pengantar-selenium.png
    lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
    alt:
---

# 🧩 Pengantar Selenium WebDriver: Automasi Pengujian Aplikasi Web

Di era pengembangan web modern, **automation testing** menjadi kebutuhan penting agar proses pengujian lebih cepat dan efisien.  
Salah satu alat yang paling populer untuk melakukan automasi pengujian pada browser adalah **Selenium**.

📂 **Akses Slide Asli:**  
[Pengantar Selenium WebDriver – Kelompok 7](https://drive.google.com/file/d/1G8XP7xVKPqGMZah4RyEfYVi3NrzOKuCo/view?usp=drive_link)

---

## 🔍 Apa Itu Selenium?

**Selenium** adalah framework *open-source* yang digunakan untuk **mengotomatisasi pengujian aplikasi web**.  
Dengan Selenium, kita dapat:
- Membuka browser secara otomatis,  
- Mengklik tombol, mengisi form, dan berpindah halaman,  
- Melakukan validasi terhadap hasil yang tampil di layar.

### 🌐 Dukungan Selenium:
- **Bahasa Pemrograman:** Python, Java, JavaScript, C#, Ruby  
- **Browser:** Chrome, Firefox, Edge, Safari  
- **Platform:** Windows, macOS, Linux  

> Selenium memungkinkan kita “menirukan tindakan pengguna manusia di browser”, tetapi secara otomatis dan terprogram.

---

## ⚙️ Apa Itu Selenium WebDriver?

**WebDriver** adalah **komponen inti** dari Selenium yang berfungsi sebagai penghubung antara kode program dengan browser.

Dengan WebDriver, kita bisa:
- Mengontrol browser (klik, isi teks, navigasi)  
- Melakukan validasi hasil (assertion)  
- Menjalankan pengujian di berbagai browser tanpa perubahan kode besar  

### 🔧 Fungsi Utama WebDriver:
| Fungsi | Deskripsi |
|--------|------------|
| **get(url)** | Membuka halaman web |
| **find_element()** | Mencari elemen HTML berdasarkan ID, Name, XPath, dsb |
| **click()** | Menekan tombol atau tautan |
| **send_keys()** | Mengisi teks pada input field |
| **quit()** | Menutup browser setelah pengujian selesai |

---

## 💡 Kenapa Harus Selenium?

| Keunggulan | Penjelasan |
|-------------|-------------|
| 💸 **Open Source dan Gratis** | Bisa digunakan bebas tanpa biaya lisensi. |
| 🧩 **Mendukung Banyak Bahasa** | Python, Java, C#, JavaScript, Ruby, dan lainnya. |
| 🌍 **Multi-Platform** | Bisa dijalankan di Windows, macOS, maupun Linux. |
| 🧠 **Integrasi Framework Testing** | Dapat digunakan bersama Pytest, JUnit, TestNG, dll. |
| 🧑‍🤝‍🧑 **Komunitas Besar** | Dokumentasi lengkap dan dukungan komunitas global. |

---

## 🧰 Instalasi Selenium (Python)

Langkah-langkah instalasi sederhana di Python:

```bash
# 1. Instal library Selenium
pip install selenium

# 2. Download WebDriver (contoh: ChromeDriver)
# Pastikan versi sesuai dengan browser Chrome kamu

## Kontak

**Developer:** Kevin Ardhana  
**GitHub:** [@kevinardhana096](https://github.com/kevinardhana096)   
**Email:** kevinardhana096@gmail.com  