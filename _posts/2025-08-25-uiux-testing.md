---
title: "UI/UX Testing"
date: 2025-08-25 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/uiux.png

---


# UI/UX Testing — Ringkasan Praktis
Dokumen ini merupakan versi ringkas dari materi **Kelompok 2** tentang pengujian antarmuka pengguna (UI) dan pengalaman pengguna (UX).

---

## Tujuan Utama
- Memastikan tampilan aplikasi konsisten dan mudah digunakan.  
- Menguji kepuasan pengguna terhadap alur (flow) dan kemudahan interaksi.  
- Menemukan hambatan usability, masalah visual, dan kesalahan navigasi.

---

## Perbedaan UI vs UX Testing

| Aspek | UI Testing | UX Testing |
|-------|-------------|-------------|
| Fokus | Tampilan & elemen visual | Pengalaman & kemudahan penggunaan |
| Tujuan | Memastikan elemen antarmuka tampil dan berfungsi benar | Mengukur kepuasan & efektivitas penggunaan |
| Contoh | Warna, ukuran tombol, layout | Flow checkout, waktu menyelesaikan tugas |

---

## Tahapan Umum UX Testing
1. Menentukan tujuan dan KPI usability.  
2. Mendesain skenario tugas (task).  
3. Melibatkan pengguna nyata (5–10 orang).  
4. Mengamati interaksi & mencatat hambatan.  
5. Analisis hasil dan buat rekomendasi perbaikan.

---

## Prinsip Heuristik (Nielsen)
1. Visibility of system status  
2. Match with real world  
3. User control & freedom  
4. Consistency & standards  
5. Error prevention  
6. Recognition over recall  
7. Efficiency of use  
8. Aesthetic & minimalist design  
9. Help users recover from errors  
10. Help & documentation  

---

## Tools Populer
- **UI Testing:** Applitools, Percy, BrowserStack  
- **UX Testing:** Maze, UserTesting, Hotjar, Microsoft Clarity  
- **Accessibility:** axe, Lighthouse, WAVE  

---

## Aksesibilitas Dasar
- Warna kontras minimal 4.5:1  
- Semua elemen bisa diakses via keyboard  
- Label teks & `alt` untuk gambar  
- Struktur heading berurutan (H1 → H2 → H3)

---

## Contoh Test Case UI/UX

| ID | Jenis | Deskripsi | Langkah | Expected Result |
|----|--------|------------|----------|----------------|
| UI-01 | UI | Konsistensi tombol login | Buka halaman A & B, bandingkan tombol login | Warna & ukuran sama |
| UX-01 | UX | Proses checkout mudah | Simulasikan pembelian | Pengguna selesai < 3 menit |
| ACC-01 | Accessibility | Navigasi keyboard pada form | Tab antar input field | Fokus berpindah logis |

---

## Checklist Sebelum Rilis
- [ ] Konsistensi tampilan antar halaman  
- [ ] Responsif di mobile & desktop  
- [ ] Flow utama diuji (login, checkout, search)  
- [ ] Tes aksesibilitas dasar lulus  
- [ ] Feedback pengguna sudah di-review  

---

## Kesimpulan
UI testing memastikan tampilan & fungsi antarmuka berjalan baik, sedangkan UX testing memastikan pengalaman pengguna menyenangkan dan efisien. Kombinasi keduanya penting untuk menciptakan produk yang **berfungsi baik sekaligus mudah digunakan.**

---