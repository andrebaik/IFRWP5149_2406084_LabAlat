<!-- skenario -->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

<!-- tabel kebutuhan -->
|  ID   |                             Kebutuhan_tugas                              |
|-------|--------------------------------------------------------------------------|
|SIA-R01|                  Mahasiswa dapat melihat jadwal kuliah                   |
|SIA-R02|               Admin akademik dapat mengelola jadwal kuliah               |
|SIA-R03|                      Mahasiswa dapat mengajukan KRS                      |
|SIA-R04|             Sistem memvalidasi KRS sebagai bagian pengajuan              |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
|SIA-R06|        Dosen wali dapat memproses persetujuan atau penolakan KRS         |

<!-- batas dan asumsi -->
Batas dan asumsi:
• Pengguna telah terautentikasi.
• Data mata kuliah, prasyarat, dan jadwal tersedia.
• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
• KRS tersimpan belum berarti disetujui.
• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.

<!-- tabel identifikasi aktor -->
| Aktor          | Tujuan terhadap sistem                       |
| :------------- | :------------------------------------------- |
| Dosen Wali     | Memproses persetujuan atau penolakan KRS     |
| Mahasiswa      | Mengajukan KRS, Mengunduh bukti jika memilih |

<!-- tabel katalog use case -->
| ID Use Case | Nama Use Case             | Aktor Primer | Sumber Kebutuhan | Deskripsi Singkat                                          |
| ----------- | ------------------------- | ------------ | ---------------- | ---------------------------------------------------------- |
| UC-SIA-03   | Ajukan KRS                | Mahasiswa    | SIA-R03          | Mengajukan KRS dengan memilih mata kuliah hingga tersimpan |
| UC-SIA-04   | Validasi KRS              | Sistem       | SIA-R04          | Memeriksa kelengkapan, prasyarat, benturan jadwal          |
| UC-SIA-05   | Unduh Bukti Pengajuan KRS | Mahasiswa    | SIA-R05          | Mengunduh bukti setelah konfirmasi penyimpanan             |
| UC-SIA-06   | Proses Keputusan KRS      | Dosen Wali   | SIA-R06          | Menyetujui/menolak KRS yang berstatus menunggu + catatan   |

<!-- relasi include -->

<!-- relasi extend -->