---
title: "API Testing"
date: 2025-09-07 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/api-testing.png

---


# API Testing — Ringkasan Praktis
Ringkasan ini berasal dari materi **Kelompok 6** yang membahas **API Testing**, yaitu pengujian antarmuka pemrograman aplikasi (Application Programming Interface) yang berfungsi untuk menghubungkan berbagai sistem dan layanan.

---

## Pengertian API Testing
**API Testing** adalah proses pengujian yang berfokus pada **lapisan logika bisnis** dan **komunikasi antar aplikasi**, bukan pada tampilan (UI).

> Tujuan utamanya adalah memastikan bahwa request dan response dari API berjalan **sesuai dengan spesifikasi fungsional dan non-fungsional**.

---

## Mengapa API Testing Penting?
- Memastikan integrasi antar sistem berjalan lancar.  
- Menemukan bug lebih cepat sebelum diuji lewat UI.  
- Menjamin keamanan (authentication & authorization).  
- Menjaga konsistensi data antar service.  
- Meningkatkan efisiensi pengujian melalui otomasi.

---

## Komponen Utama API

| Komponen | Deskripsi |
|-----------|------------|
| **Endpoint** | URL yang digunakan untuk mengakses API. |
| **Request** | Permintaan dari client (misalnya GET, POST). |
| **Response** | Balasan dari server berupa data (biasanya JSON). |
| **Header** | Informasi tambahan seperti format data atau token autentikasi. |
| **Body** | Data yang dikirim (biasanya pada metode POST atau PUT). |

---

## Jenis Metode HTTP

| Metode | Deskripsi | Contoh |
|---------|------------|--------|
| **GET** | Mengambil data dari server | `GET /api/users` |
| **POST** | Mengirim data baru ke server | `POST /api/users` |
| **PUT** | Memperbarui data yang sudah ada | `PUT /api/users/1` |
| **DELETE** | Menghapus data dari server | `DELETE /api/users/1` |
| **PATCH** | Memperbarui sebagian data | `PATCH /api/users/1` |

---

## Jenis Pengujian API
1. **Functional Testing** — memeriksa apakah fungsi API berjalan sesuai requirement.  
2. **Load Testing** — menguji performa API di bawah beban tinggi.  
3. **Security Testing** — memastikan keamanan endpoint dan autentikasi.  
4. **Validation Testing** — memverifikasi struktur, tipe data, dan response code.  
5. **Error Handling Test** — memeriksa bagaimana API merespons input salah.

---

## Tools Populer untuk API Testing

| Tools | Kegunaan |
|--------|----------|
| **Postman** | Membuat, menjalankan, dan mengelola request API secara manual atau otomatis. |
| **SoapUI** | Pengujian API SOAP & REST dengan fitur scripting. |
| **Newman** | Menjalankan koleksi Postman lewat command line (CI/CD). |
| **Katalon Studio** | Otomasi testing API dengan antarmuka visual. |
| **RestAssured** | Framework Java untuk pengujian API otomatis. |

---

## Contoh Request & Response API

**Request (POST)**  
```http
POST /api/login
Content-Type: application/json

{
  "username": "user123",
  "password": "secret"
}
```
**Response (200 OK)**  
```http
{
  "status": "success",
  "token": "abc123xyz"
}
```
## Contoh Test Script Otomatis (Postman + JavaScript)
```python
pm.test("Status code is 200", function () {
  pm.response.to.have.status(200);
});

pm.test("Response has token", function () {
  var jsonData = pm.response.json();
  pm.expect(jsonData).to.have.property("token");
});
```
## Kesimpulan
API Testing adalah bagian penting dalam proses pengujian perangkat lunak modern.
Dengan API testing yang baik, tim QA dapat:

- Memastikan integrasi antar sistem berjalan lancar,
- Menjamin keamanan data,
- Dan meningkatkan keandalan sistem sebelum dirilis ke pengguna.