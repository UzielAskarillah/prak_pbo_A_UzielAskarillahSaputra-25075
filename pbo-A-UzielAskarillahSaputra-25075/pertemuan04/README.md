# Praktikum 04 — Pewarisan (Inheritance)

**Nama:** Uziel askarillah saputra
**NPM:** 4525210075  
**Kelas:** PBO A 2025/2026  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom

### File PegawaiTetap.java

### Sebelum

[Lihat source code PegawaiTetap.java versi awal](materi&codingan-sebelumDibenarin/pert04/pewarisan/java/PegawaiTetap.java).

**Tugas yang dikerjakan:** menerapkan konsep pewarisan dari kelas `Pegawai`, menggunakan `super` untuk menginisialisasi bagian constructor milik kelas induk, serta menghitung tunjangan masa kerja sebesar 2% untuk setiap tahun dengan batas tertinggi 40%.

### Setelah

[Lihat source code PegawaiTetap.java setelah perbaikan](pbo-A-UzielAskarillahSaputra-25075\pertemuan04\src\java\PegawaiTetap.java).

Pada versi yang telah diperbaiki, constructor memanggil constructor dari kelas induk menggunakan `super`. Perhitungan gaji dilakukan dengan mengambil hasil `super.hitungGaji()` sebagai gaji pokok perhitungan, kemudian menambahkan tunjangan berdasarkan lama masa kerja pegawai.

## File Pegawai.php

### Sebelum

[Lihat source code Pegawai.php versi awal](materi&codingan-sebelumDibenarin\pert04\pewarisan\php\Pegawai.php).

**Tugas yang dikerjakan:** menyusun hubungan pewarisan antarkelas pegawai dan melengkapi mekanisme penghitungan gaji untuk beberapa jenis pegawai, yaitu pegawai tetap, pegawai kontrak, dosen, dan pegawai harian.

### Setelah

[Lihat source code Pegawai.php setelah perbaikan](pbo-A-UzielAskarillahSaputra-25075\pertemuan04\src\php\Pegawai.php).

Implementasi PHP telah mencakup kelas abstrak `Pegawai` beserta kelas-kelas turunannya. Setiap jenis pegawai memiliki aturan penggajian tersendiri. Pegawai tetap memperoleh tunjangan berdasarkan masa kerja, dosen mendapatkan tunjangan fungsional, sedangkan gaji pegawai harian ditentukan berdasarkan jumlah hari kerja.

## Hasil Pengujian

### Java — Sebelum Perbaikan

![Keluaran Java sebelum perbaikan](ssan-sebelum\pert04\javasblm.jpeg)

### Java — Setelah Perbaikan

[Lihat source code Main.java setelah perbaikan](ssan-setelah\pert04\Main.java)

### PHP — Sebelum Perbaikan

![Keluaran PHP sebelum perbaikan](ssan-sebelum\pert04\phpsblm.jpeg)

### PHP — Setelah Perbaikan

[Lihat source code Main.php setelah perbaikan](ssan-setelah\pert04\main.php)

### Kesimpulan

Penerapan pewarisan memungkinkan kelas turunan memanfaatkan atribut dan method yang tersedia pada kelas induk, kemudian menambahkan ketentuan sesuai kebutuhan masing-masing jenis pegawai. Berdasarkan hasil pengujian setelah perbaikan, perhitungan gaji sudah menghasilkan nilai sesuai implementasi program dan tidak lagi seluruhnya menunjukkan angka nol.