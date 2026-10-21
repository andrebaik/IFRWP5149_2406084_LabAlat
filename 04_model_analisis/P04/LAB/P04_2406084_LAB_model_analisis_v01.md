|Sumber| Hubungan | Tujuan|
|:---|:---|:---|
|Peminjam | Association | LAB LAB-UC01 Lihat Ketersediaan Peralatan |
|Mahasiswa| Association (khusus, tetap dariPertemuan 3) | LAB-UC05 Cetak Bukti Pengajuan |
|Mahasiswa| Generalization → | Peminjam |
|Dosen    | Generalization → | Peminjan |
|Petugas Laboratorium | Association | LAB-UC02 Kelola Data Peralatan|
|Petugas Laboratorium | Association | LAB-UC06 Proses Keputusan Peminjaman |
|Petugas Laboratorium | Association | LAB-UC11 Catat Pengembalian Peralatan | 
|Kepala Laboratorium | Association | LAB-UC07 Lihat Laporan Peminjaman |
|LAB-UC03 Ajukan Peminjaman |«include» (tetap dari Pertemuan 3) |LAB-UC04 Periksa Ketersediaan|
|LAB-UC05 Cetak Bukti Pengajuan | «extend» (tetap dari Pertemuan 3)|LAB-UC03 Ajukan Peminjaman|
|LAB-UC08 Tambah Data Peralatan |Generalization → |LAB-UC02 Kelola Data Peralatan|
|LAB-UC09 Ubah Data Peralatan| Generalization → |LAB-UC02 Kelola Data Peralatan|
|LAB-UC10 Hapus Data Peralatan |Generalization → |LAB-UC02 Kelola Data Peralatan|
|LAB-UC11 Catat Pengembalian Peralatan| «include» |LAB-UC12 Periksa Kondisi Peralatan|
|LAB-CO01 (collaboration) |Realization → |LAB-UC03 Ajukan Peminjaman|
|LAB-CO02 (collaboration) |Realization → |LAB-UC11 Catat Pengembalian Peralatan|
