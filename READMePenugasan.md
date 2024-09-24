# Smart Secure Home

## Deskripsi Proyek
Proyek **Security Home dengan IoT** adalah solusi keamanan rumah berbasis Internet of Things (IoT) yang memungkinkan pemilik rumah memantau dan mengelola sistem keamanan dari jarak jauh melalui aplikasi web dan mobile. Sistem ini dilengkapi dengan fitur canggih untuk melindungi rumah dari ancaman.

## Fitur Utama

### 1. Keamanan Koneksi
- **HTTPS (SSL/TLS):** Mengamankan komunikasi data antara server dan klien.
- **WebSockets untuk Alarm:** Notifikasi alarm real-time saat terjadi kejadian mencurigakan.

### 2. Komunikasi Perangkat
- **RabbitMQ:** Middleware untuk komunikasi cepat antar perangkat IoT.

### 3. Manajemen Data
- **MongoDB:** Penyimpanan data tidak terstruktur seperti log aktivitas.
- **PostgreSQL:** Menyimpan data terstruktur seperti informasi pengguna.

### 4. Aplikasi Admin
- Backend dengan *Spring Framework* dan frontend menggunakan Angular.
- Fitur: manajemen pengguna, konfigurasi properti, dan pengelolaan sertifikat keamanan.

### 5. Aplikasi Smart-Home
- Notifikasi alarm, pengolahan pesan dari perangkat, dan laporan kejadian.

### 6. Aplikasi Perangkat
- Mensimulasikan sinyal perangkat keamanan untuk pengujian sistem.

### 7. Manajemen Alarm dengan Drools Rules
- Mengelola logika kompleks terkait alarm dengan engine Drools.

### 8. Pengujian Keamanan
- Mematuhi standar keamanan OWASP dan melakukan pengujian penetrasi dengan OWASP ZAP dan Burp Suite Pro.

## Software yang Digunakan
- **OWASP ZAP:** Alat pengujian keamanan web.
- **Burp Suite Pro:** Suite alat untuk analisis keamanan aplikasi web.

## Instalasi dan Penggunaan

### Hal yang dibutuhkan
- Java 11 atau lebih baru
- Node.js dan npm
- Docker (untuk RabbitMQ dan MongoDB)
- PostgreSQL
- Angular CLI

### kesimpulan
Proyek Security Home dengan IoT menawarkan sistem keamanan rumah yang canggih dan fleksibel, memanfaatkan teknologi IoT untuk memberikan pemilik rumah kendali penuh atas keamanan mereka. Dengan fitur notifikasi real-time dan manajemen perangkat yang efisien, proyek ini menjawab kebutuhan akan sistem keamanan modern yang dapat diakses dari mana saja.


## Source
https://github.com/njmarko/smart-secure-home

