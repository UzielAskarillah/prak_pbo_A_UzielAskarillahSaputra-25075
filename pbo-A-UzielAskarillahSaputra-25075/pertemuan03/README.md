# Praktikum 03 — Constructor, Anggota Statis, dan Konstanta

**Nama:** Uziel askarilla saputra
**NPM:** 4525210075
**Kelas:** PBO A 2025/2026  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom

## File RekeningBank.java

### Sebelum

[Lihat source code RekeningBank.java versi awal](materi&codingan-sebelumDibenarin\pert03\java\RekeningBank.java).

**Pekerjaan yang harus diselesaikan:** melengkapi deklarasi konstanta, pengelolaan jumlah rekening, delegasi constructor, validasi saldo dan transaksi, biaya administrasi, serta mekanisme perhitungan bunga. Pada kode awal, masih terdapat beberapa bagian TODO dan nilai penghitung rekening belum sesuai dengan yang diharapkan.

### Setelah

[Lihat source code RekeningBank.java setelah perbaikan](pbo-A-UzielAskarillahSaputra-25075\pertemuan 3\src\java\RekeningBank.java).

Pada versi ini, constructor dan berbagai operasi rekening telah dilengkapi dengan pemeriksaan validitas serta penggunaan konstanta. Constructor dengan parameter yang lebih sederhana juga diarahkan ke constructor lengkap melalui mekanisme delegasi, sehingga proses inisialisasi menjadi lebih terstruktur.

## File RekeningBank.php

### Sebelum

[Lihat source code RekeningBank.php versi awal](materi&codingan-sebelumDibenarin\pert03\php\RekeningBank.php).

**Pekerjaan yang harus diselesaikan:** mengimplementasikan pengelolaan rekening menggunakan PHP, termasuk pemeriksaan data, pencatatan jumlah rekening secara statis, serta proses penyetoran dan penarikan uang.

### Setelah

[Lihat source code RekeningBank.php setelah perbaikan](pbo-A-UzielAskarillahSaputra-25075\pertemuan03\src\php\RekeningBank.php).

Implementasi PHP telah dilengkapi dengan constructor yang memungkinkan saldo awal bersifat opsional, named constructor, dan validasi untuk setiap transaksi. Selain itu, konstanta serta method statis digunakan untuk mendukung pengelolaan data rekening.

## Hasil Pengujian

### Java — Sebelum Perbaikan

![Hasil pengujian Java sebelum perbaikan](ssan-sebelum\pert03\javasblm.jpeg)

### Java — Setelah Perbaikan

![Hasil pengujian Java setelah perbaikan](ssan-setelah\pert03\javastlh.jpeg)

### PHP — Sebelum Perbaikan

![Hasil pengujian PHP sebelum perbaikan](ssan-sebelum\pert03\phpsblm.jpeg)

### PHP — Setelah Perbaikan

![Hasil pengujian PHP setelah perbaikan](ssan-setelah\pert03\mainphp2.jpeg)

## Kesimpulan

Berdasarkan hasil pengujian, implementasi PHP berhasil membuat tiga rekening dan menjalankan operasi sesuai dengan ketentuan yang diterapkan. Sementara itu, pada keluaran Java setelah perbaikan, jumlah rekening yang tercatat masih bernilai 2, bukan 3. Dengan demikian, hasil tersebut menunjukkan bahwa bagian penghitung rekening pada Java masih perlu ditinjau kembali agar sesuai dengan hasil yang diharapkan.