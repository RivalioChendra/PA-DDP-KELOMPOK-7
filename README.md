# PA-DDP-KELOMPOK-7
## TEMA: APLIKASI RESERVASI HOTEL SEDERHANA, 
**ANGGOTA:** <br> 
Ahmad Afif AlGhifary   (2509116002)<br>
Brendhen Canafaro Lie  (2509116033)<br>
Rivalio chendra        (2509116039)<br>


## Flowchart
![WhatsApp Image 2025-10-26 at 20 28 34_9034a9a6](https://github.com/user-attachments/assets/ddd77d69-92a6-42b4-8686-35e6a61fad95)
![WhatsApp Image 2025-10-26 at 20 28 35_43b6b49f](https://github.com/user-attachments/assets/9a883d25-29ee-494d-81e4-92f40a4f04ad)
![WhatsApp Image 2025-10-26 at 20 28 35_0ddb3719](https://github.com/user-attachments/assets/affb0975-9968-442a-bd50-99255d340758)
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

### Manager
- **CRUD Reservasi Lengkap**
  - Tambah reservasi baru dengan validasi ketersediaan kamar
  - Lihat semua data reservasi dalam format tabel
  - Update data reservasi (nama tamu, kamar, durasi)
  - Hapus reservasi dan otomatis membebaskan kamar

- **Monitor Ketersediaan Kamar**
  - Cek status real-time semua kamar (Tersedia/Ditempati)
  - Visualisasi dalam bentuk tabel terstruktur

### Karyawan
- **Akses Baca (Read-Only)**
  - Lihat daftar reservasi hotel
  - Cek ketersediaan kamar
  - Membantu kostumer dengan informasi yang dibutuhkan

### Kostumer
- **Pemesanan Kamar Self-Service**
  - Browse kamar tersedia dengan harga transparan
  - Pesan kamar sesuai durasi kebutuhan
  - Pembayaran otomatis menggunakan e-money

- **Manajemen E-Money**
  - Top-up saldo (minimum Rp 50.000, maksimum Rp 1.000.000)
  - Cek saldo real-time
  - Riwayat transaksi dalam struk digital

- **Member Benefits**
  - Akun VIP mendapat diskon 15% otomatis
  - Struk pembelian digital dengan detail lengkap

### Administrator
- **Manajemen Akun Global**
  - Hapus akun Manager, Karyawan, atau Kostumer
  - Kontrol penuh dengan verifikasi password admin

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

### Tabel Reservasi
Menampilkan semua data reservasi aktif dalam format tabel dengan kolom:
- **No:** Nomor urut reservasi
- **Nama Tamu:** Identitas pemesan
- **Nomor Kamar:** Kamar yang dipesan (1-10)
- **Durasi:** Lama menginap dalam hari
- **Total Harga:** Biaya total dengan format currency (Rp)

### Tabel Status Kamar
Visualisasi real-time ketersediaan 10 kamar hotel:
- **Kamar:** Nomor kamar (1-10)
- **Status:** "Tersedia" atau "Ditempati"

### Tabel Harga Kamar
Informasi pricing berdasarkan lokasi:
- **Lantai 1 (Kamar 1-5):** Rp 300.000/malam
- **Lantai 2 (Kamar 6-10):** Rp 600.000/malam

### Struk Pembelian
Dokumen digital yang diberikan setelah pembayaran berhasil, berisi:
- Nama tamu
- Tanggal transaksi
- Lantai kamar
- Harga per malam
- Durasi menginap
- Total biaya (sudah termasuk diskon jika VIP)

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
