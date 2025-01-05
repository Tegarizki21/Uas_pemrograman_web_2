Aplikasi To-Do List sederhana yang dibangun menggunakan PHP, MySQL, dan JavaScript dasar. Proyek ini menunjukkan implementasi REST API untuk menangani operasi CRUD (Create, Read, Update, Delete) pada tabel database. Antarmuka depan dirancang menggunakan HTML dan JavaScript murni untuk berinteraksi dengan REST API.

1. Fungsi CRUD:
- Create: Menambahkan tugas baru ke daftar to-do.
- Read: Melihat semua tugas dalam daftar to-do.
- Update: Mengedit tugas yang ada.
- Delete: Menghapus tugas dari daftar.

2. REST API:
- Mendukung metode HTTP berikut:
- GET: Mengambil semua tugas dari database.
- POST: Menambahkan tugas baru ke database.
- PUT: Memperbarui tugas yang ada berdasarkan ID-nya.
- DELETE: Menghapus tugas berdasarkan ID-nya.

3. Integrasi Database:
- Menggunakan MySQL untuk penyimpanan data.
- Menggunakan prepared statement untuk mencegah SQL injection.

4. Antarmuka Pengguna yang Ramah Pengguna:
- Antarmuka sederhana menggunakan HTML dan JavaScript murni untuk pengelolaan tugas yang mudah.

Struktur File
- api.php: File utama REST API yang menangani operasi CRUD.
- db.php: Berisi fungsi untuk menghubungkan ke database MySQL.
- index.php: Antarmuka depan untuk berinteraksi dengan daftar to-do.

Instruksi Pengaturan
1. Pengaturan Database:
- Buat database dan tabel dengan menggunakan perintah SQL berikut:

CREATE DATABASE uastegar;
USE uastegar;

CREATE TABLE todo_list (
    id INT AUTO_INCREMENT PRIMARY KEY,
    task VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

2. Konfigurasi Koneksi Database:
- Edit file db.php dan perbarui kredensial database:

$host = 'localhost';
$db = 'uastegar';
$user = 'root';
$pass = '';

