# Scholarship Management System (SPK Penerima Beasiswa)

Sistem Pendukung Keputusan (SPK) untuk seleksi penerima beasiswa berbasis web. Aplikasi ini dirancang untuk membantu pihak sekolah atau institusi dalam mengelola data pemohon beasiswa dan melakukan seleksi berdasarkan kriteria yang ditentukan.

## Fitur Utama
- **Manajemen Data**: Pengelolaan data siswa, kriteria beasiswa, dan bobot penilaian.
- **Seleksi Otomatis**: Perhitungan skor berdasarkan metode SPK (misalnya SAW/AHP/Profile Matching) untuk menentukan kandidat terbaik.
- **Laporan**: Cetak hasil seleksi dan laporan penerima beasiswa.
- **Multi-Role**: Akses berbeda untuk Admin, Petugas, dan Siswa.

## Teknologi & Dependencies

### Backend
- **Framework**: Laravel 8.x
- **Bahasa**: PHP >= 7.3 (Kompatibel dengan PHP 8.x)
- **Database**: MySQL

**Dependencies Utama (`composer.json`):**
- `laravel/framework`: ^8.0
- `guzzlehttp/guzzle`: ^7.0.1
- `fruitcake/laravel-cors`: ^2.0
- `fideloper/proxy`: ^4.2

### Frontend
- **Framework**: Vue.js (via Laravel Mix) / Blade Templates
- **Styling**: CSS / Bootstrap (Template Admin)
- **Build Tool**: Laravel Mix (Webpack)

**Dependencies Utama (`package.json`):**
- `laravel-mix`: ^5.0.1
- `axios`: ^0.19
- `lodash`: ^4.17.19

## Persyaratan Sistem
- PHP >= 7.3
- Composer
- Node.js & NPM
- MySQL Database

## Instalasi

1. **Clone Repository**
   ```bash
   git clone https://github.com/IkidMasmu17/ScholarshipManagement.git
   cd ScholarshipManagement
   ```

2. **Install Backend Dependencies**
   ```bash
   composer install
   ```

3. **Install Frontend Dependencies**
   ```bash
   npm install
   npm run dev
   ```

4. **Konfigurasi Environment**
   - Copy file `.env.example` menjadi `.env`.
   - Atur konfigurasi database di file `.env`.
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Setup Database**
   - Buat database baru (misal: `laravelscpk`).
   - Import file SQL yang disertakan (`laravelscpk.sql`) atau jalankan migrasi jika tersedia.
   ```bash
   # Contoh import jika ada file sql
   mysql -u root -p laravelscpk < laravelscpk.sql
   ```

6. **Jalankan Project**
   ```bash
   php artisan serve
   ```
   Akses aplikasi di `http://localhost:8000`.

## Lisensi
Project ini bersifat open-source di bawah lisensi [MIT](https://opensource.org/licenses/MIT).
