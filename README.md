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

| Minggu ke- | Hari & Tanggal | Aktivitas Pengerjaan | Output / Hasil | Status | Hash Commit |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Minggu 1** | Jumat, 13 Nov 2026 | Inisialisasi repositori GitHub `0255_GlowWise`, konfigurasi `.gitignore`, serta perumusan awal batasan fitur aplikasi GlowWise. | Repositori GitHub terinisialisasi, berkas `.gitignore`, dan lembar batasan fitur | ✅ Selesai | `f9b1a09` |
| **Minggu 1** | Sabtu, 14 Nov 2026 | Riset batasan teknis (100% Compose, MVVM StateFlow, PostgreSQL tanpa Room, JWT, YouCam API) serta penyusunan dokumen SRS Bab 1 sampai Bab 3. | Draf dokumen SRS Bab 1–3 & catatan arsitektur sistem | ✅ Selesai | `1f8892e` |
| **Minggu 2** | Senin, 16 Nov 2026 | Penyusunan dokumentasi proyek pada `README.md`, pencatatan identitas mahasiswa, dan perincian 10 kriteria fitur aplikasi. | Berkas dokumentasi `README.md` terstruktur | ✅ Selesai | `8adcc8c` |
| **Minggu 2** | Kamis, 19 Nov 2026 | Perancangan 5 entitas relasional CRUDS, pemodelan diagram UML (Use Case & Flowchart), serta penyempurnaan rincian fitur dan logbook pada `README.md`. | Diagram Use Case, Flowchart alur sistem, dan pembaruan logbook mingguan | ✅ Selesai | `4f1a185` |
| **Minggu 2** | Jumat, 20 Nov 2026 | Finalisasi dokumen SRS Bab 4 (Antarmuka Material 3), Bab 5 (NFR), Bab 6 (Kebutuhan Lainnya), Appendix A–C, serta pemodelan basis data konseptual ERD dan fisikal RAT. | Dokumen SRS Lengkap (Bab 1–6 & Appendix A–C), Diagram ERD, RAT, dan Matriks Relasi | ✅ Selesai | `c570a92` |
