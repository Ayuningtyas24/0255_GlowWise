# GlowWise: Aplikasi Identifikasi Masalah Kulit Wajah, Rekomendasi Kandungan Skincare, dan Jadwal Perawatan Harian Berbasis Jetpack Compose

Proyek Akhir Praktikum Pengembangan Aplikasi Mobile (PAM) 2026  
Program Studi Teknologi Informasi, Fakultas Teknik  
Universitas Muhammadiyah Yogyakarta  

---

## Identitas Mahasiswa

- **Nama:** Ayuningtyas Dyah Septiani
- **NIM:** 20240140255
- **Kelas:** E
- **Tema:** Kesehatan

---

## Fitur Aplikasi

- [x] **Authentication**  
  Implementasi login, registrasi, dan sistem autentikasi JWT (*Access Token* dan *Refresh Token*).

- [x] **Authorization**  
  Pemisahan hak akses antarmuka (*role-based UI*) untuk peran Admin dan User.

- [x] **Navigasi & Routing**  
  Navigasi multi-halaman berbasis deklaratif menggunakan Jetpack Compose Navigation (`NavHost` dan `NavController`).

- [x] **State Management**  
  Penerapan arsitektur MVVM murni menggunakan `ViewModel` dan `StateFlow`.

- [x] **Tabel / Data**  
  Penggunaan 5 entitas data relasional yang saling terhubung: `skin_scans`, `skincare_ingredients`, `skincare_products`, `daily_routines`, dan `skin_progress_logs`.

- [x] **Features (CRUDS)**  
  Penyediaan 5 fitur utama dengan fungsi CRUDS lengkap (Create, Read, Update, Delete, Search):
  1. Riwayat Scan Kulit
  2. Master Bahan Aktif
  3. Katalog Produk Skincare
  4. Rutinitas Harian (AM/PM)
  5. Jurnal Transformasi Kulit

- [x] **REST API Integration**  
  Integrasi layanan eksternal YouCam Skin Analysis API via Retrofit untuk analisis kondisi kulit wajah.

- [x] **Database**  
  Penyimpanan data terpusat menggunakan PostgreSQL via REST API backend (tanpa library Room).

- [x] **File Storage**  
  Penyimpanan dan pembacaan berkas PDF lokal untuk export serta preview laporan riwayat kulit secara offline.

- [x] **UI / UX**  
  Desain antarmuka 100% menggunakan Jetpack Compose Material 3.

---

## Logbook Progres Proyek

### Minggu 1

* **Jumat, 13 November 2026**
  * **Aktivitas:** Analisis permasalahan terkait iritasi akibat kombinasi bahan aktif skincare (*ingredients conflict*) dan identifikasi kebutuhan pengguna. Merumuskan latar belakang, ruang lingkup solusi, serta batasan fitur aplikasi GlowWise.
  * **Output:** Lembar analisis masalah dan ruang lingkup aplikasi.
  * **Status:** Selesai.

* **Sabtu, 14 November 2026**
  * **Aktivitas:** Melakukan riset teknis API pendukung analisis kulit wajah (YouCam Skin Analysis API), analisis batasan arsitektur sistem (100% Compose, MVVM StateFlow, PostgreSQL tanpa Room, JWT), serta penyusunan draf dokumen SRS Bab 1 (Pendahuluan, latar belakang, tujuan, ruang lingkup produk, dan daftar istilah baku).
  * **Output:** Draf dokumen SRS Bab 1 & catatan riset arsitektur sistem.
  * **Status:** Selesai.

### Minggu 2

* **Senin, 16 November 2026**
  * **Aktivitas:** Penyusunan dokumen Software Requirements Specification (SRS) Bab 2 (Deskripsi Umum Sistem): perumusan perspektif produk, fungsi utama sistem, karakteristik dan hak akses pengguna (Admin & User), batasan umum arsitektur teknologi, serta ringkasan kebutuhan antarmuka.
  * **Output:** Draf dokumen SRS Bab 2.
  * **Status:** Selesai.

* **Kamis, 19 November 2026**
  * **Aktivitas:** Inisialisasi repositori GitHub `0255_GlowWise` serta penyusunan dokumen SRS Bab 3 (Spesifikasi Kebutuhan Sistem): perumusan 7 kebutuhan fungsional (termasuk 5 fitur CRUDS penuh), kebutuhan non-fungsional, serta pemodelan sistem menggunakan diagram UML (Use Case Diagram, Flowchart alur sistem, dan Activity Diagram 3 jalur: Actor, Aplikasi, Database).
  * **Output:** Repositori GitHub `0255_GlowWise`, Dokumen SRS Lengkap (Bab 1–3), dan Diagram Pemodelan Sistem.
  * **Status:** Selesai.
