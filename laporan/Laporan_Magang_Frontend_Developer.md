# LAPORAN PL (PRAKTIK LAPANGAN)
## PERANCANGAN ANTARMUKA (UI/UX) DAN SISTEM PETA DIGITAL PARIWISATA
### POSISI: FRONTEND DEVELOPER

---
*(Halaman Judul)*

**Disusun Oleh:**
**[NAMA REKAN FRONTEND]**
**NIM. [NIM REKAN]**

**DIVISI PEMASARAN**
**DINAS PARIWISATA DAN KEBUDAYAAN KABUPATEN JEPARA**
**TAHUN 2026**

---
# KATA PENGANTAR
*(Standar)*

---
# DAFTAR ISI
1.  **BAB I: PENDAHULUAN** (Pentingnya Experience/UX bagi Wisatawan)
2.  **BAB II: LANDASAN TEORI**
    *   User Experience (UX) Design Principles
    *   CSS Framework (Tailwind CSS)
    *   Geographic Information System (GIS) Basic
    *   Responsive Web Design
3.  **BAB III: PERANCANGAN DESAIN (PROTOTYPING)**
    *   Wireframing (Low-Fidelity)
    *   Mockup & Design System (High-Fidelity)
4.  **BAB IV: IMPLEMENTASI ANTARMUKA**
    *   Slicing Design ke Blade Template
    *   Integrasi Peta Interaktif
    *   Optimasi Performa Frontend
5.  **BAB V: PENUTUP**

---

# BAB III: PERANCANGAN DESAIN
## 3.1 Design System
Sebelum implementasi kode, dibuat standar desain (Style Guide) agar tampilan konsisten:
*   **Palet Warna:** Menggunakan warna dominan Biru Laut (#...) dan Pasir (#...) yang mencerminkan identitas Jepara sebagai kota ukir dan bahari.
*   **Tipografi:** Menggunakan font *Sans-Serif* modern (Inter/Poppins) untuk keterbacaan tinggi di perangkat mobile.

## 3.2 Wireframe & Mockup
<!-- [PLACEHOLDER: GAMBAR WIREFRAME DARI FIGMA] -->
Desain dirancang *Mobile-First*, artinya prioritas utama adalah tampilan di layar HP, karena mayoritas wisatawan mengakses info saat di perjalanan.

---

# BAB IV: IMPLEMENTASI FRONTEND
## 4.1 Teknologi yang Digunakan
*   **Blade Templating Engine:** Memanfaatkan fitur `@extends`, `@section`, dan `@component` milik Laravel untuk membuat kode HTML yang modular dan rapi (misal: Navbar dan Footer dipisah jadi komponen).
*   **Tailwind CSS:** Framework *Utility-First* untuk styling yang cepat tanpa meninggalkan file HTML. Memungkinkan pembuatan *custom design* tanpa terpaku pada desain kaku framework lain (seperti Bootstrap).
*   **Alpine.js:** Digunakan untuk interaksi mikro seperti *Dropdown Menu*, *Modal*, dan *Image Slider* tanpa perlu memuat library jQuery yang berat.

## 4.2 Fitur Unggulan: Peta Wisata Interaktif (GIS)
Salah satu fitur paling kompleks di sisi Frontend adalah Peta Sebaran Wisata.
*   **Library:** LeafletJS (Open Source).
*   **Implementasi:**
    Mengambil data GeoJSON dari endpoint Backend, lalu me-render *Marker* di peta. Setiap marker memiliki *Popup* yang menampilkan foto thumbnail dan link ke detail wisata.
*   **Clustering:** Jika di satu area ada banyak wisata, marker akan menyatu (cluster) agar peta tidak terlihat berantakan.

## 4.3 Implementasi Halaman Kalender Event
Menampilkan jadwal event tahunan dengan tampilan grid yang responsif.
*   **Card Design:** Setiap event ditampilkan dalam kartu yang berisi Tanggal (Highlight), Judul, dan Lokasi.
*   **Filtering:** Menggunakan JavaScript untuk filter event berdasarkan Bulan tanpa reload halaman (AJAX Experience).

## 4.4 Responsivitas (Responsive Design)
Memastikan website tampil sempurna di berbagai ukuran layar:
*   **Desktop:** Layout grid 3-4 kolom.
*   **Tablet:** Layout grid 2 kolom.
*   **Mobile:** Layout stack (1 kolom) dengan navigasi *Hamburger Menu*.

---

# BAB V: KESIMPULAN & SARAN
## 5.1 Kesimpulan
Penerapan Tailwind CSS dan pendekatan Mobile-First berhasil menciptakan antarmuka yang ringan (load speed cepat) dan mudah digunakan oleh wisatawan. Integrasi Peta Digital menjadi nilai tambah utama yang membedakan website ini dengan blog wisata biasa.

## 5.2 Saran
Pengembangan selanjutnya dapat menambahkan fitur *PWA (Progressive Web App)* agar website bisa diinstal seperti aplikasi native dan bisa diakses saat offline (misal: saat sinyal hilang di pegunungan).

---
# LAMPIRAN
1.  **Screenshot Halaman Utama (Desktop & Mobile)**
2.  **Screenshot Peta Digital**
3.  **Link Prototype Figma**

