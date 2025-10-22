---
title: "Testing Plan"
date: 2025-09-01 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/testing-plan.png

---


# Test Plan — Ringkasan Praktis
Dokumen ini merupakan ringkasan dari materi **Kelompok 3** tentang **rencana pengujian (Test Plan)** dalam mata kuliah *Software Testing and Quality Assurance*.

---

## Pengertian Test Plan
**Test Plan** adalah dokumen yang menjelaskan strategi, ruang lingkup, pendekatan, sumber daya, dan jadwal kegiatan pengujian.  
Tujuan utamanya adalah untuk **memastikan semua aspek testing direncanakan dengan baik** sebelum eksekusi dimulai.

---

## Tujuan Utama
- Menjadi pedoman bagi tim QA dalam melaksanakan pengujian.  
- Menentukan ruang lingkup dan batas pengujian.  
- Mengatur sumber daya (orang, waktu, alat).  
- Mengurangi risiko kesalahan dan ketidakefisienan saat testing.  

---

## Struktur Umum Test Plan
Berikut elemen utama yang biasa ada dalam dokumen test plan:

1. **Test Plan ID** — identifikasi unik dokumen.  
2. **Introduction / Overview** — latar belakang, tujuan testing.  
3. **Scope of Testing**  
   - *In-Scope:* fitur yang akan diuji.  
   - *Out-of-Scope:* fitur yang tidak termasuk.  
4. **Test Strategy / Approach** — pendekatan pengujian (manual/otomasi, black/white-box).  
5. **Test Environment** — spesifikasi hardware, software, tools, data, dan network.  
6. **Test Deliverables** — dokumen hasil (test case, report, defect log).  
7. **Schedule & Milestones** — jadwal pelaksanaan, tanggal review & sign-off.  
8. **Roles & Responsibilities** — siapa yang mengerjakan bagian apa.  
9. **Entry & Exit Criteria** — kapan pengujian dimulai dan dianggap selesai.  
10. **Risk & Mitigation** — risiko yang mungkin muncul serta rencana mitigasi.

---

## Komponen Tambahan
- **Resource Plan** — jumlah tester, skill set, dan ketersediaan.  
- **Test Data Management** — bagaimana data uji disiapkan dan dijaga konsistensinya.  
- **Defect Tracking System** — alat untuk mencatat dan memantau bug (mis. Jira, Bugzilla, Trello).  

---

## Contoh Entry & Exit Criteria

| Kriteria | Deskripsi |
|-----------|------------|
| **Entry** | Semua test case siap dan disetujui; environment stabil; build aplikasi tersedia. |
| **Exit** | Semua test case telah dijalankan, defect kritis sudah diperbaiki & diverifikasi. |

---

## Contoh Ringkas Format Test Plan

| Komponen | Deskripsi |
|-----------|------------|
| **Project Name** | Sistem Pemesanan Online |
| **Test Plan ID** | TP-001 |
| **Prepared By** | Tim QA Kelompok 3 |
| **Objective** | Memastikan fungsionalitas berjalan sesuai requirement |
| **Scope** | Modul login, register, dan transaksi |
| **Approach** | Manual Testing (Black-box) |
| **Environment** | Windows 10, Chrome v120, MySQL 8 |
| **Deliverables** | Test Case, Defect Report, Test Summary |
| **Schedule** | 1–15 Oktober 2025 |
| **Risks** | Keterlambatan build dari tim dev |
| **Mitigation** | Buffer waktu 2 hari untuk regression testing |

---

## Checklist Sebelum Pengujian Dimulai
- [ ] Test Plan sudah ditinjau & disetujui QA Lead.  
- [ ] Semua test case sudah siap & terdokumentasi.  
- [ ] Test environment aktif dan stabil.  
- [ ] Test data tersedia dan valid.  
- [ ] Semua peran (tester, developer, reviewer) sudah jelas.  

---

## Metrik Pengujian yang Umum Digunakan
- **Test Execution Rate** = (Jumlah Test Case Dijalankan / Total Test Case) × 100%  
- **Pass Rate** = (Jumlah Lulus / Total Dijalankan) × 100%  
- **Defect Density** = Jumlah Bug / Ukuran Modul  
- **Defect Severity Index (DSI)** untuk menilai dampak defect terhadap sistem.

---

## Tips Menyusun Test Plan Efektif
- Gunakan template standar QA untuk memudahkan review.  
- Tulis deskripsi dengan bahasa yang jelas dan singkat.  
- Update test plan jika ada perubahan requirement.  
- Kolaborasi aktif antara QA, Developer, dan Product Owner.  

---

## Kesimpulan
Test Plan adalah **dokumen dasar pengujian** yang menentukan arah, ruang lingkup, dan strategi pelaksanaan QA.  
Dengan perencanaan yang matang, tim QA dapat bekerja lebih terstruktur, efisien, dan meminimalkan risiko defect di tahap produksi.


---
