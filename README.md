# 🛒 Sistem Informasi Manajemen Stok & Penjualan (POS)

Sistem Informasi Manajemen Stok dan Penjualan (Point of Sale) berbasis web yang dibangun menggunakan **Laravel**. Aplikasi ini dirancang untuk mempermudah pengelolaan inventaris barang, pencatatan transaksi penjualan & pembelian, serta menyajikan analitik data secara *real-time* melalui dashboard interaktif.

---

## ✨ Fitur Utama

### 📊 1. Dashboard Analitik
- Ringkasan total **Kategori**, **Produk**, **Supplier**, dan **Pengguna**.
- Peringatan stok menipis (*Low Stock Alert*) untuk produk yang mendekati habis.
- Tabel riwayat transaksi penjualan dan pembelian terbaru.

### 📦 2. Manajemen Data Master (CRUD)
- **Produk:** Kelola data barang, harga beli, harga jual, stok, dan kategori.
- **Kategori:** Pengelompokan jenis produk.
- **Supplier:** Pendataan pemasok barang.
- **Pengguna:** Manajemen hak akses pengguna (Admin & Kasir).

### 💳 3. Transaksi
- **Penjualan (POS):** Pencatatan transaksi dengan pembeli/konsumen.
- **Pembelian (Purchase):** Pencatatan pengadaan barang dari supplier.

---

## 🛠️ Teknologi yang Digunakan

| Komponen | Teknologi |
| :--- | :--- |
| **Backend Framework** | [Laravel 10.x / 11.x](https://laravel.com/) |
| **Language** | PHP >= 8.1 |
| **Database** | MySQL / MariaDB |
| **Frontend** | Blade Templating, Tailwind CSS / Bootstrap |
| **Icons & UI** | FontAwesome / Lucide Icons |

---

## ⚙️ Persyaratan Sistem

Sebelum menjalankan proyek, pastikan perangkat Anda telah memenuhi syarat berikut:
- **PHP** >= 8.1
- **Composer** (Versi terbaru)
- **MySQL** / **MariaDB**
- **Node.js** & **NPM** (Opsional, untuk kompilasi aset frontend)

---

## 🚀 Panduan Instalasi & Penggunaan

Ikuti langkah-langkah di bawah ini untuk menjalankan proyek di komputer lokal (*development*):

### 1. Clone Repository
```bash
git clone https://github.com/username/nama-repository.git
cd nama-repository
```

### 2. Install Dependency PHP
```bash
composer install
```

### 3. Konfigurasi Environment (`.env`)
Salin file `.env.example` menjadi `.env`:
```bash
cp .env.example .env
```

Buka file `.env` dan sesuaikan kredensial database Anda:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_db_anda
DB_USERNAME=root
DB_PASSWORD=
```

### 4. Generate Application Key
```bash
php artisan key:generate
```

### 5. Jalankan Migrasi & Seeder Database
Jalankan perintah ini untuk membuat tabel dan mengisi data awal (dummy):
```bash
php artisan migrate --seed
```

### 6. Install Dependency Frontend & Build Assets (Opsional)
```bash
npm install
npm run dev
```

### 7. Jalankan Server Lokal
```bash
php artisan serve
```

Buka browser dan akses aplikasi melalui tautan: `http://127.0.0.1:8000`

---

## 📂 Struktur Controller Utama

- `DashboardController.php` - Menangani logika statistik dashboard, peringatan stok menipis, dan ringkasan transaksi terbaru.
- `ProductController.php` - Menangani CRUD data barang dan stok.
- `CategoryController.php` - Menangani klasifikasi kategori produk.
- `SupplierController.php` - Menangani data pemasok barang.
- `SaleController.php` - Menangani transaksi penjualan kasir.
- `PurchaseController.php` - Menangani transaksi pembelian barang dari supplier.

---

## 🤝 Kontribusi

Jalur kontribusi terbuka untuk siapa saja. Jika Anda menemukan *bug* atau memiliki ide pengembangan fitur baru:
1. *Fork* repository ini.
2. Buat branch baru (`git checkout -b feature/fitur-baru`).
3. Commit perubahan Anda (`git commit -m 'Menambahkan fitur baru'`).
4. Push ke branch (`git push origin feature/fitur-baru`).
5. Buat **Pull Request**.

---

## 📄 Lisensi

Proyek ini dirilis di bawah [MIT License](LICENSE).
