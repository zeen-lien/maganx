# LAPORAN PL (PRAKTIK LAPANGAN)
## ANALISIS DAN PERANCANGAN SISTEM INFORMASI PARIWISATA TERPADU DI KABUPATEN JEPARA
### POSISI: SYSTEM ANALYST & PUBLIC RELATIONS

---
*(Halaman Judul)*

**Disusun Oleh:**
**[NAMA LENGKAP KAMU]**
**NIM. [NIM KAMU]**

**PROGRAM STUDI [JURUSAN KAMU]**
**FAKULTAS [NAMA FAKULTAS]**
**[NAMA LENGKAP KAMPUS/UNIVERSITAS]**
**TAHUN 2026**

---
# LEMBAR PENGESAHAN

Judul Laporan: **ANALISIS DAN PERANCANGAN SISTEM INFORMASI PARIWISATA TERPADU DI KABUPATEN JEPARA**
Nama: **[NAMA LENGKAP KAMU]**
NIM: **[NIM KAMU]**
Program Studi: **[JURUSAN KAMU]**

Telah melaksanakan Praktik Lapangan (Magang) di Dinas Pariwisata dan Kebudayaan Kabupaten Jepara mulai tanggal [TGL MULAI] sampai dengan [TGL SELESAI].

Jepara, .............................. 2026

**Mengetahui,**

| Pembimbing Lapangan | Kepala Bidang Pemasaran | Dosen Pembimbing |
| :---: | :---: | :---: |
| *(Tanda Tangan)* | *(Tanda Tangan)* | *(Tanda Tangan)* |
| **Bapak Lukman** | **Ibu Diana** | **[Nama Dosen]** |
| NIP. [Isi NIP, minta data ke kantor] | NIP. [Isi NIP, minta data ke kantor] | NIP. [Isi NIP] |

---

# KATA PENGANTAR

Puji syukur kehadirat Allah SWT yang telah melimpahkan rahmat dan hidayah-Nya, sehingga penulis dapat menyelesaikan Laporan Praktik Lapangan (Magang) ini dengan tepat waktu. Laporan ini disusun sebagai salah satu syarat akademik dan bentuk pertanggungjawaban atas kegiatan magang yang dilaksanakan di **Dinas Pariwisata dan Kebudayaan Kabupaten Jepara (Divisi Pemasaran)**.

Selama proses penyusunan laporan ini, penulis mendapatkan banyak bimbingan, arahan, dan dukungan dari berbagai pihak. Oleh karena itu, penulis ingin menyampaikan ucapan terima kasih yang sebesar-besarnya kepada:
1.  **Ibu Diana**, selaku Kepala Bidang Pemasaran Dinas Pariwisata dan Kebudayaan Kabupaten Jepara, yang telah memberikan kesempatan dan kepercayaan kepada penulis untuk magang di lingkungan dinas.
2.  **Bapak Lukman**, selaku Pembimbing Lapangan yang dengan sabar membimbing dan berbagi ilmu mengenai manajemen proyek dan strategi komunikasi di lapangan.
3.  Seluruh staf dan karyawan Dinas Pariwisata yang telah membantu mempermudah akses data.
4.  Rekan-rekan satu tim magang (Frontend, Backend, dan Dokumentasi) atas kerjasama yang solid dalam mengembangkan sistem informasi ini.

Penulis menyadari bahwa laporan ini masih memiliki kekurangan. Kritik dan saran yang membangun sangat diharapkan demi penyempurnaan di masa mendatang.

Jepara, 13 Februari 2026

**Penulis**

---

# DAFTAR ISI
*(Silakan generate otomatis di Word)*
1.  HALAMAN JUDUL
2.  LEMBAR PENGESAHAN
3.  KATA PENGANTAR
4.  DAFTAR ISI
5.  DAFTAR GAMBAR
6.  DAFTAR TABEL
7.  BAB I PENDAHULUAN
8.  BAB II LANDASAN TEORI
9.  BAB III METODOLOGI PENELITIAN
10. BAB IV HASIL DAN PEMBAHASAN
11. BAB V PENUTUP
12. DAFTAR PUSTAKA
13. LAMPIRAN

---

# BAB I
# PENDAHULUAN

## 1.1 Latar Belakang
Kabupaten Jepara dikenal sebagai salah satu destinasi wisata unggulan di Jawa Tengah, dengan potensi wisata bahari (Karimunjawa, Pantai Bandengan, Pantai Kartini), wisata sejarah (Benteng Portugis, Museum R.A. Kartini), hingga wisata religi. Berdasarkan data Dinas Pariwisata tahun 2025, tercatat lebih dari 78 destinasi wisata yang tersebar di berbagai kecamatan.

Namun, pengelolaan informasi mengenai puluhan destinasi tersebut masih menghadapi kendala, terutama dalam hal **sentralisasi data**. Informasi mengenai jam operasional, harga tiket terbaru, dan fasilitas pendukung seringkali tersebar di berbagai platform media sosial yang tidak terintegrasi, atau bahkan masih menggunakan metode manual (brosur fisik). Hal ini menyulitkan wisatawan untuk mendapatkan informasi yang akurat dan *real-time*.

Sebagai upaya mendukung program **Smart City** di Kabupaten Jepara, diperlukan sebuah sistem informasi pariwisata terpadu yang dapat diakses secara digital. Dalam pengembangan sistem ini, peran *System Analyst* sangat krusial untuk menjembatani kebutuhan bisnis (Business Requirements) dari pihak Dinas dengan solusi teknis (Technical Solutions) yang akan dikerjakan oleh tim pengembang.

## 1.2 Rumusan Masalah
Berdasarkan latar belakang di atas, rumusan masalah dalam kegiatan magang ini adalah:
1.  Bagaimana merancang sistem informasi yang dapat memetakan 78+ destinasi wisata di Jepara secara digital?
2.  Bagaimana alur validasi data lapangan agar informasi yang ditampilkan di website (seperti harga tiket) selalu akurat?
3.  Fitur apa saja yang dibutuhkan oleh Dinas Pariwisata untuk mempermudah promosi event tahunan?

## 1.3 Batasan Masalah
Agar pembahasan lebih terarah, penulis membatasi ruang lingkup sebagai berikut:
1.  Analisis sistem berfokus pada **Modul Destinasi Wisata**, **Peta GIS**, dan **Kalender Event**.
2.  Data yang diolah adalah data tahun 2025-2026 yang didapat dari survei lapangan dan arsip Dinas.
3.  Perancangan sistem menggunakan standar UML (*Unified Modeling Language*) dan Database diagram.

## 1.4 Tujuan Magang
1.  **Bagi Mahasiswa:** Mengimplementasikan ilmu Analisis Sistem (*System Analysis*) dan Perancangan Basis Data (*Database Design*) dalam proyek nyata.
2.  **Bagi Instansi:** Mendapatkan rancangan cetak biru (*blueprint*) sistem informasi yang siap dikembangkan, serta aset data wisata yang telah tervalidasi.

## 1.5 Manfaat
1.  Mempermudah wisatawan domestik dan mancanegara dalam mencari referensi wisata di Jepara.
2.  Meningkatkan efisiensi kerja staf pemasaran dalam mengelola konten promosi.
3.  Menjadikan dokumentasi digital pariwisata Jepara lebih terstruktur dan *sustainable*.

---

# BAB II
# LANDASAN TEORI

## 2.1 System Analyst
System Analyst adalah profesi yang bertugas menganalisis, merancang, dan mengimplementasikan sistem informasi. Seorang analis bertanggung jawab menerjemahkan kebutuhan pengguna menjadi spesifikasi teknis yang dapat dimengerti oleh programmer. Dalam proyek ini, analis juga berperan sebagai jembatan komunikasi (*Public Relations*) saat melakukan survei lapangan.

## 2.2 SDLC (System Development Life Cycle) - Model Agile
Pengembangan sistem ini menggunakan metode **Agile Development**, yang mengutamakan fleksibilitas dan iterasi cepat. Tahapan yang dilakukan meliputi:
1.  *Requirement Gathering* (Pengumpulan Kebutuhan)
2.  *Design* (Perancangan)
3.  *Development* (Pengembangan - Backend & Frontend)
4.  *Testing* (Pengujian)
5.  *Deployment* (Penerapan)

## 2.3 UML (Unified Modeling Language)
UML digunakan sebagai standar visualisasi perancangan sistem. Diagram yang digunakan dalam laporan ini antara lain:
*   **Use Case Diagram:** Menggambarkan interaksi antara aktor (user/admin) dengan sistem.
*   **Activity Diagram:** Menggambarkan alur kerja (workflow) proses bisnis.
*   **Entity Relationship Diagram (ERD):** Menggambarkan struktur database dan relasi antar tabel.

---

# BAB III
# METODOLOGI PELAKSANAAN

## 3.1 Metode Pengumpulan Data
Untuk mendapatkan data yang akurat, penulis menggunakan tiga metode utama:

### 1. Observasi Lapangan (*Field Observation*)
Penulis terjun langsung ke lokasi wisata prioritas seperti Pantai Bandengan, Pantai Kartini, dan Benteng Portugis.
*   **Aktivitas:** Mengambil titik koordinat GPS, mencatat fasilitas yang tersedia (toilet, mushola, parkir), dan validasi harga tiket masuk.
*   **Hasil:** Terkumpulnya data fisik yang kemudian didigitalkan menjadi format JSON (`data_wisata_jepara.json`).

### 2. Wawancara (*Interview*)
Melakukan tanya jawab dengan stakeholder terkait:
*   **Ibu Diana (Kabid Pemasaran):** Untuk mengetahui visi misi promosi wisata tahun 2026.
*   **Pengelola Wisata:** Untuk memastikan jam operasional dan kontak pengelola yang bisa dihubungi.

### 3. Studi Pustaka (*Literature Study*)
Mempelajari dokumen-dokumen internal Dinas, seperti "Calendar of Event 2026", serta referensi teknis mengenai pengembangan Geographic Information System (GIS).

## 3.2 Alat Bantu Perancangan (Tools)
Dalam melaksanakan tugasnya, penulis menggunakan perangkat lunak berikut:
1.  **Visual Studio Code:** Untuk mengelola file JSON dan Markdown laporan.
2.  **Laragon:** Sebagai web server lokal untuk menjalankan framework Laravel.
3.  **Draw.io / StarUML:** Untuk membuat diagram UML dan ERD.
4.  **Google Maps:** Untuk verifikasi koordinat lokasi wisata.

---

# BAB IV
# HASIL DAN PEMBAHASAN

## 4.1 Analisis Sistem Berjalan
Saat ini, promosi wisata di Kabupaten Jepara masih mengandalkan beberapa kanal terpisah seperti Instagram, Facebook, dan brosur cetak.
*   **Kelemahan:** Informasi sering tenggelam (tertumpuk postingan baru), sulit dicari kembali, dan tidak adanya fitur peta interaktif yang memandu wisatawan ke lokasi.
*   **Kebutuhan:** Diperlukan satu portal web terpusat yang menjadi "Single Source of Truth" bagi wisatawan.

## 4.2 Analisis Kebutuhan Sistem (System Requirements)
Berdasarkan wawancara dengan mentor (Bapak Lukman), berikut adalah spesifikasi kebutuhan sistem yang harus dibangun:

### A. Kebutuhan Fungsional (Functional Requirements)
1.  **Manajemen Destinasi:** Admin Dinas dapat menambah (Create), membaca (Read), mengubah (Update), dan menghapus (Delete) data wisata.
2.  **Peta GIS:** Sistem harus menampilkan sebaran lokasi wisata dalam bentuk peta digital dengan *marker* yang bisa diklik.
3.  **Kalender Event:** Sistem menampilkan jadwal event budaya dalam tampilan kalender bulanan.
4.  **Kategorisasi:** Wisatawan dapat memfilter destinasi berdasarkan kategori (Wisata Alam, Religi, Kuliner, Buatan).
5.  **Multibahasa:** Sistem mendukung Bahasa Indonesia dan Inggris untuk menjangkau wisatawan asing.

### B. Kebutuhan Non-Fungsional (Non-Functional Requirements)
1.  **Usability:** Antarmuka harus responsif (bisa dibuka di HP) dan mudah digunakan (*User Friendly*).
2.  **Performance:** Loading peta tidak boleh lebih dari 3 detik.
3.  **Security:** Akses Admin harus dilindungi dengan login yang aman.

## 4.3 Perancangan Sistem (System Design)

### 4.3.1 Use Case Diagram
Diagram ini menggambarkan siapa saja yang berinteraksi dengan sistem dan apa yang bisa mereka lakukan.

<!-- [SILAKAN MASUKKAN GAMBAR USE CASE DIAGRAM DI SINI] -->

**Deskripsi Aktor:**
1.  **Admin Dinas:** Memiliki hak akses penuh untuk mengelola data master (Wisata, Event, Kategori) dan melihat statistik pengunjung.
2.  **Wisatawan (Guest):** Pengguna umum yang hanya bisa melihat informasi, menggunakan peta, dan melakukan pencarian.

### 4.3.2 Activity Diagram
Berikut adalah alur aktivitas utama dalam sistem:

**A. Activity Diagram: Input Data Wisata (Admin)**
1.  Admin Login ke Dashboard.
2.  Memilih menu "Data Wisata".
3.  Klik "Tambah Wisata Baru".
4.  Admin mengisi formulir (Nama, Deskripsi, Lokasi, Upload Foto).
5.  Sistem memvalidasi kelengkapan data.
6.  Jika valid, data disimpan ke Database.
7.  Sistem menampilkan notifikasi "Berhasil Disimpan".

<!-- [SILAKAN MASUKKAN GAMBAR ACTIVITY DIAGRAM DI SINI] -->

### 4.3.3 Entity Relationship Diagram (ERD) - Struktur Database
Perancangan basis data adalah tahap kritikal. Berikut adalah skema database yang telah dirancang dan diimplementasikan oleh tim Backend:

**1. Tabel `users` (Pengguna)**
*   Menyimpan data akun Admin Dinas.
*   Key: `id`, `name`, `email`, `password`.

**2. Tabel `categories` (Kategori Wisata)**
*   Menyimpan jenis-jenis wisata (contoh: Wisata Alam, Wisata Religi).
*   Key: `id`, `name` (Varchar), `slug`.

**3. Tabel `places` (Destinasi Wisata)**
Ini adalah tabel utama yang menyimpan 78+ data wisata.
*   `id` (Primary Key).
*   `category_id` (Foreign Key): Menghubungkan ke tabel categories.
*   `name`: Nama Objek Wisata.
*   `slug`: URL ramah SEO (contoh: pantai-kartini).
*   `description`: Penjelasan detail wisata.
*   `address`: Alamat lengkap.
*   `latitude` & `longitude`: Koordinat untuk Peta GIS.
*   `facilities`: Kolom tipe JSON untuk menyimpan daftar fasilitas (Toilet, Parkir, Mushola).
*   `ticket_price`: Informasi harga tiket.

**4. Tabel `events` (Agenda Budaya)**
*   Menyimpan jadwal festival seperti Pesta Lomban dan Perang Obor.
*   Key: `title`, `description`, `start_date`, `location`.

<!-- [SILAKAN MASUKKAN GAMBAR ERD / RELASI TABEL API DI SINI] -->

## 4.4 Implementasi dan Hasil Analisis Data
Sebagai System Analyst, penulis juga bertugas memvalidasi data sebelum masuk ke sistem. Berikut adalah ringkasan aset data yang berhasil dikumpulkan:

| No | Kategori Data | Jumlah Entitas | Sumber Data | Keterangan |
| :-- | :--- | :---: | :--- | :--- |
| 1 | Destinasi Wisata | 78 Lokasi | Survei Lapangan | Data lengkap (Foto + Desc) |
| 2 | Event Budaya | 73 Agenda | Bidang Pemasaran | Kalender 2026 |
| 3 | Data Akomodasi | 15 Hotel | Asosiasi PHRI | Data Pendukung |

*(Data lengkap terlampir pada dokumen JSON di folder `Maganx`)*

## 4.5 Pengujian Sistem (Testing)
Pengujian dilakukan menggunakan metode **Black Box Testing** untuk memastikan fungsi input-output berjalan sesuai rancangan.

**Tabel Hasil Pengujian:**
| No | Skenario Pengujian | Hasil yang Diharapkan | Hasil Nyata | Kesimpulan |
| :-- | :--- | :--- | :--- | :--- |
| 1 | Login Admin dengan kredensial salah | Sistem menolak dan muncul pesan error | Muncul pesan "Invalid credentials" | **BERHASIL** |
| 2 | Input data wisata tanpa nama | Sistem menolak penyimpanan | Form tidak bisa disubmit (Required) | **BERHASIL** |
| 3 | Filter Peta berdasarkan kategori "Alam" | Peta hanya menampilkan marker wisata alam | Marker lain hilang, sisa wisata alam | **BERHASIL** |
| 4 | Akses halaman detail wisata | Muncul foto, deskripsi, dan info tiket | Semua data tampil sesuai input | **BERHASIL** |

---

# BAB V
# PENUTUP

## 5.1 Kesimpulan
Berdasarkan kegiatan magang yang telah dilakukan, dapat disimpulkan bahwa:
1.  Peran System Analyst sangat vital dalam menerjemahkan kebutuhan Dinas Pariwisata menjadi spesifikasi teknis bagi Tim Developer.
2.  Sistem Informasi Pariwisata yang dibangun telah berhasil mengintegrasikan 78 destinasi wisata ke dalam satu platform digital berbasis Web GIS.
3.  Validasi data lapangan yang dilakukan penulis menjamin akurasi informasi yang ditampilkan kepada wisatawan, meminimalisir kesalahan informasi di masa depan.

## 5.2 Saran
1.  **Pengembangan Mobile App:** Di masa depan, disarankan sistem ini dikembangkan menjadi aplikasi Android/iOS agar bisa memberikan notifikasi *real-time* kepada wisatawan.
2.  **Fitur E-Ticketing:** Perluasan fitur untuk pemesanan tiket online secara langsung guna mengurangi antrean di lokasi wisata.
3.  **Update Berkala:** Dinas Pariwisata perlu menunjuk admin khusus yang bertugas melakukan update konten minimal sebulan sekali.

---

# DAFTAR PUSTAKA
1.  Pressman, R. S. (2019). *Software Engineering: A Practitioner's Approach*. McGraw-Hill Education.
2.  Satzinger, J. W., Jackson, R. B., & Burd, S. D. (2016). *Systems Analysis and Design in a Changing World*. Cengage Learning.
3.  Dokumen Rencana Induk Pembangunan Kepariwisataan Daerah (RIPPARDA) Kabupaten Jepara 2020-2025.

---

# LAMPIRAN
*(Bagian ini disediakan untuk menyisipkan bukti fisik. Silakan copy-paste foto/scan Anda di halaman ini)*

**Lampiran 1: Surat Penerimaan Magang**
<!-- [PASTE FOTO SURAT DI SINI] -->

**Lampiran 2: Dokumentasi Wawancara dengan Kabid Pemasaran**
<!-- [PASTE FOTO WAWANCARA DI SINI] -->

**Lampiran 3: Foto Kegiatan Survei Lapangan (Pantai Bandengan & Benteng Portugis)**
<!-- [PASTE FOTO KEGIATAN LAPANGAN DI SINI] -->

**Lampiran 4: Logbook Harian / Daftar Hadir**
<!-- [PASTE SCAN LOGBOOK DI SINI] -->

**Lampiran 5: Cuplikan Data JSON (Hasil Kerja Analyst)**
<!-- [PASTE SCREENSHOT KODE JSON DI SINI] -->
