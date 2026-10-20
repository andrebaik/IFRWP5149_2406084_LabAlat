## Melihat jadwal kuliah
| Elemen                 | SIA-UC01                                               |
| :--------------------- | ------------------------------------------------------ |
| Tujuan                 | Melihat jadwal kuliah sebelum mengajukan KRS           |
| Aktor utama            | Mahasiswa                                              |
| Sumber kebutuhan       | SIA-R01                                                |
| Pemicu                 | Mahasiswa memilih fungsi lihat jadwal kuliah           |
| Prasyarat              | Mahasiswa telah terautentikasi; jadwal kuliah tersedia |
| Pascakondisi berhasil  | Jadwal kuliah diperlihatkan                            |
| keputusan Pascakondisi | gagal Tidak dapat menampilkan jadwal kuliah            |
| Include                | -                                                      |
| Extension point        | -                                                      |
| Extend                 | -                                                      |


## Kelola jadwal kuliah
| Elemen                 | SIA-UC02                   |
| :--------------------- | --------------------------------------------------------- |
| Tujuan                 | Mengelola jadwal kuliah sebelum mahasiswa mengajukan KRS  |
| Aktor utama            | Admin akademik                                            |
| Sumber kebutuhan       | SIA-R02                                                   |
| Pemicu                 | Admin akademik memilih fungsi kelola jadwal kuliah        |
| Prasyarat              | Admin telah terautentikasi; kelola jadwal kuliah tersedia |
| Pascakondisi berhasil  | Pengelolaan jadwal kuliah dapat dilakukan                 |
| keputusan Pascakondisi | gagal Tidak dapat mengelola jadwal kuliah                 |
| Include                | -                                                         |
| Extension point        | -                                                         |
| Extend                 | -                                                         |

## Pengajuan KRS
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC03 — Ajukan KRS |
| Sumber kebutuhan | SIA-R03 (perilaku disertakan: SIA-R04; perilaku tambahan: SIA-R05) |
| Tujuan | Menghasilkan pengajuan KRS yang tersimpan berstatus Menunggu persetujuan dosen wali |
| Aktor utama | Mahasiswa |
| Aktor pendukung | Tidak ada (validasi dijalankan sistem melalui SIA-UC04; dosen wali tidak berinteraksi di use case ini) |
| Pemicu | Mahasiswa memilih fungsi pengajuan KRS |
| Prasyarat | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia |
| Include | SIA-UC04 — Validasi KRS (selalu, pada langkah 3) |
| Extension point | Bukti pengajuan tersedia — setelah langkah 5 |
| Extend | SIA-UC05 — Unduh bukti pengajuan KRS, jika [mahasiswa memilih unduh bukti] |
| Pascakondisi berhasil | Pengajuan KRS tersimpan dengan nomor dan status Menunggu persetujuan dosen wali |
| Pascakondisi gagal | Tidak ada pengajuan baru yang tersimpan |
| Aturan bisnis/asumsi | Unduh bukti tidak menjadi syarat keberhasilan; KRS tersimpan belum berarti disetujui |

## Validasi KRS
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC04 — Validasi KRS |
| Sumber kebutuhan | SIA-R04 |
| Tujuan | Memastikan pengajuan memenuhi kelengkapan, prasyarat mata kuliah, dan bebas benturan jadwal sebelum disimpan |
| Aktor utama | Tidak ada aktor manusia; dijalankan sistem sebagai bagian dari SIA-UC03 |
| Aktor pendukung | — |
| Pemicu | Pengajuan dikirim pada langkah 3 SIA-UC03 |
| Prasyarat | Data mata kuliah, prasyarat, dan jadwal tersedia |
| Pascakondisi berhasil | Pengajuan dinyatakan sah; kendali kembali ke SIA-UC03 untuk disimpan |
| Pascakondisi gagal | Pengajuan tidak sah untuk disimpan; penyebab kegagalan dilaporkan ke SIA-UC03 |
| Aturan bisnis/asumsi | Kegagalan hasil pemeriksaan tidak berarti pemeriksaan bersifat opsional |

## Unduh Bukti
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC05 — Unduh bukti pengajuan KRS |
| Sumber kebutuhan | SIA-R05 |
| Tujuan | Memberikan berkas bukti pengajuan KRS kepada mahasiswa |
| Aktor utama | Mahasiswa |
| Aktor pendukung | — |
| Pemicu | Mahasiswa memilih unduh bukti pada konfirmasi penyimpanan SIA-UC03 (extension point "Bukti pengajuan tersedia") |
| Prasyarat | Pengajuan KRS berhasil tersimpan (memiliki nomor dan status) |
| Pascakondisi berhasil | Mahasiswa memperoleh berkas bukti (nomor, mata kuliah, waktu, status Menunggu persetujuan) |
| Pascakondisi gagal | Pengajuan tetap tersimpan; mahasiswa belum memperoleh berkas dan dapat mengulangi unduhan |
| Aturan bisnis/asumsi | Unduh bukti tidak menjadi syarat keberhasilan pengajuan; perilaku ini tidak mengubah status pengajuan |

## Proses Keputusan
| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC06 — Proses keputusan KRS |
| Sumber kebutuhan | SIA-R06 |
| Tujuan | Menghasilkan keputusan persetujuan atau penolakan beserta catatan atas KRS yang menunggu |
| Aktor utama | Dosen Wali |
| Aktor pendukung | — |
| Pemicu | Dosen wali membuka pengolahan keputusan KRS |
| Prasyarat | Dosen wali terautentikasi; terdapat KRS berstatus Menunggu persetujuan |
| Pascakondisi berhasil | Keputusan tersimpan: KRS berstatus Disetujui atau Ditolak, disertai catatan keputusan |
| Pascakondisi gagal | Tidak ada keputusan tersimpan; status KRS tetap Menunggu persetujuan |
| Aturan bisnis/asumsi | Setiap keputusan disertai catatan; sistem hanya mencatat keputusan (notifikasi dan perubahan jadwal tidak dimodelkan) |