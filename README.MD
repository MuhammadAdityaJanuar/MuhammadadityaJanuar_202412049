# 📚 Sistem Perpustakaan (OOP Python)

Program ini merupakan simulasi sederhana sistem perpustakaan yang dibangun menggunakan konsep **Object-Oriented Programming (OOP)** dalam bahasa Python.  
Program ini menerapkan konsep:

- Encapsulation (Public, Protected, Private)
- Association
- Aggregation
- Composition
- Instansiasi objek
- Interaksi antar objek OOP

---

## 🔧 1. Struktur Class

### **1.1 Class Buku**
Atribut:
- Public: `judul`, `penulis`, `kode_buku`
- Protected: `_stok`
- Private: `__lokasi_rak`

Method:
- `get_lokasi_rak()`
- `set_lokasi_rak()`
- `tambah_stok()`
- `kurangi_stok()`
- `info()`

---

### **1.2 Class Peminjaman** (Association dengan Buku)
Atribut:
- `buku`
- `tanggal_pinjam`
- `tanggal_kembali`
- `status`

Method:
- `info()`

---

### **1.3 Class Anggota** (Aggregation dengan Peminjaman)
Atribut:
- Public: `id_anggota`, `nama`
- Protected: `_maks_pinjam`
- Private: `__status_aktif`
- Aggregation: `daftar_peminjaman`

Method:
- `pinjam_buku()`
- `kembalikan_buku()`
- `info_anggota()`
- `info_peminjaman()`

---

### **1.4 Class Perpustakaan** (Composition dengan Buku)
Atribut:
- `nama`
- `daftar_buku`

Method:
- `tambah_buku()`
- `tampilkan_buku()`

---

## 🏛 2. Relasi Antar Class

| Class ↔ Class | Jenis Relasi | Penjelasan |
|---------------|--------------|------------|
| Buku ↔ Peminjaman | Association | Peminjaman menyimpan referensi objek Buku |
| Anggota ↔ Peminjaman | Aggregation | Anggota memiliki daftar peminjaman |
| Perpustakaan ↔ Buku | Composition | Buku dibuat dan dimiliki sepenuhnya oleh Perpustakaan |

---

## 🧪 3. Demo Program

Program mendemonstrasikan:
- Pembuatan **3 buku**
- Pembuatan **2 anggota**
- Anggota 1 meminjam 2 buku
- Anggota 2 meminjam 1 buku
- Proses **pengembalian buku**
- Menampilkan informasi:
  - Daftar buku & stok
  - Daftar peminjaman setiap anggota

---

## 📌 4. Fitur Utama

- Manajemen stok buku
- Simulasi proses peminjaman dan pengembalian
- Validasi jumlah pinjaman anggota
- Penyimpanan data peminjaman per anggota
- Relasi antar objek sesuai konsep OOP

---

## ▶️ 5. Cara Menjalankan Program

1. Pastikan Python sudah terinstall minimal versi **3.8+**
2. Jalankan perintah:

```bash
python perpus.py
