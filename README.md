# Portfolio Nur Hidayati

Website satu halaman berbasis Astro, dengan desain ivory–burgundy dan font yang di-host lokal. Konten bersumber dari CV yang diberikan. Dokumentasi dan sertifikat sengaja menggunakan placeholder, bukan karya rekaan.

## Menjalankan

```sh
npm install
npm run dev
```

Di PowerShell dengan execution policy ketat, gunakan `npm.cmd` sebagai pengganti `npm`.

```sh
npm run check
npm run build
npm run preview
```

## Mengisi konten

- `src/data/portfolio.ts`: profil, pengalaman, karya, sertifikasi, penghargaan.
- `src/pages/index.astro`: struktur halaman dan teks bagian lainnya.
- `src/styles/global.css`: warna, tipografi, dan layout responsif.
- `src/components/MediaSlot.astro`: placeholder yang otomatis menjadi gambar setelah `src` tersedia.
- `public/cv-nur-hidayati.pdf`: CV unduhan.

Simpan foto di `public/images/`, lalu isi properti `image` dengan `/images/nama-file.webp`. Isi `profile.portrait` untuk foto utama. Untuk dokumentasi organisasi, tambahkan `src` pada `MediaSlot` dengan `variant="team-media"` di halaman utama. Gunakan foto potret rasio sekitar 4:5, karya 4:3, dan sertifikat dengan seluruh isi tetap terbaca. Jika perlu menampilkan sertifikat penuh, ubah `object-fit` khusus sertifikat menjadi `contain`.

Pastikan contoh laporan tidak memuat data pribadi karyawan atau dokumen perusahaan yang tidak boleh dipublikasikan. Klaim dan status pekerjaan mengikuti CV dan perlu diperbarui ketika berubah.

Setup mengikuti dokumentasi resmi: https://docs.astro.build/en/install-and-setup/
