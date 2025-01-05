Aplikasi To-Do List REST API

Aplikasi To-Do List sederhana yang dibangun menggunakan PHP, MySQL, dan JavaScript dasar. Proyek ini menunjukkan implementasi REST API untuk menangani operasi CRUD (Create, Read, Update, Delete) pada tabel database. Antarmuka depan dirancang menggunakan HTML dan JavaScript murni untuk berinteraksi dengan REST API.



Fitur

1. Fungsi CRUD:
   - Create: Menambahkan tugas baru ke daftar to-do.
   - Read: Melihat semua tugas dalam daftar to-do.
   - Update: Mengedit tugas yang ada.
   - Delete: Menghapus tugas dari daftar.

2. REST API:
   - Mendukung metode HTTP berikut:
     - `GET`: Mengambil semua tugas dari database.
     - `POST`: Menambahkan tugas baru ke database.
     - `PUT`: Memperbarui tugas yang ada berdasarkan ID-nya.
     - `DELETE`: Menghapus tugas berdasarkan ID-nya.

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
     ```
     CREATE DATABASE uastegar;
     USE uastegar;

     CREATE TABLE todo_list (
         id INT AUTO_INCREMENT PRIMARY KEY,
         task VARCHAR(255) NOT NULL,
         created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
     );
     

2. Clone Repository:
   ```
   git clone https://github.com/username/todo-list-rest-api.git
   cd todo-list-rest-api
   

3. Konfigurasi Koneksi Database:
   - Edit file `db.php` dan perbarui kredensial database:
     ```
     $host = 'localhost';
     $db = 'uastegar';
     $user = 'root';
     $pass = '';
     

4. **Jalankan Aplikasi**:
   - Tempatkan file-file di direktori server web Anda (misalnya `htdocs` untuk XAMPP).
   - Akses aplikasi melalui `http://localhost/UAS-TODO-LIST/index.php`.


Cara Kerja

1. Endpoint API:
   - GET: Ambil semua tugas.
     ```bash
     curl -X GET http://localhost/todo-list-rest-api/api.php
     
   - POST: Tambahkan tugas baru.
     ```
     curl -X POST -H "Content-Type: application/json" -d '{"task":"Tugas Anda"}' http://localhost/todo-list-rest-api/api.php
     
   - PUT: Perbarui tugas yang ada.
     ```
     curl -X PUT -H "Content-Type: application/json" -d '{"id":1,"task":"Tugas Diperbarui"}' http://localhost/todo-list-rest-api/api.php
     
   - DELETE: Hapus tugas.
     ```
     curl -X DELETE -H "Content-Type: application/json" -d '{"id":1}' http://localhost/todo-list-rest-api/api.php
     

2. Antarmuka Pengguna:
   - Antarmuka sederhana memungkinkan pengguna untuk:
     - Menambahkan tugas menggunakan kolom input dan tombol.
     - Melihat daftar tugas yang diperbarui secara dinamis menggunakan JavaScript.
     - Menghapus tugas dengan tombol "Delete" di setiap tugas.

Teknologi yang Digunakan

- PHP (Backend REST API)
- MySQL (Database)
- JavaScript (Logika Antarmuka Pengguna)
- HTML (Antarmuka Pengguna)
