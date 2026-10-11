## Identitas

- Nama           : [Uziel Askarillah saputra]
- NPM            : [4525210075]
- Mata Kuliah    : [Praktikum PBO-A]
- Dosen Pengampu : [Adi Wahyu Pribadi, S.Si., M.Kom]

---

---

## Mahasiswa.java

### Sebelum

[Lihat kode Mahasiswa.java sebelum](../../materi&codingan-sebelumDibenarin/pert02/java/Mahasiswa.java).


Pada versi awal, `Mahasiswa.java` masih berupa kerangka kode dengan tujuh bagian TODO yang harus diselesaikan. Pekerjaannya mencakup:

1. Mendeklarasikan atribut. `nim` dan `nama` menggunakan `final` karena nilainya harus tetap, sementara nilai tugas, UTS, dan UAS masih dapat berubah.
2. Memvalidasi NIM agar nilai `null` atau teks kosong ditolak melalui `IllegalArgumentException` dengan pesan yang jelas.
3. Memastikan nilai tugas, UTS, dan UAS berada pada rentang 0 sampai 100.
4. Membuat method privat `pastikanNilaiSah` agar validasi nilai bisa digunakan ulang dan tidak perlu ditulis tiga kali.
5. Menghitung `nilaiAkhir()` menggunakan konstanta bobot: tugas 30%, UTS 30%, dan UAS 40%.
6. Menentukan `hurufMutu()` dengan ketentuan nilai >= 80 mendapat A, >= 70 B, >= 60 C, >= 50 D, dan selebihnya E.
7. Menyediakan getter yang diperlukan tanpa membuat method `setNim()`.

### Setelah

[Lihat kode Mahasiswa.java setelah](src/java/Mahasiswa.java).

Setelah diselesaikan, kelas `Mahasiswa.java` sudah menerapkan validasi dan perhitungan nilai sesuai aturan.

- Atribut `nim` dan `nama` ditetapkan sebagai `private final`, sehingga nilainya tidak dapat diubah setelah objek dibuat.
- Constructor mengecek apakah NIM bernilai `null` atau kosong setelah diproses dengan `trim()`. Jika tidak valid, program melempar `IllegalArgumentException("NIM tidak boleh kosong atau null")` sebelum mengisi atribut.
- Method `pastikanNilaiSah(namaKomponen, nilai)` dipanggil untuk ketiga komponen nilai. Pesan kesalahan menyebut komponen yang bermasalah, rentang yang diperbolehkan, dan nilai yang dimasukkan.
- Method `nilaiAkhir()` menggunakan konstanta `BOBOT_TUGAS`, `BOBOT_UTS`, dan `BOBOT_UAS`, bukan angka bobot yang ditulis langsung dalam method.
- Method `hurufMutu()` memeriksa kategori nilai melalui rangkaian `if`, dimulai dari nilai tertinggi.
- Getter yang tersedia yaitu `getNim()`, `getNama()`, dan `getNilaiAkhir()`. Tidak adanya `setNim()` menjaga agar NIM tidak bisa diganti.

---

## Main.java

### Sebelum

[Lihat kode Main.java sebelum](../../materi&codingan-sebelumDibenarin/pert02/java/Main.java).

`Main.java` berperan sebagai program pengujian. Program membuat tiga objek mahasiswa dan menampilkan rekap nilai. Selanjutnya, program mencoba membuat objek dengan nilai 150 serta NIM kosong. Kedua masukan tersebut semestinya ditolak oleh proses validasi.

### Setelah

[Lihat kode Main.java setelah](pbo-A-UzielAskarillahSaputra-25075/pertemuan02/src/java/Main.java).

Kode `Main.java` dibiarkan seperti semula sesuai instruksi. Perubahan hasil terjadi karena implementasi `Mahasiswa.java` sudah dilengkapi. Dua blok `try-catch` menangkap `IllegalArgumentException` dan menampilkan pesan bahwa masukan tersebut ditolak.

---

## Mahasiswa.php

### Sebelum

[Lihat kode Mahasiswa.php sebelum](materi&codingan-sebelumDibenarin/pert02/php/Mahasiswa.php)

File PHP ini merupakan implementasi kelas mahasiswa dengan tujuan yang sama seperti versi Java, tetapi masih memiliki bagian TODO. Beberapa hal yang digunakan dalam versi PHP antara lain:

- Atribut dapat dideklarasikan melalui constructor property promotion. Kata kunci `readonly` membatasi perubahan nilai, dengan fungsi yang serupa dengan `final` pada Java.
- Validasi menggunakan exception `InvalidArgumentException`.
- Penentuan huruf mutu dapat menggunakan ekspresi `match (true) { ... }`.

### Setelah

[Lihat kode Mahasiswa.php setelah](pbo-A-UzielAskarillahSaputra-25075/pertemuan02/src/php/Mahasiswa.php)

Pada versi yang sudah dilengkapi, kelas PHP menerapkan validasi dan perhitungan nilai sebagai berikut.

- Atribut `nim` dan `nama` memakai `private readonly`, sehingga tidak dapat diubah setelah objek dibuat.
- Constructor memeriksa NIM kosong menggunakan `trim($nim) === ''`, lalu memanggil `self::pastikanNilaiSah()` untuk setiap nilai.
- Method `pastikanNilaiSah()` melempar `InvalidArgumentException` jika nilai tidak memenuhi batas. Pesan kesalahannya memuat nama komponen, rentang yang sah, dan nilai yang diterima.
- Method `nilaiAkhir()` menghitung nilai menggunakan konstanta `self::BOBOT_*`.
- Method `hurufMutu()` menggunakan `match (true)` dengan cabang `default` untuk menghasilkan E jika nilai tidak memenuhi kategori lainnya.
- Getter yang disediakan adalah `getNim()`, `getNama()`, dan `getNilaiAkhir()`. Method `setNim()` tidak tersedia.

---

## main.php

### Sebelum

[Lihat kode Main.php sebelum](materi&codingan-sebelumDibenarin/pert02/php/main.php)

`main.php` merupakan program uji untuk implementasi PHP. File ini memuat `Mahasiswa.php`, menampilkan rekap nilai tiga mahasiswa, kemudian mencoba memasukkan nilai 150 dan NIM kosong. Kedua kasus tersebut seharusnya menghasilkan penolakan.

### Setelah

[Lihat kode Main.php setelah](pbo-A-UzielAskarillahSaputra-25075/pertemuan02/src/php/main.php)

Kode `main.php` tetap sama seperti sebelumnya. Keluaran program menjadi sesuai harapan karena `Mahasiswa.php` telah dilengkapi. Blok `try-catch` menangani `InvalidArgumentException` dan menampilkan pesan penolakan untuk masukan yang tidak valid.

---

## Hasil Pengujian

### Sebelum diperbaiki (Java)

![Tampilan program sebelum perbaikan](ssan-sebelum/pert02/javasblm.jpeg)

Sebelum TODO diselesaikan, semua nilai akhir masih menunjukkan `0.00`, huruf mutu tampil sebagai `?`, dan program memunculkan pesan `MASALAH`. Ini menandakan nilai 150 dan NIM kosong belum ditangani sebagai masukan yang tidak sah.

### Setelah diperbaiki (Java)

![Tampilan program Java setelah perbaikan](ssan-setelah/pert02/javastlh(1).jpeg)

### Setelah diperbaiki (PHP)

![Tampilan program PHP setelah perbaikan](ssan-setelah/pert02/phpstlh.jpeg)

### Kesimpulan

Sesudah semua TODO diselesaikan, versi Java dan PHP menghasilkan keluaran yang sepadan. Nilai akhir Ani adalah 84.90 dengan huruf A, Budi memperoleh 59.30 dengan huruf D, sedangkan Citra memperoleh 92.00 dengan huruf A. Dua masukan yang melanggar aturan juga berhasil ditolak dengan pesan yang informatif.

Penerapan ini menunjukkan bahwa enkapsulasi dan validasi membantu mempertahankan aturan data (*invariant*) pada objek:

- NIM tidak dapat diubah setelah objek dibuat karena menggunakan `final` di Java atau `readonly` di PHP, serta tidak memiliki method `setNim()`.
- NIM kosong dan nilai di luar rentang 0–100 ditolak ketika constructor dijalankan, sehingga objek dengan data tidak valid tidak berhasil dibuat.
- Bobot penilaian didefinisikan sebagai konstanta. Jika bobot perlu diubah, penyesuaian cukup dilakukan pada definisi konstanta tersebut.
- Walaupun sintaks Java dan PHP berbeda, kedua bahasa tetap dapat menerapkan konsep validasi, perhitungan nilai, dan enkapsulasi yang sama.
