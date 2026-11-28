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
  Penggunaan 5 entitas data relasional yang saling terhubung: `skin_scans`, `skincare_ingredients`, `skincare_products`, `daily_routines`, dan `product_reviews`.

- [x] **Features (CRUDS)**  
  Penyediaan 5 fitur utama dengan fungsi CRUDS lengkap (Create, Read, Update, Delete, Search):
  1. Riwayat Scan Kulit
  2. Master Bahan Aktif
  3. Katalog Produk Skincare
  4. Rutinitas Harian (AM/PM)
  5. Ulasan & Evaluasi Produk Skincare (Product Reviews)

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

Berikut adalah linimasa pengembangan proyek **GlowWise** berdasarkan riwayat pengerjaan dan *commit* GitHub:

### Minggu 1 (9 November 2026 – 15 November 2026)

*Fokus: Analisis Permasalahan, Riset Arsitektur Sistem & Draf Awal SRS Bab 1*

- *Jumat, 13 November 2026*
  - Melakukan analisis permasalahan dan perumusan ruang lingkup aplikasi **GlowWise**:
    - **Identifikasi Masalah:** Analisis risiko iritasi kulit akibat kombinasi bahan aktif kosmetik yang kontraindikatif (*ingredients conflict*) serta kebutuhan pengguna awam dan admin katalog.
    - **Pemetaan 7 Fitur Utama:** Perumusan ruang lingkup fitur Autentikasi, Scan Wajah, Bahan Aktif & *Conflict Checker*, Katalog Produk, Jadwal Rutinitas AM/PM, Ulasan Produk, dan Ekspor PDF Lokal.
- *Sabtu, 14 November 2026*
  - Melakukan riset batasan teknis arsitektur dan penyusunan draf awal **SRS Bab 1**:
    - **Batasan Teknis:** 100% Jetpack Compose tanpa XML, pola MVVM (`ViewModel` + `StateFlow`), PostgreSQL terpusat via REST API tanpa Room, JWT *Access/Refresh Token* untuk multi-role Admin & User, integrasi YouCam Skin Analysis API, serta Android *Scoped Storage*.
    - **Draf SRS Bab 1:** Penyusunan pendahuluan (*Purpose*), konvensi penulisan, ruang lingkup proyek, dan glosarium istilah awal.

### Minggu 2 (16 November 2026 – 22 November 2026)

*Fokus: Penyusunan Dokumen SRS Lengkap, Pemodelan UML & Basis Data, serta Inisialisasi Proyek Android*

- *Senin, 16 November 2026*
  - Penyusunan draf **SRS Bab 2 (*Overall Description*)**:
    - Perumusan perspektif produk *client-server*, pemetaan 7 fitur sistem (`SF-01` s.d. `SF-07`), karakteristik kelas pengguna Admin dan User, lingkungan operasi Android, serta batasan desain dan asumsi API eksternal.
- *Kamis, 19 November 2026*
  - Inisialisasi repositori GitHub, dokumentasi proyek & penyusunan **SRS Bab 1–3** (`f9b1a09`, `1f8892e`, `8adcc8c`, `4f1a185`):
    - **Repositori & Dokumentasi:** Inisialisasi repositori `0255_GlowWise`, konfigurasi `.gitignore`, serta penyusunan identitas mahasiswa dan daftar fitur aplikasi pada `README.md`.
    - **SRS Bab 1–3 & UML:** Penyusunan rincian kebutuhan fungsional (`FR-AUTH` hingga `FR-FILE`) serta pemodelan awal Use Case Diagram dan Flowchart sistem.
- *Jumat, 20 November 2026*
  - Finalisasi **SRS Bab 4–6, Appendix A–C & Pemodelan Basis Data** (`79f2041`):
    - **Bab 4–6 & Lampiran:** Penyusunan Antarmuka Eksternal Material 3, integrasi Retrofit/OkHttp & HTTPS JSON, Kebutuhan Non-Fungsional (NFR), Penafian Medis & Privasi Data, serta Appendix A–C (Glosarium, Model Analisis, Daftar Isu).
    - **Pemodelan Basis Data:** Penyusunan diagram konseptual ERD, fisikal Relasi Antar Tabel (RAT), dan Matriks Relasi.
- *Sabtu, 21 November 2026*
  - Inisialisasi proyek Android Studio berbasis **Jetpack Compose** (`9a53a07`):
    - **Struktur Proyek & Gradle:** Konfigurasi `build.gradle.kts`, `gradle/libs.versions.toml`, `gradle.properties`, dan `AndroidManifest.xml` pada package `com.example.a0255_glowwise`.
    - **Tema Material 3:** Penyiapan dasar tema antarmuka (`Color.kt`, `Theme.kt`, `Type.kt`) dan sumber daya aplikasi (`res/`).

### Minggu 3 (23 November 2026 – 29 November 2026)

*Fokus: Penyesuaian Entitas `product_reviews`, Pemisahan Diagram CRUDS Mandiri & Finalisasi SRS*

- *Rabu, 25 November 2026*
  - Penyesuaian spesifikasi entitas CRUDS ke-5 menjadi **`product_reviews`** (`2485ba1`):
    - Mengubah entitas ke-5 pada `README.md` dari `skin_progress_logs` menjadi `product_reviews` (Ulasan & Evaluasi Produk Skincare) agar selaras dengan 5 entitas utama (`skin_scans`, `skincare_ingredients`, `skincare_products`, `daily_routines`, `product_reviews`).
- *Kamis, 26 November 2026 – Sabtu, 28 November 2026*
  - Revisi menyeluruh pemodelan diagram SRS dan finalisasi dokumen `SRS_GlowWise.md` serta `SRS_GlowWise.docx`:
    - **Diagram CRUDS Mandiri (Revisi Asdos):** Pemisahan Flowchart dan Activity Diagram menjadi diagram mandiri per aksi CRUDS (*Create, Read, Update, Delete, Search*) untuk fitur `SF-01` s.d. `SF-07` dengan aturan satu titik akhir (`Selesai`/`stop`).
    - **Pembaruan ERD & RAT (6 Tabel):** Memasukkan entitas `product_reviews` dan memperjelas relasi antar tabel (`users`, `skin_scans`, `skincare_ingredients`, `skincare_products`, `daily_routines`, `product_reviews`) beserta aturan integritas referensial (`ON DELETE CASCADE` dan `ON DELETE RESTRICT`).
    - **Finalisasi Dokumen SRS:** Penyelarasan seluruh Bab 1–6 dan Lampiran A–C beserta tabel matriks kebutuhan fungsional ke dalam dokumen siap pakai.

