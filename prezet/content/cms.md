---
title: Laravel Filament Blog
excerpt: Belajar cara install CMS di Laravel dan setup proyekmu buat aplikasi CMS dengan Filament Blog, kamu bisa pengelolaan konten blog dengan dukungan editor rich text dan markdown. Dengan plugin ini, kamu bisa mengatur postingan, kategori, dan penulis tanpa batasan tampilan di frontend. Ikuti langkah-langkah berikut buat setup proyekmu dan mulai buat aplikasi CRM dengan Krayin.
slug: cms
date: 2024-12-02
image: /prezet/img/ogimages/draft.webp
---

Nah, buat kamu yang lagi nyari cara buat bikin aplikasi CRM dengan Laravel, Krayin bakal jadi solusi yang keren. Dengan Filament, kita bisa setup panel admin yang super fleksibel buat ngelola konten dan data pelanggan dengan mudah. Gak perlu ribet, semua bisa disesuaikan sesuai kebutuhan proyekmu. Yuk, simak langkah-langkah berikut buat setup Filament CMS.

## Step 1: Install Filament dan Panel Admin

Pertama-tama, kamu perlu install Filament Panel Builder dulu. Caranya gampang banget, tinggal jalankan perintah-perintah ini di direktori proyek Laravel kamu: bash Copy code

```bash
composer require filament/filament:"^3.2" -W
php artisan filament:install --panels
```

Dengan perintah ini, Filament bakal otomatis bikin dan daftar service provider baru yang namanya `app/Providers/Filament/AdminPanelProvider.php`. Jadi, siap-siap deh buat panel admin yang keren.

## Step 2: Migrasi Database

Sekarang, tinggal migrasi database supaya semua tabel dan struktur yang dibutuhkan bisa langsung otomatis terbentuk. Cukup jalankan perintah berikut:

```bash
php artisan migrate
```

Dengan perintah ini, database kamu siap buat nambahin data user panel admin, jadi prosesnya lebih cepat dan lancar.

```html +parse
<x-prezet::alert
    type="warning"
    title="PERINGATAN"
    body="Kalau kamu dapet error pas akses panel, cek apakah service provider-nya udah terdaftar di bootstrap/providers.php (untuk Laravel 11 ke atas) atau config/app.php (untuk Laravel 10 ke bawah). Kalau belum, kamu harus tambahin manual deh."
/>
```

## Step 3: Bikin User Panel Admin

Buat kamu yang mau bikin akun pengguna baru buat akses panel admin, tinggal jalankan perintah ini aja:

```bash
php artisan make:filament-user
```

Setelah itu, buka `/admin` di browser kamu, login, dan mulai deh ngebangun aplikasi CRM kamu dengan Krayin.

## Step 4: Setup Filament Blog

Buat kamu yang pengen nambahin fitur blog, tinggal install Filament Blog di Laravel. Ikutin aja langkah berikut: 

```bash
composer require stephenjude/filament-blog
php artisan filament-blog:install
```

Dengan dua perintah itu, kamu udah siap buat setup fitur blog langsung di panel admin kamu. Jadi, kamu bisa bikin dan kelola artikel atau konten di aplikasi tanpa ribet.

## Step 5: Membuat Storage Link

Biar file yang diupload bisa diakses secara publik, kita perlu bikin storage link. Gampang banget caranya:

```bash
php artisan storage:link
```

Perintah ini bakal nge-link folder storage ke folder public, jadi file yang disimpen di storage bisa tampil langsung di aplikasi kamu.

## Step 6: Integrasi Filament Blog

Terakhir, kita integrasi Filament Blog ke dalam panel admin kamu. Cukup tambahkan kode ini di file panel:

```php
use Stephenjude\FilamentBlog\BlogPlugin;
public function panel (Panel $panel): Panel 
    { 
        return $panel 
            ->plugin( 
                BlogPlugin::make()
            ); 
     }
```

Dengan kode ini, fitur blog bakal langsung terintegrasi ke dalam dashboard Filament kamu. Jadi, kamu bisa ngelola blog dan konten lainnya dalam satu tempat, makin praktis kan?