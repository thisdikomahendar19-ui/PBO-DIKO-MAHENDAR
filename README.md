# PBO-PerpustakaanDigital

Sistem Informasi Perpustakaan Digital - Aplikasi Desktop berbasis Java

## 📖 Deskripsi

Sistem Informasi Perpustakaan Digital adalah aplikasi desktop yang dikembangkan menggunakan Java Swing dan MariaDB untuk mengelola operasional perpustakaan secara digital. Aplikasi ini menyediakan fitur lengkap untuk manajemen buku, anggota, peminjaman, pengembalian, dan laporan.

## 🎯 Fitur Utama

### 1. Manajemen Buku
- Tambah, ubah, hapus data buku
- Pencarian buku berdasarkan kode, judul, atau pengarang
- Kategorisasi buku
- Tracking stok buku tersedia

### 2. Manajemen Anggota
- Registrasi anggota baru
- Update data anggota
- Status keanggotaan (Aktif/Nonaktif/Suspended)
- Tracking masa berlaku keanggotaan

### 3. Transaksi Peminjaman
- Proses peminjaman buku
- Pengembalian buku
- Sistem denda otomatis untuk keterlambatan
- Riwayat peminjaman

### 4. Laporan
- Laporan data buku
- Laporan peminjaman
- Statistik perpustakaan
- Export ke PDF dan Excel

### 5. Manajemen Petugas
- Multi-level user (Admin & Petugas)
- Autentikasi login
- Manajemen hak akses

## 🛠️ Teknologi yang Digunakan

- **Bahasa Pemrograman**: Java 11
- **GUI Framework**: Java Swing
- **Database**: MariaDB
- **Build Tool**: Maven
- **Libraries**:
  - MariaDB JDBC Driver 3.1.4
  - JCalendar 1.4
  - iText PDF 5.5.13.3
  - Apache POI 5.2.3

## 📋 Prasyarat

Sebelum menjalankan aplikasi, pastikan sudah terinstal:

1. **Java Development Kit (JDK) 11** atau lebih tinggi
   - Download: https://www.oracle.com/java/technologies/downloads/
   
2. **MariaDB Server**
   - Download: https://mariadb.org/download/
   
3. **Maven** (optional, untuk build)
   - Download: https://maven.apache.org/download.cgi

4. **IDE** (pilih salah satu):
   - IntelliJ IDEA
   - Eclipse
   - NetBeans

## 🚀 Instalasi dan Konfigurasi

### 1. Clone Repository

```bash
git clone https://github.com/username/PBO-PerpustakaanDigital.git
cd PBO-PerpustakaanDigital
```

### 2. Setup Database

1. Buat database baru di MariaDB:
```sql
CREATE DATABASE perpustakaan_db;
```

2. Import schema database:
```bash
mysql -u root -p perpustakaan_db < database/schema.sql
```

Atau jalankan file `database/schema.sql` melalui phpMyAdmin atau HeidiSQL.

### 3. Konfigurasi Koneksi Database

Edit file `src/main/java/com/perpustakaan/util/DatabaseConnection.java`:

```java
private static final String URL = "jdbc:mariadb://localhost:3306/perpustakaan_db";
private static final String USER = "root";
private static final String PASSWORD = "your_password";
```

### 4. Build dan Run

#### Menggunakan Maven:
```bash
mvn clean package
java -jar target/PerpustakaanDigital-1.0.0.jar
```

#### Menggunakan IDE:
1. Import project sebagai Maven project
2. Run class `MainApp.java`

## 👤 Login Default

Setelah instalasi, gunakan kredensial berikut untuk login:

**Admin:**
- Username: `admin`
- Password: `admin123`

**Petugas:**
- Username: `petugas1`
- Password: `petugas123`

⚠️ **Penting**: Segera ubah password default setelah login pertama!

## 📁 Struktur Direktori

```
PBO-PerpustakaanDigital/
├── database/
│   ├── schema.sql              # Database schema
│   └── ERD.png                 # Entity Relationship Diagram
├── docs/
│   ├── Dokumentasi.docx        # Dokumentasi lengkap
│   ├── images/                 # Screenshot aplikasi
│   └── UML/                    # Diagram UML
├── src/
│   └── main/
│       └── java/
│           └── com/perpustakaan/
│               ├── model/      # Entity classes
│               ├── dao/        # Data Access Objects
│               ├── controller/ # Business logic
│               ├── view/       # GUI classes
│               ├── util/       # Utility classes
│               └── MainApp.java
├── pom.xml                     # Maven configuration
└── README.md                   # File ini
```

## 📊 Diagram UML

### Class Diagram
![Class Diagram](docs/UML/class-diagram.png)

### Use Case Diagram
![Use Case Diagram](docs/UML/usecase-diagram.png)

### Entity Relationship Diagram (ERD)
![ERD](database/ERD.png)

## 🖼️ Screenshot Aplikasi

### Login
![Login](docs/images/login.png)

### Dashboard
![Dashboard](docs/images/dashboard.png)

### Manajemen Buku
![Buku](docs/images/buku.png)

### Peminjaman
![Peminjaman](docs/images/peminjaman.png)

## 🤝 Kontribusi

Kontribusi sangat diterima! Untuk berkontribusi:

1. Fork repository ini
2. Buat branch baru (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

## 📝 Lisensi

Project ini dilisensikan di bawah MIT License - lihat file [LICENSE](LICENSE) untuk detail.

## 📧 Kontak

Nama Lengkap - [DIKOMAHENDAR](https://github.com/thisdikomahendar19-ui/PBO-DIKO-MAHENDAR)

Project Link: [https://github.com/username/PBO-PerpustakaanDigital](https://github.com/username/PBO-PerpustakaanDigital)

## 🙏 Acknowledgments

- Terima kasih kepada dosen dan asisten mata kuliah Pemrograman Berorientasi Objek
- Dokumentasi Java Swing
- MariaDB Documentation
- Stack Overflow Community

---

Dibuat dengan ❤️ untuk tugas Pemrograman Berorientasi Objek

