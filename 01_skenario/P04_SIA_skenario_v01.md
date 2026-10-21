## Skenario
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin Akademik mengelola data mahasiswa: menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

## Identifikasi aktor
| Aktor | Kedudukan | Tujuan |
|---|---|---|
| Civitas Akademika | Aktor umum baru P04 | Melihat kalender akademik; fungsi diwariskan kepada Mahasiswa dan Dosen. |
| Mahasiswa | Aktor khusus Civitas Akademika; tetap P02/P03 | Melihat jadwal, mengajukan KRS, mengunduh bukti, melihat KHS, dan mewarisi akses kalender. |
| Dosen | Aktor khusus Civitas Akademika; baru P04 | Melihat kalender dan menginput nilai mata kuliah yang diampu. |
| Admin Akademik | Tetap P02 | Mengelola jadwal kuliah dan data mahasiswa. |
| Dosen Wali | Tetap P03 | Memproses keputusan KRS. |

## Keputusan generalization aktor
Mahasiswa dan Dosen merupakan spesialisasi Civitas Akademika karena keduanya dapat melihat kalender akademik. Asosiasi SIA-UC07 digambar satu kali dari aktor umum. Fungsi khusus tetap dihubungkan langsung dengan aktor yang sesuai.

## Keputusan generalization use case
SIA-UC10 Kelola Data Mahasiswa adalah use case umum. SIA-UC11 Tambah Data Mahasiswa, SIA-UC12 Ubah Data Mahasiswa, dan SIA-UC13 Hapus Data Mahasiswa adalah use case khusus yang mewarisi perilaku umum.

## Keputusan collaboration
- SIA-CO01 Input Nilai Mata Kuliah merealisasikan SIA-UC08 Input Nilai Mata Kuliah.
- SIA-CO02 Lihat KHS merealisasikan SIA-UC09 Lihat KHS.

## Relasi P03 yang tetap berlaku
- SIA-UC03 Ajukan KRS «include» SIA-UC04 Validasi KRS.
- SIA-UC05 Unduh Bukti Pengajuan KRS «extend» SIA-UC03 Ajukan KRS, dengan kondisi mahasiswa memilih unduh bukti saat konfirmasi dan extension point “Bukti pengajuan tersedia”.
- Asosiasi Mahasiswa ke UC01, UC03, UC05; Admin Akademik ke UC02; dan Dosen Wali ke UC06 tetap dipertahankan.
