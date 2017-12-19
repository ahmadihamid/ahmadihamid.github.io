---
layout: post
title: Membangun Website dalam Jaringan DarkNet
tags: [Darknet, Web, Onion, Tor]
category: linux
comments: true
author: ahmadi
--- 

Sebelum kita ke judul yang terlihat `angker` di atas yuk sejenak kita lempar imajinasi 100 tahun ke masa depan dimana ternyata dunia dikuasai seorang diktator yang melarang segala aktivitas berkebun. **Gila!** Bahkan seluruh bentuk tulisan dari buku sampai sekedar blog semacam [ahmadihamid.com](ahmadihamid.com) pun kena *cyduk* tim khusus penyensoran milik sang tiran. **Wow!** 
Hal ini terjadi karena sang autokrat memandang berkebun adalah teknik `hiperpurba` yang sudah seharusnya digantikan demi membawa peradaban manusia menuju era `hipermodern` dibawah kekuasaannya.

Hampir 97% makanan saat ini adalah hasil sintesis buatan pabrik milik pemerintah! **Ajig!**

Mungkin kamu bertanya 3% nya apa?

Sisa 3% tersebut adalah makanan alami nan lezat yang beredar di pasar `hipergelap!` Jeng jeng.. Yang hanya bisa dibeli melalui situs `onion` di dalam jaringan darkweb.

つづく

`...`

Wah saya punya bakat lain sepertinya.

Bakat menulis cerita buruk.

`...`

Yang ingin saya bahas kali ini yaitu membuat "situs bawang" alias `onion.`

Saya terpaksa membuat ilustrasi imajiner amat miris di atas karena khawatir ada pembaca yang malah terinspirasi kalau saya tulis ilustrasi sebenarnya.

Atau mungkin sebaiknya enggak usah ambil judul ini kali ya..

🤔

Ya intinya semua yang terjadi akibat tulisannya ini bukan tanggung jawab penulis. Dan sebagai catatan amat **penting** tulisan ini **enggak** akan bikin kamu tak teridentifikasi sama sekali. Butuh [perjalanan amat panjang](https://www.bentasker.co.uk/documentation/linux/307-building-a-tor-hidden-service-from-scratch-part-1)  buat itu dan sekali lagi itu **tak ada di artikel ini!**

Oke kita bahas sedikit tentang `Tor` terlebih dahulu. Tor adalah sebuah jaringan komputer yang memungkinkan kita untuk meningkatkan privasi dalam ber-internet. Pengguna Tor menjelajah area publik internet melalui serangkaian *relay* anonim alih-alih terhubung langsung ke tujuan. Karena hal tersebut Tor secara tidak langsung memungkinkan pengguna buat mengakses tujuan atau konten yang diblokir. Tor juga dapat digunakan untuk mempublikasikan halaman web yang lokasinya disembunyikan, halaman web onion berkebun sesuai cerita pembuka tadi, yang bakal kita coba. Tapi ijinkan saya cerita Tor sedikit lagi.

![](/img/tor-deepweb.jpg)
[sumber gambar](https://dreammarketdrugs.com/the-deep-web-dark-web-and-the-darknet-marketplaces/) 

Mungkin kamu sering mendengar cerita negatif soal Tor ini. Deepweb. Darknet. Pasar gelap lah, obat terlarang lah, pornografi anak lah. Area gelapnya internet pokoknya. Terlepas dari keburukan tersebut Tor banyak dimanfaatkan oleh para aktivis untuk melindungi keselamatannya. Wartawan misalnya memanfaatkan jaringan Tor agar narasumber yang mesti dijaga identitasnya mau berbagi cerita. Atau hanya sekedar manusia sederhana yang enggak pengen kegiatan ber-internet-nya diawasi pemerintah dan perusahaan `hiperkepo` di luar sana. Bayangkan enggak cuma Tuhan dan malaikatnya yang tau kamu nonton bokep! 

Dan banyak lainnya yang bisa kamu baca di [halaman resmi](https://www.torproject.org/about/overview.html.en) milik Tor.

Dah ah. Yuk kita bikin web onion pertama kita.

Di sini saya melakukan *setup* di komputer server dengan sistem operasi Ubuntu tapi kalau kamu mau coba di komputer rumah ya sama saja.

**Instalasi Web Server (LAMP)**

```shell
sudo apt-get update
sudo apt-get install tasksel
sudo tasksel install lamp-server
```

Di atas adalah langkah singkat setup LAMP Stack pada Ubuntu 16.04. Buat kamu yang pengen mempelajari lebih jauh, bisa baca [ini](https://help.ubuntu.com/lts/serverguide/index.html) atau [ini](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04).

**Instalasi Tor**

```shell
sudo apt install tor
```

Beruntung paket tor sudah tersedia di repo resmi Ubuntu jadi kita enggak perlu repot tambah repo lain, biar semua diatur manajer paket Ubuntu.

**Tor Hidden Services**

Setelah tor terpasang tugas kita selanjutnya adalah mengkonfigurasi `Hidden Services` milik tor yang terdapat pada file `/etc/tor/torrc` *uncomment* atau tambahkan baris berikut :

```
HiddenServiceDir /var/lib/tor/hidden_service/
HiddenServicePort 80 127.0.0.1:8080
```

Simpan perubahan yang dibuat dan restart layanan tor. 

```shell
sudo service tor restart
```

Inilah keistimewaan Ubuntu, selesai instalasi sebuah paket sistem otomatis menjalankan layanannya di latar belakang. Terimakasih Ubuntu!

🙄

```shell
ls /var/lib/tor/hidden_service/
hostname  private_key

cat /var/lib/tor/hidden_service/hostname 
hqpr5nq4qf7mrssy.onion
```
Setelah tor berjalan, tor akan membuat sebuah folder `HiddenServiceDir` sesuai konfigurasi kita tadi kemudian membuat dua buah berkas yaitu `private_key` dan `hostname` untuk layanan onion kita. Simpan baik-baik yang pertama dan viralkan yang kedua.

😉

**Mengakses Website Onion**

Di atas bisa kita lihat alamat web onion saya yaitu [hqpr5nq4qf7mrssy.onion](hqpr5nq4qf7mrssy.onion), alamat ini tidak dapat dibuka dari jaringan internet normal atau kita sebut saja "clear net" karena memang TLD `.onion` hanya terdapat pada jaringan tor. Oleh karena itu untuk mengakses web onion kita harus terhubung dahulu ke jaringan tor.

Di sini kita akan mencoba terhubung ke jaringan tor melalui ponsel Android yaitu menggunakan [Orbot](https://play.google.com/store/apps/details?id=org.torproject.android) yang bisa kamu pasang langsung dari PlayStore. Kemudian untuk browser kita gunakan [Orfox](https://play.google.com/store/apps/details?id=info.guardianproject.orfox) yang sebenarnya browser hasil modifikasi Firefox.

![](/img/tor-orbot.jpg)

Selesai deh! Selamat berselantjar dan berkarja di DarkNet.

😎

**Referensi**

<https://t.me/halamanbelakang>

<https://www.torproject.org/docs/documentation.html.en>
