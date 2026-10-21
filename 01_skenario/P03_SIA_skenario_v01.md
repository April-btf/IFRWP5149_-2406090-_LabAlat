<!-- Deksripsi -->

Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

<!-- Tabel Kebutuhan  -->

<<<<<<< HEAD
|  ID   |                             Kebutuhan_tugas                              |
|-------|--------------------------------------------------------------------------|
|SIA-R01|                  Mahasiswa dapat melihat jadwal kuliah                   |
|SIA-R02|               Admin akademik dapat mengelola jadwal kuliah               |
|SIA-R03|                      Mahasiswa dapat mengajukan KRS                      |
|SIA-R04|             Sistem memvalidasi KRS sebagai bagian pengajuan              |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
|SIA-R06|        Dosen wali dapat memproses persetujuan atau penolakan KRS         |
=======
|  ID   |                             Kebutuhan_tugas                               |
|-------|---------------------------------------------------------------------------|
|SIA-R01| Mahasiswa dapat melihat jadwal kuliah                                     |
|SIA-R02| Admin akademik dapat mengelola jadwal kuliah                              |
|SIA-R03| Mahasiswa dapat mengajukan KRS                                            |
|SIA-R04| Sistem memvalidasi KRS sebagai bagian pengajuan                           |
|SIA-R05| Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
|SIA-R06| Dosen wali dapat memproses persetujuan atau penolakan KRS                 |
>>>>>>> 2599aee1c54fc8d09a37c91575f7023161810a11

<!-- Batas sistem dan aturan -->

• Pengguna telah terautentikasi.

• Data mata kuliah, prasyarat, dan jadwal tersedia.

• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.

• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.

• KRS tersimpan belum berarti disetujui.

• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar tugas.

<!-- Tabel Identifikasi Aktor  -->

| Aktor          | Tujuan terhadap sistem                                                     |
| -------------- | -------------------------------------------------------------------------- |
| Mahasiswa      | Mengajukan KRS dan mengunduh bukti pengajuan jika diperlukan.              |
| Dosen wali     | Memproses persetujuan atau penolakan KRS dan memberikan catatan keputusan. |
| Admin Akademik | Mengelola Jadwal Kuliah                                                    |

<!-- Katalog Use Case -->

| ID       | Nama Fungsi               | Aktor terkait                                 | Sumber kebutuhan |
| -------- | ------------------------- | --------------------------------------------- | ---------------- |
| SIA-UC01 | jadwal Kuliah             | Mahasiswa                                     | SIA-R01          |
| SIA-UC02 | Kelola Jadwal Kuliah      | Admin Akademik                                | SIA-R02          |
| SIA-UC03 | Ajukan KRS                | Mahasiswa                                     | SIA-R03, SIA-R04 |
| SIA-UC04 | Validasi KRS              | Sistem                                        | SIA-R04          |
| SIA-UC05 | Unduh bukti pengajuan KRS | Mahasiswa                                     | SIA-R05          |
| SIA-UC06 | Proses keputusan KRS      | Dosen wali                                    | SIA-R06          |

<!-- Relasi Include -->

SIA-UC01 Ajukan KRS <<include>> SIA-UC02 Validasi KRS

Alasan: Setiap pengajuan KRS harus menjalankan validasi untuk memeriksa kelengkapan data, prasyarat mata kuliah, dan benturan jadwal.

<!-- Relasi Extand -->

SIA-UC03 Unduh bukti pengajuan KRS <<extend>> SIA-UC01 Ajukan KRS

Extension point: Konfirmasi penyimpanan pengajuan.

Kondisi: [mahasiswa memilih mengunduh bukti].

Alasan: Pengajuan KRS tetap berhasil meskipun mahasiswa tidak mengunduh bukti.