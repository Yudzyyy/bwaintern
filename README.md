
Proyek ini adalah penyelesaian tantangan teknis untuk posisi Backend Developer Intern. Tantangan ini mencakup desain ERD dan pembuatan skema database menggunakan Laravel Migration untuk sistem booking cuci mobil sederhana.

## Desain ERD
Berikut adalah desain struktur database yang diimplementasikan dalam proyek ini. Desain ini mencakup entitas untuk pengguna, layanan, mobil, dan booking.


## Struktur Database

-   **users**: Menyimpan data pelanggan yang melakukan booking.
-   **services**: Menyimpan jenis-jenis layanan cuci mobil yang ditawarkan beserta harganya.
-   **cars**: Menyimpan data mobil milik pelanggan (memiliki relasi *one-to-many* dengan tabel `users`).
-   **bookings**: Tabel utama yang mencatat transaksi booking, menghubungkan `users`, `cars`, dan `services`.

---

## Cara Menjalankan Proyek

1.  **Clone repository ini:**
    ```bash
    git clone [URL_REPOSITORY_ANDA]
    ```

2.  **Masuk ke direktori proyek:**
    ```bash
    cd nama-folder-proyek
    ```

3.  **Install dependensi PHP via Composer:**
    ```bash
    composer install
    ```

4.  **Salin file `.env.example` menjadi `.env`:**
    ```bash
    cp .env.example .env
    ```

5.  **Generate application key Laravel:**
    ```bash
    php artisan key:generate
    ```

6.  **Konfigurasikan koneksi database** di dalam file `.env`

7.  **Jalankan migrasi untuk membuat semua tabel:**
    ```bash
    php artisan migrate
    ```