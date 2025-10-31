---
title : Testing Plan
description: Pelajari apa itu Testing Plan, tujuan penyusunannya, serta contoh penerapan nyata pada proyek pengujian aplikasi BMI. Artikel ini menjelaskan komponen-komponen penting dalam rencana pengujian berdasarkan standar IEEE 829.
author: Ikhsan Saputra
date: 2025-10-25
categories: [Software Testing & Quality assurance, Testing Plan]
Tag: [Software, Testing, Quality Assurance]
image:
    path: /assets/img/testing-plan.png
    lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
    alt:
---

# 🧪 Testing Plan dalam Pengujian Perangkat Lunak

Dalam proses **Software Testing**, dibutuhkan panduan resmi agar pengujian berjalan **terarah, konsisten, dan terdokumentasi dengan baik**. Panduan ini disebut **Testing Plan (Rencana Pengujian)** — dokumen utama yang menentukan bagaimana, kapan, dan apa yang akan diuji.

📂 **Akses Slide Asli:**  
[Testing Plan – Google Drive](https://drive.google.com/file/d/1Pjx6n08veg7o6P-4LjazQCGOx29xH-YS/view?usp=drive_link)

📄 **Contoh Implementasi:**  
[Demo Test Plan – Aplikasi BMI (Kelompok 3)](https://drive.google.com/file/d/1YiN3oNnXvhQmShckutGpIXPgNi7Ci-vi/view?usp=drive_link)

---

## 🔍 Apa Itu Testing Plan?

**Testing Plan** atau **Rencana Pengujian** adalah dokumen panduan yang menjelaskan **bagaimana proses pengujian perangkat lunak akan dilakukan**.  
Di dalamnya terdapat informasi seperti:
- Ruang lingkup pengujian,  
- Strategi atau metodologi pengujian,  
- Sumber daya yang digunakan (tim, alat, dan data uji),  
- Jadwal pelaksanaan, serta  
- Kriteria keberhasilan dan kegagalan pengujian.  

Fungsi utama dari Testing Plan adalah menjadi **acuan resmi** bagi tim penguji agar semua kegiatan pengujian dapat dilakukan secara **terarah dan terukur**.

---

## 🎯 Tujuan Testing Plan

Testing Plan memiliki beberapa tujuan penting, yaitu:

1. **Memberikan gambaran yang jelas** tentang apa yang akan diuji dan bagaimana pengujian dilakukan.  
2. **Menjamin kualitas perangkat lunak** agar mencapai standar yang dapat diterima pengguna.  
3. **Mengoptimalkan waktu, biaya, dan tenaga** dalam proses pengujian.  
4. **Menyediakan dokumentasi resmi** yang dapat dijadikan referensi atau bahan evaluasi di proyek berikutnya.  
5. **Menjadi alat komunikasi** antara tim developer, tester, dan manajer proyek agar seluruh pihak memiliki pemahaman yang sama terhadap ruang lingkup pengujian.

---

## 🧩 Komponen-Komponen dalam Testing Plan (IEEE 829 Standard)

Standar **IEEE 829-1988** mendefinisikan berbagai bagian yang harus ada dalam sebuah test plan. Berikut penjelasan dan fungsinya:

| Komponen | Penjelasan Singkat |
|-----------|--------------------|
| **Plan Identifier** | Penanda unik untuk setiap test plan (misalnya: *TP_1.0*) agar mudah dibedakan antar versi atau proyek. |
| **References** | Daftar dokumen pendukung seperti spesifikasi kebutuhan, standar kualitas, atau panduan teknis. |
| **Introduction** | Bagian pembuka yang menjelaskan tujuan dan ruang lingkup pengujian. |
| **Test Items** | Fitur, modul, atau komponen yang akan diuji. |
| **Software Risk Issues** | Daftar risiko yang berpotensi muncul selama pengujian. |
| **Features to be Tested** | Daftar fitur atau fungsi yang termasuk dalam pengujian. |
| **Features not to be Tested** | Fitur yang dikecualikan dari pengujian dan alasan pengecualiannya. |
| **Approach** | Strategi umum yang digunakan, misalnya metode manual, otomatis, black-box, atau white-box. |
| **Pass/Fail Criteria** | Standar objektif untuk menentukan apakah pengujian berhasil atau gagal. |
| **Suspension Criteria & Resumption Requirements** | Kondisi kapan pengujian dihentikan dan bagaimana melanjutkannya. |
| **Test Deliverables** | Hasil nyata dari pengujian seperti laporan bug, test case, dan ringkasan hasil uji. |
| **Remaining Test Tasks** | Daftar pekerjaan pengujian yang belum selesai. |
| **Environmental Needs** | Spesifikasi lingkungan pengujian seperti hardware, software, data uji, dan jaringan. |
| **Responsibilities** | Pembagian peran dan tanggung jawab tiap anggota tim. |
| **Staffing and Training Needs** | Kebutuhan personel dan pelatihan sebelum pengujian dimulai. |
| **Schedule** | Jadwal keseluruhan pengujian hingga rilis. |
| **Glossary** | Daftar istilah teknis yang digunakan dalam dokumen. |
| **Approvals** | Persetujuan resmi dari pihak manajemen atau stakeholder proyek. |

---

## 🧠 Contoh: Demo Test Plan – Aplikasi BMI

Sebagai contoh, berikut cuplikan nyata dari **Test Plan Aplikasi BMI** yang disusun oleh *Kelompok 3*:

| Komponen | Cuplikan dari Demo Test Plan |
|-----------|------------------------------|
| **Identifier** | BMI Calculator Testing `TP_1.0` |
| **References** | Dokumen kebutuhan aplikasi BMI, Standar WHO, IEEE 829 |
| **Test Items** | Validasi berat dan tinggi badan, perhitungan BMI, tampilan hasil, klasifikasi kesehatan |
| **Features to be Tested** | Input valid/invalid, perhitungan akurat, tampilan hasil, histori data |
| **Features not to be Tested** | Login, print/export, multi-bahasa |
| **Approach** | Manual testing dengan pembagian skenario antar penguji |
| **Pass Criteria** | Hasil perhitungan akurat 100%, error validasi bekerja, >95% test case lulus |
| **Fail Criteria** | Perhitungan salah, aplikasi crash, atau fungsi utama gagal |
| **Deliverables** | Laporan hasil test, bug report, dan rekomendasi perbaikan |
| **Schedule** | Minggu 1: Eksekusi test – Minggu 2: Retest & approval |
| **Approvals** | Disetujui oleh Test Manager dan Project Manager sebelum rilis |

Dari contoh ini, dapat dilihat bahwa test plan membantu tim memastikan **akurasi hasil**, **konsistensi fungsi**, dan **stabilitas sistem sebelum peluncuran aplikasi**.

---

## ✅ Kesimpulan

**Testing Plan** adalah fondasi penting dalam manajemen pengujian perangkat lunak.  
Dengan rencana yang matang, tim dapat:
- Menghindari pengujian yang tumpang tindih,  
- Mendeteksi risiko sejak dini,  
- Mendokumentasikan seluruh proses secara profesional.

> “A good test plan turns testing from guesswork into a repeatable process.”  
> — *Software Quality Assurance Principle*

---

📎 **Referensi:**
- [Kelompok 3 – Testing Plan PDF](https://drive.google.com/file/d/1Pjx6n08veg7o6P-4LjazQCGOx29xH-YS/view?usp=drive_link)  
- [Demo Test Plan – Aplikasi BMI (Kelompok 3)](https://drive.google.com/file/d/1YiN3oNnXvhQmShckutGpIXPgNi7Ci-vi/view?usp=drive_link)
