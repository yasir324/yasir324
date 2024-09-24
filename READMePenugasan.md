
# Security Home dengan IoT

Proyek **Security Home dengan IoT** adalah sebuah solusi keamanan rumah berbasis Internet of Things (IoT) yang memungkinkan pemilik rumah untuk memantau dan mengelola sistem keamanan rumah mereka dari jarak jauh melalui aplikasi web dan mobile. Sistem ini dilengkapi dengan berbagai fitur canggih seperti notifikasi alarm real-time, manajemen perangkat, serta pengujian keamanan untuk memastikan bahwa sistem aman dari ancaman cyber.

## Fitur Utama

### 1. **Keamanan Koneksi**
   - **HTTPS (SSL/TLS):** Semua komunikasi antara server dan klien dilindungi dengan protokol SSL/TLS untuk memastikan keamanan data yang dikirimkan.
   - **WebSockets untuk Alarm:** Sistem mendukung WebSocket untuk pengiriman notifikasi alarm secara real-time kepada pengguna ketika terjadi kejadian mencurigakan di rumah.

### 2. **Komunikasi Perangkat**
   - **RabbitMQ:** Sistem menggunakan RabbitMQ sebagai middleware untuk komunikasi antara perangkat IoT yang terhubung dengan aplikasi smart-home. Ini memungkinkan data perangkat untuk dikirim dan diterima dengan cepat dan efisien.

### 3. **Manajemen Data**
   - **MongoDB:** Penyimpanan data tidak terstruktur, seperti log aktivitas dan informasi perangkat, dikelola oleh MongoDB. Database ini cocok untuk menyimpan data berbasis dokumen yang fleksibel.
   - **PostgreSQL:** Untuk data yang lebih terstruktur seperti informasi pengguna, konfigurasi properti, dan pengaturan alarm, sistem menggunakan PostgreSQL.

### 4. **Aplikasi Admin**
   - **Backend:** Dibangun menggunakan *Spring Framework*, yang menyediakan layanan REST API untuk pengelolaan sistem backend.
   - **Frontend:** Dibangun dengan Angular untuk pengalaman pengguna yang dinamis dan responsif.
   - **Fitur Utama:**
     - **Pembuatan CSR (Certificate Signing Request):** Aplikasi admin memungkinkan administrator untuk membuat CSR yang diperlukan untuk penerbitan sertifikat SSL/TLS.
     - **Pembuatan dan Pengelolaan Sertifikat:** Fitur ini memungkinkan administrator mengelola sertifikat keamanan untuk komunikasi yang aman antara perangkat dan server.
     - **Manajemen Pengguna:** Admin dapat mengelola akses pengguna, termasuk pembuatan akun baru, pengelolaan izin akses, dan penghapusan akun jika diperlukan.
     - **Konfigurasi Real Estate:** Sistem memungkinkan konfigurasi properti, yang mencakup penambahan dan pengelolaan informasi real estate yang dilindungi oleh sistem keamanan.
     - **Konfigurasi Perangkat:** Admin dapat menambahkan, menghapus, atau mengatur perangkat yang terhubung di setiap properti.
     - **Konfigurasi Alarm:** Pengaturan alarm yang fleksibel dapat disesuaikan untuk mendeteksi kejadian tertentu di rumah berdasarkan parameter yang telah ditentukan.
     - **Notifikasi Alarm Real-Time:** Ketika terjadi pelanggaran keamanan, notifikasi akan dikirimkan secara langsung ke aplikasi admin melalui WebSocket.
     - **Log Aktivitas:** Semua aktivitas yang terkait dengan sistem dicatat dalam log untuk tujuan audit dan pemantauan.

### 5. **Aplikasi Smart-Home**
   - **Backend:** Sistem backend dibangun dengan *Spring Framework* untuk menyediakan layanan REST API bagi aplikasi mobile dan web.
   - **Frontend:** Aplikasi pengguna dibangun dengan Angular, memberikan UI yang intuitif dan responsif.
   - **Fitur Utama:**
     - **Notifikasi Alarm Real-Time:** Pengguna menerima notifikasi langsung di aplikasi mobile atau web ketika alarm terpicu.
     - **Pesan Objek dari Perangkat:** Sistem menerima dan memproses pesan dari perangkat IoT yang memberikan informasi status atau kondisi lingkungan rumah.
     - **Laporan Alarm Berdasarkan Waktu:** Pengguna dapat menghasilkan laporan alarm berdasarkan periode waktu tertentu untuk memantau kejadian di rumah.

### 6. **Aplikasi Perangkat**
   - **Backend:** Dibangun dengan *Spring Framework*, aplikasi ini mensimulasikan sinyal perangkat keamanan yang terhubung ke sistem.
   - **Simulasi Sinyal Perangkat:** Sistem mensimulasikan sinyal dari perangkat seperti sensor gerak, kamera, dan perangkat keamanan lainnya untuk menguji dan memverifikasi fungsionalitas sistem.

### 7. **Manajemen Alarm dengan Drools Rules**
   - **Rules KJAR (Knowledge JAR):** Proyek ini menggunakan Drools sebagai engine rule untuk mengelola logika kompleks terkait alarm.
   - **Templates dan Complex Event Processing (CEP):** Sistem menggunakan template dan *Complex Event Processing* untuk mendeteksi dan merespon pola-pola yang terjadi dalam data perangkat secara real-time.
   - **Device-Rules KJAR:** Mengatur logika terkait alarm yang dipicu dari perangkat IoT, dengan kemampuan untuk memproses event secara kompleks.

### 8. **Pengujian Keamanan**
   - Sistem ini dirancang dengan mempertimbangkan isu-isu keamanan teratas dari OWASP (*Open Web Application Security Project*), termasuk potensi serangan seperti *SQL Injection*, *Cross-Site Scripting (XSS)*, *Cross-Site Request Forgery (CSRF)*, dan lainnya.
   - **Pengujian Penetrasi:** Pengujian keamanan aplikasi dilakukan secara menyeluruh menggunakan alat-alat seperti OWASP ZAP dan Burp Suite Pro untuk memastikan bahwa aplikasi ini tahan terhadap serangan cyber yang umum.

## Software yang Digunakan
- **OWASP ZAP:** Alat otomatisasi pengujian keamanan web untuk mengidentifikasi kerentanan dalam aplikasi web.
- **Burp Suite Pro:** Suite alat yang digunakan untuk menguji keamanan aplikasi web melalui analisis lalu lintas HTTP, pemindaian kerentanan, dan manipulasi permintaan.
  
## Instalasi dan Penggunaan

### 1. Prasyarat
Pastikan Anda telah menginstal perangkat lunak berikut sebelum memulai:
- Java 11 atau lebih baru
- Node.js dan npm
- Docker (untuk menjalankan RabbitMQ dan MongoDB)
- PostgreSQL
- Angular CLI

### 2. Langkah Instalasi
1. **Clone repositori** ini ke mesin lokal Anda:
   ```
   git clone https://github.com/nama-user/security-home-iot.git
   ```
2. **Backend:** Masuk ke direktori backend dan jalankan:
   ```
   cd backend
   ./mvnw spring-boot:run
   ```
3. **Frontend:** Masuk ke direktori frontend dan jalankan:
   ```
   cd frontend
   npm install
   ng serve
   ```
4. **Jalankan RabbitMQ dan MongoDB** menggunakan Docker:
   ```
   docker-compose up
   ```

### 3. Konfigurasi Database
Konfigurasikan PostgreSQL dan MongoDB dengan skema yang sesuai untuk mendukung aplikasi.

### 4. Jalankan Aplikasi
Aplikasi sekarang dapat diakses melalui browser di `http://localhost:4200` untuk frontend dan `http://localhost:8080` untuk backend API.


