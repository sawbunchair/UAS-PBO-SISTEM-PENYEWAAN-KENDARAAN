# Sistem Penyewaan Kendaraan

### Identitas Mahasiswa
* **Nama:** [NAJAMUDDIN SYIHAB]
* **NIM:** [251240001691]
* **Program Studi:** Teknik Informatika
* **Instansi:** Universitas Islam Nahdlatul Ulama (UNISNU) Jepara

---

### Ringkasan Proyek
Aplikasi ini merupakan sistem manajemen logistik dan administrasi persewaan kendaraan berbasis antarmuka baris perintah (CLI). Sistem dirancang dengan menerapkan pilar-pilar utama *Object-Oriented Programming* (OOP) di bahasa Dart untuk mengelola ketersediaan unit armada seperti Mobil dan Motor secara dinamis.

### Fitur Utama Aplikasi
1. **Registrasi Varian Kendaraan (Input Validatif):** Menambahkan armada Mobil atau Motor ke dalam sistem. Input plat nomor dan tarif sewa langsung diproteksi ketat menggunakan `SewaException` agar menghindari data kosong atau tidak logis.
2. **Cetak Manifes Armada (Polymorphism):** Menampilkan spesifikasi mendetail dan tarif per hari dari masing-masing jenis kendaraan yang terdaftar memanfaatkan konsep *method overriding*.
3. **Pelacakan Plat Nomor (Higher-Order Function):** Menyaring data armada secara instan berdasarkan potongan karakter plat nomor menggunakan fungsi `.where()`.
4. **Kalkulasi Potensi Omzet (Higher-Order Function):** Mengakumulasikan total tarif sewa harian seluruh kendaraan yang tersedia menggunakan fungsi `.fold()`.
5. **Sinkronisasi Cloud (Asynchronous):** Simulasi pengiriman dan pencadangan data lokal ke server pusat persewaan menggunakan mekanisme `async/await`.

---

### Arsitektur OOP & Struktur Kode
* **Encapsulation:** Mengamankan variabel sensitif seperti properti `_platNomor` dan `_tarifPerHari` menggunakan akses *private fields* serta gerbang *getter-setter*.
* **Inheritance:** Class `Mobil` dan `Motor` mewarisi karakteristik umum dari *abstract class* `Kendaraan`.
* **Collection:** Menampung kumpulan objek polimorfis ke dalam `List<Kendaraan>`.
* **Exception Handling:** Mengisolasi potensi *crash* program akibat kesalahan *user input* via blok *try-catch*.

---

### Cara Menjalankan Program
1. Pastikan perangkat Anda sudah terpasang **Dart SDK** dengan baik.
2. Buka aplikasi Terminal atau Command Prompt, lalu arahkan direktori ke folder utama proyek ini[cite: 1]:
   ```bash
   cd project_uas
