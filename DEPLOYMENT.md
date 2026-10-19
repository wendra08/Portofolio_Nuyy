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
