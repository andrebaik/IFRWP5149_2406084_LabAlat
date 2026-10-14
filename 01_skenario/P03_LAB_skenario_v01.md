<!-- skenario -->
Mahasiswa mengajukan peminjaman peralatan dengan memilih alat,
jumlah, dan rentang waktu. Sistem memeriksa ketersediaan. Jika
tersedia dan data lengkap, sistem menyimpan pengajuan berstatus
menunggu keputusan. Pada tampilan konfirmasi, mahasiswa dapat
memilih mencetak bukti pengajuan. Petugas mengelola data peralatan
serta menyetujui atau menolak pengajuan. Kepala laboratorium melihat
laporan peminjaman.

<!-- tabel kebutuhan -->
| ID      | Kebutuhan                                                                                        |
| :------ | :----------------------------------------------------------------------------------------------- |
| LAB-R01 | Mahasiswa dapat melihat ketersediaan peralatan                                                   |
| LAB-R02 | Petugas dapat mengelola data peralatan                                                           |
| LAB-R03 | Mahasiswa dapat mengajukan peminjaman; sistem memeriksa ketersediaan sebelum menyimpan pengajuan |
| LAB-R04 | Mahasiswa dapat mencetak bukti pada konfirmasi pengajuan jika memilihnya                         |
| LAB-R05 | Petugas dapat menetapkan persetujuan atau penolakan pengajuan                                    |
| LAB-R06 | Kepala laboratorium dapat melihat laporan peminjaman                                             |

<!-- batas sistem dan aturan -->
Batas sistem dan aturan:
• Sistem mencatat dan menyediakan informasi; perpindahan fisik alat tidak terjadi di dalam perangkat lunak.
• Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
• Pengajuan yang diterima sistem berstatus Menunggu keputusan, bukan otomatis Disetujui.
• Pengajuan dengan peralatan tidak tersedia tidak disimpan sebagai pengajuan berhasil.
• Pencetakan bukti tidak menjadi syarat keberhasilan pengajuan.
• Persetujuan petugas belum dimodelkan sebagai reservasi teknis stok.
• Pengambilan, pengembalian, kondisi alat, dan denda belum dianalisis pada potongan model ini.

<!-- tabel identifikasi aktor -->
| Aktor                | Tujuan terhadap sistem                                          |
| :------------------- | :-------------------------------------------------------------- |
| Mahasiswa            | Melihat ketersediaan, mengajukan peminjaman, dan mencetak bukti |
| Petugas laboratorium | Mengelola peralatan dan memproses keputusan                     |
| Kepala laboratorium  | Melihat laporan peminjaman                                      |


<!-- tabel katalog use case -->
|   ID   |Nama_use_case|                 Peran_dalam_model                  |
|--------|-------------|----------------------------------------------------|
|LAB-UC01|    Lihat    |   ketersediaan peralatan Fungsi utama mahasiswa    |
|LAB-UC02|   Kelola    |        data peralatan Fungsi utama petugas         |
|LAB-UC03|   Ajukan    |         peminjaman Fungsi utama mahasiswa          |
|LAB-UC04|   Periksa   |     ketersediaan Perilaku yang disertakan UC03     |
|LAB-UC05|    Cetak    |    bukti pengajuan Tambahan bersyarat pada UC03    |
|LAB-UC06|   Proses    |     keputusan peminjaman Fungsi utama petugas      |
|LAB-UC07|    Lihat    |laporan peminjaman Fungsi utama kepala laboratorium |

<!-- relasi include -->
LAB-UC03 «include» LAB-UC04
Alasan: pemeriksaan menjadi bagian validasi pengajuan.

<!-- relasi extend -->
LAB-UC05 «extend» LAB-UC03
Extension point: Bukti pengajuan tersedia.
Kondisi: [mahasiswa memilih cetak].
Alasan: pengajuan tetap berhasil tanpa pencetakan.