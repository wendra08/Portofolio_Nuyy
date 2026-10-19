# Deployment Vercel

Domain utama: https://nurhidayati.my.id

Project menggunakan Astro dengan output statis. Tidak memerlukan adapter server atau environment variable.

## Pengaturan project

- Framework Preset: Astro
- Root Directory: folder yang berisi package.json dan astro.config.mjs (jika repository langsung berisi project ini, gunakan root repository)
- Build Command: npm run build
- Output Directory: dist
- Install Command: default Vercel

Build dan output juga ditetapkan di vercel.json.

## Domain

1. Buka project Vercel, Settings > Domains.
2. Tambahkan nurhidayati.my.id.
3. Masukkan record DNS persis seperti yang ditampilkan Vercel pada panel penyedia DNS domain. Jangan menebak IP atau target CNAME.
4. Jika menggunakan www.nurhidayati.my.id, tambahkan juga dan pilih redirect ke nurhidayati.my.id.
5. Pastikan domain menunjukkan konfigurasi valid dan HTTPS aktif.

Konfigurasi source tidak otomatis menghubungkan domain atau mengubah DNS.

## Pembaruan

Jalankan npm run check dan npm run build sebelum mengirim perubahan ke repository yang terhubung dengan Vercel. Deployment produksi mengikuti branch produksi yang dipilih pada project Vercel.

URL canonical, Open Graph, robots.txt, dan sitemap.xml menggunakan site di astro.config.mjs. Sitemap saat ini memuat halaman utama karena portfolio ini berupa satu halaman.

Konfigurasi .openai/hosting.json adalah peninggalan hosting Sites dan tidak digunakan oleh Vercel.

## Pratinjau saat link dibagikan

Gambar berbagi: public/images/nur-hidayati-social-v1.jpg (1200 × 630, JPEG).
Metadata Open Graph dan Twitter Card berada di src/pages/index.astro dan sudah dirender dalam HTML statis agar bisa dibaca crawler tanpa JavaScript.

Setelah redeploy, pastikan https://nurhidayati.my.id/images/nur-hidayati-social-v1.jpg dapat dibuka tanpa login. Kemudian coba tempel URL situs pada pesan baru. Bentuk dan ukuran pratinjau ditentukan oleh aplikasi penerima; metadata tidak menjamin semua aplikasi menampilkan kartu yang sama. Pengujian lokal tidak memverifikasi hasil pratinjau di WhatsApp.

Jika desain gambar diganti lagi, gunakan nama versi file baru dan perbarui socialImageURL agar URL gambar berbeda dari versi sebelumnya.
