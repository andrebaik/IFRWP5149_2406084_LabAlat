## Kebutuhan tugas
| ID | Kebutuhan |
|---|---|
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik. |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya. |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan. |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa. |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |

## Batas dan asumsi
- Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02(Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetapmempunyai identitas berbeda.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Kalender akademik pada tugas ini adalah agenda resmi institusi (awal semester, batas KRS, masa ujian, dan sejenisnya); jangan menyamakannya dengan jadwal kuliah pada Pertemuan 2.
- Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut. Nilai yang diinput belum terpublikasi sebelum dinyatakan resmi oleh ketentuan tugas ini: KHS hanya menampilkan nilai yang sudah dipublikasikan.
- Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif. Ketentuan ini fiktif untuk latihan.
- Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif dari Pertemuan 3. Pembayaran dan perancangan basis data berada di luar tugas ini.
- Fungsi KRS dari Pertemuan 3 tetap ada pada diagram kumulatif.

## Katalog use case kumulatif
| ID | Nama | Aktor terkait | Kebutuhan | Status |
|---|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | SIA-R01 | Tetap, P02 |
| SIA-UC02 | Kelola Jadwal Kuliah | Admin Akademik | SIA-R02 | Tetap, P02 |
| SIA-UC03 | Ajukan KRS | Mahasiswa | SIA-R03 | Tetap, P03 |
| SIA-UC04 | Validasi KRS | Sistem | SIA-R04 | Tetap, P03 |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | SIA-R05 | Tetap, P03 |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | SIA-R06 | Tetap, P03 |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | SIA-R07 | Baru, P04 |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | SIA-R08 | Baru, P04 |
| SIA-UC09 | Lihat KHS | Mahasiswa | SIA-R09 | Baru, P04 |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | SIA-R10 | Baru, umum |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik | SIA-R11 | Baru, khusus |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik | SIA-R11 | Baru, khusus |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik | SIA-R11 | Baru, khusus |

## Generalization aktor
Civitas Akademika merupakan aktor umum. Mahasiswa dan Dosen merupakan aktor khusus yang mewarisi kemampuan melihat kalender akademik. Asosiasi ke SIA-UC07 hanya digambar satu kali dari Civitas Akademika. Admin Akademik dan Dosen Wali tetap menjadi aktor tersendiri.

## Generalization use case
SIA-UC10 Kelola Data Mahasiswa adalah use case umum. SIA-UC11 Tambah Data Mahasiswa memasukkan data baru; SIA-UC12 Ubah Data Mahasiswa memperbarui data yang tersimpan; SIA-UC13 Hapus Data Mahasiswa menghapus data hanya jika tidak memiliki data akademik aktif. Panah generalization dari UC11, UC12, UC13 mengarah ke UC10 dengan segitiga kosong di sisi UC10.

## Collaboration
| ID | Nama collaboration | Use case yang direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09 Lihat KHS |