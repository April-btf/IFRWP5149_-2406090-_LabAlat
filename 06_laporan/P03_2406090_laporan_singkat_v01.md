<!-- Review dan Revisi -->

| No. | Temuan | Perbaikan yang Perlu | Alasan |
|---|---|---|---|
| 1 | Aktor Mahasiswa diletakkan di dalam batas sistem | Pindahkan aktor Mahasiswa ke luar batas sistem | Aktor berada di luar batas sistem |
| 2 | Use case Lihat Jadwal Kuliah berbentuk kotak | Ubah menjadi elips | Use case seharusnya berbentuk elips |
| 3 | Mahasiswa terhubung ke Kelola Jadwal Kuliah | Hubungkan Mahasiswa ke Lihat Jadwal Kuliah | Sesuai dengan skenario SIA |
| 4 | Judul sistem masih menggunakan Sistem Laboratorium | Ganti dengan Sistem Informasi Akademik (SIA) | Sesuai dengan judul studi kasus |
| 5 | Relasi `<<include>>` antara Ajukan KRS dan Validasi KRS belum tepat | Hubungkan SIA-UC03 ke SIA-UC04 menggunakan relasi `<<include>>` | Validasi merupakan bagian wajib dari pengajuan KRS |
| 6 | Relasi `<<extend>>` antara Unduh Bukti Pengajuan KRS dan Ajukan KRS belum tepat | Hubungkan SIA-UC05 ke SIA-UC03 menggunakan relasi `<<extend>>` | Pengunduhan bukti bersifat opsional |
| 7 | Kondisi `<<extend>>` dan extension point belum dicantumkan | Tambahkan kondisi `[mahasiswa memilih mengunduh bukti]` dan extension point `Konfirmasi penyimpanan pengajuan KRS` | Menjelaskan kondisi dan titik perluasan use case |
| 8 | Hubungan aktor dengan use case belum seluruhnya sesuai katalog | Periksa kembali hubungan Mahasiswa, Admin Akademik, dan Dosen Wali dengan use case masing-masing | Menjaga konsistensi diagram dengan katalog dan skenario SIA |