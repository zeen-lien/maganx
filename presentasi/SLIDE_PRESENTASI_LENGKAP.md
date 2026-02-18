---
marp: true
theme: default
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
header: '🏝️ Jelajah Jepara - Portal Pariwisata Digital'
footer: '© 2026 Tim UNISNU Jepara | 19 Februari 2026'
---

<!-- _class: lead -->
# 🏝️ **JELAJAH JEPARA**
## Portal Resmi Pariwisata Kabupaten Jepara

### Presentasi Sistem Digital Terintegrasi

**Tim Mahasiswa Magang UNISNU Jepara**
**Tanggal: 19 Februari 2026**

---

<!-- _class: lead -->
# 👥 **TIM MAHASISWA UNISNU JEPARA**

### Jurusan Teknik Informatika

**Zaini Leon** - System Analyst
**Dany Akmallun** - Backend Developer
**Indonesiana Prima** - Frontend Developer
**Adimas Satria** - Multimedia

**Kerja Sama dengan:**
Dinas Pariwisata dan Kebudayaan Kabupaten Jepara

---

<!-- _class: lead -->
# 📋 **AGENDA PRESENTASI**

**Part 1:** Overview & Konsep (Zaini Leon)
**Part 2:** Fitur & Demo Publik (Indonesiana Prima)
**Part 3:** Dashboard Admin & Backend (Dany Akmallun)
**Part 4:** Teknologi & Roadmap (Adimas Satria)

**Total Durasi:** 50-60 Menit (termasuk Q&A)

---

<!-- _class: lead -->
# 🎯 **PART 1**
# **OVERVIEW & KONSEP**

**Presenter: Zaini Leon**
**System Analyst**

---

# 🎯 **VISI PROJECT**

> "Menjadikan Kabupaten Jepara sebagai destinasi wisata digital terdepan di Jawa Tengah melalui transformasi teknologi informasi yang modern, transparan, dan mudah diakses."

---

# 🚀 **MISI PROJECT**

### 1. **Digitalisasi Sektor Pariwisata**
Mengubah sistem manual menjadi digital end-to-end

### 2. **Promosi Wisata yang Efektif**
Menampilkan destinasi dengan visualisasi menarik

### 3. **Transparansi Keuangan**
Sistem e-ticketing untuk mencegah kebocoran pendapatan

### 4. **Kemudahan Akses Informasi**
Satu platform untuk semua kebutuhan pariwisata

---

# ❌ **PERMASALAHAN SAAT INI**

### A. Promosi Wisata
- ❌ Informasi tersebar di berbagai platform
- ❌ Tidak ada peta interaktif
- ❌ Konten tidak terstruktur
- ❌ Tidak ada dukungan bahasa Inggris

### B. Sistem Tiket Manual
- ❌ Penjualan tiket masih paper-based
- ❌ Potensi kebocoran pendapatan tinggi
- ❌ Sulit tracking pengunjung
- ❌ Antrian panjang di loket

---

# ❌ **PERMASALAHAN (Lanjutan)**

### C. Pengelolaan Konten
- ❌ Update informasi lambat
- ❌ Tidak ada sistem manajemen terpusat
- ❌ Sulit koordinasi antar pengelola

### D. Pelaporan Keuangan
- ❌ Laporan manual & memakan waktu
- ❌ Tidak ada transparansi real-time
- ❌ Sulit audit dan rekonsiliasi

---

<!-- _class: lead -->
# ✅ **SOLUSI: JELAJAH JEPARA**

## Platform Digital Pariwisata Terintegrasi

---

# ✅ **SOLUSI YANG DITAWARKAN**

### 1. Portal Wisata Modern
- ✅ Website responsif & user-friendly
- ✅ Peta interaktif 3D (MapLibre GL JS)
- ✅ Pencarian lokasi berbasis GIS
- ✅ Multilingual (Indonesia & Inggris)
- ✅ SEO Optimized

---

# ✅ **SOLUSI (Lanjutan)**

### 2. Sistem E-Ticketing Cashless
- ✅ Pembelian tiket online 24/7
- ✅ Pembayaran digital (GoPay, QRIS, VA)
- ✅ Tiket QR Code untuk validasi cepat
- ✅ Notifikasi otomatis via email
- ✅ Download tiket PDF

---

# ✅ **SOLUSI (Lanjutan)**

### 3. Dashboard Admin Komprehensif
- ✅ Manajemen destinasi wisata
- ✅ Manajemen tiket & harga
- ✅ Scan QR Code di pintu masuk
- ✅ Laporan keuangan real-time
- ✅ Export data ke Excel/PDF

---

# ✅ **SOLUSI (Lanjutan)**

### 4. Sistem Role & Permission
- ✅ Multi-level akses sesuai jabatan
- ✅ Super Admin, Admin Wisata, Admin Berita
- ✅ Audit trail untuk tracking aktivitas
- ✅ Keamanan berlapis dengan Google OAuth

---

# 🏗️ **ARSITEKTUR SISTEM**

```
┌─────────────────────────────────────┐
│     PRESENTATION LAYER              │
│  Website Publik | Admin Dashboard  │
└─────────────────────────────────────┘
              ↕
┌─────────────────────────────────────┐
│     APPLICATION LAYER               │
│  Laravel | Business Logic | Payment │
└─────────────────────────────────────┘
              ↕
┌─────────────────────────────────────┐
│        DATA LAYER                   │
│  MySQL | File Storage | External API│
└─────────────────────────────────────┘
```

---

# 🛠️ **TECHNOLOGY STACK**

### Backend
- **PHP 8.2+** - Server language
- **Laravel 12.0** - Framework
- **MySQL 8.0+** - Database

### Frontend
- **Tailwind CSS 3.4** - CSS framework
- **Alpine.js 3.4** - JS framework
- **Livewire 4.1** - Real-time UI

### Mapping
- **MapLibre GL JS 5.15** - Peta 3D
- **Leaflet.js 1.9** - GIS mapping

---

# 📈 **MANFAAT UNTUK STAKEHOLDER**

### 🏛️ Untuk Dinas Pariwisata
- ✅ Transparansi pendapatan real-time
- ✅ Data analytics untuk keputusan
- ✅ Efisiensi operasional
- ✅ Promosi wisata lebih efektif

### 🧳 Untuk Wisatawan
- ✅ Kemudahan akses informasi
- ✅ Pembelian tiket online 24/7
- ✅ Pembayaran cashless aman
- ✅ Tiket digital (paperless)

---

<!-- _class: lead -->
# 🎯 **PART 2**
# **FITUR & DEMO PUBLIK**

**Presenter: Indonesiana Prima**
**Frontend Developer**

---

# 🏠 **LANDING PAGE**

### Hero Section dengan Peta 3D
- ✅ Peta 3D interaktif (MapLibre GL JS)
- ✅ Animasi smooth dengan GSAP
- ✅ Tombol CTA yang jelas
- ✅ Responsive di semua device

### First Impression yang Kuat
- Visual menarik dengan peta 3D
- Navigasi intuitif
- Loading cepat (< 2 detik)

---

# 🏖️ **DESTINASI PILIHAN**

### 20 Destinasi Wisata Unggulan Jepara

**Pantai & Laut:**
- 🏖️ Pantai Kartini
- 🏝️ Karimunjawa
- 🌊 Pantai Bandengan

**Budaya & Sejarah:**
- 🏛️ Museum Kartini
- 🏰 Benteng Portugis

**Hiburan:**
- 🎢 Jepara Ourland Park

---

# 🗺️ **PETA INTERAKTIF**

### Multiple Layers
- 📍 Destinasi Wisata (Places)
- 🏛️ Batas Administratif (Boundaries)
- 🛣️ Infrastruktur (Roads, Irrigation)
- 🌾 Penggunaan Lahan (Land Use)

### Interactive Features
- ✅ Zoom In/Out
- ✅ Pan (drag peta)
- ✅ Marker Clustering
- ✅ Popup Information
- ✅ Search location
- ✅ Filter by category

---

# 🏖️ **KATALOG DESTINASI**

### Fitur Pencarian & Filter
- 🔍 Search bar dengan auto-complete
- 🏷️ Filter by kategori (Pantai, Museum, Taman)
- ⭐ Sort by rating
- 📍 Sort by distance

### Detail Page
- Gallery foto (multiple images)
- Deskripsi lengkap (bilingual)
- Peta lokasi
- Jam operasional
- Harga tiket
- Tombol "Beli Tiket"

---

# 🌍 **MULTILINGUAL**

### Dukungan 2 Bahasa

**🇮🇩 Bahasa Indonesia**
- Untuk wisatawan lokal
- Konten lengkap

**🇬🇧 English**
- Untuk wisatawan mancanegara
- Professional content

### Switch Language
- Toggle button di header
- Seamless transition

---

# 🎟️ **E-TICKETING**

### Flow Pembelian Tiket
```
1. Browse Tiket
2. Pilih Tiket & Tanggal
3. Isi Data Pengunjung
4. Login Google OAuth
5. Checkout & Review
6. Pilih Pembayaran
7. Bayar (GoPay/QRIS/VA)
8. Terima Tiket Digital
```

---

# 💳 **METODE PEMBAYARAN**

### E-Wallet
- 💚 **GoPay** - QR Code + Deep Link
- 🟠 **ShopeePay** - Deep Link

### QRIS
- 📱 **Universal QR Code** - Semua e-wallet

### Virtual Account
- 🔵 BCA | 🟠 BNI | 🔴 BRI | 🟡 Mandiri

---

# 📱 **TIKET DIGITAL**

### Format Tiket QR Code
- ✅ QR Code unik per tiket
- ✅ Download PDF
- ✅ Download QR Code (PNG)
- ✅ Tampilkan di browser (paperless)
- ✅ Kirim otomatis ke email
- ✅ Status tiket real-time

### Status Tiket
- ⏳ Pending (menunggu pembayaran)
- ✅ Paid (sudah dibayar)
- ✔️ Used (sudah digunakan)

---

# 📰 **BERITA & EVENT**

### Sistem Berita
- Grid layout dengan thumbnail
- Kategori berita
- Tanggal publikasi
- View count

### Calendar of Events
- Interactive calendar view
- Filter by month
- Event markers
- Detail event lengkap

---

# 🖥️ **DEMO LIVE WEBSITE**

### Skenario Demo:
1. **Jelajah Destinasi** - Browse & detail destinasi
2. **Peta Interaktif** - Zoom, search, filter
3. **Pembelian Tiket** - Full flow checkout
4. **Switch Language** - ID ↔ EN

**Highlight:** UX yang smooth & fitur lengkap

---

# ⭐ **FITUR UNGGULAN**

### 1. Peta 3D Interaktif
Visualisasi modern dengan MapLibre GL JS
**Tidak ada kompetitor lokal yang punya!**

### 2. E-Ticketing Terintegrasi
Cashless payment + QR Code validation

### 3. Multilingual Support
Indonesia & English untuk wisatawan asing

### 4. Responsive Design
Mobile-friendly, optimal di semua device

---

<!-- _class: lead -->
# 🎯 **PART 3**
# **DASHBOARD ADMIN & BACKEND**

**Presenter: Dany Akmallun**
**Backend Developer**

---

# 🔐 **ROLE & PERMISSION (RBAC)**

### Hierarki Role
- **Super Admin** - Akses penuh sistem
- **Admin Wisata** - Kelola destinasi & tiket
- **Admin Berita** - Kelola konten
- **Pengelola Wisata** - Scan QR Code

### Keamanan
- ✅ Authentication (email & password)
- ✅ Google OAuth
- ✅ CSRF Protection
- ✅ SQL Injection Prevention
- ✅ Activity Log (Audit Trail)

---

# 📊 **DASHBOARD ADMIN**

### Widget Statistik Real-time
```
🎟️ TIKET: 245 (↗️ +12%)
💰 PENDAPATAN: Rp 3.450.000 (↗️ +15%)
👥 PENGUNJUNG: 520 (↗️ +8%)
```

### Grafik & Visualisasi
- Grafik Penjualan Tiket (7 Hari)
- Top 5 Destinasi Terpopuler
- Metode Pembayaran (Pie Chart)

---

# 🏖️ **MANAJEMEN DESTINASI**

### Fitur CRUD Destinasi
- Daftar destinasi dengan filter & search
- Form tambah/edit destinasi
- Upload foto (multiple)
- Pilih lokasi di peta interaktif
- Rich text editor (TinyMCE)
- Bilingual content (ID & EN)

### Informasi Lengkap
- Nama, kategori, deskripsi
- Lokasi (lat/long, alamat)
- Jam operasional
- Kontak & fasilitas

---

# 🎟️ **MANAJEMEN TIKET**

### Fitur Tiket
- Daftar tiket per destinasi
- Harga weekday & weekend
- Kuota harian
- Masa berlaku
- Status (Aktif/Nonaktif)

### Daftar Pesanan
- Filter by status (Pending/Paid/Used)
- Filter by tanggal & destinasi
- Detail pesanan lengkap
- Export laporan

---

# 📱 **SCAN QR CODE**

### Sistem Validasi Tiket
1. Pengelola buka halaman scan
2. Kamera smartphone aktif
3. Scan QR Code pada tiket
4. Sistem validasi otomatis
5. Tampilkan hasil (Valid/Invalid)

### Status Validasi
- ✅ **VALID** - Tiket dapat digunakan
- ❌ **INVALID** - Tiket tidak valid
  (Belum dibayar, sudah digunakan, expired, dll)

---

# 💰 **LAPORAN KEUANGAN**

### Ringkasan Pendapatan
```
HARI INI: Rp 3.450.000 (↗️ +15%)
BULAN INI: Rp 85.200.000 (↗️ +22%)
TAHUN INI: Rp 950.000.000 (↗️ +35%)
```

### Fitur Laporan
- Filter periode (hari/minggu/bulan/tahun)
- Breakdown per destinasi
- Breakdown per metode pembayaran
- Grafik trend pendapatan
- Export ke Excel/PDF

---

# 📊 **ANALYTICS LANJUTAN**

### Metrics Penting
- **Conversion Rate** - Visitor → Buyer
- **Customer Insights** - Asal pengunjung
- **Peak Times** - Jam & hari sibuk
- **Repeat Customer** - Customer loyalty

### Transparansi
- ✅ Audit trail lengkap
- ✅ Laporan keuangan akurat
- ✅ Data tidak bisa dimanipulasi
- ✅ Akuntabilitas tinggi

---

# 🖥️ **DEMO DASHBOARD**

### Skenario Demo:
1. **Login & Dashboard** - Statistik real-time
2. **Kelola Destinasi** - CRUD destinasi
3. **Scan QR Code** - Validasi tiket (WOW!)
4. **Laporan Keuangan** - Export Excel

**Highlight:** QR Code validation yang cepat & akurat

---

# ⭐ **KEUNGGULAN BACKEND**

### 1. RBAC System
Multi-level access control yang aman

### 2. Real-time Dashboard
Data update otomatis tanpa refresh

### 3. QR Code Validation
Scan cepat & akurat di pintu masuk

### 4. Comprehensive Reporting
Laporan keuangan lengkap & transparan

### 5. Audit Trail
Semua aktivitas tercatat

---

<!-- _class: lead -->
# 🎯 **PART 4**
# **TEKNOLOGI & ROADMAP**

**Presenter: Adimas Satria**
**Multimedia**

---

# 🏗️ **ARSITEKTUR TEKNIS**

### Backend Stack
- **Laravel 12.0** - Framework PHP modern
- **Eloquent ORM** - Database abstraction
- **Middleware** - Request filtering
- **Queue System** - Background jobs

### Key PHP Packages
- Spatie Permission (RBAC)
- Midtrans PHP (Payment)
- Intervention Image (Image processing)
- Bacon QR Code (QR generation)
- Laravel Socialite (OAuth)

---

# 🎨 **FRONTEND STACK**

### Modern JavaScript
- **Tailwind CSS 3.4** - Utility-first CSS
- **Alpine.js 3.4** - Lightweight JS
- **MapLibre GL 5.15** - 3D maps
- **Chart.js 4.5** - Data visualization
- **TinyMCE 8.3** - Rich text editor
- **html5-qrcode 2.3** - QR scanner

### Build Tools
- **Vite 7.0** - Lightning-fast build
- **PostCSS** - CSS processing
- **Autoprefixer** - Browser compatibility

---

# 🗄️ **DATABASE**

### MySQL 8.0+ with Spatial Extensions
- Point data (lat/long)
- Polygon data (boundaries)
- Spatial queries
- Distance calculations

### Optimasi
- ✅ Indexing strategy
- ✅ Query optimization
- ✅ Eager loading (N+1 problem)
- ✅ Database connection pooling

### Backup
- Daily automated backup
- Point-in-time recovery
- Offsite backup storage

---

# 💳 **PAYMENT GATEWAY**

### Midtrans Integration
```
1. User checkout
2. Create Snap Token
3. Show payment page
4. User pays
5. Webhook notification
6. Update order status
7. Send ticket email
```

### Security
- ✅ PCI-DSS Compliant
- ✅ 3D Secure
- ✅ Fraud Detection
- ✅ Signature verification
- ✅ Encrypted communication

---

# 🔒 **SECURITY**

### Application Security
- ✅ CSRF Protection
- ✅ XSS Prevention
- ✅ SQL Injection Prevention
- ✅ Authentication & Authorization
- ✅ Rate Limiting (DDoS protection)

### Data Protection
- ✅ SSL/TLS (HTTPS)
- ✅ Password Hashing (Bcrypt)
- ✅ Sensitive Data Encryption
- ✅ GDPR compliance ready

---

# 🚀 **DEPLOYMENT**

### Production Environment
```
Load Balancer (Nginx)
       ↓
Application Servers (Laravel)
       ↓
Database Server (MySQL)
```

### Server Requirements
- **CPU:** 4 cores
- **RAM:** 8 GB
- **Storage:** 100 GB SSD
- **Bandwidth:** 1 Gbps

---

# 🚀 **HOSTING & DOMAIN**

### Domain Setup
- **Domain:** jelajahjepara.id
- **DNS:** Cloudflare (CDN + DDoS protection)
- **SSL:** Let's Encrypt (free, auto-renew)

### Hosting Options
- **VPS:** DigitalOcean, Linode ($20-50/month)
- **Cloud:** AWS, Google Cloud (Pay-as-you-go)

---

# 🔧 **MAINTENANCE**

### Regular Maintenance
- **Daily:** Automated backup
- **Weekly:** Security updates
- **Monthly:** Performance review
- **Quarterly:** Feature updates

### Support System
- 📧 Email support
- 📱 WhatsApp support
- 💬 Live chat
- 📞 Phone support (jam kerja)

---

# 🗺️ **ROADMAP 2026**

### Q2 2026 (Apr - Jun)
- ✅ Launch MVP
- ✅ User feedback collection
- ✅ Bug fixes & optimization
- ✅ Marketing campaign

### Q3 2026 (Jul - Sep)
- 🔄 Mobile app (Android/iOS)
- 🔄 Advanced analytics
- 🔄 AI chatbot support
- 🔄 Integration dengan hotel booking

---

# 🗺️ **ROADMAP 2026-2027**

### Q4 2026 (Oct - Dec)
- 🔄 Virtual tour (360°)
- 🔄 Augmented Reality (AR)
- 🔄 Loyalty program
- 🔄 Multi-currency support

### 2027: Expansion
- 🔮 Integration dengan OTA (Traveloka, Tiket.com)
- 🔮 Partnership dengan travel agent
- 🔮 B2B portal untuk tour operator
- 🔮 AI recommendation engine

---

# 📊 **PROJECTED GROWTH**

### Year 1 (2026)
```
👥 Users: 50,000+
🎟️ Tickets sold: 100,000+
💰 Revenue: Rp 1.5 Miliar
📈 Growth: 200%
```

### Year 2 (2027)
```
👥 Users: 150,000+
🎟️ Tickets sold: 300,000+
💰 Revenue: Rp 4.5 Miliar
📈 Growth: 300%
```

---

# 📊 **ROI PROJECTION**

### Investment
```
💰 Development: Rp 150 Juta
💰 Infrastructure: Rp 50 Juta/tahun
💰 Marketing: Rp 100 Juta/tahun
💰 Maintenance: Rp 75 Juta/tahun
───────────────────────────────
💰 Total Year 1: Rp 375 Juta
```

### Return
```
💰 Revenue Year 1: Rp 1.5 Miliar
📈 ROI: 300%
⏰ Payback Period: 6-8 bulan
```

---

<!-- _class: lead -->
# 🎯 **KESIMPULAN**

---

# 🎯 **KESIMPULAN KESELURUHAN**

### Jelajah Jepara adalah:

1. ✅ **Portal wisata modern** dengan peta 3D interaktif
2. ✅ **E-ticketing cashless** terintegrasi Midtrans
3. ✅ **Dashboard admin** dengan RBAC & analytics
4. ✅ **Teknologi terkini** (Laravel 12, MapLibre, etc)
5. ✅ **Roadmap jelas** untuk pengembangan

---

# 🎯 **VALUE PROPOSITION**

### Untuk Dinas Pariwisata
- 💰 Transparansi pendapatan
- 📊 Data analytics real-time
- 🚀 Efisiensi operasional
- 📈 Potensi peningkatan PAD

### Untuk Wisatawan
- 🎟️ Kemudahan pembelian tiket
- 🗺️ Informasi lengkap destinasi
- 💳 Pembayaran cashless
- 🌍 Multilingual support

---

# 🎯 **COMPETITIVE ADVANTAGE**

### Yang Membedakan Kami:

1. **Peta 3D Interaktif** - Tidak ada kompetitor lokal
2. **E-Ticketing Terintegrasi** - End-to-end solution
3. **QR Code Validation** - Cepat & akurat
4. **Real-time Analytics** - Data-driven decision
5. **Scalable Architecture** - Siap untuk growth

---

# 🎯 **NEXT STEPS**

### Implementasi

**Phase 1: Soft Launch (1 bulan)**
- Deploy ke production
- Training admin & pengelola
- Pilot test di 5 destinasi
- Feedback & improvement

**Phase 2: Full Launch (2 bulan)**
- Marketing campaign
- Onboard semua destinasi
- Monitor & optimize
- Scale infrastructure

---

# 🎯 **CALL TO ACTION**

### Mari Bersama Memajukan Pariwisata Jepara!

**Kami siap untuk:**
- ✅ Deployment & implementation
- ✅ Training & support
- ✅ Maintenance & updates
- ✅ Continuous improvement

---

<!-- _class: lead -->
# 🙏 **TERIMA KASIH**

## Jelajah Jepara
### Portal Resmi Pariwisata Kabupaten Jepara

**Tim Mahasiswa Magang UNISNU Jepara**
Zaini Leon | Dany Akmallun | Indonesiana Prima | Adimas Satria

**19 Februari 2026**

---

<!-- _class: lead -->
# ❓ **Q&A SESSION**

**Silakan ajukan pertanyaan**

Kami siap menjawab pertanyaan tentang:
- Teknis sistem
- Implementasi
- Biaya & ROI
- Timeline
- Dan lainnya

---

<!-- _class: lead -->
# 🚀 **SELAMAT PRESENTASI!**

**Good luck, Tim UNISNU Jepara!**

You got this! 💪

---
