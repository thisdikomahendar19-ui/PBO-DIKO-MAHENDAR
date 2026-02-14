# 🚀 QUICK START GUIDE
# Sistem Informasi Perpustakaan Digital

Panduan cepat untuk memulai menggunakan sistem perpustakaan.

---

## 📋 Checklist Persiapan

Sebelum memulai, pastikan Anda sudah:

- [ ] Install Java JDK 11 atau lebih tinggi
- [ ] Install MariaDB Server
- [ ] Download atau clone project ini
- [ ] Install Maven (optional, tapi direkomendasikan)

---

## ⚡ 5 Menit Setup

### Step 1: Database Setup (2 menit)

```bash
# Buka terminal/command prompt
# Login ke MariaDB
mysql -u root -p

# Ketik password root Anda, lalu:
CREATE DATABASE perpustakaan_db;
exit

# Import schema
mysql -u root -p perpustakaan_db < database/schema.sql
```

### Step 2: Konfigurasi (1 menit)

Edit file `src/main/java/com/perpustakaan/util/DatabaseConnection.java`

Ubah line ini sesuai setup Anda:
```java
private static final String PASSWORD = "your_password";  // Ganti dengan password database Anda
```

### Step 3: Build & Run (2 menit)

```bash
# Di folder project, jalankan:
mvn clean package

# Tunggu sampai selesai, lalu:
java -jar target/PerpustakaanDigital-1.0.0.jar
```

### Step 4: Login

Aplikasi akan terbuka. Login dengan:
- **Username**: `admin`
- **Password**: `admin123`

✅ **Done! Aplikasi siap digunakan.**

---

## 🎯 Fitur Cepat

### Tambah Buku Baru
1. Klik menu "Data Buku"
2. Klik tombol "Tambah"
3. Isi form
4. Klik "Simpan"

### Tambah Anggota
1. Klik menu "Data Anggota"
2. Klik tombol "Tambah"
3. Isi form
4. Klik "Simpan"

### Proses Peminjaman
1. Klik menu "Peminjaman"
2. Pilih anggota
3. Pilih buku
4. Tentukan tanggal jatuh tempo
5. Klik "Proses Peminjaman"

### Proses Pengembalian
1. Klik menu "Peminjaman"
2. Tab "Riwayat Peminjaman"
3. Pilih peminjaman yang aktif
4. Klik "Kembalikan"
5. Sistem akan hitung denda otomatis

---

## 🔍 Troubleshooting Cepat

### ❌ "Cannot connect to database"

**Solusi:**
```bash
# Pastikan MariaDB running
# Windows: Services → MariaDB → Start
# Linux: sudo systemctl start mariadb
# macOS: brew services start mariadb
```

### ❌ "Driver not found"

**Solusi:**
```bash
# Re-download dependencies
mvn clean install -U
```

### ❌ "Access denied"

**Solusi:**
Cek username & password di `DatabaseConnection.java`

---

## 📖 Dokumentasi Lengkap

Baca dokumentasi detail di:
- `README.md` - Overview dan fitur
- `INSTALLATION.md` - Panduan instalasi lengkap
- `PROJECT_SUMMARY.md` - Ringkasan teknis proyek
- `docs/Dokumentasi_Sistem_Perpustakaan.docx` - Dokumentasi lengkap format buku

---

## 💡 Tips

1. **Backup Database**
   ```bash
   mysqldump -u root -p perpustakaan_db > backup_$(date +%Y%m%d).sql
   ```

2. **Ubah Password Default**
   Segera ubah password admin setelah login pertama!

3. **Export Laporan**
   Gunakan tombol "Export PDF" atau "Export Excel" di menu Laporan

---

## 🆘 Butuh Bantuan?

- 📧 Email: support@perpustakaan.com
- 🐛 GitHub Issues: [Report Bug]
- 📚 Dokumentasi: Folder `docs/`

---

**Happy Coding! 🎉**
