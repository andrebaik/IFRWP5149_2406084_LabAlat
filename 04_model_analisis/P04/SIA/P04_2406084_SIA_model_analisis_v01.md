| Sumber | Hubungan | Tujuan |
|---|---|---|
| Civitas Akademika | Association | SIA-UC07 Lihat Kalender Akademik |
| Mahasiswa | Association | SIA-UC01 Lihat Jadwal Kuliah |
| Mahasiswa | Association | SIA-UC03 Ajukan KRS |
| Mahasiswa | Association | SIA-UC05 Unduh Bukti Pengajuan KRS |
| Mahasiswa | Association | SIA-UC09 Lihat KHS |
| Mahasiswa | Generalization (segitiga kosong menunjuk aktor umum) | Civitas Akademika |
| Dosen | Association | SIA-UC08 Input Nilai Mata Kuliah |
| Dosen | Generalization (segitiga kosong menunjuk aktor umum) | Civitas Akademika |
| Admin Akademik | Association | SIA-UC02 Kelola Jadwal Kuliah |
| Admin Akademik | Association | SIA-UC10 Kelola Data Mahasiswa |
| Dosen Wali | Association | SIA-UC06 Proses Keputusan KRS |
| SIA-UC03 Ajukan KRS | «include» (tetap dari Pertemuan 3) | SIA-UC04 Validasi KRS |
| SIA-UC05 Unduh Bukti Pengajuan KRS | «extend» [mahasiswa memilih unduh bukti], extension point *Bukti pengajuan tersedia* (tetap dari Pertemuan 3) | SIA-UC03 Ajukan KRS |
| SIA-UC11 Tambah Data Mahasiswa | Generalization → | SIA-UC10 Kelola Data Mahasiswa |
| SIA-UC12 Ubah Data Mahasiswa | Generalization → | SIA-UC10 Kelola Data Mahasiswa |
| SIA-UC13 Hapus Data Mahasiswa | Generalization → | SIA-UC10 Kelola Data Mahasiswa |
| SIA-CO01 (collaboration) | Realization → | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 (collaboration) | Realization → | SIA-UC09 Lihat KHS |