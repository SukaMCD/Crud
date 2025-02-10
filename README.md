#CRUD PHP

Proyek ini adalah implementasi sederhana dari CRUD (Create, Read, Update, Delete) menggunakan PHP dan MySQL. Terdapat tiga kategori utama dalam sistem ini:

Kategori

Produk

User

Setiap kategori memiliki fitur CRUD lengkap dengan struktur file sebagai berikut:

index.php - Menampilkan daftar data

tambah.php - Form untuk menambah data baru

tambah_aksi.php - Proses penyimpanan data ke database

edit.php - Form untuk mengedit data

edit_aksi.php - Proses update data ke database

hapus.php - Menghapus data dari database

koneksi.php - File koneksi ke database

Struktur Folder

- crud/
  - kategori/
    - index.php
    - tambah.php
    - tambah_aksi.php
    - edit.php
    - edit_aksi.php
    - hapus.php
    - koneksi.php
  - produk/
    - index.php
    - tambah.php
    - tambah_aksi.php
    - edit.php
    - edit_aksi.php
    - hapus.php
    - koneksi.php
  - user/
    - index.php
    - tambah.php
    - tambah_aksi.php
    - edit.php
    - edit_aksi.php
    - hapus.php
    - koneksi.php

Database

Proyek ini menggunakan database bernama crud. Pastikan untuk membuat database dengan nama yang sama dan menyesuaikan koneksi database di file koneksi.php.

CREATE DATABASE crud;
USE crud;

CREATE TABLE kategori (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nama_kategori VARCHAR(255) NOT NULL
);

CREATE TABLE produk (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nama_barang VARCHAR(255) NOT NULL,
    deskripsi TEXT NOT NULL,
    stok INT NOT NULL,
    harga VARCHAR(255) NOT NULL,
    kategori VARCHAR(255) NOT NULL,
    gambar_produk VARCHAR(255) NOT NULL
);

CREATE TABLE user (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    password VARCHAR(255) NOT NULL,
    level VARCHAR(255) NOT NULL
);

Cara Menggunakan

Clone repository ini:

git clone https://github.com/username/repository.git

Buat database crud dan jalankan script SQL di atas.

Pastikan server lokal (XAMPP, LAMP, atau WAMP) sudah aktif.

Sesuaikan konfigurasi koneksi.php dengan kredensial database.

Jalankan di browser dengan mengakses http://localhost/crud/kategori/, http://localhost/crud/produk/, atau http://localhost/crud/user/.

Lisensi

Proyek ini bebas digunakan dan dimodifikasi sesuai kebutuhan.

Dibuat oleh Fabian (SukaMCD)
