|   Elemen    |                                    LAB-UC11:_Catat_Pengembalian_Peralatan                                    |
|-------------|--------------------------------------------------------------------------------------------------------------|
|   Sumber    |                                        kebutuhan LAB-R09 dan LAB-R10                                         |
|   Tujuan    |                 Pengembalian tercatat dan status peminjaman serta kondisi peralatan terbarui                 |
|    Aktor utama   |                                           Petugas Laboratorium                                          |
|   Pemicu    |       Petugas memilih fungsi pencatatan pengembalian dan menentukan peminjaman yang akan dikembalikan        |
|  Prasyarat  |                     Petugas telah terautentikasi; peminjaman terpilih berstatus Dipinjam                     |
|Pascakondisi berhasil | Pengembalian tercatat dengan tanggal kembali dan kondisi eralatan; status peminjaman menjadi Selesai |
|Pascakondisi gagal|                Tidak ada pengembalian baru yang tercatat; status peminjaman tidak berubah               |
|   Include   |                                     LAB-UC12: Periksa Kondisi Peralatan                                      |
|Collaboration|                                    LAB-CO02: Catat Pengembalian Peralatan                                    |
