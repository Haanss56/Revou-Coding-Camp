# Rencana Implementasi: Simple Landing Page

## Ikhtisar

Implementasi landing page statis menggunakan HTML5, CSS3, dan Vanilla JavaScript dengan pendekatan mobile-first. Tiga file utama (`index.html`, `style.css`, `script.js`) dibangun secara bertahap, dimulai dari struktur HTML, kemudian styling, lalu interaktivitas JavaScript.

## Tugas

- [x] 1. Buat struktur HTML dasar (`index.html`)
  - Buat file `index.html` dengan deklarasi `<!DOCTYPE html>`, elemen `<html>`, `<head>`, dan `<body>`
  - Tambahkan meta viewport tag `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
  - Tambahkan tag `<link>` untuk memuat `style.css` dan tag `<script>` untuk memuat `script.js` secara eksternal
  - Tambahkan tag `<noscript>` sebagai fallback ketika JavaScript dinonaktifkan
  - _Requirements: 1.1, 1.2, 6.1, 7.4_

- [x] 2. Implementasi komponen Header dan Navigasi di HTML
  - [x] 2.1 Buat elemen `<header>` dengan logo dan navbar
    - Tambahkan elemen `<header id="header">` berisi div logo dan elemen `<nav>`
    - Buat `<ul class="nav-links">` dengan minimal 3 item `<li><a href="#...">` sebagai anchor link
    - Tambahkan `<button class="hamburger" aria-label="Toggle menu" aria-expanded="false">` dengan tiga elemen `<span>` di dalamnya
    - _Requirements: 2.1, 2.2_

- [x] 3. Implementasi Hero Section, Feature Section, dan Footer di HTML
  - [x] 3.1 Buat elemen `<section id="hero">`
    - Tambahkan elemen `<h1>` untuk headline utama dan `<p>` untuk deskripsi singkat
    - Tambahkan elemen `<a href="#features" class="cta-button">` sebagai tombol CTA
    - _Requirements: 3.1, 3.2, 3.3_

  - [x] 3.2 Buat elemen `<section id="features">`
    - Tambahkan `<h2>` sebagai judul section
    - Buat `<div class="feature-grid">` berisi minimal 3 `<div class="feature-card">`, masing-masing dengan ikon (emoji), `<h3>`, dan `<p>`
    - _Requirements: 4.1, 4.4_

  - [x] 3.3 Buat elemen `<footer id="footer">`
    - Tambahkan teks hak cipta dengan tahun menggunakan `<p>`
    - Tambahkan minimal satu tautan kontak menggunakan `<a href="mailto:...">`
    - _Requirements: 5.1, 5.2_

- [x] 4. Implementasi styling dasar dan variabel CSS (`style.css`)
  - Buat file `style.css` dengan CSS reset/normalisasi dasar
  - Definisikan variabel CSS (custom properties) untuk palet warna: minimal satu warna utama (`--color-primary`) dan satu warna latar belakang (`--color-bg`)
  - Atur `font-size` dasar minimal 16px untuk elemen `<p>` dan body
  - Tambahkan `html { scroll-behavior: smooth; }` sebagai fallback smooth scroll
  - _Requirements: 6.2, 6.4, 6.5, 7.3_

- [~] 5. Implementasi styling Header dan Navbar
  - [x] 5.1 Styling Header (sticky dan tampilan umum)
    - Terapkan `position: sticky; top: 0` pada `<header>` agar tetap terlihat saat scroll
    - Atur tata letak header menggunakan Flexbox (logo di kiri, nav di kanan)
    - _Requirements: 2.4_

  - [x] 5.2 Styling Navbar untuk mobile (< 768px)
    - Sembunyikan `.nav-links` secara default pada mobile (misal: `display: none` atau `max-height: 0`)
    - Tampilkan `.hamburger` hanya pada viewport < 768px
    - Tambahkan style untuk class `.active` pada `.nav-links` agar menu muncul saat toggle
    - _Requirements: 2.5, 7.1_

  - [-] 5.3 Styling Navbar untuk desktop (≥ 768px) menggunakan media query
    - Gunakan `@media (min-width: 768px)` untuk menampilkan `.nav-links` secara horizontal
    - Sembunyikan `.hamburger` pada viewport ≥ 768px
    - _Requirements: 6.2, 6.3_

- [~] 6. Implementasi styling Hero Section, Feature Section, dan Footer
  - [~] 6.1 Styling Hero Section
    - Terapkan `min-height: 100vh` pada `#hero`
    - Atur tata letak teks dan tombol CTA menggunakan Flexbox atau Grid
    - Tambahkan media query untuk menyesuaikan ukuran teks dan tata letak pada mobile (< 768px)
    - _Requirements: 3.4, 3.5_

  - [~] 6.2 Styling Feature Section
    - Terapkan `display: grid; grid-template-columns: repeat(3, 1fr)` atau `display: flex` pada `.feature-grid` untuk desktop
    - Tambahkan media query `< 768px` untuk mengubah layout menjadi satu kolom
    - Styling setiap `.feature-card` agar tampil konsisten
    - _Requirements: 4.2, 4.3_

  - [~] 6.3 Styling Footer
    - Terapkan `background-color` yang berbeda dari warna latar belakang konten utama
    - _Requirements: 5.3_

- [~] 7. Checkpoint — Pastikan semua tes lulus
  - Pastikan semua tes lulus, tanyakan kepada pengguna jika ada pertanyaan.

- [~] 8. Implementasi interaktivitas JavaScript (`script.js`)
  - [~] 8.1 Implementasi toggle menu hamburger
    - Buat file `script.js`
    - Tambahkan event listener `click` pada `.hamburger`
    - Saat diklik, toggle class `active` pada `.nav-links` dan perbarui atribut `aria-expanded` pada tombol hamburger
    - _Requirements: 7.1_

  - [~] 8.2 Implementasi penutupan menu otomatis saat nav link diklik
    - Tambahkan event listener `click` pada setiap elemen `<a>` di dalam `.nav-links`
    - Saat diklik, hapus class `active` dari `.nav-links` dan set `aria-expanded="false"` pada hamburger
    - _Requirements: 7.2_

  - [ ]* 8.3 Tulis unit test untuk logika toggle hamburger
    - Verifikasi bahwa class `active` ditambahkan saat hamburger diklik pertama kali
    - Verifikasi bahwa class `active` dihapus saat hamburger diklik kedua kali
    - Verifikasi bahwa `aria-expanded` diperbarui dengan benar
    - _Requirements: 7.1_

  - [ ]* 8.4 Tulis unit test untuk penutupan menu otomatis
    - Verifikasi bahwa class `active` dihapus dari `.nav-links` setelah nav link diklik
    - _Requirements: 7.2_

- [~] 9. Verifikasi aksesibilitas dan fallback no-JavaScript
  - Pastikan atribut `aria-label` dan `aria-expanded` ada pada tombol hamburger
  - Pastikan tag `<noscript>` menyembunyikan hamburger dan menampilkan nav-links saat JS dinonaktifkan
  - Pastikan semua elemen `<img>` (jika ada) memiliki atribut `alt` yang deskriptif
  - _Requirements: 1.4, 7.4_

- [~] 10. Checkpoint akhir — Pastikan semua tes lulus
  - Pastikan semua tes lulus, tanyakan kepada pengguna jika ada pertanyaan.

## Catatan

- Tugas bertanda `*` bersifat opsional dan dapat dilewati untuk MVP yang lebih cepat
- Setiap tugas merujuk ke requirements spesifik untuk keterlacakan
- Pendekatan mobile-first: CSS ditulis untuk mobile terlebih dahulu, kemudian diperluas untuk desktop
- Tidak ada property-based test karena fitur ini adalah halaman statis tanpa logika bisnis kompleks
