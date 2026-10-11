# Dokumentasi Perbandingan Program Sebelum dan Sesudah — PBO A

## 1. Susunan direktori proyek

Folder utama berisi dua bagian besar, yaitu kumpulan materi dan kode awal sebelum diperbaiki, serta repository Git yang berisi versi pengerjaan setelah dirapikan.

```text
pbo-a-UzielAskarillahSaputra-25075/
├── Materi-Pembelajaran&Codingan-sebelumdibenerin/      ← VERSI AWAL
│   └── codingansebelum/
│       ├── pertemuan02/   Mahasiswa.java, Main.java, Mahasiswa.php, main.php, Modul-Praktikum-02-*.docx
│       ├── pertemuan03/   RekeningBank.java, Main.java, RekeningBank.php, main.php
│       ├── pertemuan04/
│       │   ├── Pewarisan.zip
│       │   └── Pewarisan/
│       │       ├── java/  Pegawai, PegawaiTetap, PegawaiKontrak, Main (.java)
│       │       ├── php/   Pegawai.php, main.php
│       │       └── 1695367759.pptx, 1789524381.pptx
│       ├── pertemuan05/   BangunDatar, Lingkaran, Persegi, AntiPattern, Main (.java),
│       │                  BangunDatar.php, main.php, notifikasi.php, Modul-*.docx, *.pptx
│       └── pertemuan06/06-abstract-class-interface-enum-dan-trait/
│           ├── README.md, Modul-Praktikum-06-*.docx
│           └── starter/
│               ├── java/  Movable, Fuelable, Kendaraan, Mobil, TipeBahanBakar, Main (.java)
│               └── php/   abstraksi.php, main.php
│
└── pbo-a-MuhamadRashaZein-25042/                       ← VERSI SETELAH (repository Git)
    ├── prak01/  LAPORAN GIT & GITHUB_...docx / .pdf
    ├── prak02/  src/java, src/php, bin, .vscode
    ├── prak03/  src/java, src/php, bin, .vscode
    ├── prak04/  src/java, src/php, bin, .vscode, README.md
    ├── prak05/  src/java (+AntiPatternRefaktor, Segitiga, Trapesium), src/php, bin, .vscode
    └── prak06/  src/java (+Sepeda), src/php, bin, .vscode, README.md, keputusan.md
```

## 2. Menjalankan program versi awal

Jalankan perintah dari direktori `Materi-Pembelajaran&Codingan-sebelumdibenerin/codingansebelum/`. Karena nama salah satu folder mengandung karakter `&`, gunakan tanda kutip saat menuliskan path folder tersebut di terminal apabila diperlukan.

| Pertemuan | Java | PHP |
|---|---|---|
| 02 | `cd pertemuan02`<br>`javac *.java && java Main` | `php pertemuan02/main.php` |
| 03 | `cd pertemuan03`<br>`javac *.java && java Main` | `php pertemuan03/main.php` |
| 04 | `cd pertemuan04/Pewarisan/java`<br>`javac *.java && java Main` | `php pertemuan04/Pewarisan/php/main.php` |
| 05 | `cd pertemuan05`<br>`javac *.java && java Main` (opsi lain: `java AntiPattern`) | `php pertemuan05/main.php`<br>`php pertemuan05/notifikasi.php` |
| 06 | `cd pertemuan06/06-abstract-class-interface-enum-dan-trait/starter/java`<br>`javac *.java && java -Dfile.encoding=UTF-8 Main` | `php pertemuan06/06-abstract-class-interface-enum-dan-trait/starter/php/main.php` |

## 3. Menjalankan program versi setelah dirapikan

Untuk versi yang telah disusun ke dalam repository Git, masuk terlebih dahulu ke direktori `pbo-a-MuhamadRashaZein-25042/pbo-a-MuhamadRashaZein-25042/`.

| Pertemuan | Java | PHP |
|---|---|---|
| 02 | `cd prak02`<br>`javac -d bin src/java/*.java`<br>`java -cp bin Main` | `php src/php/main.php` |
| 03 | `cd prak03`, kemudian gunakan perintah kompilasi dan eksekusi Java yang sama seperti pertemuan 02 | `php src/php/main.php` |
| 04 | `cd prak04`, kemudian gunakan perintah kompilasi dan eksekusi Java yang sama seperti pertemuan 02 | `php src/php/main.php` |
| 05 | `cd prak05`<br>`javac -d bin src/java/*.java`<br>`java -cp bin Main`<br>Program tambahan: `java -cp bin AntiPattern` dan `java -cp bin AntiPatternRefaktor` | `php src/php/main.php`<br>`php src/php/BangunDatar.php`<br>`php src/php/notifikasi.php` |
| 06 | `cd prak06`<br>`javac -d bin src/java/*.java`<br>`java -Dfile.encoding=UTF-8 -cp bin Main` | `php src/php/main.php` |

**Catatan Windows:** Pada CMD, pola path Java dapat ditulis menggunakan garis miring terbalik, misalnya `src\java\*.java`. Jika karakter tertentu tidak muncul dengan benar, jalankan `chcp 65001` terlebih dahulu.

## 4. Perbandingan keluaran program dan dokumentasi screenshot

Catatan berikut merangkum keluaran yang dicatat setelah program dijalankan menggunakan JDK 21 dan PHP 8.3.

| Pertemuan | Kondisi versi awal | Kondisi versi setelah diperbaiki |
|---|---|---|
| 02 | Program Java dan PHP menghasilkan `akhir=0.00 mutu=?`. Ada dua pesan `MASALAH: ... seharusnya ditolak!` yang menunjukkan validasi belum berjalan sesuai harapan. | Keluaran nilai akhir menjadi `84.90 mutu=A`, `59.30 D`, dan `92.00 A`. Dua kasus yang tidak valid menampilkan pesan `Ditolak: ...`. |
| 03 | Java menunjukkan jumlah rekening `-1`, pesan masalah pada proses penarikan, dan bunga `Rp0.00`. PHP berhenti karena **Fatal error** dengan pesan `TODO 5 belum dikerjakan`. | Java menampilkan jumlah rekening `2`, menolak penarikan yang tidak memenuhi ketentuan, dan menghitung bunga `Rp37,500.00`. Untuk kondisi PHP, periksa catatan pada bagian 6. |
| 04 | Nilai gaji pada program Java dan PHP masih `Rp0`. | Java menampilkan gaji Ani sebesar `7,800,000` dengan total `12,800,000`. PHP menampilkan empat pegawai dengan total `26.440.000,00`. |
| 05 | Perhitungan luas atau keliling di Java dan PHP masih menunjukkan `0.00`. | Java menghasilkan luas Lingkaran `153.94`, Persegi `25.00`, dan jumlah `178.94`. PHP menambahkan Segitiga dengan nilai `6.00`, sehingga totalnya `184.94`. |
| 06 | Java masih memuat `(TODO 1 belum dikerjakan)` dan biaya `Rp0`. Pada PHP, label bahan bakar belum terisi (`?`) dan biayanya `Rp0`. | Java menampilkan Avanza dan Polygon dengan biaya `Rp540,000`. PHP menghitung biaya `Rp450.000` serta menampilkan bagian yang berkaitan dengan Trait. |

Untuk dokumentasi pertemuan 04 versi awal, sertakan juga tangkapan layar pesan kesalahan kompilasi dari percobaan yang tercatat di `catatan.md` apabila diminta dosen. Pada pertemuan 06 versi terbaru, dokumentasikan isi `keputusan.md` dan pesan error yang muncul ketika komentar pada pemanggilan `isiPenuh(sepeda)` dibuka.

## 5. Bagian versi terbaru yang masih perlu ditinjau

Beberapa hal berikut sebaiknya diperiksa kembali sebelum mengambil screenshot akhir agar hasil dokumentasi sesuai dengan kondisi program.

1. **PHP pada prak03:** Berkas `RekeningBank.php` masih berisi TODO. Selain itu, `main.php` tampaknya masih menggunakan salinan dari prak02 dan memanggil `Mahasiswa.php`, padahal berkas tersebut tidak tersedia pada prak03. Kondisi ini dapat menyebabkan *Fatal error*. Sesuaikan isi `main.php` dengan program `pertemuan03/main.php` pada direktori versi awal.
2. **Java pada prak03:** Constructor singkat belum meneruskan parameter melalui `this(nomor, pemilik, 0)`. Akibatnya, penghitung rekening tercatat `2`, sedangkan hasil yang diharapkan adalah `3`. Validasi untuk nomor rekening kosong dan saldo awal negatif juga belum tersedia.
3. **Java pada prak04:** `Main.java` baru memuat dua pegawai. Sementara itu, kelas `Dosen` dan `PegawaiHarian` baru ditemukan pada implementasi PHP.
4. **Java pada prak05:** Objek `Segitiga` dan `Trapesium` belum dimasukkan ke dalam array pada `Main.java`.
5. **Berkas `AntiPatternRefaktor.java` di prak05:** Format `"%.2f5n"` perlu diganti menjadi `"%.2f%n"`. Jika dibiarkan, keluaran dapat tertulis `184.945n`.
6. **prak06:** Tarif bahan bakar pada Java dan PHP belum sama. Java menggunakan bensin `12.000`, sedangkan PHP menggunakan bensin `10.000` dan solar `6.800`. Samakan nilai tarif apabila kedua bahasa perlu menghasilkan perhitungan yang sebanding.
7. **README prak04 dan prak06:** README bawaan VS Code sebaiknya diganti dengan dokumentasi yang sesuai dengan isi dan kebutuhan masing-masing proyek.
