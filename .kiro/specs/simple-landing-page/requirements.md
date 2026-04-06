# Dokumen Requirements

## Pendahuluan

Proyek ini bertujuan membangun sebuah landing page sederhana yang responsif sebagai tugas Coding Camp. Landing page dibangun menggunakan teknologi web dasar (HTML5, CSS3, dan Vanilla JavaScript) tanpa framework tambahan. Halaman ini mencakup navigasi, bagian hero, section konten/fitur, dan footer dengan tampilan yang bersih, modern, dan mobile-friendly.

## Glosarium

- **Landing_Page**: Halaman web tunggal yang menjadi tujuan utama pengunjung
- **Header**: Bagian paling atas halaman yang berisi logo dan navigasi
- **Navbar**: Komponen navigasi berisi tautan ke setiap section halaman
- **Hero_Section**: Bagian utama halaman yang menampilkan headline dan tombol CTA
- **CTA**: Call-to-Action, tombol atau elemen yang mendorong pengguna melakukan tindakan tertentu
- **Feature_Section**: Bagian halaman yang menampilkan fitur atau konten utama
- **Footer**: Bagian paling bawah halaman yang berisi informasi tambahan
- **Viewport**: Area tampilan yang terlihat oleh pengguna di layar perangkat
- **Breakpoint**: Titik lebar layar tertentu di mana tata letak halaman berubah untuk menyesuaikan ukuran perangkat

---

## Requirements

### Requirement 1: Struktur Halaman Utama

**User Story:** Sebagai pengunjung, saya ingin melihat halaman yang terstruktur dengan baik, agar saya dapat menavigasi konten dengan mudah.

#### Acceptance Criteria

1. THE Landing_Page SHALL memiliki struktur HTML5 yang valid dengan elemen `<!DOCTYPE html>`, `<html>`, `<head>`, dan `<body>`
2. THE Landing_Page SHALL memuat file `style.css` dan `script.js` secara eksternal
3. THE Landing_Page SHALL menampilkan Header, Hero_Section, Feature_Section, dan Footer secara berurutan dari atas ke bawah
4. WHEN halaman dimuat di browser, THE Landing_Page SHALL menampilkan seluruh konten tanpa error di konsol browser

---

### Requirement 2: Header dan Navigasi

**User Story:** Sebagai pengunjung, saya ingin melihat header dengan navigasi yang jelas, agar saya dapat berpindah ke section yang diinginkan dengan cepat.

#### Acceptance Criteria

1. THE Header SHALL menampilkan nama atau logo proyek di sisi kiri
2. THE Navbar SHALL menampilkan minimal 3 tautan navigasi yang mengarah ke section di halaman yang sama menggunakan anchor link
3. WHEN pengunjung mengklik tautan navigasi, THE Navbar SHALL menggulir halaman secara halus (smooth scroll) ke section yang dituju
4. WHILE halaman digulir melewati posisi awal Header, THE Header SHALL tetap terlihat di bagian atas layar (sticky/fixed position)
5. WHEN Viewport memiliki lebar kurang dari 768px, THE Navbar SHALL menyembunyikan tautan navigasi dan menampilkan ikon menu hamburger

---

### Requirement 3: Hero Section

**User Story:** Sebagai pengunjung, saya ingin melihat bagian hero yang menarik, agar saya segera memahami tujuan halaman dan terdorong untuk mengambil tindakan.

#### Acceptance Criteria

1. THE Hero_Section SHALL menampilkan sebuah headline utama dan teks deskripsi singkat
2. THE Hero_Section SHALL menampilkan minimal satu tombol CTA dengan label yang jelas
3. WHEN pengunjung mengklik tombol CTA, THE Hero_Section SHALL menggulir halaman ke Feature_Section
4. THE Hero_Section SHALL menggunakan tinggi minimal 100vh agar memenuhi seluruh area Viewport
5. WHEN Viewport memiliki lebar kurang dari 768px, THE Hero_Section SHALL menyesuaikan ukuran teks dan tata letak agar tetap terbaca dengan baik

---

### Requirement 4: Feature Section

**User Story:** Sebagai pengunjung, saya ingin melihat section yang menampilkan fitur atau konten utama, agar saya memahami nilai yang ditawarkan.

#### Acceptance Criteria

1. THE Feature_Section SHALL menampilkan minimal 3 kartu fitur (feature card) yang masing-masing berisi ikon atau gambar, judul, dan deskripsi singkat
2. THE Feature_Section SHALL menggunakan CSS Grid atau Flexbox untuk menata kartu fitur secara horizontal pada layar lebar
3. WHEN Viewport memiliki lebar kurang dari 768px, THE Feature_Section SHALL menata kartu fitur secara vertikal (satu kolom)
4. THE Feature_Section SHALL memiliki judul section yang terlihat jelas di atas kumpulan kartu fitur

---

### Requirement 5: Footer

**User Story:** Sebagai pengunjung, saya ingin melihat footer yang informatif, agar saya dapat menemukan informasi tambahan di bagian bawah halaman.

#### Acceptance Criteria

1. THE Footer SHALL menampilkan teks hak cipta dengan tahun yang sesuai
2. THE Footer SHALL menampilkan minimal satu tautan atau informasi kontak
3. THE Footer SHALL menggunakan warna latar belakang yang berbeda dari bagian konten utama untuk memberi batas visual yang jelas

---

### Requirement 6: Responsivitas dan Tampilan

**User Story:** Sebagai pengunjung yang mengakses dari berbagai perangkat, saya ingin halaman tampil dengan baik di semua ukuran layar, agar pengalaman membaca tetap nyaman.

#### Acceptance Criteria

1. THE Landing_Page SHALL menggunakan meta viewport tag `<meta name="viewport" content="width=device-width, initial-scale=1.0">` untuk mendukung tampilan mobile
2. THE Landing_Page SHALL mendefinisikan Breakpoint pada lebar 768px untuk membedakan tata letak mobile dan desktop
3. WHEN Viewport memiliki lebar kurang dari 768px, THE Landing_Page SHALL menyesuaikan seluruh tata letak menggunakan CSS media queries
4. THE Landing_Page SHALL menggunakan palet warna yang konsisten dengan minimal satu warna utama (primary) dan satu warna latar belakang (background)
5. THE Landing_Page SHALL menggunakan tipografi yang terbaca dengan ukuran font minimal 16px untuk teks paragraf

---

### Requirement 7: Interaktivitas dengan JavaScript

**User Story:** Sebagai pengunjung, saya ingin merasakan interaksi yang responsif saat menggunakan halaman, agar pengalaman menjelajah terasa lebih hidup.

#### Acceptance Criteria

1. WHEN Viewport memiliki lebar kurang dari 768px dan pengunjung mengklik ikon hamburger, THE Navbar SHALL menampilkan atau menyembunyikan menu navigasi secara toggle
2. WHEN pengunjung mengklik tautan navigasi pada menu mobile, THE Navbar SHALL menutup menu secara otomatis setelah tautan diklik
3. THE Landing_Page SHALL mengimplementasikan smooth scroll menggunakan JavaScript atau properti CSS `scroll-behavior: smooth`
4. IF JavaScript dinonaktifkan di browser, THEN THE Landing_Page SHALL tetap menampilkan seluruh konten statis tanpa kehilangan informasi penting
