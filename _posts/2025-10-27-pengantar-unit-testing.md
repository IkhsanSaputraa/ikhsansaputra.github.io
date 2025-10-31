---
title : Pengantar Unit Testing
description: Pelajari apa itu Unit Testing, mengapa penting dalam pengembangan perangkat lunak, pola dasar Arrange-Act-Assert (AAA), serta framework populer seperti JUnit, Pytest, dan Jest.
author: Kevin Ardhana
date: 2025-10-27
categories: [Software Testing & Quality assurance, Pengantar Unit Testing]
Tag: [Software, Testing, Quality Assurance]
image:
    path: /assets/img/pengantar-unit-testing.png
    lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
    alt:
---

# 🧩 Pengantar Unit Testing: Konsep, Manfaat, dan Framework Populer

Ingin **coding tanpa khawatir bug**?  
Jawabannya adalah **Unit Testing** — salah satu pilar utama dalam menjaga kualitas perangkat lunak.

📂 **Akses Slide Asli:**  
[Pengantar Unit Testing – Kelompok 5](https://drive.google.com/file/d/1qSDpXubcQlTiRXuM2tdDO30rPo-3GkCS/view?usp=drive_link)

---

## 🧠 Apa Itu Unit Testing?

**Unit Testing** adalah jenis pengujian perangkat lunak yang berfokus pada **unit terkecil dari kode program**, seperti:
- Fungsi (function)
- Metode (method)
- Kelas (class)

Tujuan utamanya adalah **memastikan setiap bagian kecil kode berfungsi dengan benar secara terpisah**, tanpa bergantung pada modul lain.

Biasanya, Unit Testing dilakukan **paling awal** oleh developer sebelum melakukan **Integration Test** atau **System Test**.

### 🔧 Sederhananya:
> Unit testing = Menguji bagian terkecil dari sistem untuk memastikan logikanya berjalan benar sebelum dirakit menjadi aplikasi utuh.

---

## 🚗 Analogi Unit Testing

Bayangkan kamu sedang merakit mobil.  
Sebelum mobil dirakit menjadi satu kesatuan, **setiap komponen (ban, mesin, rem)** diuji satu per satu terlebih dahulu.

Jika setiap bagian lolos pengujian, maka mobil utuh akan lebih mudah dirakit dan lebih andal.  
Jika ditemukan masalah, kamu tahu letaknya — **langsung di komponen yang diuji**.

> 🔍 Unit Testing = Menguji setiap “komponen mobil” sebelum dipasang menjadi satu kendaraan utuh.

---

## 🎯 Mengapa Unit Testing Itu Penting?

Unit Testing bukan sekadar formalitas — ia memberikan banyak manfaat nyata bagi pengembang maupun tim QA:

| Manfaat | Penjelasan |
|----------|-------------|
| 🐛 **Mendeteksi Bug Lebih Awal** | Bug dapat ditemukan sebelum kode digabungkan ke sistem utama. |
| 🧠 **Meningkatkan Kepercayaan Diri Developer** | Developer lebih yakin bahwa perubahan kode tidak akan merusak bagian lain. |
| 💰 **Menghemat Waktu dan Biaya** | Memperbaiki bug di tahap awal jauh lebih murah dibanding setelah deployment. |
| ⚙️ **Mempermudah Refactoring** | Kode bisa diubah tanpa takut merusak fungsionalitas lama. |
| 📘 **Memberikan Dokumentasi Hidup** | Test unit berfungsi sebagai dokumentasi aktif yang menjelaskan bagaimana kode seharusnya bekerja. |

---

## 🧩 Pola Dasar: Arrange – Act – Assert (AAA)

Pola ini adalah **struktur paling umum** dalam penulisan Unit Test yang sederhana dan efektif.

| Tahap | Penjelasan |
|--------|-------------|
| **ARRANGE** | Menyiapkan kondisi awal tes (input, variabel, atau objek yang diperlukan). |
| **ACT** | Menjalankan fungsi atau metode yang ingin diuji. |
| **ASSERT** | Memverifikasi hasil output agar sesuai dengan ekspektasi. |

### 📘 Contoh Sederhana (Python)
```python
def add(a, b):
    return a + b

def test_addition():
    # Arrange
    a = 2
    b = 3

    # Act
    result = add(a, b)

    # Assert
    assert result == 5

## Kontak

**Developer:** Kevin Ardhana  
**GitHub:** [@kevinardhana096](https://github.com/kevinardhana096)   
**Email:** kevinardhana096@gmail.com  