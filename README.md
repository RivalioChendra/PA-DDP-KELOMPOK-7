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
![WhatsApp Image 2025-10-26 at 20 28 35_0ddb3719](https://github.com/user-attachments/assets/affb0975-9968-442a-bd50-99255d340758)
## Sistem Karyawan
![WhatsApp Image 2025-10-26 at 20 28 35_43b6b49f](https://github.com/user-attachments/assets/9a883d25-29ee-494d-81e4-92f40a4f04ad)
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

### Halaman Login Utama

Menu login yang menampilkan pilihan role dan fitur registrasi akun baru.

<img width="603" height="300" alt="Cuplikan layar 2025-10-26 204652" src="https://github.com/user-attachments/assets/8be0ce93-b254-49bb-bed8-57dcbc9cd4f9" />


### 👨‍💼 Manager

#### 1. Menu Utama Manager

Interface lengkap untuk mengelola reservasi hotel.

<img width="576" height="338" alt="Cuplikan layar 2025-10-26 204931" src="https://github.com/user-attachments/assets/26363b7a-6d87-46e9-ba32-013ec1bb3145" />



#### 2. Tambah Reservasi

Fitur untuk menambahkan data reservasi baru dengan validasi ketersediaan kamar.

**Input:**

<img width="622" height="422" alt="Cuplikan layar 2025-10-26 205047" src="https://github.com/user-attachments/assets/4de3122b-532d-43c6-917f-d928b94a0e1d" />



**Output:**

<img width="422" height="266" alt="Cuplikan layar 2025-10-26 205122" src="https://github.com/user-attachments/assets/8e7e8096-1a2d-40c9-b3b2-528ae22bc91f" />



#### 3. Lihat Reservasi

Menampilkan semua data reservasi dalam bentuk tabel terstruktur.

**Output:**

<img width="672" height="610" alt="Cuplikan layar 2025-10-26 205205" src="https://github.com/user-attachments/assets/02302c51-0fb5-4e1f-82e2-a2e34b11469b" />




#### 4. Ubah Reservasi

Mengupdate data reservasi yang sudah ada (nama, kamar, durasi).

**Input:**

<img width="674" height="671" alt="Cuplikan layar 2025-10-26 205526" src="https://github.com/user-attachments/assets/85336f31-f7af-436a-a756-44f09673e64d" />



**Output:**

Reservasi diubah!

<img width="360" height="197" alt="Cuplikan layar 2025-10-26 205553" src="https://github.com/user-attachments/assets/d1a2e30b-a284-4db2-9c7c-2c1d772c6080" />


#### 5. Hapus Reservasi

Menghapus reservasi dan otomatis membebaskan kamar.

**Input:**

<img width="682" height="343" alt="Cuplikan layar 2025-10-26 205628" src="https://github.com/user-attachments/assets/018fc903-26a0-402e-af2e-e368fecd658c" />



**Output:**

<img width="439" height="123" alt="Cuplikan layar 2025-10-26 205653" src="https://github.com/user-attachments/assets/4e339dc9-61ae-4e9a-b1cf-e6a9a739d14f" />

(Kamar 4 otomatis berubah status menjadi "Tersedia")



#### 6. Lihat Ketersediaan Kamar

Menampilkan status real-time semua kamar hotel.

**Output:**

<img width="626" height="669" alt="Cuplikan layar 2025-10-26 205742" src="https://github.com/user-attachments/assets/4be05839-da12-4f03-b24f-cb38edf67216" />





### 👷 Karyawan

#### 1. Menu Utama Karyawan

Menu untuk karyawan melihat informasi hotel.


<img width="570" height="253" alt="image" src="https://github.com/user-attachments/assets/7bb9cec8-ed07-404d-af73-58cdb7f5fc0a" />



#### 2. Lihat Reservasi (Karyawan)

Output sama dengan Manager, namun tanpa akses edit/hapus.

**Output:**

<img width="678" height="544" alt="image" src="https://github.com/user-attachments/assets/ea0904bd-76b3-4f8c-92d6-5a3fa5faf791" />




### 🧳 Kostumer

#### 1. Menu Utama Kostumer

Interface self-service untuk pemesanan dan manajemen saldo.

<img width="587" height="262" alt="image" src="https://github.com/user-attachments/assets/1235bdc5-16cb-4f38-bc5c-6d50f610b007" />



#### 2. Pesan Kamar

Proses booking kamar dengan pembayaran e-money dan diskon VIP.

**Input:**

Ingin memesan? (Iya/Keluar): iya

<img width="523" height="694" alt="image" src="https://github.com/user-attachments/assets/f2898c4c-5529-4356-8be1-83a9670a7943" />




#### 3. Struk Pembelian Digital

Struk otomatis setelah pembayaran berhasil.

**Output:**

<img width="610" height="403" alt="image" src="https://github.com/user-attachments/assets/3abd8fd8-df16-4554-8ebb-7d243761eb5d" />


#### 4. Tambah Saldo E-Money

Top-up saldo dengan validasi minimum dan maksimum.

**Input:**

<img width="630" height="210" alt="image" src="https://github.com/user-attachments/assets/4067b65d-db4f-49ba-962b-a659ecce8e4d" />



**Output:**

<img width="576" height="325" alt="image" src="https://github.com/user-attachments/assets/dab2f25e-cef2-4eab-bd70-0f44659afed7" />


#### 5. Lihat Saldo E-Money

Cek saldo terkini.

**Output:**

<img width="569" height="290" alt="image" src="https://github.com/user-attachments/assets/3bed6b76-91ee-47b8-9162-e5d06f628a78" />



---

###  Administrasi

#### 1. Hapus Akun

**Input:**

Masukkan Password Admin: unmul123

<img width="602" height="331" alt="image" src="https://github.com/user-attachments/assets/89642cd0-323f-4f26-84c1-1744f2029a3f" />



**Output:**

Akun Karyawan 'karyawan3' berhasil dihapus.



### 📝 Registrasi Akun Baru

Interface untuk membuat akun baru (Manager, Karyawan, atau Kostumer).

**Input:**

<img width="582" height="335" alt="image" src="https://github.com/user-attachments/assets/f774089b-3744-4d9d-a0d3-bb1818974a4f" />



**Output:**

Registrasi sukses! Akun Karyawan baru telah ditambahkan.




**Library yang Digunakan:**
- `prettytable` - Membuat tampilan tabel data yang rapi dan terstruktur
- `pwinput` - Input password tersembunyi untuk keamanan
- `json` - Parsing dan manipulasi data JSON 
- `os` - Operasi sistem seperti clear screen
- `time` - Delay dan timestamp
- `datetime` - Menangani data tanggal

### 3. Struktur File
Pastikan semua file JSON berada dalam direktori yang sama dengan `ReservasiHotel.py`:

<img width="160" height="160" alt="image" src="https://github.com/user-attachments/assets/23440c61-db44-459d-8afe-a118bf345ad3" />




## Penjelasan Output Program

### 📊 Tabel Reservasi
Menampilkan semua data reservasi aktif dalam format tabel dengan kolom:
- **No:** Nomor urut reservasi
- **Nama Tamu:** Identitas pemesan
- **Nomor Kamar:** Kamar yang dipesan (1-10)
- **Durasi:** Lama menginap dalam hari
- **Total Harga:** Biaya total dengan format currency (Rp)

**Contoh Output:**
<img width="460" height="351" alt="image" src="https://github.com/user-attachments/assets/2902f5ed-412e-48b1-b3cd-d138aa433966" />




### Tabel Status Kamar
Visualisasi real-time ketersediaan 10 kamar hotel:
- **Kamar:** Nomor kamar (1-10)
- **Status:** "Tersedia" atau "Ditempati"

**Contoh Output:**

<img width="173" height="310" alt="image" src="https://github.com/user-attachments/assets/5dfbcdf9-4cfe-4070-9ed5-c37fd2a723e7" />


### Tabel Harga Kamar
Informasi pricing berdasarkan lokasi:
- **Lantai 1 (Kamar 1-5):** Rp 300.000/malam
- **Lantai 2 (Kamar 6-10):** Rp 600.000/malam

**Contoh Output:**

<img width="343" height="140" alt="image" src="https://github.com/user-attachments/assets/19a3e828-83a1-4082-abcc-b37ccf59d450" />


---

### Struk Pembelian
Dokumen digital yang diberikan setelah pembayaran berhasil, berisi:
- Nama tamu
- Tanggal transaksi
- Lantai kamar
- Harga per malam
- Durasi menginap
- Total biaya (sudah termasuk diskon jika VIP)

**Contoh Output:**
<img width="382" height="263" alt="image" src="https://github.com/user-attachments/assets/a3e81a68-26f1-47d2-abaf-303c59c457be" />

---

---

### Error Handling
Output menangani untuk berbagai kondisi error atau validasi.

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
---

### Status Tertolak Dalam Percobaan Login
Program menampilkan status pemrosesan dan delay untuk pengguna dalam percobaan login.

**Contoh Output:**

<img width="396" height="76" alt="image" src="https://github.com/user-attachments/assets/262588a8-ec89-464a-aa2c-799a0dbabb02" /> <br>

<img width="387" height="78" alt="image" src="https://github.com/user-attachments/assets/015b9b48-4f0d-4c0c-aa82-c3bb6edd123e" /> <br>

<img width="389" height="74" alt="image" src="https://github.com/user-attachments/assets/e65442fd-8bfa-45a4-8591-941ac87794f9" />


# Keluar sistem
<img width="722" height="46" alt="image" src="https://github.com/user-attachments/assets/856a634f-0fb8-4192-986d-91a2f91515df" />





---

 
