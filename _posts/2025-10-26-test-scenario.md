---
title : Test Scenario, Test Case, dan Bug Report dalam Pengujian Aplikasi BMI
description: Pelajari pengertian, perbedaan, serta contoh nyata Test Scenario, Test Case, dan Bug Report berdasarkan pengujian aplikasi BMI. Termasuk template dan tips menghindari bug dalam pengembangan perangkat lunak.
author: Kevin Ardhana
date: 2025-10-26
categories: [Software Testing & Quality assurance, Tes Scenario]
Tag: [Software, Testing, Quality Assurance]
image:
    path: /assets/img/test-scenario.png
    lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
    alt:
---

# 🧩 Test Scenario, Test Case, dan Bug Report dalam Pengujian Aplikasi BMI

Dalam proses **Software Testing**, terdapat tiga elemen penting yang saling melengkapi, yaitu:  
1. **Test Scenario**  
2. **Test Case**  
3. **Bug Report**

Ketiganya berperan penting untuk memastikan bahwa aplikasi berfungsi sesuai kebutuhan, bebas dari kesalahan, dan memberikan pengalaman pengguna yang baik.

📂 **Akses Slide Asli:**  
[Test Scenario, Test Case, dan Bug Report – Kelompok 4](https://drive.google.com/file/d/1er2wwoA69y6OFqgGZCR4S9YeQEx0rM6z/view?usp=drive_link)

---

## 🧠 Pengertian Singkat

| Konsep | Penjelasan |
|--------|-------------|
| **Test Scenario** | Gambaran umum tentang *apa yang diuji* untuk memastikan fungsi aplikasi bekerja sesuai kebutuhan. |
| **Test Case** | Langkah-langkah detail untuk melaksanakan pengujian, termasuk input, proses, dan hasil yang diharapkan. |
| **Bug Report** | Laporan resmi yang mendokumentasikan kesalahan pada sistem, cara mereproduksi bug, dan hasil aktual saat diuji. |

Ketiganya membentuk satu siklus:  
> **Test Scenario → Test Case → Bug Report**

---

## 🧩 Template Sederhana

### 🧱 Template Test Scenario
| Field | Keterangan |
|--------|-------------|
| **ID Scenario** | Nomor unik skenario |
| **Deskripsi** | Ringkasan skenario pengujian |
| **Modul/Fitur** | Modul atau fitur yang diuji |

### 🧪 Template Test Case
| Field | Keterangan |
|--------|-------------|
| **ID Test Case** | Nomor unik test case |
| **Deskripsi** | Ringkasan singkat tentang pengujian |
| **Precondition** | Kondisi awal sebelum pengujian |
| **Test Steps** | Langkah-langkah detail pengujian |
| **Test Data** | Data yang digunakan |
| **Expected Result** | Hasil yang diharapkan |
| **Actual Result** | Hasil aktual |
| **Status** | Pass / Fail |

---

## ⚙️ Test Scenario dan Test Case pada Aplikasi BMI

Berdasarkan presentasi *Kelompok 3*, berikut contoh skenario dan test case yang digunakan untuk menguji **aplikasi kalkulator BMI**.

### 🧩 **Daftar Test Scenario**

| ID Scenario | Deskripsi | Modul/Fitur yang diuji |
|--------------|------------|------------------------|
| TS001 | Periksa fungsi slider input berat dan tinggi badan | Slider input |
| TS002 | Periksa hasil perhitungan dan klasifikasi BMI | Perhitungan BMI |
| TS003 | Periksa fungsi penyimpanan history BMI | History BMI |

---

### 🧠 **Rincian Test Case**

#### 🔹 Scenario TS001 – Slider Input Berat dan Tinggi
| ID Test Case | Deskripsi | Precondition | Test Steps | Test Data | Expected Result |
|---------------|------------|----------------|-------------|-------------|----------------|
| TC001 | Verifikasi slider input berat | Aplikasi terbuka | 1. Geser slider berat ke nilai tertentu.<br>2. Periksa nilai yang tampil di label. | 60 kg | Label berat menampilkan “60 kg” sesuai posisi slider. |
| TC002 | Verifikasi slider input tinggi | Aplikasi terbuka | 1. Geser slider tinggi ke nilai tertentu.<br>2. Periksa nilai yang tampil di label. | 170 cm | Label tinggi menampilkan “170 cm” sesuai posisi slider. |

---

#### 🔹 Scenario TS002 – Perhitungan dan Klasifikasi BMI
| ID Test Case | Deskripsi | Precondition | Test Steps | Test Data | Expected Result |
|---------------|------------|----------------|-------------|-------------|----------------|
| TC003 | Verifikasi hasil perhitungan BMI sesuai rumus standar (kg/m²) | Aplikasi terbuka | 1. Masukkan tinggi 170 cm<br>2. Masukkan berat 65 kg | 170 cm, 65 kg | Hasil BMI = 22.49 |
| TC004 | Verifikasi kategori “Underweight” | Aplikasi terbuka | 1. Masukkan tinggi 170 cm<br>2. Masukkan berat 45 kg | 170 cm, 45 kg | BMI = 15.6 → tampil kategori “Underweight” |
| TC005 | Verifikasi kategori “Normal” | Aplikasi terbuka | 1. Masukkan tinggi 165 cm<br>2. Masukkan berat 60 kg | 165 cm, 60 kg | BMI = 22.0 → tampil kategori “Normal” |
| TC006 | Verifikasi kategori “Overweight” | Aplikasi terbuka | 1. Masukkan tinggi 170 cm<br>2. Masukkan berat 75 kg | 170 cm, 75 kg | BMI ≈ 25.95 → tampil kategori “Overweight” |
| TC007 | Verifikasi kategori “Obese” | Aplikasi terbuka | 1. Masukkan tinggi 165 cm<br>2. Masukkan berat 90 kg | 165 cm, 90 kg | BMI ≈ 33.06 → tampil kategori “Obese” |

---

#### 🔹 Scenario TS003 – Penyimpanan History BMI
| ID Test Case | Deskripsi | Precondition | Test Steps | Test Data | Expected Result |
|---------------|------------|----------------|-------------|-------------|----------------|
| TC008 | Verifikasi penyimpanan hasil BMI ke history | Aplikasi terbuka | 1. Geser slider berat dan tinggi ke nilai tertentu<br>2. Tekan tombol “Simpan History” | 170 cm, 65 kg | Data BMI terbaru tersimpan dan muncul di halaman history. |
| TC009 | Verifikasi penyimpanan banyak data tanpa kehilangan data lama | Aplikasi terbuka & memiliki history | 1. Simpan beberapa hasil BMI<br>2. Buka halaman history | Beberapa kombinasi input | Semua data tampil lengkap sesuai urutan penyimpanan. |

---

## 🐞 Bug Report

### 📋 **Pengertian Bug Report**
**Bug Report** adalah dokumen formal yang mencatat kesalahan (*bug*) yang ditemukan selama pengujian.  
Tujuannya adalah memberi informasi lengkap kepada **developer** untuk memperbaiki masalah dengan cepat dan efisien.

Bug biasanya diklasifikasikan berdasarkan dua aspek penting:
- **Severity (Keparahan)** — seberapa besar bug memengaruhi sistem.  
- **Priority (Prioritas)** — seberapa cepat bug harus diperbaiki.

---

### ⚖️ **Kategori Severity & Priority**

| Severity | Penjelasan |
|-----------|-------------|
| **Low** | Bug kecil, tidak memengaruhi fungsionalitas sistem. |
| **Minor (Medium)** | Tidak memengaruhi fungsi utama, tapi menyebabkan ketidaknyamanan pengguna. |
| **Major (High)** | Fungsi utama tidak berjalan dengan benar, namun sistem tidak crash. |
| **Critical** | Bug menyebabkan aplikasi gagal total atau data rusak. |

| Priority | Penjelasan |
|-----------|-------------|
| **P1 – Urgent/Critical** | Harus segera diperbaiki, berdampak pada seluruh sistem. |
| **P2 – High** | Bug penting yang memengaruhi banyak pengguna. |
| **P3 – Medium** | Bisa diperbaiki pada rilis berikutnya. |
| **P4 – Low** | Masalah kecil, kosmetik, atau tidak mendesak. |

---

### 🧾 **Contoh Bug Report – Aplikasi BMI**

| Field | Keterangan |
|--------|-------------|
| **Bug Title** | Perhitungan BMI salah saat input berat 60 kg dan tinggi 170 cm |
| **Bug ID** | BMI-001 |
| **Step to Reproduce** | 1. Buka aplikasi BMI<br>2. Masukkan Berat = 60<br>3. Masukkan Tinggi = 170<br>4. Klik tombol “Hitung” |
| **Actual Result** | Hasil BMI = 12.5 |
| **Expected Result** | Hasil BMI seharusnya = 20.8 |
| **Build Number** | Version 1.0.0 |
| **Severity** | Major (High) |
| **Priority** | P2 – High |
| **Assignee** | Developer |
| **Reporter** | SQA (Software Quality Assurance) |
| **Reported On** | 31-08-2025 |
| **Testing Environment** | Android Device |

---

## 💡 Cara Menghindari Bug

Untuk meminimalkan kemunculan bug, beberapa praktik terbaik dapat diterapkan di seluruh **siklus pengembangan perangkat lunak**:

1. 🧩 **Pahami Persyaratan** – Pastikan semua anggota tim memahami kebutuhan sistem dengan jelas.  
2. 🧠 **Unit Testing** – Uji bagian terkecil kode lebih awal agar bug terdeteksi sejak dini.  
3. 🔍 **Code Review** – Lakukan pemeriksaan silang antar pengembang untuk mendeteksi kesalahan logika.  
4. 📋 **Rencana Pengujian (Test Plan)** – Susun test plan yang komprehensif sesuai standar IEEE 829.  
5. ⚙️ **Automation Testing** – Gunakan alat otomatis untuk mempercepat dan mengefisienkan proses uji.  
6. 🤝 **Kolaborasi Tim** – Bangun komunikasi yang baik antara pengembang dan penguji.

---

## ✅ Kesimpulan

**Test Scenario**, **Test Case**, dan **Bug Report** adalah komponen inti dari aktivitas pengujian perangkat lunak.  
Mereka memastikan setiap fungsi aplikasi diuji, kesalahan terdokumentasi, dan pengembang memiliki dasar kuat untuk melakukan perbaikan.

> “Quality software doesn’t happen by chance — it’s the result of careful planning, testing, and collaboration.”

## Kontak

**Developer:** Kevin Ardhana  
**GitHub:** [@kevinardhana096](https://github.com/kevinardhana096)   
**Email:** kevinardhana096@gmail.com  