<!-- Deksripsi Uce Case -->

<!-- Ajukan KRS -->

| Elemen                | SIA-UC01 — Ajukan KRS                                                                  |
| --------------------- | -------------------------------------------------------------------------------------- |
| Sumber kebutuhan      | SIA-R03 dan SIA-R04                                                                    |
| Tujuan                | Mahasiswa berhasil mengajukan KRS dan memperoleh nomor pengajuan.                      |
| Aktor utama           | Mahasiswa                                                                              |
| Pemicu                | Mahasiswa memilih fungsi pengajuan KRS.                                                |
| Prasyarat             | Mahasiswa telah terautentikasi; data mata kuliah, prasyarat, dan jadwal tersedia.      |
| Pascakondisi berhasil | Pengajuan tersimpan dengan nomor pengajuan dan status Menunggu persetujuan dosen wali. |
| Pascakondisi gagal    | Tidak ada pengajuan baru yang berhasil tersimpan.                                      |
| Include               | SIA-UC02 — Validasi KRS                                                                |
| Extend                | SIA-UC03 — Unduh bukti pengajuan KRS                                                   |
| Extension point       | Konfirmasi penyimpanan pengajuan.                                                      |
| Kondisi extend        | Mahasiswa memilih mengunduh bukti.                                                     |

<!-- Validasi KRS -->

| Elemen                | SIA-UC02 — Validasi KRS                                                                                          |
| --------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Sumber kebutuhan      | SIA-R04                                                                                                          |
| Tujuan                | Memastikan pengajuan KRS memenuhi ketentuan validasi yang disebutkan dalam skenario.                             |
| Aktor utama           | Tidak ada aktor yang memulai secara langsung; validasi dijalankan oleh sistem sebagai bagian dari pengajuan KRS. |
| Aktor pendukung       | Mahasiswa sebagai pemilik pengajuan.                                                                             |
| Pemicu                | SIA-UC01 menjalankan validasi setelah mahasiswa mengirim pengajuan.                                              |
| Prasyarat             | Mahasiswa telah terautentikasi dan data mata kuliah, prasyarat, serta jadwal tersedia.                           |
| Pascakondisi berhasil | Hasil validasi menyatakan pengajuan memenuhi pemeriksaan dan dapat disimpan.                                     |
| Pascakondisi gagal    | Pengajuan belum berhasil tersimpan.                                                                              |

<!-- Unduh Bukti Pengajuan -->

| Elemen                | SIA-UC03 — Unduh bukti pengajuan KRS                                            |
| --------------------- | ------------------------------------------------------------------------------- |
| Sumber kebutuhan      | SIA-R05                                                                         |
| Tujuan                | Mahasiswa memperoleh bukti pengajuan KRS.                                       |
| Aktor utama           | Mahasiswa                                                                       |
| Aktor pendukung       | Tidak ada yang disebutkan secara langsung dalam skenario.                       |
| Pemicu                | Mahasiswa memilih mengunduh bukti pada konfirmasi penyimpanan pengajuan.        |
| Prasyarat             | Pengajuan KRS telah berhasil tersimpan dan konfirmasi pengajuan tersedia.       |
| Pascakondisi berhasil | Bukti pengajuan tersedia untuk diunduh oleh mahasiswa.                          |
| Pascakondisi gagal    | Pengajuan KRS yang telah tersimpan tetap berhasil meskipun bukti tidak diunduh. |
| Relasi                | <<extend>> SIA-UC01 — Ajukan KRS                                                |
| Kondisi               | [mahasiswa memilih mengunduh bukti]                                             |
| Extension point       | Konfirmasi penyimpanan pengajuan.                                               |


<!-- Proses Keputusan KRS -->

| Elemen                | Deskripsi                                                                              |
| --------------------- | -------------------------------------------------------------------------------------- |
| ID dan nama           | SIA-UC04 — Proses keputusan KRS                                                        |
| Sumber kebutuhan      | SIA-R06                                                                                |
| Tujuan                | Dosen wali menetapkan persetujuan atau penolakan KRS dan memberikan catatan keputusan. |
| Aktor utama           | Dosen wali                                                                             |
| Aktor pendukung       | Tidak ada yang disebutkan secara langsung dalam skenario.                              |
| Pemicu                | Dosen wali memilih fungsi pemrosesan keputusan KRS.                                    |
| Prasyarat             | Dosen wali telah terautentikasi dan pengajuan KRS tersedia untuk diproses.             |
| Pascakondisi berhasil | Keputusan persetujuan atau penolakan beserta catatan keputusan tercatat pada sistem.   |
| Pascakondisi gagal    | Keputusan belum berhasil diproses dan dicatat.                                         |