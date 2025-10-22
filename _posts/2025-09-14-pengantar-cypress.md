---
title: "Pengantar Cypress"
date: 2025-09-14 08:30:00
categories: [Software Testing and Quality Assurance]
tags: [STQA]
image: /assets/images/pengantar-cypress.png

---

#  Cypress Testing — Ringkasan Materi
Ringkasan dari materi **Kelompok 8** tentang *Cypress Testing*, yaitu framework pengujian otomatis berbasis JavaScript untuk aplikasi web modern. Cypress banyak digunakan karena kemudahannya dalam menulis, menjalankan, dan memantau hasil pengujian UI maupun API.

---

##  Pengertian Cypress
**Cypress** adalah framework *end-to-end testing* berbasis JavaScript yang digunakan untuk menguji aplikasi web langsung di browser.  
Cypress memungkinkan developer dan tester menulis pengujian cepat, stabil, dan mudah dibaca.

> Cypress berbeda dengan Selenium karena berjalan di dalam browser yang sama dengan aplikasi yang diuji (real-time execution).

---

##  Fitur Utama Cypress
-  **Realtime Reloading:** setiap perubahan kode test langsung dijalankan ulang otomatis.  
-  **Automatic Screenshots & Videos:** hasil pengujian direkam otomatis.  
-  **Time Travel:** dapat melihat kembali langkah eksekusi test di browser.  
-  **Network Traffic Control:** dapat mengontrol, stub, dan memantau request API.  
-  **Debug Friendly:** pesan error mudah dipahami dan dapat dilihat langsung di DevTools.  

---

##  Komponen Testing di Cypress

| Komponen | Deskripsi |
|-----------|------------|
| **Test Runner** | GUI interaktif untuk menjalankan test dan melihat hasilnya. |
| **Command Log** | Log eksekusi setiap perintah (klik, input, visit, dll). |
| **Fixtures** | File JSON untuk menyimpan data uji. |
| **Integration Folder** | Menyimpan file test utama (.cy.js). |
| **Support Folder** | Menyimpan konfigurasi umum (beforeEach, custom commands). |

---

##  Instalasi Cypress
Cypress dapat dipasang menggunakan **Node.js** dan **npm**.

```bash
# 1. Inisialisasi project Node.js
npm init -y

# 2. Instal Cypress
npm install cypress --save-dev

# 3. Jalankan Cypress
npx cypress open
```
## Contoh Test Case Sederhana

File: cypress/integration/login.cy.js
```javascript
describe('Login Testing', () => {
  it('Login berhasil dengan kredensial valid', () => {
    cy.visit('https://www.saucedemo.com/')
    cy.get('#user-name').type('standard_user')
    cy.get('#password').type('secret_sauce')
    cy.get('#login-button').click()
    cy.url().should('include', '/inventory.html')
  })
})
```
## Penjelasan:
- cy.visit() — membuka URL aplikasi.
- cy.get(selector) — mencari elemen menggunakan CSS selector.
- .type() — mengetik input.
- .click() — menekan tombol.
-.should() — melakukan assertion hasil.

## Contoh Assertion Cypress
```javascript
// Memastikan elemen tampil
cy.get('.inventory_item').should('be.visible')

// Memastikan teks sesuai
cy.get('.title').should('contain', 'Products')

// Memastikan jumlah item sesuai
cy.get('.inventory_item').should('have.length', 6)
```

## Command Cypress yang Umum Digunakan

| Perintah            | Fungsi                          |
| ------------------- | ------------------------------- |
| `cy.visit(url)`     | Membuka halaman web             |
| `cy.get(selector)`  | Mengambil elemen                |
| `cy.type(value)`    | Menulis input                   |
| `cy.click()`        | Klik elemen                     |
| `cy.contains(text)` | Mencari elemen berdasarkan teks |
| `cy.url()`          | Mengambil URL saat ini          |
| `cy.screenshot()`   | Mengambil tangkapan layar       |
| `cy.request()`      | Melakukan pengujian API         |

### Kesimpulan
Cypress merupakan alat pengujian modern yang sangat cocok untuk web berbasis JavaScript.
Dengan kemudahan setup, dokumentasi lengkap, dan hasil visual yang interaktif, Cypress menjadi salah satu framework favorit QA modern untuk melakukan UI dan API Testing secara cepat dan akurat.