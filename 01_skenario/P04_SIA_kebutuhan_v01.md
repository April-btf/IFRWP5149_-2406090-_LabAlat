<!-- Skenario -->

Mahasiswa dan dosen merupakan Civitas Akademika yang dapat melihat
kalender akademik. Dosen menginput nilai mata kuliah yang diampunya
setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi
(KHS) untuk semester yang nilainya sudah dipublikasikan.

Admin Akademik mengelola data mahasiswa melalui kegiatan menambah,
mengubah, dan menghapus data mahasiswa. Dua use case utama, yaitu
Input Nilai Mata Kuliah dan Lihat KHS, direalisasikan oleh collaboration
dengan nama yang sama.

Diagram bersifat kumulatif. Fungsi jadwal kuliah dan pengajuan KRS
dari pertemuan sebelumnya tetap dipertahankan.

<!-- Kebutuhan -->

| ID | Kebutuhan |
|---|---|
| SIA-R01–SIA-R06 | Kebutuhan pertemuan sebelumnya tetap berlaku dan tidak diubah artinya. |
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik. |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya. |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan. |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa terdiri atas Tambah Data Mahasiswa, Ubah Data Mahasiswa, dan Hapus Data Mahasiswa. |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |

<!-- Batas dan Asumsi -->

1. Pengguna telah terautentikasi dan memiliki hak akses sesuai perannya.
2. Kalender akademik merupakan agenda resmi institusi, seperti awal
   semester, batas pengisian KRS, dan masa ujian. Kalender akademik
   berbeda dari jadwal kuliah.
3. Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut.
4. Nilai yang berhasil diinput belum otomatis dipublikasikan.
5. KHS hanya menampilkan nilai yang sudah dipublikasikan.
6. Data mahasiswa hanya boleh dihapus apabila mahasiswa tersebut
   tidak memiliki data akademik aktif.
7. Fungsi jadwal kuliah dan pengajuan KRS tetap dicantumkan dalam
   diagram kumulatif.
8. Pembayaran dan perancangan basis data berada di luar lingkup tugas.
9. Berkas Pertemuan 3 tetap dipertahankan. Pengembangan diagram
   dilakukan pada salinan dengan nama berkas Pertemuan 4.