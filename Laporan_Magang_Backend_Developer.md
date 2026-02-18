# LAPORAN PL (PRAKTIK LAPANGAN)
## PENGEMBANGAN BACKEND SISTEM INFORMASI PARIWISATA (LARAVEL FRAMEWORK)
### POSISI: BACKEND DEVELOPER

---
*(Halaman Judul)*

**Disusun Oleh:**
**[NAMA REKAN BACKEND]**
**NIM. [NIM REKAN]**

**DIVISI PEMASARAN**
**DINAS PARIWISATA DAN KEBUDAYAAN KABUPATEN JEPARA**
**TAHUN 2026**

---
# KATA PENGANTAR
*(Standar)*

---
# DAFTAR ISI
1.  **BAB I: PENDAHULUAN** (Fokus ke kebutuhan server-side yang handal & aman)
2.  **BAB II: LANDASAN TEORI**
    *   Framework MVC (Model-View-Controller)
    *   Laravel 10 Features (Eloquent, Blade, Artisan)
    *   RESTful API Service
    *   Database Relasional (MySQL)
3.  **BAB III: ANALISIS & PERANCANGAN SISTEM** (Teknis Database)
4.  **BAB IV: IMPLEMENTASI SISTEM (CODING)**
    *   Struktur Folder & Konfigurasi
    *   Migrasi Database (Migrations)
    *   Implementasi Model & Relations
    *   Pembuatan API Endpoints
    *   Integrasi Payment Gateway (Midtrans)
5.  **BAB V: PENUTUP**

---

# BAB III: PERANCANGAN DATABASE (SCHEMA)
## 3.1 Struktur Tabel (Migrations)
Berdasarkan analisis kebutuhan, berikut skema database utama yang dibangun:

### A. Tabel Core (`Places` & `Events`)
Sistem menggunakan tabel `places` untuk menyimpan 78+ destinasi wisata.
```php
Schema::create('places', function (Blueprint $table) {
    $table->id();
    $table->foreignId('category_id')->constrained();
    $table->string('name');
    $table->string('slug')->unique();
    $table->text('description');
    $table->string('address');
    $table->decimal('latitude', 10, 8)->nullable();
    $table->decimal('longitude', 11, 8)->nullable();
    $table->json('facilities')->nullable(); // Menyimpan array fasilitas
    $table->json('rides')->nullable(); // Menyimpan array wahana
    $table->timestamps();
});
```
*   **Optimasi:** Penggunaan tipe data `JSON` untuk kolom `facilities` dan `rides` memungkinkan fleksibilitas data tanpa perlu membuat tabel pivot yang terlalu banyak (Denormalisasi terkontrol).

### B. Tabel Transaksi (`Tickets` & `Transactions`)
Untuk fitur E-Ticketing, relasi `One-to-Many` diterapkan antara `User` dan `Transaction`.
*   `tickets`: Master data tiket per wisata.
*   `ticket_orders`: Menyimpan history pembelian user.

## 3.2 Relasi Antar Model (Eloquent ORM)
Implementasi relasi pada Model Laravel:
**File: `app/Models/Place.php`**
```php
class Place extends Model {
    protected $casts = [
        'facilities' => 'array', // Auto-convert JSON to Array PHP
        'rides' => 'array'
    ];

    public function category() {
        return $this->belongsTo(Category::class);
    }
    
    public function tickets() {
        return $this->hasMany(Ticket::class);
    }
}
```

---

# BAB IV: IMPLEMENTASI BACKEND
## 4.1 Routing System (`web.php` & `api.php`)
Kami memisahkan route untuk `Public` (Akses Wisatawan) dan `Admin` (Dashboard Dinas).
*   **Middleware:** Digunakan `auth:admin` untuk memproteksi halaman pengelolaan data.
*   **Route Groups:** Grouping route berdasarkan prefix `/admin` dan `/api` untuk kerapian kode.

## 4.2 Logic Controller
**PlaceController** bertugas menangani logika bisnis:
1.  **Filtering:** Menggunakan `Query Scopes` untuk filter berdasarkan kategori dan pencarian nama.
2.  **GeoJSON API:** Membuat endpoint khusus `/places.geojson` yang mengembalikan data format GeoJSON untuk dikonsumsi library LeafletJS di Frontend.

## 4.3 Integrasi Payment Gateway
Backend mengimplementasikan **Midtrans Snap API** untuk fitur pembayaran tiket online.
*   **Webhook Handler:** Dibuat controller khusus untuk menangani *callback* status pembayaran dari Midtrans (Pending -> Success/Failure) secara realtime tanpa input manual.

## 4.4 Keamanan Sistem (Security)
*   **CSRF Protection:** Semua form input dilindungi token CSRF bawaan Laravel.
*   **SQL Injection Prevention:** Penggunaan Eloquent ORM secara otomatis memfilter input berbahaya.
*   **Data Validation:** Implementasi `FormRequest` class untuk memvalidasi input sebelum masuk database (misal: format tanggal harus valid, email harus unik).

---

# BAB V: KESIMPULAN TEKNIS
Pengembangan backend menggunakan Laravel 10 terbukti efisien untuk menangani kompleksitas relasi data pariwisata. Fitur Eloquent dan Migrations mempermudah perubahan struktur database di tengah jalan (Agile).

**Rekomendasi:**
Perlu diterapkan *Caching* (Redis) untuk endpoint API data wisata, mengingat data tersebut jarang berubah namun sering diakses (High Read Traffic).

---
# LAMPIRAN
1.  **Snippets Kode (Controller Utama)**
2.  **Screenshot Database (phpMyAdmin)**
3.  **Dokumentasi API (Postman Collection)**

