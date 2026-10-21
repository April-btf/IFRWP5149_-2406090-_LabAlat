
<!-- Aktor -->

Aktor	Peran
Civitas Akademika	Aktor umum yang dapat melihat kalender akademik.
Mahasiswa	Aktor khusus Civitas Akademika; melihat jadwal kuliah, mengajukan KRS, mengunduh bukti pengajuan, dan melihat KHS.
Dosen	Aktor khusus Civitas Akademika; menginput nilai mata kuliah yang diampunya.
Admin Akademik	Mengelola jadwal kuliah dan data mahasiswa.
Dosen Wali	Memproses keputusan pengajuan KRS.

<!-- Katalog use case kumulatif -->
ID	Nama use case	Aktor terkait	Sumber kebutuhan	Status
SIA-UC01	Lihat Jadwal Kuliah	Mahasiswa	SIA-R01	Tetap, P02
SIA-UC02	Kelola Jadwal Kuliah	Admin Akademik	SIA-R02	Tetap, P02
SIA-UC03	Ajukan KRS	Mahasiswa	SIA-R03	Tetap, P03
SIA-UC04	Validasi KRS	Bagian dari proses pengajuan	SIA-R04	Tetap, P03
SIA-UC05	Unduh Bukti Pengajuan KRS	Mahasiswa	SIA-R05	Tetap, P03
SIA-UC06	Proses Keputusan KRS	Dosen Wali	SIA-R06	Tetap, P03
SIA-UC07	Lihat Kalender Akademik	Civitas Akademika	SIA-R07	Baru, P04
SIA-UC08	Input Nilai Mata Kuliah	Dosen	SIA-R08	Baru, P04
SIA-UC09	Lihat KHS	Mahasiswa	SIA-R09	Baru, P04
SIA-UC10	Kelola Data Mahasiswa	Admin Akademik	SIA-R10	Baru, P04
SIA-UC11	Tambah Data Mahasiswa	Mewarisi aktor dari UC10	SIA-R11	Baru, P04
SIA-UC12	Ubah Data Mahasiswa	Mewarisi aktor dari UC10	SIA-R11	Baru, P04
SIA-UC13	Hapus Data Mahasiswa	Mewarisi aktor dari UC10	SIA-R11	Baru, P04

<!-- generalization use case -->
Use case umum adalah SIA-UC10 Kelola Data Mahasiswa. 
Use case ini memiliki tiga use case khusus.
Use case umum	Use case khusus	Perilaku pembeda
SIA-UC10 Kelola Data Mahasiswa	SIA-UC11 Tambah Data Mahasiswa	Menambahkan data mahasiswa baru ke dalam sistem.
SIA-UC10 Kelola Data Mahasiswa	SIA-UC12 Ubah Data Mahasiswa	Memperbarui data mahasiswa yang sudah terdaftar.
SIA-UC10 Kelola Data Mahasiswa	SIA-UC13 Hapus Data Mahasiswa	Menghapus data mahasiswa yang tidak memiliki data akademik aktif.

<!-- Tetapkan collaboration -->
Dua collaboration yang diwajibkan oleh SIA-R12 adalah:
ID collaboration	Nama collaboration	Use case yang direalisasikan
SIA-CO01	Input Nilai Mata Kuliah	SIA-UC08 Input Nilai Mata Kuliah
SIA-CO02	Lihat KHS	SIA-UC09 Lihat KHS