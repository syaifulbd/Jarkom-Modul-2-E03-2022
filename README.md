# Jarkom-Modul-2-E03-2022

## Kelompok E03
- Pedro T. Korwa              05111940007003
- Made Rianja Richo Dainino   5025201236
- Syaiful Bahri Dirgantara    5025201203

### 1. WISE akan dijadikan sebagai DNS Master, Berlint akan dijadikan DNS Slave, dan Eden akan digunakan sebagai Web Server. Terdapat 2 Client yaitu SSS, dan Garden. Semua node terhubung pada router Ostania, sehingga dapat mengakses internet

- Membuat Topologi seperti pada gambar
![image](https://user-images.githubusercontent.com/33245436/198837557-0573c099-ce8e-4431-9d86-87850425be22.png)

- Konfigurasi node-node seperti berikut :

a. Ostania
![image](https://user-images.githubusercontent.com/33245436/198837585-282783ce-7603-4801-8181-99de98f021c5.png)

b. WISE
![image](https://user-images.githubusercontent.com/33245436/198837611-6dc6ba69-b425-49ed-b5b3-aa7ccb558177.png)

c. SSS
![image](https://user-images.githubusercontent.com/33245436/198837631-d2c392dc-6092-42ec-9302-92fbb36679b8.png)

d. Garden
![image](https://user-images.githubusercontent.com/33245436/198837645-5c464c3d-4b7f-4d99-9cb8-4df197c63fd3.png)

e. Berlint
![image](https://user-images.githubusercontent.com/33245436/198837661-f982689b-164e-4aee-a178-ee1055ab8b5f.png)

f. Eden
![image](https://user-images.githubusercontent.com/33245436/198837671-a9b20950-8094-4c9d-9af4-0b4bb85af406.png)

- Konfigurasi WISE sebagai DNS Master
![image](https://user-images.githubusercontent.com/33245436/198837751-67909619-0f20-45aa-90b3-f2cb765107d9.png)

- Konfigurasi Berlint sebagai DNS Slave
![image](https://user-images.githubusercontent.com/33245436/198837887-f0a52054-8832-49a5-91fc-65d398444dd7.png)

- Konfigurasi Eden sebagai Web Server
![image](https://user-images.githubusercontent.com/33245436/198837928-35296833-2f50-45f5-bbba-e45e03e94c36.png)

- Arahkan SSS ke WISE
![image](https://user-images.githubusercontent.com/33245436/198838055-daa079e5-5bc4-42e4-8deb-8aba9b1d42d3.png)

- Arahkan Garden ke WISE
![image](https://user-images.githubusercontent.com/33245436/198838071-09010b2e-ca4d-42cb-b801-65d89b135bd0.png)

### 2. Untuk mempermudah mendapatkan informasi mengenai misi dari Handler, bantulah Loid membuat website utama dengan akses wise.yyy.com dengan alias www.wise.yyy.com pada folder wise

- Membuat file /etc/bind/named.conf.local untuk pembuatan domain wise.e03.com di WISE, buat juga konfigurasi CNAME untuk membuat alias www.wise.e03.com
![image](https://user-images.githubusercontent.com/33245436/198838106-bf4bff93-028c-46b0-b5a5-4fc6057882d0.png)

- Membuat file /etc/bind/wise/wise.e03.com
![image](https://user-images.githubusercontent.com/33245436/198838131-8a7998d4-cf96-4a60-8488-3610a43f3da6.png)

- Bukti wise.e03.com sudah terbuat
![image](https://user-images.githubusercontent.com/33245436/198838152-35659967-0da5-4ee5-a676-5287e136f867.png)

- Bukti www.wise.e03.com sudah berjalan
![image](https://user-images.githubusercontent.com/33245436/198838176-4a81e74c-0bef-4658-81e9-331cfde54635.png)

### 3. Setelah itu ia juga ingin membuat subdomain eden.wise.yyy.com dengan alias www.eden.wise.yyy.com yang diatur DNS-nya di WISE dan mengarah ke Eden

- Tambahkan konfigurasi subdomain eden.wise.e03.com di file /etc/bind/wise/wise.e03.com yang mengarah ke IP Eden

- Tambahkan juga di file tersebut alias www.eden.wise.e03.com dengan CNAME
![image](https://user-images.githubusercontent.com/33245436/198838202-25e75136-eebd-4ca2-9d25-c6076bc7d85b.png)

- Bukti eden.wise.e03.com sudah terbuat\
![image](https://user-images.githubusercontent.com/33245436/198838269-d38e1f40-3100-4596-b1d8-9e27a206f4b8.png)

- Bukti www.eden.wise.e03.com sudah berjalan
![image](https://user-images.githubusercontent.com/33245436/198838257-59cac164-4a35-4a7a-9d23-9dd29eb3d820.png)

### 4. Buat juga reverse domain untuk domain utama

- Membuat Konfigurasi reverse di file /etc/bind/named.conf.local
![image](https://user-images.githubusercontent.com/33245436/198837772-ab0bf5e4-3348-4786-ab03-76ec1460623a.png)

- Membuat file /etc/bind/wise/1.23.10.in-addr.arpa dengan konfiguasi sebagai berikut
![image](https://user-images.githubusercontent.com/33245436/198838310-5f9c0025-fef1-4d0a-812d-592ace990171.png)

- Bukti reverse telah berjalan
![image](https://user-images.githubusercontent.com/33245436/198838278-832a2307-df45-4c3b-9656-5fff9f719e86.png)

### 5. Agar dapat tetap dihubungi jika server WISE bermasalah, buatlah juga Berlint sebagai DNS Slave untuk domain utama
Jawaban : Untuk menyelesaikan soal ini kami melakukan langkah-langkah sesuai pada modul yakni modul DNS bagian 1.2.F dengan menggunakan IP Berlint.
![image](https://user-images.githubusercontent.com/33245436/198837871-5cd270df-ef38-4d20-9e82-49c2a90a8a4b.png)

### 6. Karena banyak informasi dari Handler, buatlah subdomain yang khusus untuk operation yaitu operation.wise.yyy.com dengan alias www.operation.wise.yyy.com yang didelegasikan dari WISE ke Berlint dengan IP menuju ke Eden dalam folder operation
Jawaban : Untuk menyelesaikan soal ini kami juga mengikuti langkah sesuai pada modul DNS bagian 1.2.H dan menambahkan alias www pada konfigurasi node Berlint.
![image](https://user-images.githubusercontent.com/33245436/198837895-2e29eb57-4bf3-4ba4-9947-c476e20c0ce5.png)
![image](https://user-images.githubusercontent.com/33245436/198838370-5303ed3b-a922-4eb1-9af1-b1d08396aea3.png)
![image](https://user-images.githubusercontent.com/33245436/198838808-5e815294-21e1-4497-9741-0d9996806992.png)

### 7. Untuk informasi yang lebih spesifik mengenai Operation Strix, buatlah subdomain melalui Berlint dengan akses strix.operation.wise.yyy.com dengan alias www.strix.operation.wise.yyy.com yang mengarah ke Eden
Jawaban : Penyelesaian soal ini sama seperti penyelesaian soal nomor 2 namun konfigurasi dilakukan pada node Berlint.
![image](https://user-images.githubusercontent.com/33245436/198838357-5065cc3e-a648-4a34-9663-af6379d25bb4.png)
![image](https://user-images.githubusercontent.com/33245436/198838825-71c2083a-8410-4206-8e59-94b5600e0dfa.png)

### 8. Setelah melakukan konfigurasi server, maka dilakukan konfigurasi Webserver. Pertama dengan webserver www.wise.yyy.com. Pertama, Loid membutuhkan webserver dengan DocumentRoot pada /var/www/wise.yyy.com
Jawaban : Penyelesaian soal ini kami melakukannya dengan mengubah DocumentRoot pada `/etc/apache2/sites-available/wise.e03.com.conf` menyesuaikan permintaan soal yakni menjadi /var/www/wise.yyy.com
![image](https://user-images.githubusercontent.com/33245436/198837952-24ecfbe0-71a4-4c43-a4f7-abafc79fb22e.png)
![image](https://user-images.githubusercontent.com/33245436/198839106-6f047419-533a-4d9e-a0b8-f6b0e0dfa0e4.png)

### 9. Setelah itu, Loid juga membutuhkan agar url www.wise.yyy.com/index.php/home dapat menjadi menjadi www.wise.yyy.com/home
Jawaban : Dengan mengikuti modul Web Server bagian C. Directory Alias, kami menambahkan Alias "/home" "var/www/wise.e03.com/index.php/home"
![image](https://user-images.githubusercontent.com/33245436/198838605-e2406ac5-014a-42c2-b158-5ad7f041d422.png)
![image](https://user-images.githubusercontent.com/33245436/198839117-ee48e9bd-a41b-4b3f-bcdb-9f7d56edcfc7.png)

### 10. Setelah itu, pada subdomain www.eden.wise.yyy.com, Loid membutuhkan penyimpanan aset yang memiliki DocumentRoot pada /var/www/eden.wise.yyy.com
Jawaban : Sama seperti soal nomor 8, melakukan konfigurasi DocumentRoot pada node Eden dengan menambahkan file baru yakni eden.wise.e03.com.conf.
![image](https://user-images.githubusercontent.com/33245436/198838767-7b1f22d1-f437-4333-9d65-bdb5db392b95.png)

### 11. Akan tetapi, pada folder /public, Loid ingin hanya dapat melakukan directory listing saja
Jawaban : Menggunakan acuan modul Web Server bagian B. Directory Listing, kami melakukan konfigurasi pada file .conf, menambahkan
`<Directory /var/www/wise.e03.com/public>
     Options +Indexes
 </Directory>` 
![image](https://user-images.githubusercontent.com/33245436/198838766-0e667746-5a02-4368-b7d2-045ba14fcdaa.png)
![image](https://user-images.githubusercontent.com/33245436/198839512-ed558fa9-d0e7-4f36-831b-a4ff473f091f.png)

### 12. Tidak hanya itu, Loid juga ingin menyiapkan error file 404.html pada folder /error untuk mengganti error kode pada apache
Jawaban : Dalam penyelesaian soal ini kami melakukan pencarian di google dan ditemukan bahwa cara menyelesaikannya yakni dengan menambahkan konfigurasi berikut pada file .conf `ErrorDocument 404 /error/404.html`
![image](https://user-images.githubusercontent.com/33245436/198838765-66d5a5e3-ff65-4bcf-a27f-62ca1a8f6ea7.png)
![image](https://user-images.githubusercontent.com/33245436/198839528-a7f77a83-3a8b-4ce4-b64f-47d4b7deea75.png)
