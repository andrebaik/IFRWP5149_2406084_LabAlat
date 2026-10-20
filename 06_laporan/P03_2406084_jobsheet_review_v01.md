**Validasi berhasil dan mahasiswa tidak mengunduh bukti → KONSISTEN.**
Diagram: SIA-UC03 menjalankan SIA-UC04 (include); hasil berhasil, pengajuan
tersimpan. Kondisi extend tidak terpenuhi sehingga SIA-UC05 tidak terjadi; tanpa
SIA-UC05 pun SIA-UC03 tetap mencapai pascakondisi berhasil (use case dasar tetap
bermakna tanpa perluasan). Deskripsi: alur utama langkah 1–7 dengan langkah 6
dilewati (alternatif 6a) — pengajuan tersimpan berstatus Menunggu persetujuan
tanpa bukti. Diagram dan deskripsi memberi hasil yang sama.

**Validasi gagal → KONSISTEN.**
Diagram: SIA-UC04 tetap dijalankan (include selalu terjadi meski hasilnya gagal);
SIA-UC03 tidak menyimpan pengajuan. SIA-UC05 tidak dapat terjadi karena extension
point "Bukti pengajuan tersedia" tidak pernah tercapai dan prasyarat SIA-UC05
(pengajuan tersimpan) tidak terpenuhi. Deskripsi: alur alternatif 3a — pascakondisi
gagal "tidak ada pengajuan baru yang tersimpan", tidak ada bukti. Kedua model sepakat.

**Validasi berhasil dan mahasiswa memilih mengunduh bukti → KONSISTEN.**
Diagram: setelah SIA-UC03 menyimpan pengajuan, extension point tercapai; kondisi
`[mahasiswa memilih unduh bukti]` terpenuhi sehingga SIA-UC05 berjalan menuju
SIA-UC03 tanpa mengubah keberhasilan pengajuan. Deskripsi: langkah 6 memicu
SIA-UC05; mahasiswa memperoleh bukti; status tetap Menunggu persetujuan (KRS
tersimpan belum berarti disetujui).