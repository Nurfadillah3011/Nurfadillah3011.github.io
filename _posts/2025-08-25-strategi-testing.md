---
title: "Strategi Testing"
date: 2025-08-25 07:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/strategi-testing.png

---


# Testing Strategy — Ringkasan Praktis
Dokumen ringkas ini memuat poin-poin penting dari materi **Kelompok 1** tentang strategi pengujian perangkat lunak. Cocok untuk dibagikan ke teman sebagai cheat-sheet cepat.

---

## Inti Tujuan Testing (singkat)
- Menemukan dan mendokumentasikan cacat (bug).  
- Memastikan perangkat lunak sesuai requirement (verifikasi & validasi).  
- Mengurangi risiko saat rilis dan meningkatkan kualitas produk.

---

## STLC — Fase Utama (ringkas)
1. **Planning**: scope, strategi, resource, timeline.  
2. **Design**: buat test case & test data.  
3. **Environment setup**: staging/dev sesuai versi.  
4. **Execution**: jalankan test, catat hasil & defect.  
5. **Reporting**: test summary, metrik, rekomendasi.  
6. **Closure**: sign-off & dokumentasi akhir.

---

## Level Pengujian (singkat)
- **Unit** — oleh developer (fungsi/kode).  
- **Integration** — antar modul.  
- **System / E2E** — seluruh sistem.  
- **Acceptance** — verifikasi user/PO.

---

## Pendekatan Testing
- **Black-box**: fokus fungsionalitas tanpa lihat kode.  
- **White-box**: tes berdasarkan struktur kode (coverage).  
- **Manual vs Otomasi**: manual untuk exploratory/usability; otomasi untuk regresi & smoke.

---

## Checklist Cepat Sebelum Release
- [ ] Semua test case kritis lulus.  
- [ ] Tidak ada bug *critical* yang belum ditangani.  
- [ ] Smoke test pada build release lulus.  
- [ ] Backup & rollback plan siap.  
- [ ] Approval QA & PO diperoleh.

---

## Contoh Test Case

| ID    | Deskripsi singkat       | Precondition        | Langkah singkat                         | Expected Result                       |
|-------|-------------------------|---------------------|-----------------------------------------|---------------------------------------|
| TC-01 | Login sukses            | Akun terdaftar      | 1. Buka login 2. Masukkan user+pwd      | Masuk ke dashboard                    |
| TC-02 | Login gagal (wrong pw)  | Akun terdaftar      | 1. Buka login 2. Masukkan pwd salah     | Pesan "invalid credentials" muncul    |

---

## Metrik Penting (pilihan)
- **Pass Rate** = passed / executed × 100%  
- **Defect Density** = defects / module-size  
- **MTTR** = rata-rata waktu perbaikan defect

---

## Contoh Entry / Exit Criteria (singkat)
- **Entry**: Test environment ready & test cases tersedia.  
- **Exit**: Semua test case utama dieksekusi, critical bugs fixed & verified.

---

## Tips Praktis
- Mulai test sejak fase desain (shift-left).  
- Gunakan otomasi untuk regression suite.  
- Prioritaskan testing untuk fitur high-risk.  
- Dokumentasikan langkah reproduksi bug yang jelas (screenshot + logs).

---

## Kesimpulan singkat
Strategi testing yang efektif adalah yang terencana, menggabungkan level pengujian tepat, dan memakai otomasi hanya pada area yang memberi nilai (regression/smoke). Dokumentasi & komunikasi dengan tim dev/PO sama pentingnya.

---


