<!-- Identifikasi Aktor -->

| Aktor | Peran |
|---|---|
| Civitas Akademika | Aktor umum yang dapat melihat kalender akademik. |
| Mahasiswa | Aktor khusus Civitas Akademika; melihat jadwal kuliah, mengajukan KRS, mengunduh bukti pengajuan KRS, dan melihat KHS. |
| Dosen | Aktor khusus Civitas Akademika; menginput nilai mata kuliah yang diampunya. |
| Admin Akademik | Mengelola jadwal kuliah dan data mahasiswa. |
| Dosen Wali | Memproses persetujuan atau penolakan KRS dan memberikan catatan keputusan. |

<!-- Katalog Use Case Kumulatif -->

| ID | Nama use case | Aktor terkait | Sumber kebutuhan | Status |
|---|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | SIA-R01 | Tetap, P02 |
| SIA-UC02 | Kelola Jadwal Kuliah | Admin Akademik | SIA-R02 | Tetap, P02 |
| SIA-UC03 | Ajukan KRS | Mahasiswa | SIA-R03, SIA-R04 | Tetap, P03 |
| SIA-UC04 | Validasi KRS | Dijalankan sebagai bagian dari Ajukan KRS | SIA-R04 | Tetap, P03 |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | SIA-R05 | Tetap, P03 |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | SIA-R06 | Tetap, P03 |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | SIA-R07 | Baru, P04 |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | SIA-R08 | Baru, P04 |
| SIA-UC09 | Lihat KHS | Mahasiswa | SIA-R09 | Baru, P04 |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | SIA-R10 | Baru, P04 |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik, diwarisi dari SIA-UC10 | SIA-R11 | Baru, P04 |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik, diwarisi dari SIA-UC10 | SIA-R11 | Baru, P04 |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik, diwarisi dari SIA-UC10 | SIA-R11 | Baru, P04 |

<!-- Generalization Aktor -->

| Aktor khusus | Aktor umum | Fungsi yang diwarisi |
|---|---|---|
| Mahasiswa | Civitas Akademika | SIA-UC07 Lihat Kalender Akademik |
| Dosen | Civitas Akademika | SIA-UC07 Lihat Kalender Akademik |

Generalization digunakan karena Mahasiswa dan Dosen memiliki
kemampuan yang sama untuk melihat kalender akademik.

Asosiasi ke Lihat Kalender Akademik cukup digambar satu kali dari
Civitas Akademika. Mahasiswa dan Dosen mewarisi asosiasi tersebut
sehingga tidak perlu dihubungkan langsung ke use case yang sama.

Panah generalization digambar dari Mahasiswa menuju Civitas
Akademika dan dari Dosen menuju Civitas Akademika. Garisnya utuh,
dengan segitiga kosong menunjuk Civitas Akademika.

<!-- Fungsi Khusus Aktor -->

| Aktor | Fungsi khusus |
|---|---|
| Mahasiswa | Lihat Jadwal Kuliah, Ajukan KRS, Unduh Bukti Pengajuan KRS, dan Lihat KHS. |
| Dosen | Input Nilai Mata Kuliah yang diampunya. |
| Admin Akademik | Kelola Jadwal Kuliah dan Kelola Data Mahasiswa. |
| Dosen Wali | Proses Keputusan KRS. |

Dosen dan Dosen Wali dimodelkan sebagai dua peran yang berbeda
sesuai skenario tugas.

<!-- Generalization Use Case -->

Use case umum adalah SIA-UC10 Kelola Data Mahasiswa. Ketiga use
case khusus mewarisi tujuan dasar pengelolaan data mahasiswa dan
aktor terkait, yaitu Admin Akademik.

| Use case khusus | Use case umum | Perilaku pembeda |
|---|---|---|
| SIA-UC11 Tambah Data Mahasiswa | SIA-UC10 Kelola Data Mahasiswa | Menyimpan data mahasiswa baru. |
| SIA-UC12 Ubah Data Mahasiswa | SIA-UC10 Kelola Data Mahasiswa | Memperbarui data mahasiswa yang sudah tersimpan. |
| SIA-UC13 Hapus Data Mahasiswa | SIA-UC10 Kelola Data Mahasiswa | Menghapus data mahasiswa yang tidak memiliki data akademik aktif. |

Panah generalization menggunakan garis utuh dengan segitiga kosong
menunjuk SIA-UC10 Kelola Data Mahasiswa.

<!-- Collaboration dan Realization -->

| ID collaboration | Nama collaboration | Use case yang direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09 Lihat KHS |

Kedua collaboration ditetapkan berdasarkan SIA-R12 untuk menunjukkan
realisasi dua use case utama layanan hasil studi.

Collaboration digambar sebagai elips garis putus-putus. Nama setiap
collaboration sama persis dengan nama use case yang direalisasikan.

Realization menggunakan garis putus-putus dengan segitiga kosong
menunjuk use case. Tidak ada hubungan langsung dari aktor ke
collaboration.