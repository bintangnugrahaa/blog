---
title: Laravel Breeze  
excerpt: Belajar cara install Breeze dan mulai bikin fitur autentikasi seperti login, register, reset password, verifikasi email, dan halaman profil. Ikuti langkah-langkah berikut buat setup proyekmu dan mulai autentikasi dengan Breeze.  
slug: breeze  
date: 2024-12-05  
image: /prezet/img/ogimages/configuration.webp  
---

Laravel Breeze adalah cara simpel buat nambahin semua fitur autentikasi yang biasa ada di Laravel, seperti login, register, reset password, verifikasi email, dan konfirmasi password. Gak cuma itu, Breeze juga ngasih halaman "profil" yang super gampang buat update nama, email, dan password pengguna. Penasaran? Yuk, simak langkah-langkah buat setup Breeze di aplikasi Laravel kamu.

## Step 1: Install Laravel Breeze

Kalau kamu udah punya aplikasi Laravel dan belum pake starter kit, kamu bisa install Laravel Breeze secara manual pake Composer. Tinggal jalankan perintah ini di terminal:

```bash
composer require laravel/breeze --dev
```

Setelah Composer selesai install package Laravel Breeze, lanjutkan dengan perintah berikut buat ngejalanin `breeze:install` di Artisan. Perintah ini bakal nge-publish tampilan autentikasi, route, controller, dan resource lainnya ke aplikasimu. Jadi, semua kode autentikasi bakal ditaruh langsung di aplikasi kamu, biar bisa langsung dikontrol dan dipahami implementasinya.

## Step 2: Setup Laravel Breeze

Setelah install Breeze, kamu perlu setup stack frontend dan framework testing yang sesuai sama proyek kamu. Jalankan perintah ini buat memulai setup: 

```bash
php artisan breeze:install
```

Begitu dijalankan, sistem bakal nanya stack frontend mana yang kamu pilih, apakah menggunakan Blade atau Inertia.js dengan Vue.js. Pilih aja yang cocok sama kebutuhan aplikasi kamu.

## Step 3: Migrasi Database

Sekarang, saatnya migrasi database buat nyiapin tabel-tabel yang dibutuhkan buat autentikasi. Jalankan perintah berikut: 

```bash
php artisan migrate
```

Dengan perintah ini, database kamu bakal diupdate otomatis dengan semua tabel yang diperlukan, seperti tabel pengguna, password resets, dll. Setelah itu, fitur-fitur login, register, dan lainnya siap banget buat dipakai.
