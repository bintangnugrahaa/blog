---
title: Laravel Krayin  
excerpt: Belajar cara install Krayin di Laravel dan setup proyekmu buat aplikasi CRM dengan Krayin. Dengan Krayin, kamu bisa kelola pelanggan, data, dan semua fitur penting dalam satu aplikasi dengan mudah. Ikuti langkah-langkah berikut buat setup proyekmu dan mulai buat aplikasi CRM dengan Krayin.  
slug: krayin  
date: 2024-11-30  
image: /prezet/img/ogimages/index.webp  
---

Krayin CRM itu adalah framework CRM yang dirancang khusus dengan teknologi open-source yang keren banget. Dibangun pakai Laravel (framework PHP yang powerful) dan Vue.js (framework JavaScript progresif), Krayin bikin kamu bisa membangun aplikasi CRM yang gak cuma canggih, tapi juga gampang banget dipakai. Yuk, ikutin langkah-langkah berikut buat mulai bikin aplikasi CRM kamu.

## Step 1: Buat Project Laravel CRM

Pertama-tama, tentuin folder tempat kamu mau install Krayin. Setelah itu, buka terminal dan masuk ke folder tersebut. Kalau udah siap, jalankan perintah ini untuk install Krayin di project Laravel kamu:

```bash
composer create-project krayin/laravel-crm
```

Perintah ini bakal bikin project Laravel CRM baru. Setelah itu, masuk ke folder project-nya dan kamu udah siap deh mulai kembangkan aplikasi CRM kamu.

## Step 2: Install dan Setup Krayin CRM

Langsung aja, jalankan perintah berikut buat install dan setup Krayin CRM: 

```bash
php artisan krayin-crm:install
```

Perintah `php artisan krayin-crm:install` ini bakal nginstall dan nyiapin Krayin CRM di Laravel kamu. Begitu selesai, aplikasi CRM kamu udah siap pakai dengan fitur default yang udah terpasang.

```html +parse
<x-prezet::alert
    type="warning"
    title="PERINGATAN"
    body="Kalau pas proses instalasi file .env nggak ada, installer bakal minta kamu masukin informasi yang diperlukan."
/>
```

## Step 3: Setup Aplikasi dan Buat Admin Credentials

Selama proses instalasi, kamu bakal diminta untuk masukin beberapa informasi. Ini dia yang perlu kamu isi: 

```bash
- Please enter the application name : 
- Please enter the application URL : 
- Please select the default application locale : 
- Please select the default currency : 
- Please select the database connection : 
- Please select the database host : 
- Please select the database name : 
- Please enter your database username : 
- Please enter your database password : 
```

Selain itu, kamu juga bakal diminta buat bikin kredensial admin. Isi aja informasi berikut buat ngebuat akun admin kamu:

```bash
- Enter the name of the admin user :
- Enter the email address of the admin user :
- Configure the password for the admin user :
```
