---
title: "Test Scenario, Test Case and Bug Report"
date: 2025-09-01 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/test-scenarion-test-case-and-bug-report.png

---

# Test Scenario, Test Case, and Bug Report (Kelompok 4)

Ringkasan dari materi **Kelompok 4** mengenai *Test Scenario*, *Test Case*, dan *Bug Report*. Materi ini menjelaskan cara menyusun skenario uji, membuat test case yang efektif, serta menulis laporan bug yang terstruktur dalam proses pengujian perangkat lunak.

---

## Pengantar
Dalam pengujian perangkat lunak, tiga dokumen ini saling berkaitan:

| Konsep | Fungsi Utama | Fokus |
|--------|---------------|-------|
| **Test Scenario** | Menjabarkan apa yang akan diuji | Gambaran besar |
| **Test Case** | Menjelaskan langkah uji secara detail | Langkah dan data uji |
| **Bug Report** | Melaporkan kesalahan yang ditemukan | Perbaikan bug |

---

## 1. Test Scenario
### Definisi
**Test Scenario** adalah deskripsi singkat tentang fungsi atau fitur yang perlu diuji.  
Berfungsi sebagai panduan umum sebelum menyusun test case.

### Tujuan
- Memastikan seluruh fitur teruji dengan benar.  
- Menghemat waktu pembuatan test case.  
- Memberikan gambaran luas cakupan pengujian.

### Contoh

| ID | Deskripsi Skenario | Modul | Catatan |
|----|--------------------|--------|----------|
| TS001 | Verifikasi proses login pengguna | Login | Uji kredensial valid dan tidak valid |
| TS002 | Verifikasi perhitungan BMI | BMI Calculator | Pastikan hasil sesuai formula BMI |
| TS003 | Verifikasi penyimpanan data history BMI | History | Pastikan hasil tersimpan dengan benar |

---

## 2. Test Case
### Definisi
**Test Case** adalah serangkaian langkah terperinci untuk memverifikasi apakah suatu fitur bekerja sesuai dengan requirement.

### Komponen Test Case
- **ID Test Case**
- **Deskripsi Pengujian**
- **Precondition**
- **Langkah Pengujian (Test Steps)**
- **Data Uji (Test Data)**
- **Expected Result**
- **Actual Result**
- **Status (Pass/Fail)**
- **Catatan Tambahan**

### Contoh Test Case

| ID | Deskripsi | Precondition | Test Steps | Test Data | Expected Result | Status |
|----|------------|---------------|-------------|------------|----------------|--------|
| TC001 | Verifikasi login sukses | Aplikasi terbuka | 1. Masukkan username dan password valid 2. Klik tombol login | user=“dina”, pass=“12345” | User berhasil masuk dashboard | Pass |
| TC002 | Verifikasi login gagal | Aplikasi terbuka | 1. Masukkan username dan password salah 2. Klik login | user=“dina”, pass=“abcde” | Pesan error muncul “Invalid credentials” | Pass |
| TC003 | Perhitungan BMI | Aplikasi terbuka | 1. Masukkan tinggi dan berat 2. Klik “Hitung BMI” | tinggi=170, berat=65 | BMI = 22.5 (Normal) | Pass |
| TC004 | Simpan hasil BMI | Data BMI tersedia | 1. Klik “Simpan History” 2. Buka halaman History | - | Data muncul di daftar History | Pass |

---

## 3. Bug Report
### Definisi
**Bug Report** adalah dokumen untuk melaporkan kesalahan (defect) yang ditemukan selama pengujian agar developer dapat memperbaikinya.

### Komponen Utama Bug Report
- **Bug ID**
- **Title**
- **Module / Feature**
- **Severity & Priority**
- **Steps to Reproduce**
- **Expected Result**
- **Actual Result**
- **Attachments (Screenshot, Log)**
- **Status**
- **Assignee**

### Contoh Bug Report

| Field | Keterangan |
|--------|------------|
| **Bug ID** | BMI-001 |
| **Title** | Nilai BMI salah saat input berat 60 dan tinggi 170 |
| **Module** | BMI Calculator |
| **Severity** | Major |
| **Priority** | P2 (High) |
| **Steps to Reproduce** | 1. Masukkan Berat = 60, Tinggi = 170 2. Klik “Hitung BMI” |
| **Expected Result** | BMI = 20.8 |
| **Actual Result** | BMI = 12.5 |
| **Status** | Open |
| **Reported By** | QA Tester |
| **Assigned To** | Developer |
| **Attachment** | Screenshot hasil perhitungan |

---

## 4. Severity vs Priority

| Severity | Penjelasan | Contoh |
|-----------|-------------|--------|
| **Critical** | Sistem crash atau data hilang | Aplikasi menutup tiba-tiba setelah login |
| **Major** | Fungsi utama tidak berjalan | Tombol “Submit” tidak berfungsi |
| **Minor** | Gangguan kecil, tidak mempengaruhi fungsional utama | Typo di halaman utama |
| **Low** | Gangguan visual atau non-urgent | Warna tombol tidak konsisten |

| Priority | Penjelasan | Contoh |
|-----------|-------------|--------|
| **P1 (Critical)** | Harus diperbaiki segera | Bug yang menghentikan testing |
| **P2 (High)** | Harus diperbaiki pada rilis berikutnya | Fungsi utama tidak berjalan |
| **P3 (Medium)** | Bisa diperbaiki kemudian | Performa lambat di browser tertentu |
| **P4 (Low)** | Tidak mendesak | Error kosmetik kecil |

---

## Tips Menulis Bug Report yang Efektif
1. **Gunakan judul yang ringkas tapi jelas.**  
   ➜ *Contoh: “Login gagal dengan password valid.”*
2. **Langkah reproduksi harus jelas.**  
   ➜ Sertakan data uji dan hasil aktual.
3. **Sertakan bukti visual (screenshot/video).**
4. **Gunakan severity dan priority secara tepat.**
5. **Pastikan bug bisa direproduksi secara konsisten.**

---

##  Alur Hubungan Antar Dokumen
```text
Test Scenario → Test Case → Bug Report
```
---