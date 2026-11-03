Tugas Praktik RPL: *Software Construction & Good Coding Practices*
Bentuk Pengerjaan: Kelompok proyek masing-masing
Durasi: 60–75 menit (praktik di kelas)
Topik: Implementasi, Code Review, dan Refactoring
A. Tujuan
Mahasiswa mampu menerapkan prinsip konstruksi perangkat lunak dan praktik coding yang baik dalam pengembangan proyek RPL masing-masing.
B. Instruksi Tugas
Setiap kelompok melanjutkan proyek RPL yang telah dirancang pada pertemuan sebelumnya, dengan mengacu pada Functional Requirements (FR), Use Case, Activity Diagram, Sequence Diagram, dan ERD yang sudah dibuat pada tugas sebelumnya (UTS)
Tahap 1 — Pemilihan Fitur (10 menit)
Pilih minimal satu Functional Requirement (FR) utama dari proyek kelompok yang akan diimplementasikan atau diperbaiki.
Step:
1. Mulai identifikasi Kode dan deskripsi FR.
2. Alur proses berdasarkan rancangan sebelumnya.
3. Input, proses, dan output yang diharapkan.
4. Komponen atau modul yang akan dikembangkan.
Tahap 2 — Software Construction (30 menit)
1. Implementasikan atau perbaiki fitur yang dipilih dengan menerapkan prinsip berikut:
2. Meaningful Naming: Penamaan variabel, fungsi, dan kelas yang jelas. Pake format camel ya
3. Modularity: Pemisahan kode berdasarkan fungsi dan tanggung jawab.
4. Single Responsibility Principle: Setiap fungsi atau modul memiliki tanggung jawab yang jelas.
5. DRY: Menghindari duplikasi kode yang tidak diperlukan.
6. Input Validation: Memastikan input sesuai aturan bisnis.
7. Error Handling: Menangani kondisi kesalahan secara tepat.
8. Code Readability: Menjaga konsistensi format, indentasi, dan struktur kode.
Setiap anggota kelompok harus berkontribusi dalam implementasi atau pemeriksaan kode.
Tahap 3 — Code Review & Refactoring (15 menit)
1. Lakukan code review bersama terhadap fitur yang telah dikembangkan.
2. Identifikasi minimal tiga bagian kode yang dapat ditingkatkan kualitasnya.
3. Untuk setiap temuan, dokumentasikan: Bagian kode, Masalah, Perbaikan
Contoh: fungsi validasi
1. Logika berulang
2. Membuat fungsi validasi terpisah
3. Lakukan refactoring tanpa mengubah perilaku fungsional yang telah ditetapkan.
Tahap 4 — Testing (10 menit)
Lakukan minimal tiga pengujian:
1. Normal case — input valid.
2. Invalid input — data tidak sesuai ketentuan.
3. Edge case — kondisi batas atau kondisi khusus (misal dicoba dengan memasukkan karakter khusus atau SQL Injection)
Dokumentasikan expected result, actual result, dan status pengujian.
C. Luaran Tugas
Setiap kelompok mengumpulkan:
1. Link repository GitHub/GitLab yang berisi kode hasil implementasi.
2. Identifikasi FR yang dikerjakan dan keterkaitannya dengan rancangan sebelumnya.
3. Dokumentasi minimal tiga temuan code review dan hasil refactoring (before–after).
4. Tabel hasil pengujian, simpel aja ya.. FR, steps, sesuai atau tidak (pakai checklist)
5. Daftar kontribusi anggota kelompok.
Dokumentasi dapat disertakan dalam README.md pada repository proyek.
Link submit git akan tersedia di LMS.

Pengerjaan
1. Pilihan FR : 
FR-01 (Melaporkan Fasilitas Rusak): Laporan baru berhasil disimpan ke dalam database dan mutlak mendapatkan status awal "Menunggu verifikasi".
2. Use Case yang dipakai : 
Kode UC
Nama Use Case
Aktor Utama
FR Terkait
Penjelasan Singkat
UC-01
Melaporkan Fasilitas Rusak
User, Admin
FR-01
Aktor membuat laporan kerusakan fasilitas hingga tersimpan dengan status "Menunggu verifikasi". 


3. Skenario sistem : 
Pengguna yang ingin melaporkan fasilitas rusak dapat membuka formulir pelaporan. Pelapor mengisikan detail kerusakan meliputi nama barang, deskripsi kendala, serta menentukan lokasi kerusakan menggunakan Interactive Map atau GPS. Pelapor wajib mengunggah foto bukti fisik kerusakan. Foto tersebut dianalisis oleh AI OpenCV untuk menghitung perkiraan persentase tingkat kerusakan barang secara otomatis. Setelah data divalidasi lengkap oleh sistem, laporan tersimpan dengan nomor tiket unik dan status awal "Menunggu Verifikasi".
4. Activity diagram : 


Activity Diagram ini menggambarkan alur pengajuan laporan kerusakan fasilitas oleh pengguna yang melibatkan interaksi antara User dan Sistem. Proses dimulai ketika User memilih menu Lapor pada aplikasi, yang kemudian direspons oleh Sistem dengan menampilkan form Laporan. User selanjutnya mengisikan detail kerusakan beserta dokumen pendukung pada formulir dan mengirimkannya ke sistem. Sistem kemudian memvalidasi kelengkapan data yang telah diisikan.
Jika hasil validasi menyatakan data tidak lengkap, Sistem akan menampilkan pesan "Data tidak Lengkap" dan meminta User untuk melengkapi kembali formulir. Sebaliknya, jika data dinyatakan lengkap, Sistem akan menyimpan data laporan dengan status awal "Menunggu Verifikasi", menampilkan konfirmasi bahwa laporan berhasil diterima, serta mengarahkan User untuk dapat melihat status penanganan laporan tersebut.
5. Sequence diagram : 

Urutan sequence pelaporan fasilitas rusak
Pengguna → Halaman Pelaporan: memilih menu laporan.


Halaman Pelaporan → Pengguna: menampilkan formulir pelaporan.


Pengguna → Halaman Pelaporan: mengisi detail kerusakan dan mengunggah foto.


Halaman Pelaporan → Sistem: mengirimkan data laporan.


Sistem → Sistem: memvalidasi kelengkapan data laporan.








