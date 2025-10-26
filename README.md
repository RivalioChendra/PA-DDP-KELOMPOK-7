# PA-DDP-KELOMPOK-7
## TEMA: APLIKASI RESERVASI HOTEL SEDERHANA, 
**ANGGOTA:** <br> 
Ahmad Afif AlGhifary   (2509116002)<br>
Brendhen Canafaro Lie  (2509116033)<br>
Rivalio chendra        (2509116039)<br>


## FLOWCHART
## Sistem Login
![WhatsApp Image 2025-10-26 at 20 28 34_9034a9a6](https://github.com/user-attachments/assets/ddd77d69-92a6-42b4-8686-35e6a61fad95)
## Sistem Manager
![WhatsApp Image 2025-10-26 at 20 28 35_43b6b49f](https://github.com/user-attachments/assets/9a883d25-29ee-494d-81e4-92f40a4f04ad)
## Sistem Karyawan
![WhatsApp Image 2025-10-26 at 20 28 35_0ddb3719](https://github.com/user-attachments/assets/affb0975-9968-442a-bd50-99255d340758)
## Sistem Kostumer
![WhatsApp Image 2025-10-26 at 20 28 34_fc2f37cf](https://github.com/user-attachments/assets/65f427bd-354f-4190-abfc-5ed4cb9cfad3)


## Deskripsi Singkat Program

Sistem Reservasi Hotel adalah aplikasi berbasis console yang dirancang untuk mengelola operasional hotel dengan 10 kamar tersedia. Program ini menyediakan tiga tingkat akses berbeda (Manager, Karyawan, dan Kostumer) dengan fitur yang disesuaikan untuk setiap role. Semua data disimpan dalam format JSON, memungkinkan persistensi data antar sesi. Sistem ini mencakup fitur manajemen reservasi lengkap, pengelolaan saldo e-money untuk kostumer, dan sistem diskon khusus untuk member VIP.

## Fitur Unggulan ⭐

### Sistem Multi-Role dengan Hak Akses Berbeda
Program mengimplementasikan role-based access control (RBAC) yang membedakan hak akses antara Manager, Karyawan, dan Kostumer. Setiap role memiliki menu dan fungsi spesifik yang disesuaikan dengan kebutuhan operasional mereka.

### E-Money Payment System
Kostumer dapat mengelola saldo digital mereka langsung dalam aplikasi. Sistem ini dilengkapi dengan validasi pembayaran, riwayat transaksi, dan struk digital otomatis setelah pemesanan berhasil.

### Dynamic Pricing & VIP Discount
Hotel memiliki dua tier pricing berdasarkan lantai (Lantai 1: Rp 300.000, Lantai 2: Rp 600.000). Member VIP mendapatkan diskon otomatis 15% untuk setiap transaksi, mendorong loyalitas pelanggan.

## Fitur Program Berdasarkan Role

### 🔐 Halaman Login Utama

Menu login yang menampilkan pilihan role dan fitur registrasi akun baru.

```
# ====================================================
# =               Login Sistem                       =
# ====================================================
=            1.     Manager                          =
=            2.     Karyawan                         =
=            3.     Kostumer                         =
=            4.     Buat Akun                        =
=            5.     Hapus Akun                       =
=            6.     Keluar                           =
======================================================
Masukkan pilihan: _
```

![Login Menu](https://via.placeholder.com/600x300/2c3e50/ffffff?text=Login+Menu+Sistem+Reservasi)

---

### 👨‍💼 Manager

#### 1. Menu Utama Manager

Interface lengkap untuk mengelola reservasi hotel.

```
====================================================
=              Sistem Reservasi Hotel              =
====================================================
====================================================
=            1.     Tambah Reservasi               =
=            2.     Lihat Reservasi                =
=            3.     Ubah Reservasi                 =
=            4.     Hapus Reservasi                =
=            5.     Lihat Ketersediaan Kamar       =
=            6.     Kembali Halaman Login          =
====================================================
Masukkan pilihan: _
```

![Manager Menu](https://via.placeholder.com/600x300/27ae60/ffffff?text=Menu+Manager)

#### 2. Tambah Reservasi

Fitur untuk menambahkan data reservasi baru dengan validasi ketersediaan kamar.

**Input:**
```
Kamar tersedia: [5, 6, 8, 9, 10]
Nama Tamu: John Doe
Nomor Kamar (dari tersedia): 8
Durasi (hari): 3
```

**Output:**
```
Reservasi berhasil! Total: Rp 1,800,000
```

![Tambah Reservasi](https://via.placeholder.com/600x350/3498db/ffffff?text=Tambah+Reservasi)

#### 3. Lihat Reservasi

Menampilkan semua data reservasi dalam bentuk tabel terstruktur.

**Output:**
```
+------------------------------------+
|    Daftar Reservasi Hotel         |
+----+-------------+-------------+--------+---------------+
| No | Nama Tamu   | Nomor Kamar | Durasi | Total Harga   |
+----+-------------+-------------+--------+---------------+
| 1  | Fred        | 1           | 1      | Rp 300,000    |
| 2  | Jajajaja    | 2           | 2      | Rp 600,000    |
| 3  | Brenden     | 3           | 3      | Rp 765,000    |
| 4  | Jaajaaa     | 7           | 1      | Rp 510,000    |
| 5  | John Doe    | 8           | 3      | Rp 1,800,000  |
+----+-------------+-------------+--------+---------------+
```

![Tabel Reservasi](https://via.placeholder.com/650x300/9b59b6/ffffff?text=Tabel+Reservasi+Hotel)

#### 4. Ubah Reservasi

Mengupdate data reservasi yang sudah ada (nama, kamar, durasi).

**Input:**
```
Nomor Reservasi untuk diubah: 3
Nama Tamu baru: Brandon Smith
Nomor Kamar baru: 6
Durasi baru: 5
```

**Output:**
```
Reservasi diubah!
```

![Ubah Reservasi](https://via.placeholder.com/600x300/e67e22/ffffff?text=Ubah+Data+Reservasi)

#### 5. Hapus Reservasi

Menghapus reservasi dan otomatis membebaskan kamar.

**Input:**
```
Nomor Reservasi untuk dihapus: 2
```

**Output:**
```
Reservasi dihapus!
(Kamar 2 otomatis berubah status menjadi "Tersedia")
```

![Hapus Reservasi](https://via.placeholder.com/600x300/e74c3c/ffffff?text=Hapus+Reservasi)

#### 6. Lihat Ketersediaan Kamar

Menampilkan status real-time semua kamar hotel.

**Output:**
```
+-------------------------+
|     Status Kamar        |
+--------+----------------+
| Kamar  |     Status     |
+--------+----------------+
| 1      | Ditempati      |
| 2      | Tersedia       |
| 3      | Ditempati      |
| 4      | Ditempati      |
| 5      | Tersedia       |
| 6      | Tersedia       |
| 7      | Ditempati      |
| 8      | Tersedia       |
| 9      | Tersedia       |
| 10     | Tersedia       |
+--------+----------------+
```

![Status Kamar](https://via.placeholder.com/500x350/16a085/ffffff?text=Status+Ketersediaan+Kamar)

---

### 👷 Karyawan

#### 1. Menu Utama Karyawan

Menu read-only untuk karyawan melihat informasi hotel.

```
====================================================
=              Sistem Reservasi Hotel              =
====================================================
====================================================
=            1.     Lihat Reservasi                =
=            2.     Lihat Ketersediaan Kamar       =
=            3.     Kembali Halaman Login          =
====================================================
Masukkan pilihan: _
```

![Karyawan Menu](https://via.placeholder.com/600x250/f39c12/ffffff?text=Menu+Karyawan)

#### 2. Lihat Reservasi (Karyawan)

Output sama dengan Manager, namun tanpa akses edit/hapus.

**Output:**
```
+------------------------------------+
|    Daftar Reservasi Hotel         |
+----+-------------+-------------+--------+---------------+
| No | Nama Tamu   | Nomor Kamar | Durasi | Total Harga   |
+----+-------------+-------------+--------+---------------+
| 1  | Fred        | 1           | 1      | Rp 300,000    |
| 2  | Jajajaja    | 2           | 2      | Rp 600,000    |
+----+-------------+-------------+--------+---------------+
```

![Karyawan View](https://via.placeholder.com/650x250/d35400/ffffff?text=View+Reservasi+Karyawan)

---

### 🧳 Kostumer

#### 1. Menu Utama Kostumer

Interface self-service untuk pemesanan dan manajemen saldo.

```
====================================================
=              Menu Kostumer                       =
====================================================
=            1.     Pesan Kamar                    =
=            2.     Tambah Saldo E-Money           =
=            3.     Lihat Saldo E-Money            =
=            4.     Kembali Halaman Login          =
====================================================
Masukkan pilihan: _
```

![Kostumer Menu](https://via.placeholder.com/600x300/1abc9c/ffffff?text=Menu+Kostumer)

#### 2. Pesan Kamar

Proses booking kamar dengan pembayaran e-money dan diskon VIP.

**Input:**
```
Ingin memesan? (Iya/Keluar): iya

+-------------------------------------+
|      Daftar Harga Kamar            |
+----+--------+--------+------------------+
| No | Kamar  | Lantai | Harga per Malam |
+----+--------+--------+------------------+
| 1  | 1 - 5  | 1      | Rp 300.000      |
| 2  | 6 - 10 | 2      | Rp 600.000      |
+----+--------+--------+------------------+

Kamar tersedia: [5, 6, 8, 9, 10]
Nama Anda: Sarah Wilson
Pilih Kamar: 9
Durasi (hari): 2
```

**Output (Akun VIP):**
```
Selamat! Sebagai akun VIP, Anda mendapat diskon 15%: Rp 180000
Saldo Anda sekarang: Rp 820,000

Pemesanan berhasil! Total: Rp 1,020,000. 
Hubungi staff untuk konfirmasi.
```

![Pesan Kamar](https://via.placeholder.com/600x350/8e44ad/ffffff?text=Proses+Pemesanan+Kamar)

#### 3. Struk Pembelian Digital

Struk otomatis setelah pembayaran berhasil.

**Output:**
```
====================================================
=                Pembelian Kamar                   =
====================================================
    Nama            : Sarah Wilson
    Tanggal         : 2025-10-26
    Lantai Kamar    : 2
    Harga Per Malam : Rp 600,000
    Durasi          : 2 Hari
====================================================
=   Total            : Rp 1,020,000
====================================================
= Terima Kasih atas Kunjungan Anda!                =
= Silakan Simpan Struk Ini sebagai Bukti.          =
====================================================
```

![Struk Digital](https://via.placeholder.com/550x400/c0392b/ffffff?text=Struk+Pembelian)

#### 4. Tambah Saldo E-Money

Top-up saldo dengan validasi minimum dan maksimum.

**Input:**
```
Masukkan jumlah saldo yang ingin ditambah: 200000
```

**Output:**
```
Saldo berhasil ditambahkan!
Saldo Anda sekarang: Rp 700,000
```

![Top Up Saldo](https://via.placeholder.com/600x250/2ecc71/ffffff?text=Tambah+Saldo+E-Money)

#### 5. Lihat Saldo E-Money

Cek saldo terkini.

**Output:**
```
Saldo Anda: Rp 700,000
```

![Cek Saldo](https://via.placeholder.com/500x200/27ae60/ffffff?text=Saldo+E-Money)

---

### 🔧 Administrator

#### 1. Hapus Akun

Fitur khusus admin untuk menghapus akun dengan verifikasi password.

**Input:**
```
Masukkan Password Admin: unmul123

====================================================
=                Hapus Akun                       =
====================================================
=            1.     Hapus Akun Manager            =
=            2.     Hapus Akun Karyawan           =
=            3.     Hapus Akun Kostumer           =
=            4.     Kembali                       =
====================================================
Masukkan pilihan: 2

Masukkan Username Karyawan yang ingin dihapus: karyawan2
```

**Output:**
```
Akun Karyawan 'karyawan2' berhasil dihapus.
```

![Hapus Akun](https://via.placeholder.com/600x300/34495e/ffffff?text=Admin+Hapus+Akun)

---

### 📝 Registrasi Akun Baru

Interface untuk membuat akun baru (Manager, Karyawan, atau Kostumer).

**Input:**
```
====================================================
=                Registrasi Akun                   =
====================================================
=            1.     Manager                        =
=            2.     Karyawan                       =
=            3.     Kostumer                       =
=            4.     Kembali Halaman Login          =
====================================================
Masukkan pilihan: 3

Masukkan username baru untuk Kostumer: newuser
Masukkan password baru: ****
Pilih tipe akun (VIP/Reguler): vip
```

**Output:**
```
Registrasi sukses! Akun Kostumer VIP baru telah ditambahkan.
```

![Registrasi](https://via.placeholder.com/600x350/95a5a6/ffffff?text=Form+Registrasi)

## Persyaratan Sistem

### Software Requirements
- Python 3.7 atau lebih tinggi
- Terminal/Command Prompt dengan dukungan UTF-8
- Windows/Linux/MacOS

### Dependencies
Program memerlukan beberapa library eksternal yang harus diinstal terlebih dahulu:

```bash
pip install prettytable pwinput
```

**Library yang Digunakan:**
- `prettytable` - Membuat tampilan tabel data yang rapi dan terstruktur
- `pwinput` - Input password tersembunyi untuk keamanan
- `json` - Parsing dan manipulasi data JSON (built-in)
- `os` - Operasi sistem seperti clear screen (built-in)
- `time` - Delay dan timestamp (built-in)
- `datetime` - Menangani data tanggal (built-in)

## Instalasi & Konfigurasi

### 1. Clone Repository
```bash
git clone [URL_REPOSITORY]
cd [NAMA_FOLDER]
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

Atau install manual:
```bash
pip install prettytable pwinput
```

### 3. Struktur File
Pastikan semua file JSON berada dalam direktori yang sama dengan `ReservasiHotel.py`:

```
project/
│
├── ReservasiHotel.py
├── DataReservasi.json
├── DataCheckList.json
├── DataHarga.json
├── DataKaryawan.json
├── DataManager.json
└── DataKostumer.json
```

## Cara Menjalankan Aplikasi

### Menjalankan Program
```bash
python ReservasiHotel.py
```

### Login Credentials (Default)

**Manager:**
```
Username: manager1
Password: 111
```

**Karyawan:**
```
Username: karyawan1
Password: 111
```

**Kostumer VIP:**
```
Username: vip1
Password: vip123
E-Money: Rp 500.000
```

**Kostumer Reguler:**
```
Username: reguler1
Password: reg123
E-Money: Rp 100.000
```

**Admin (Hapus Akun):**
```
Password: unmul123
```

## Contoh Penggunaan

### Skenario 1: Manager Menambah Reservasi

```python
# Login sebagai Manager
Username: manager1
Password: 111

# Pilih menu "Tambah Reservasi"
Masukkan pilihan: 1

# Input data reservasi
Nama Tamu: John Doe
Nomor Kamar: 3
Durasi (hari): 2

# Output
Reservasi berhasil! Total: Rp 600,000
```

### Skenario 2: Kostumer VIP Memesan Kamar

```python
# Login sebagai Kostumer VIP
Username: vip1
Password: vip123

# Pilih "Pesan Kamar"
Masukkan pilihan: 1

# Input pemesanan
Nama Anda: Jane Smith
Pilih Kamar: 7
Durasi (hari): 3

# Output (dengan diskon 15%)
Total sebelum diskon: Rp 1,800,000
Diskon VIP (15%): Rp 270,000
Total akhir: Rp 1,530,000

# Struk digital otomatis ditampilkan
====================================================
=                Pembelian Kamar                   =
====================================================
    Nama            : Jane Smith
    Tanggal         : 2025-10-26
    Lantai Kamar    : 2
    Harga Per Malam : Rp 600,000
    Durasi          : 3 Hari
====================================================
=   Total            : Rp 1,530,000
====================================================
```

### Skenario 3: Karyawan Melihat Status Kamar

```python
# Login sebagai Karyawan
Username: karyawan1
Password: 111

# Pilih "Lihat Ketersediaan Kamar"
Masukkan pilihan: 2

# Output
+--------+-------------+
|  Kamar |    Status   |
+--------+-------------+
|    1   |  Ditempati  |
|    2   |  Ditempati  |
|    3   |  Tersedia   |
|    4   |  Tersedia   |
|   ...  |     ...     |
+--------+-------------+
```

## Penjelasan Output Program

### 📊 Tabel Reservasi
Menampilkan semua data reservasi aktif dalam format tabel dengan kolom:
- **No:** Nomor urut reservasi
- **Nama Tamu:** Identitas pemesan
- **Nomor Kamar:** Kamar yang dipesan (1-10)
- **Durasi:** Lama menginap dalam hari
- **Total Harga:** Biaya total dengan format currency (Rp)

**Contoh Output:**
```
+------------------------------------+
|    Daftar Reservasi Hotel         |
+----+-------------+-------------+--------+---------------+
| No | Nama Tamu   | Nomor Kamar | Durasi | Total Harga   |
+----+-------------+-------------+--------+---------------+
| 1  | Fred        | 1           | 1      | Rp 300,000    |
| 2  | Jajajaja    | 2           | 2      | Rp 600,000    |
| 3  | Brenden     | 3           | 3      | Rp 765,000    |
+----+-------------+-------------+--------+---------------+
```

![Output Tabel Reservasi](https://via.placeholder.com/650x300/3498db/ffffff?text=Output+Tabel+Reservasi)

---

### 🏨 Tabel Status Kamar
Visualisasi real-time ketersediaan 10 kamar hotel:
- **Kamar:** Nomor kamar (1-10)
- **Status:** "Tersedia" atau "Ditempati"

**Contoh Output:**
```
+-------------------------+
|     Status Kamar        |
+--------+----------------+
| Kamar  |     Status     |
+--------+----------------+
| 1      | Ditempati      |
| 2      | Tersedia       |
| 3      | Ditempati      |
| 4      | Ditempati      |
| 5      | Tersedia       |
| 6      | Tersedia       |
| 7      | Ditempati      |
| 8      | Tersedia       |
| 9      | Tersedia       |
| 10     | Tersedia       |
+--------+----------------+
```

![Output Status Kamar](https://via.placeholder.com/500x350/27ae60/ffffff?text=Output+Status+Kamar)

---

### 💰 Tabel Harga Kamar
Informasi pricing berdasarkan lokasi:
- **Lantai 1 (Kamar 1-5):** Rp 300.000/malam
- **Lantai 2 (Kamar 6-10):** Rp 600.000/malam

**Contoh Output:**
```
+-------------------------------------+
|      Daftar Harga Kamar            |
+----+--------+--------+------------------+
| No | Kamar  | Lantai | Harga per Malam |
+----+--------+--------+------------------+
| 1  | 1 - 5  | 1      | Rp 300.000      |
| 2  | 6 - 10 | 2      | Rp 600.000      |
+----+--------+--------+------------------+
```

![Output Tabel Harga](https://via.placeholder.com/600x250/e67e22/ffffff?text=Output+Daftar+Harga)

---

### 🧾 Struk Pembelian
Dokumen digital yang diberikan setelah pembayaran berhasil, berisi:
- Nama tamu
- Tanggal transaksi
- Lantai kamar
- Harga per malam
- Durasi menginap
- Total biaya (sudah termasuk diskon jika VIP)

**Contoh Output:**
```
====================================================
=                Pembelian Kamar                   =
====================================================
    Nama            : Sarah Wilson
    Tanggal         : 2025-10-26
    Lantai Kamar    : 2
    Harga Per Malam : Rp 600,000
    Durasi          : 2 Hari
====================================================
=   Total            : Rp 1,020,000
====================================================
= Terima Kasih atas Kunjungan Anda!                =
= Silakan Simpan Struk Ini sebagai Bukti.          =
====================================================
```

![Output Struk](https://via.placeholder.com/550x400/9b59b6/ffffff?text=Output+Struk+Pembelian)

---

### ✅ Pesan Sukses
Output konfirmasi untuk berbagai operasi berhasil.

**Contoh Output:**
```
# Reservasi berhasil
Reservasi berhasil! Total: Rp 1,800,000

# Login berhasil
Login sukses!

# Registrasi berhasil
Registrasi sukses! Akun Kostumer VIP baru telah ditambahkan.

# Saldo ditambahkan
Saldo berhasil ditambahkan!
Saldo Anda sekarang: Rp 700,000

# Akun dihapus
Akun Karyawan 'karyawan2' berhasil dihapus.

# Data diubah
Reservasi diubah!

# Data dihapus
Reservasi dihapus!
```

![Output Success](https://via.placeholder.com/600x300/2ecc71/ffffff?text=Pesan+Sukses)

---

### ❌ Pesan Error
Output peringatan untuk berbagai kondisi error atau validasi.

**Contoh Output:**
```
# Login gagal
Username atau password salah coba lagi! (10 Maksimal)
Percobaan 3

# Kamar tidak tersedia
Kamar tidak tersedia! Coba lagi.

# Saldo tidak cukup
Uang Tidak Cukup

# Hotel penuh
Maaf, semua kamar penuh (maksimal 10).

# Input tidak valid
Input harus angka!

# Password terlalu pendek
Password minimal 4 karakter!

# File tidak ditemukan
File DataReservasi.json tidak ditemukan. Membuat file kosong.
```

![Output Error](https://via.placeholder.com/600x300/e74c3c/ffffff?text=Pesan+Error)

---

### 🔄 Status Loading & Delay
Program menampilkan status pemrosesan dan delay untuk user experience.

**Contoh Output:**
```
# Menampilkan struk (5 detik)
[Struk ditampilkan selama 5 detik...]

# Penalty login (30-90 detik)
Tunggu 30 detik untuk mencoba lagi
[Countdown timer...]

# Keluar sistem
Keluar dari sistem...
[Loading 1 detik...]
```

![Output Loading](https://via.placeholder.com/600x200/95a5a6/ffffff?text=Status+Loading)

## Keamanan & Validasi

### Security Features
- Password tersembunyi saat input menggunakan `pwinput`
- Verifikasi admin untuk fitur sensitif (hapus akun)
- Rate limiting: maksimal 10 percobaan login dengan penalty delay
- Case-insensitive login untuk user experience lebih baik

### Input Validation
- Validasi tipe data (integer untuk kamar, durasi, saldo)
- Cek ketersediaan kamar sebelum pemesanan
- Validasi saldo minimum (Rp 50.000) dan maksimum (Rp 1.000.000)
- Password minimal 4 karakter
- Exception handling untuk mencegah crash

## Troubleshooting

### Error: "File JSON tidak ditemukan"
**Solusi:** Program akan otomatis membuat file kosong. Restart aplikasi.

### Error: "ModuleNotFoundError: prettytable/pwinput"
**Solusi:** Install dependencies:
```bash
pip install prettytable pwinput
```

### Error: "Kamar tidak tersedia"
**Solusi:** Cek status kamar terlebih dahulu, pastikan kamar dalam status "Tersedia".

### Program tidak clear screen
**Solusi:** Pada Linux/Mac, ubah `os.system("cls")` menjadi `os.system("clear")` di file Python.

## Kontribusi & Development

Program ini dikembangkan sebagai proyek pembelajaran manajemen hotel. Saran pengembangan lebih lanjut:
- Integrasi database SQL untuk skalabilitas
- GUI menggunakan Tkinter atau PyQt
- Fitur checkout otomatis berdasarkan durasi
- Laporan keuangan dan statistik occupancy
- Notifikasi email/SMS untuk konfirmasi booking

---

**Terima kasih telah menggunakan Sistem Reservasi Hotel!** 

Untuk pertanyaan atau dukungan, silakan hubungi tim pengembang.
