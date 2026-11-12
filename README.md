# ♛ Voting Kakang & Senduk Ponorogo

Aplikasi berbasis web untuk pemilihan Duta Wisata Kakang & Senduk Ponorogo secara online. Aplikasi ini memungkinkan masyarakat melihat profil kontestan, memberikan suara, dan melihat hasil voting.

## 📌 Deskripsi Project

Voting Kakang & Senduk Ponorogo merupakan sistem informasi pemilihan Duta Wisata Daerah yang dibuat untuk mempermudah proses pemungutan suara secara online, transparan, dan terstruktur.

## ✨ Fitur Aplikasi

### 1. Halaman Pengunjung
- Halaman utama.
- Informasi pemilihan Kakang & Senduk.
- Daftar kontestan.
- Detail profil kontestan.
- Klasemen hasil voting.

### 2. Fitur Pemilih
- Registrasi akun.
- Login dan logout.
- Melihat kontestan Kakang dan Senduk.
- Melakukan voting.
- Mencegah pemilih memberikan suara lebih dari satu kali pada setiap kategori.

### 3. Fitur Admin
- Dashboard admin.
- Mengelola data kontestan.
- Menambah, mengedit, dan menghapus kontestan.
- Mengelola data pemilih.
- Mengatur periode voting.
- Melihat hasil voting.

### 4. Payment Gateway
- Integrasi Duitku POP.
- Mode pengujian Sandbox.
- Rencana pembayaran untuk membuka akses voting.

**Catatan:** Integrasi pembayaran masih dalam tahap konfigurasi dan pengujian.

## 🛠️ Teknologi yang Digunakan

- PHP Native
- MySQL / MariaDB
- HTML5
- CSS3
- JavaScript
- Bootstrap 5.3.3
- Bootstrap Icons
- Duitku Payment Gateway (Sandbox)

## 📂 Struktur Folder

```text
voting-kakang-senduk/
│
├── admin/
│   ├── dashboard.php
│   ├── kontestan.php
│   ├── tambah-kontestan.php
│   ├── edit-kontestan.php
│   ├── pemilih.php
│   ├── hasil-voting.php
│   └── periode.php
│
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── img/
│
├── auth/
│   ├── login.php
│   ├── register.php
│   └── logout.php
│
├── config/
│   ├── koneksi.php
│   └── duitku.php
│
├── pages/
│   ├── index.php
│   ├── kontestan.php
│   ├── detail-kontestan.php
│   ├── voting.php
│   └── klasemen.php
│
├── payment/
│
├── proses/
│   └── simpan-voting.php
│
├── uploads/
│
└── index.php
```

## ⚙️ Cara Instalasi

### 1. Persiapan
Pastikan sudah menginstal:
- XAMPP
- PHP
- MySQL
- Browser

### 2. Clone Repository

```bash
git clone URL_REPOSITORY
```

Atau download ZIP repository dan ekstrak ke:

```text
C:\xampp\htdocs\
```

### 3. Buat Database

Buka phpMyAdmin:

```text
http://localhost/phpmyadmin
```

Buat database:

```sql
CREATE DATABASE db_voting_kakang_senduk;
```

Buat tabel sesuai struktur database aplikasi.

### 4. Konfigurasi Database

Buka file:

```text
config/koneksi.php
```

Sesuaikan konfigurasi database:

```php
<?php
$host = "localhost";
$user = "root";
$password = "";
$database = "db_voting_kakang_senduk";

$conn = mysqli_connect(
    $host,
    $user,
    $password,
    $database
);

if (!$conn) {
    die("Koneksi database gagal: " . mysqli_connect_error());
}

mysqli_set_charset($conn, "utf8mb4");
?>
```

### 5. Jalankan Aplikasi

Aktifkan Apache dan MySQL melalui XAMPP.

Buka browser:

```text
http://localhost/voting-kakang-senduk/
```

## 🗳️ Alur Penggunaan

1. Pengunjung membuka halaman utama.
2. Pengunjung melakukan registrasi.
3. Pemilih login menggunakan akun.
4. Pemilih melihat daftar kontestan.
5. Pemilih memberikan suara untuk kategori Kakang dan Senduk.
6. Sistem menyimpan suara.
7. Hasil voting ditampilkan melalui halaman klasemen.

## 🔐 Keamanan

- Password pengguna disimpan menggunakan hashing.
- Login menggunakan session.
- Hak akses dibedakan antara admin dan pemilih.
- Setiap pemilih hanya dapat melakukan voting satu kali untuk setiap kategori.
- API Key Duitku disimpan di konfigurasi server dan tidak boleh dipublikasikan.

## 👩‍💻 Pengembang

**Nama:** Lefina Restiana Wahyu Saputri  
**Kelas:** XII RPL 2  
**Konsentrasi Keahlian:** Rekayasa Perangkat Lunak

## 📄 Lisensi

Project ini dibuat untuk keperluan pembelajaran dan pengembangan aplikasi berbasis web.

---

**Voting Kakang & Senduk Ponorogo**  
*Dukung Generasi Muda, Lestarikan Budaya, Promosikan Pariwisata Ponorogo.*
