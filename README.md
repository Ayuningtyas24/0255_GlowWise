# 📱 GlowWise - Skincare Routine & Skin Health Assistant
> **Proyek Akhir Pengembangan Aplikasi Mobile (PAM) 2026**  
> Program Studi Informatika - Fakultas Teknik - Universitas Muhammadiyah Yogyakarta  
> **Nama Repository:** `0255_GlowWise`

---

## 👤 Identitas Mahasiswa
* **Nama Lengkap:** Ayuningtyas
* **NIM:** [NIM Lengkap Anda, misal: 20220140255]
* **Kelas:** [Kelas PAM Anda]
* **Dosen Pengampu:** Tim Dosen PAM 2026
* **Tema Proyek:** Kesehatan (*Skin Problem Identification, Conflict Checker & Skincare Routine*)

---

## 📋 Status Pemenuhan Persyaratan Minimal Aplikasi (Pedoman Bagian D)
> *Sesuai Petunjuk Teknis E.5: Mahasiswa wajib memperbarui status fitur di README GitHub selama pengerjaan proyek.*

| No | Kategori Persyaratan | Ketentuan Minimal Pedoman | Implementasi pada GlowWise | Status Fitur |
| :---: | :--- | :--- | :--- | :---: |
| **1** | **Authentication** | Login, Register, Access Token (JWT), Refresh Token. | JWT berpasangan (*Access Token* 15 mnt, *Refresh Token* 7 hari), enkripsi password BCrypt, auto-refresh via OkHttp Authenticator. | **SRS Selesai**<br>*(Siap Koding)* |
| **2** | **Authorization** | Role-based UI atau hak akses terbatas (minimal 1 peran). | Pemisahan antarmuka reaktif berbasis peran: **Admin Pakar** (kelola master bahan & katalog) vs **User** (data personal). | **SRS Selesai**<br>*(Siap Koding)* |
| **3** | **Navigasi & Routing** | Multi-page app HANYA menggunakan **Navigator Compose**. | Navigasi deklaratif `NavHost` & `NavController` dengan *Bottom Navigation Bar* dan *Scaffold Material 3*. | **SRS Selesai**<br>*(Siap Koding)* |
| **4** | **State Management** | Wajib menggunakan **MVVM**. | Arsitektur MVVM murni (`ViewModel` + `StateFlow` + `Repository Pattern`) dengan *Unidirectional Data Flow* (UDF). | **SRS Selesai**<br>*(Siap Koding)* |
| **5** | **Tabel / Data** | Minimal 4 entitas data utama saling terhubung (dinamis). | Menggunakan **5 Entitas Relasional Terhubung**: `skin_scans`, `skincare_ingredients`, `skincare_products`, `daily_routines`, dan `skin_progress_logs`. | **SRS Selesai**<br>*(Siap Koding)* |
| **6** | **Features (CRUDS)** | Minimal 5 fitur dengan method **CRUDS penuh** (Create, Read, Update, Delete, Search). | **5 Fitur CRUDS Penuh**:<br>1. Riwayat Scan Kulit (`FR-SCAN`)<br>2. Master Bahan Aktif (`FR-INGR`)<br>3. Katalog Produk (`FR-PROD`)<br>4. Rutinitas Harian AM/PM (`FR-ROUT`)<br>5. Jurnal Transformasi Kulit (`FR-LOG`) | **SRS Selesai**<br>*(Siap Koding)* |
| **7** | **REST API Integration** | Request dan parsing JSON dari REST API. | Integrasi **YouCam Skin Analysis API (Perfect Corp)** untuk analisis 28+ klinis kulit wajah via HTTP POST Multipart & Retrofit2. | **SRS Selesai**<br>*(Siap Koding)* |
| **8** | **Database** | Minimal MySQL/Postgres. **Room dilarang**. | **PostgreSQL Terpusat** via REST API Backend (bebas dari library Room lokal sesuai larangan pedoman). | **SRS Selesai**<br>*(Siap Koding)* |
| **9** | **File Storage** | Simpan dan baca file lokal. | Pemanfaatan `android.graphics.pdf.PdfDocument` dan **Android Scoped Storage** untuk *export* & *view* berkas PDF secara *offline*. | **SRS Selesai**<br>*(Siap Koding)* |
| **10** | **UI / UX** | Penerapan **100% Jetpack Compose**. | Antarmuka deklaratif Material Design 3 (tanpa XML sama sekali), palet warna kesehatan (Teal, Cyan, Rose Coral). | **SRS Selesai**<br>*(Siap Koding)* |

---

## 📌 Logbook Progres Mingguan (Ketentuan Teknis C.1 & Penilaian F.3)
> *Sesuai Ketentuan Teknis C.1: Wajib ada update progress setiap minggu minimal 1 progress ke dalam GitHub yang dicantumkan ke dalam README dan wajib commit bertahap (minimal 30 commit).*

| Minggu / Sesi | Hari & Tanggal | Rincian Aktivitas Pengembangan | Luaran (*Deliverables*) | Status |
| :---: | :---: | :--- | :--- | :---: |
| **Minggu 1** | **Jumat, 13 Nov 2026** | **Inisiasi Proyek & Tema Kesehatan:**<br>- Menetapkan tema kesehatan kulit wajah dan nama aplikasi **GlowWise**.<br>- Merumuskan masalah iritasi akibat salah racik bahan aktif (*active ingredients conflict*).<br>- Menyusun ide solusi asisten pemilihan skincare dan identifikasi masalah wajah. | - Konsep Ide Proyek<br>- Lembar Rumusan Masalah |  **Selesai** |
| **Minggu 1** | **Sabtu, 14 Nov 2026** | **Riset API & Pembatasan Arsitektur:**<br>- Riset teknis YouCam Skin Analysis API (Perfect Corp).<br>- Menetapkan batasan teknologi: 100% Compose, MVVM StateFlow, PostgreSQL (No Room), JWT, Scoped Storage.<br>- Inisiasi repositori GitHub `[4NIMBelakang]_GlowWise`. | - Repositori GitHub<br>- Dokumen Arsitektur Awal |  **Selesai** |
| **Minggu 2** | **Kamis, 19 Nov 2026**<br>*(Hari Ini)* | **Penyusunan Dokumen SRS (Bab 1, Bab 2, dan Bab 3):**<br>- **Bab 1:** Tujuan, ruang lingkup, referensi IEEE 830, konvensi kodefikasi (`FR-[MODUL]-[NO]`), dan 27 singkatan istilah baku.<br>- **Bab 2:** Perspektif produk, fungsi umum sistem, 6 batasan arsitektur mutlak, kelas pengguna (*Admin* vs *User*), dan dokumentasi pengguna (*User Documentation*).<br>- **Bab 3:** Menyusun 7 fitur sistem lengkap dengan spesifikasi CRUDS penuh.<br>- **Diagram Pemodelan UML:**<br>&nbsp;&nbsp;* Membuat **Use Case Diagram (List Feature)**.<br>&nbsp;&nbsp;* Membuat **Flowchart alur sistem** per fitur.<br>&nbsp;&nbsp;* Membuat **Activity Diagram format 3 Jalur (Actor, Aplikasi, Database)** berbasis kode PlantUML.<br>- Melengkapi rincian penanganan kondisi galat (*error handling*). | - Berkas SRS Bab 1 Final<br>- Berkas SRS Bab 2 Final<br>- Berkas SRS Bab 3 Final<br>- Diagram Use Case PlantUML<br>- 7 Flowchart Sistem<br>- 7 Activity Diagram 3-Line |  **Selesai** |

---

## 🛠️ Panduan Menjalankan Proyek (Setup & Run)
*(Akan diperbarui bertahap saat masuk tahap pengkodean Android Studio)*
* Clone repositori:
  ```bash
  git clone https://github.com/Ayuningtyas24/0255_GlowWise.git
  ```
* Buka proyek menggunakan **Android Studio Ladybug / Koala (versi terbaru)**.
* Pastikan SDK Platform Android minimal API 26 (Android 8.0 Oreo) terpasang.
