# Jarkom-Modul-2-E03-2022

## Kelompok E03
- Pedro T. Korwa              05111940007003
- Made Rianja Richo Dainino   5025201236
- Syaiful Bahri Dirgantara    5025201203

### 1. WISE akan dijadikan sebagai DNS Master, Berlint akan dijadikan DNS Slave, dan Eden akan digunakan sebagai Web Server. Terdapat 2 Client yaitu SSS, dan Garden. Semua node terhubung pada router Ostania, sehingga dapat mengakses internet

- Membuat Topologi seperti pada gambar

(Gambar Topologi)

- Konfigurasi node-node seperti berikut :

a. Ostania

(Gambar Konfigurasi Ostania)

b. WISE

(Gambar Konfigurasi WISE)

c. SSS

(Gambar Konfigurasi SSS)

d. Garden

(Gambar Konfigurasi Garden)

e. Berlint

(Gambar Konfigurasi Berlint)

f. Eden

(Gambar Konfigurasi Eden)

- Konfigurasi WISE sebagai DNS Master

(Gambar DNS Master)

- Konfigurasi Berlint sebagai DNS Slave

(Gambar DNS Slave)

- Konfigurasi Eden sebagai Web Server

(Gambar Web Server)

- Arahkan SSS ke WISE

(Gambar mengarahkan SSS ke IP WISE)

- Arahkan Garden ke WISE

(Gambar mengarahkan Garden ke IP WISE)

### 2. Untuk mempermudah mendapatkan informasi mengenai misi dari Handler, bantulah Loid membuat website utama dengan akses wise.yyy.com dengan alias www.wise.yyy.com pada folder wise

- Membuat file /etc/bind/named.conf.local untuk pembuatan domain wise.e03.com di WISE, buat juga konfigurasi CNAME untuk membuat alias www.wise.e03.com

(Gambar konfigurasi domain di /etc/bind/named.conf.local)

- Membuat file /etc/bind/jarkom/wise.e03.com

(Gambar file /etc/bind/jarkom/wise.e03.com)

- Bukti wise.e03.com sudah terbuat

(Gambar ping wise.e03.com)

- Bukti www.wise.e03.com sudah berjalan

(Gambar ping www.wise.e03.com)

### 3. Setelah itu ia juga ingin membuat subdomain eden.wise.yyy.com dengan alias www.eden.wise.yyy.com yang diatur DNS-nya di WISE dan mengarah ke Eden

- Tambahkan konfigurasi subdomain eden.wise.e03.com di file /etc/bind/jarkom/wise.e03.com yang mengarah ke IP Eden

- Tambahkan juga di file tersebut alias www.eden.wise.e03.com dengan CNAME

(Gambar /etc/bind/jarkom/wise.e03.com dengan sudah ada konfigurasi subdomain)

- Bukti eden.wise.e03.com sudah terbuat
(Gambar ping eden.wise.e03.com)

- Bukti www.eden.wise.e03.com sudah berjalan
(Gambar ping www.eden.wise.e03.com)

