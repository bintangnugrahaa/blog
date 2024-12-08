---
title: Laravel Prezet  
excerpt: Belajar cara install Prezet dan mulai bikin blog, artikel, atau dokumentasi yang SEO-friendly. Ikuti langkah-langkah berikut buat setup proyekmu dan mulai blogging dengan Prezet.
slug: /prezet  
date: 2024-12-08  
image: /prezet/img/ogimages/installation.webp
---

Mau bikin blog, artikel, atau dokumentasi yang SEO-friendly di Laravel? Prezet adalah paket blogging markdown yang tepat banget buat kamu. Panduan ini bakal ngebantu kamu install Prezet dan siapin proyek kamu buat mulai blogging. Yuk, langsung ikuti langkah-langkahnya.

## Step 1: Install Paket Prezet

Pertama-tama, kita perlu install paket Prezet di proyek Laravel kamu. Gampang banget, cukup pake Composer:

```bash
composer require benbjurstrom/prezet
```

Cuma butuh beberapa saat, dan Prezet siap digunakan di proyek kamu.

## Step 2: Jalankan Installer Paketnya

```html +parse
<x-prezet::alert
    type="warning"
    title="Aplikasi yang Sudah Ada"
    body="Perintah install ini bakal nge-overwrite file vite.config.js dan postcss.config.js yang udah ada. Pastikan kamu udah backup file-file itu dulu sebelum lanjut."
/>
```

Untuk sekarang jalankan installer Prezet dengan perintah berikut: 

```bash
php artisan prezet:install
```

Perintah ini bakal melakukan beberapa hal, di antaranya:

- Menyalin file konfigurasi Prezet ke config/prezet.php
- Nambahin disk penyimpanan Prezet di config/filesystems.php
- Menyalin content stubs ke folder penyimpanan proyek kamu
- Mempublish file Blade vendor yang dibutuhkan
- Menyalin file konfigurasi Tailwind
- Install dependencies Node.js yang diperlukan buat Prezet

Pokoknya, Prezet bakal terinstall dengan lengkap di aplikasi kamu.

## Step 3: Mulai Server Kamu

Setelah instalasi selesai, saatnya mulai server Laravel kamu. Cukup ketikkan perintah ini di terminal: 

```bash
php artisan serve
```

Setelah server berjalan, buka browser dan ketikkan alamat:

[http://localhost:8000/prezet](http://localhost:8000/prezet)

Di sini kamu bakal langsung lihat blog markdown pertama kamu yang udah siap pakai dan didukung sama Prezet.

## Step 4: Generate SQLite Index

Setelah semuanya terinstall dan siap, kita perlu generate SQLite index buat memudahkan pencarian konten. Jalankan perintah berikut di terminal: 

```bash
php artisan prezet:index
```

SQLite index ini penting banget buat mempermudah proses query dan manajemen konten. Buat info lebih lanjut soal fungsinya, cek dokumentasi [Prezet SQLite Index](/index).

## Langkah Selanjutnya

Sekarang, dengan Prezet udah terpasang, kamu udah siap deh buat mulai bikin konten dan sesuaikan blog kamu! Kamu bisa mulai dengan:

-   [Menulis konten markdown](features/markdown)
-   [Pakai komponen Blade di markdown](features/blade)
-   [Optimasi gambar](features/images)
-   [Kustomisasi route](customize/routes), [front matter](customize/frontmatter), dan masih banyak lagi.

Jadi, tunggu apa lagi? Selamat nge-blog pakai Prezet, bikin artikel dan dokumentasi SEO-friendly jadi lebih mudah dan seru.