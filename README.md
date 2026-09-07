# backend-5053241043

Repo tugas mata kuliah **Pengembangan Backend Dasar**, dibuat dari template [`webdev-if-its/backend-template`](https://github.com/webdev-if-its/backend-template). Ganti judul di atas jadi nama repo kalian sendiri (`backend-nrp`, contoh: `backend-5025201012`).

## Aturan Umum

- Tugas tiap pertemuan disimpan di folder `pertemuan-XX/` pada repo ini.
- Commit message wajib menyebut level yang dicapai: `pertemuan-XX: level N selesai`.
- Deadline push: sebelum pertemuan berikutnya dimulai.
- Semua level dicek otomatis lewat `go test` — baca `pertemuan-XX/SOAL.md` tiap minggu untuk detail levelnya.

## Mengambil Pertemuan Baru Tiap Minggu

Repo ini **tidak otomatis sinkron** dengan template dosen. Begitu ada pertemuan baru, jalankan (ganti `pertemuan-02` sesuai minggu berjalan):

```bash
git fetch https://github.com/webdev-if-its/backend-template.git main
git checkout FETCH_HEAD -- pertemuan-02
```

Perintah ini **aman dijalankan kapan pun** — tidak akan menimpa folder pertemuan lain yang sudah kalian kerjakan, karena hanya mengambil folder yang disebutkan. Setelah itu, commit folder barunya seperti biasa.

Kalau dosen memperbaiki sesuatu di pertemuan yang sudah dirilis (mis. ada bug di test), biasanya cukup ambil ulang file yang diperbaiki saja, bukan seluruh folder — akan diumumkan file mana yang berubah.

---

Bagian di bawah ini **isi bertahap** sesuai level yang sedang kalian kerjakan (lihat `pertemuan-01/SOAL.md`) — heading-nya dicek otomatis, jangan diganti namanya.

## Identitas
- Nama: Muhammad Alfaraldi Raihan
- NRP: 5053241043
- Kelas: M

## Commit vs Push
Commit berfungsi menyimpan snapshot perubahan ke riwayat repository yang ada di komputer lokal, dan proses ini bisa dilakukan tanpa koneksi internet. Push baru mengirimkan commit-commit tersebut ke remote repository agar bisa terlihat dan diakses dari sana. Contohnya seorang anggota tim sudah commit perbaikan bug di laptopnya, tapi lupa push ke remote. Anggota tim lain yang pull dari remote tidak akan melihat perbaikan itu sama sekali, sehingga mereka mengira bug belum diperbaiki dan bisa jadi malah mengerjakan ulang hal yang sama, atau melanjutkan pekerjaan di atas kode yang masih bermasalah.


## Reproducibility
Untuk program sederhana seperti ini, perbedaan versi Go pada umumnya tidak menimbulkan masalah. Fungsi runtime.Version() hanya menampilkan informasi versi Go yang digunakan saat proses compile, dan tidak memengaruhi logika program itu sendiri. Artinya, apabila anggota tim menjalankan program ini dengan versi Go yang berbeda, output program akan tetap sama, kecuali pada bagian yang menampilkan versi tersebut.

Namun, perbedaan versi Go dapat menjadi masalah nyata dalam kondisi tertentu, terutama jika kode program sudah menggunakan fitur bahasa yang baru tersedia pada versi tertentu. Sebagai contoh, jika seorang anggota tim menulis kode menggunakan fitur ini, sementara anggota lain masih menggunakan versi Go yang lebih lama, kode tersebut akan gagal di-compile pada perangkat anggota tim yang bersangkutan. Selain itu, perubahan kecil pada perilaku standard library antarversi juga berpotensi menghasilkan keluaran program yang berbeda meskipun kode sumbernya identik.

Untuk mencegah masalah tersebut, sebaiknya versi Go yang digunakan disepakati bersama, sehingga seluruh anggota tim memiliki acuan versi minimum yang harus digunakan.

## Catatan Merge Conflict
(tulis disini)
## Kenapa .gitignore Penting
(tulis disini)
## Refleksi
(tulis disini)