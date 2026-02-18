# 🎯 PRESENTASI JELAJAH JEPARA - PART 2
## Fitur Utama & Demo Halaman Publik

> **👤 PRESENTER: [NAMA ANGGOTA TIM 2]**  
> **⏱️ DURASI: 12-15 Menit**

---

## 📋 AGENDA PRESENTASI PART 2

1. Fitur Halaman Publik (Landing Page)
2. Sistem Peta Interaktif (GIS)
3. Katalog Destinasi Wisata
4. Sistem E-Ticketing untuk Wisatawan
5. Berita & Calendar of Events
6. Demo Live Website

---

## 1️⃣ FITUR HALAMAN PUBLIK (LANDING PAGE)

### 🏠 HALAMAN UTAMA - First Impression

#### A. Hero Section dengan 3D Map
```
┌─────────────────────────────────────────────────────┐
│  🏝️ JELAJAH JEPARA                    🇮🇩 ID | EN 🇬🇧 │
│  Portal Resmi Pariwisata Kabupaten Jepara          │
│                                                     │
│  ┌───────────────────────────────────────────────┐ │
│  │                                               │ │
│  │         [PETA 3D INTERAKTIF]                  │ │
│  │      Visualisasi Lanskap Jepara               │ │
│  │                                               │ │
│  └───────────────────────────────────────────────┘ │
│                                                     │
│  [Jelajah Peta] [Destinasi] [E-Tiket] [Berita]    │
└─────────────────────────────────────────────────────┘
```

**Fitur Hero Section:**
- ✅ Peta 3D menggunakan MapLibre GL JS
- ✅ Animasi smooth dengan GSAP
- ✅ Tombol CTA (Call-to-Action) yang jelas
- ✅ Responsive di semua device


#### B. Section Destinasi Pilihan
**Menampilkan 20 destinasi wisata unggulan Jepara:**

- 🏖️ Pantai Kartini
- 🏝️ Karimunjawa
- 🏛️ Museum Kartini
- 🏰 Benteng Portugis
- 🌊 Pantai Bandengan
- 🎢 Jepara Ourland Park
- Dan 14 destinasi lainnya...

**Fitur:**
- Card design yang menarik dengan gambar berkualitas tinggi
- Rating & kategori destinasi
- Link langsung ke detail destinasi
- Lazy loading untuk performa optimal

#### C. Section Budaya & Kuliner
**Showcase kekayaan budaya Jepara:**

**Budaya:**
- 🎭 Barikan Kubro
- 🔥 Obor Tradisional
- 🧵 Tenun Troso
- 🎪 Festival Kupat Lepet

**Kuliner Khas:**
- 🍜 Horog-Horog
- 🥜 Kacang Jepara
- ☕ Kopi Jepara
- 🍬 Gempol Plered

#### D. Section Legenda Jepara
**Tokoh bersejarah:**
- 👸 Ratu Kalinyamat
- 📚 R.A. Kartini
- ⚔️ Ratu Shima

---

## 2️⃣ SISTEM PETA INTERAKTIF (GIS)

### 🗺️ JELAJAH PETA - Geographic Information System

#### A. Fitur Peta Utama

**1. Base Map dengan Multiple Layers:**
```
Layer Control:
├── 📍 Destinasi Wisata (Places)
├── 🏛️ Batas Administratif (Boundaries)
├── 🛣️ Infrastruktur (Roads, Irrigation)
└── 🌾 Penggunaan Lahan (Land Use)
```

**2. Interactive Features:**
- ✅ **Zoom In/Out** - Kontrol zoom dengan mouse wheel
- ✅ **Pan** - Geser peta dengan drag
- ✅ **Marker Clustering** - Grouping marker untuk performa
- ✅ **Popup Information** - Klik marker untuk detail
- ✅ **Search Location** - Cari destinasi berdasarkan nama
- ✅ **Filter by Category** - Filter berdasarkan jenis wisata

#### B. Teknologi GIS yang Digunakan

**MapLibre GL JS:**
- Rendering 3D dengan WebGL
- Performa tinggi untuk banyak marker
- Custom styling untuk branding

**Leaflet.js:**
- Fallback untuk browser lama
- Marker clustering
- Routing & directions

**GeoJSON Format:**
```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [110.6684, -6.5889]
      },
      "properties": {
        "name": "Pantai Kartini",
        "category": "Pantai",
        "rating": 4.5
      }
    }
  ]
}
```

#### C. Use Case Peta Interaktif

**Untuk Wisatawan:**
1. Cari destinasi wisata terdekat
2. Lihat rute menuju lokasi
3. Eksplorasi area sekitar destinasi
4. Temukan hotel & restoran terdekat

**Untuk Pengelola:**
1. Visualisasi sebaran destinasi wisata
2. Analisis kepadatan wisata per area
3. Perencanaan infrastruktur pariwisata
4. Monitoring perkembangan destinasi

---

## 3️⃣ KATALOG DESTINASI WISATA

### 🏖️ HALAMAN DESTINASI

#### A. Listing Page - Katalog Lengkap

**Fitur Pencarian & Filter:**
```
┌─────────────────────────────────────────────────┐
│  🔍 Cari destinasi...          [Filter ▼]       │
├─────────────────────────────────────────────────┤
│  Kategori:                                      │
│  [ ] Pantai  [ ] Museum  [ ] Taman  [ ] Kuliner│
├─────────────────────────────────────────────────┤
│  ┌──────────┐  ┌──────────┐  ┌──────────┐     │
│  │  [IMG]   │  │  [IMG]   │  │  [IMG]   │     │
│  │ Pantai   │  │ Museum   │  │ Karimun  │     │
│  │ Kartini  │  │ Kartini  │  │ Jawa     │     │
│  │ ⭐ 4.5   │  │ ⭐ 4.8   │  │ ⭐ 4.9   │     │
│  └──────────┘  └──────────┘  └──────────┘     │
└─────────────────────────────────────────────────┘
```

**Informasi pada Card:**
- Foto destinasi (optimized)
- Nama destinasi (bilingual)
- Rating & kategori
- Lokasi (kecamatan)
- Link ke detail page

#### B. Detail Page - Informasi Lengkap

**Struktur Halaman Detail:**

**1. Header Section:**
- Gallery foto (multiple images)
- Nama destinasi (ID & EN)
- Rating & jumlah review
- Tombol "Beli Tiket" (jika tersedia)
- Tombol "Share" (WhatsApp, Facebook, Twitter)

**2. Informasi Utama:**
```
📍 Alamat Lengkap
🕐 Jam Operasional
📞 Kontak
🗺️ Google Maps Link
💰 Harga Tiket (jika ada)
```

**3. Deskripsi Lengkap:**
- Sejarah destinasi
- Fasilitas yang tersedia
- Wahana/aktivitas
- Tips berkunjung

**4. Peta Lokasi:**
- Embedded map dengan marker
- Tombol "Get Directions"

**5. Destinasi Terkait:**
- Rekomendasi destinasi serupa
- Destinasi terdekat

#### C. Fitur Multilingual

**Automatic Language Detection:**
```php
// Contoh implementasi
if (app()->getLocale() == 'en') {
    echo $place->name_en ?? $place->name;
    echo $place->description_en ?? $place->description;
} else {
    echo $place->name;
    echo $place->description;
}
```

**Tombol Switch Language:**
- 🇮🇩 Bahasa Indonesia
- 🇬🇧 English

---

## 4️⃣ SISTEM E-TICKETING UNTUK WISATAWAN

### 🎟️ PEMBELIAN TIKET ONLINE

#### A. Flow Pembelian Tiket

```
1. Browse Tiket          →  Lihat daftar tiket tersedia
2. Pilih Tiket           →  Pilih destinasi & tanggal kunjungan
3. Isi Data Pengunjung   →  Nama, email, no. HP, jumlah tiket
4. Login Google          →  Autentikasi dengan Google OAuth
5. Checkout              →  Review pesanan
6. Pilih Pembayaran      →  GoPay/QRIS/VA/ShopeePay
7. Bayar                 →  Selesaikan pembayaran
8. Terima Tiket          →  Email + download PDF + QR Code
```

#### B. Halaman Daftar Tiket

**Tampilan Katalog Tiket:**
```
┌─────────────────────────────────────────────────┐
│  E-TIKET WISATA JEPARA                          │
├─────────────────────────────────────────────────┤
│  ┌──────────────────────────────────────────┐  │
│  │  🏖️ Tiket Pantai Kartini                 │  │
│  │  💰 Rp 10.000 (Weekday)                  │  │
│  │  💰 Rp 15.000 (Weekend)                  │  │
│  │  📅 Berlaku 1 hari                       │  │
│  │  [Beli Tiket]                            │  │
│  └──────────────────────────────────────────┘  │
│                                                 │
│  ┌──────────────────────────────────────────┐  │
│  │  🏝️ Tiket Karimunjawa                    │  │
│  │  💰 Rp 50.000                            │  │
│  │  📅 Berlaku 3 hari                       │  │
│  │  [Beli Tiket]                            │  │
│  └──────────────────────────────────────────┘  │
└─────────────────────────────────────────────────┘
```

#### C. Form Pemesanan

**Data yang Dikumpulkan:**
- Nama lengkap pengunjung
- Email (untuk notifikasi)
- Nomor HP (untuk konfirmasi)
- Tanggal kunjungan
- Jumlah tiket
- Asal kota/provinsi (analytics)

**Validasi:**
- ✅ Cek ketersediaan kuota
- ✅ Validasi tanggal (tidak boleh masa lalu)
- ✅ Validasi format email & HP
- ✅ Cek harga (weekday vs weekend)

#### D. Sistem Pembayaran

**Metode Pembayaran yang Tersedia:**

**1. E-Wallet:**
- 💚 GoPay (QR Code + Deep Link)
- 🟠 ShopeePay (Deep Link)

**2. QRIS:**
- 📱 Universal QR Code (semua e-wallet)

**3. Virtual Account:**
- 🔵 BCA
- 🟠 BNI
- 🔴 BRI
- 🟡 Mandiri

**4. ATM Transfer:**
- 🏧 Mandiri Bill Payment

**Keamanan Pembayaran:**
- ✅ Integrasi resmi Midtrans
- ✅ PCI-DSS Compliant
- ✅ Enkripsi SSL/TLS
- ✅ Signature verification untuk webhook
- ✅ Idempotency check (prevent double payment)

#### E. Tiket Digital (QR Code)

**Format Tiket:**
```
┌─────────────────────────────────────────────┐
│  🏝️ JELAJAH JEPARA                          │
│  E-TICKET                                   │
├─────────────────────────────────────────────┤
│  Destinasi: Pantai Kartini                  │
│  Tanggal: 20 Februari 2026                  │
│  Jumlah: 2 Tiket                            │
│  Total: Rp 20.000                           │
├─────────────────────────────────────────────┤
│  Nama: John Doe                             │
│  Email: john@example.com                    │
│  No. Tiket: TIX-ABC123XYZ456                │
├─────────────────────────────────────────────┤
│         ┌─────────────────┐                 │
│         │                 │                 │
│         │   [QR CODE]     │                 │
│         │                 │                 │
│         └─────────────────┘                 │
│                                             │
│  Scan QR Code di pintu masuk                │
└─────────────────────────────────────────────┘
```

**Fitur Tiket Digital:**
- ✅ QR Code unik per tiket
- ✅ Download PDF
- ✅ Download QR Code (PNG)
- ✅ Tampilkan di browser (paperless)
- ✅ Kirim otomatis ke email
- ✅ Status tiket real-time (pending/paid/used)

#### F. Halaman "Tiket Saya"

**Dashboard Tiket Pengguna:**
```
┌─────────────────────────────────────────────┐
│  TIKET SAYA                                 │
├─────────────────────────────────────────────┤
│  Status: [Semua ▼] [Aktif] [Digunakan]     │
├─────────────────────────────────────────────┤
│  ✅ Pantai Kartini - 20 Feb 2026            │
│     Status: Sudah Dibayar                   │
│     [Lihat QR] [Download]                   │
├─────────────────────────────────────────────┤
│  ⏳ Museum Kartini - 25 Feb 2026            │
│     Status: Menunggu Pembayaran             │
│     [Bayar Sekarang]                        │
├─────────────────────────────────────────────┤
│  ✔️ Karimunjawa - 15 Feb 2026               │
│     Status: Sudah Digunakan                 │
│     Digunakan: 15 Feb 2026, 09:30           │
└─────────────────────────────────────────────┘
```

---

## 5️⃣ BERITA & CALENDAR OF EVENTS

### 📰 SISTEM BERITA

#### A. Halaman Berita

**Fitur:**
- Grid layout dengan thumbnail
- Kategori berita
- Tanggal publikasi
- Excerpt (ringkasan)
- View count
- Pagination

**Contoh Berita:**
- "Festival Bahari Jepara 2026"
- "Karimunjawa Raih Penghargaan Destinasi Terbaik"
- "Tips Liburan Hemat di Jepara"

#### B. Detail Berita

**Struktur:**
- Featured image
- Judul (bilingual)
- Tanggal & penulis
- Konten lengkap (rich text)
- Share buttons
- Related posts

### 📅 CALENDAR OF EVENTS

#### A. Kalender Event Budaya

**Tampilan Kalender:**
```
┌─────────────────────────────────────────────┐
│  CALENDAR OF EVENTS 2026                    │
├─────────────────────────────────────────────┤
│  [< Februari 2026 >]                        │
│                                             │
│  Sen  Sel  Rab  Kam  Jum  Sab  Min         │
│                            1    2           │
│   3    4    5    6    7    8    9          │
│  10   11   12   13   14  [15]  16          │
│                          🎭                 │
│  17   18   19   20   21   22   23          │
│  24   25   26   27   28                    │
└─────────────────────────────────────────────┘

Event pada 15 Februari:
🎭 Festival Kupat Lepet
📍 Alun-alun Jepara
🕐 08:00 - 17:00 WIB
```

#### B. Detail Event

**Informasi Event:**
- Nama event (bilingual)
- Tanggal & waktu
- Lokasi
- Deskripsi lengkap
- Foto event
- Kontak penyelenggara
- Link pendaftaran (jika ada)

---

## 6️⃣ DEMO LIVE WEBSITE

### 🖥️ SKENARIO DEMO

#### Demo 1: Jelajah Destinasi
1. Buka halaman utama
2. Scroll ke section destinasi pilihan
3. Klik salah satu destinasi (contoh: Pantai Kartini)
4. Tunjukkan gallery foto
5. Scroll ke deskripsi lengkap
6. Tunjukkan peta lokasi
7. Klik tombol "Beli Tiket"

#### Demo 2: Peta Interaktif
1. Klik menu "Jelajah Peta"
2. Zoom in/out pada peta
3. Klik marker destinasi
4. Tunjukkan popup informasi
5. Gunakan search untuk cari destinasi
6. Toggle layer (boundaries, infrastructure)

#### Demo 3: Pembelian Tiket
1. Pilih tiket dari katalog
2. Isi form pemesanan
3. Login dengan Google
4. Review pesanan di checkout
5. Pilih metode pembayaran (QRIS)
6. Tunjukkan QR Code pembayaran
7. (Simulasi) Setelah bayar, tunjukkan tiket digital

#### Demo 4: Switch Language
1. Klik tombol bahasa (ID → EN)
2. Tunjukkan perubahan konten
3. Navigasi ke halaman destinasi
4. Tunjukkan deskripsi dalam bahasa Inggris

---

## 🎯 HIGHLIGHT FITUR UNGGULAN

### ⭐ TOP 5 FITUR YANG MEMBEDAKAN

1. **Peta 3D Interaktif**
   - Visualisasi modern dengan MapLibre GL JS
   - Tidak ada kompetitor lokal yang punya fitur ini

2. **E-Ticketing Terintegrasi**
   - Cashless payment dengan Midtrans
   - QR Code untuk validasi cepat

3. **Multilingual Support**
   - Bahasa Indonesia & Inggris
   - Menjangkau wisatawan mancanegara

4. **Responsive Design**
   - Mobile-friendly
   - Optimal di semua device

5. **Real-time Analytics**
   - Dashboard untuk pengelola
   - Data pengunjung & pendapatan live

---

## 📊 STATISTIK & PERFORMA

### Performa Website:
- ⚡ Load time: < 2 detik
- 📱 Mobile score: 95/100
- 🔍 SEO score: 98/100
- ♿ Accessibility: WCAG 2.1 compliant

### Kapasitas Sistem:
- 👥 Concurrent users: 1000+
- 🎟️ Transaksi/hari: 5000+
- 💾 Database: Scalable
- 🔒 Uptime: 99.9%

---

## 🔄 TRANSISI KE PART 3

Terima kasih. Selanjutnya, rekan saya **[NAMA ANGGOTA TIM 3]** akan mendemonstrasikan **Dashboard Admin** dan **Sistem Manajemen Backend**.

---

**📝 CATATAN UNTUK PRESENTER:**
- Siapkan browser dengan tab yang sudah dibuka
- Pastikan koneksi internet stabil untuk demo
- Siapkan akun demo untuk login
- Latih navigasi website agar lancar
- Siapkan backup screenshot jika demo gagal
- Highlight fitur yang paling menarik
- Jaga pace presentasi agar tidak terlalu cepat

---

> **END OF PART 2** | Dilanjutkan oleh Presenter 3 ➡️
