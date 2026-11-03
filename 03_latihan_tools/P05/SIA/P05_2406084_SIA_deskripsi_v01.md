## Lihat Kalender Akademik
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC07: Lihat Kalender Akademik |
| Sumber kebutuhan | SIA-R07 |
| Tujuan | Civitas Akademika melihat agenda resmi institusi (awal semester, batas KRS, masa ujian, dan sejenisnya) |
| Aktor utama | Civitas Akademika (umum); Mahasiswa dan Dosen dapat menjalankannya melalui pewarisan |
| Pemicu | Aktor memilih fungsi kalender akademik |
| Prasyarat | Aktor telah terautentikasi |
| Pascakondisi berhasil | Agenda kalender akademik tampil |
| Pascakondisi gagal | Tidak ada agenda yang ditampilkan (mis. data kalender belum tersedia) |



## Input Nilai Mata Kuliah
| Elemen | UC08: Input Nilai Mata Kuliah |
|---|---|
| Sumber | Kebutuhan input nilai mata kuliah oleh dosen |
| Tujuan | Nilai mahasiswa pada mata kuliah yang diampu tercatat di sistem |
| Aktor utama | Dosen |
| Pemicu | Dosen memilih fungsi input nilai dan menentukan mata kuliah yang akan diinput nilainya |
| Prasyarat | Dosen telah terautentikasi; dosen merupakan pengampu mata kuliah terpilih; periode perkuliahan telah berakhir |
| Alur Utama | 1. Dosen memilih mata kuliah. 2. Sistem menampilkan daftar mahasiswa. 3. Dosen memasukkan nilai mahasiswa. 4. Sistem memvalidasi dan menyimpan nilai. 5. Sistem menampilkan notifikasi berhasil |
| Alur Alternatif | Nilai berada di luar rentang yang sah: sistem menolak nilai dan menampilkan pesan kesalahan agar dosen memperbaikinya |
| Pascakondisi berhasil | Nilai berhasil disimpan sebagai nilai yang belum dipublikasikan secara resmi |
| Pascakondisi gagal | Tidak ada nilai baru yang tersimpan dari proses yang gagal; data nilai sebelumnya tidak berubah |
| Include | Tidak ada |
| Collaboration | CO01: Input Nilai Mata Kuliah |


## Lihat KHS
| Elemen | UC09: Lihat KHS |
|---|---|
| Sumber | Kebutuhan mahasiswa untuk melihat hasil studi |
| Tujuan | Mahasiswa dapat melihat Kartu Hasil Studi berdasarkan semester |
| Aktor utama | Mahasiswa |
| Pemicu | Mahasiswa memilih fungsi Lihat KHS dan menentukan semester |
| Prasyarat | Mahasiswa telah terautentikasi |
| Alur Utama | 1. Mahasiswa memilih menu KHS. 2. Sistem menampilkan pilihan semester. 3. Mahasiswa memilih semester. 4. Sistem menampilkan hasil studi yang nilainya telah dipublikasikan secara resmi |
| Alur Alternatif | Nilai belum dipublikasikan: nilai tersebut tidak ditampilkan pada KHS |
| Pascakondisi berhasil | KHS ditampilkan dengan hanya menyertakan nilai yang sudah dipublikasikan secara resmi |
| Pascakondisi gagal | KHS tidak berhasil ditampilkan; data hasil studi tidak berubah |
| Include | Tidak ada |
| Collaboration | CO02: Lihat KHS |

## Kelola Data Mahasiswa
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC10: Kelola Data Mahasiswa |
| Sumber kebutuhan | SIA-R10 |
| Tujuan | Admin Akademik mengelola data mahasiswa melalui tiga bentuk khususnya |
| Aktor utama | Admin Akademik |
| Pemicu | Admin Akademik memilih fungsi pengelolaan data mahasiswa |
| Prasyarat | Admin Akademik telah terautentikasi |
| Generalization | Use case **umum** bagi SIA-UC11 (Tambah), SIA-UC12 (Ubah), dan SIA-UC13 (Hapus) Data Mahasiswa |
| Collaboration | Tidak ada (bukan use case utama yang ditunjukkan realisasinya) |
| Pascakondisi berhasil | Data mahasiswa terkelola sesuai bentuk khusus yang dijalankan |
| Pascakondisi gagal | Data mahasiswa tidak berubah |

## Tambah Data Mahasiswa
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC11: Tambah Data Mahasiswa |
| Sumber kebutuhan | SIA-R11 |
| Generalization | Khusus dari SIA-UC10 Kelola Data Mahasiswa |
| Perilaku pembeda | Menghasilkan data mahasiswa **baru** yang tersimpan |
| Pascakondisi berhasil | Data mahasiswa baru tersimpan dengan data diri yang lengkap |
| Pascakondisi gagal | Tidak ada data mahasiswa baru yang tersimpan (mis. isian tidak lengkap) |

## Ubah Data Mahasiswa
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC12: Ubah Data Mahasiswa |
| Sumber kebutuhan | SIA-R11 |
| Generalization | Khusus dari SIA-UC10 Kelola Data Mahasiswa |
| Perilaku pembeda | Menghasilkan data mahasiswa yang **berubah** |
| Pascakondisi berhasil | Perubahan data mahasiswa tersimpan |
| Pascakondisi gagal | Data mahasiswa tetap seperti semula |

## Hapus Data Mahasiswa
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC13: Hapus Data Mahasiswa |
| Sumber kebutuhan | SIA-R11 |
| Generalization | Khusus dari SIA-UC10 Kelola Data Mahasiswa |
| Perilaku pembeda | Menghasilkan data mahasiswa yang **terhapus**, hanya untuk mahasiswa yang **tidak memiliki data akademik aktif** |
| Pascakondisi berhasil | Data mahasiswa terhapus dari sistem |
| Pascakondisi gagal | Data mahasiswa tetap ada |

