| Elemen | Isi |
|---|---|
| ID dan nama | SIA-UC08 — Input Nilai Mata Kuliah |
| Tujuan | Memungkinkan dosen pengampu memasukkan nilai mahasiswa untuk mata kuliah yang diampunya setelah masa perkuliahan berakhir. |
| Aktor utama | Dosen |
| Sumber kebutuhan | SIA-R08 |
| Pemicu | Dosen memilih fungsi input nilai untuk mata kuliah yang diampunya. |
| Prasyarat | Dosen terautentikasi, memiliki hak akses, merupakan dosen pengampu mata kuliah, dan masa perkuliahan telah berakhir. |
| Alur utama | 1. Dosen membuka mata kuliah yang diampunya. 2. Sistem menampilkan daftar mahasiswa dan form nilai. 3. Dosen memasukkan nilai. 4. Sistem memeriksa kelengkapan dan rentang nilai sah. 5. Jika valid, sistem menyimpan nilai dalam keadaan belum dipublikasikan. 6. Sistem menampilkan konfirmasi. |
| Alur alternatif | **A1 — Bukan dosen pengampu:** sistem menolak akses dan tidak menyimpan perubahan. **A2 — Nilai di luar rentang sah:** sistem menolak nilai, menampilkan kesalahan, dan meminta perbaikan; nilai tidak disimpan sampai valid. |
| Pascakondisi berhasil | Nilai tersimpan untuk mata kuliah terkait dalam keadaan belum dipublikasikan. |
| Pascakondisi gagal | Tidak ada perubahan nilai yang tersimpan; nilai sebelumnya tetap tidak berubah. |
| Include / Extend | Tidak ditetapkan oleh jobsheet. |
| Collaboration | SIA-CO01 — Input Nilai Mata Kuliah. |
| Aturan bisnis | Hanya dosen pengampu boleh menginput nilai. KHS hanya menampilkan nilai yang sudah dipublikasikan secara resmi. Jobsheet tidak menentukan rentang angka nilai sah. |