---
layout: post
title: Telegram Desktop untuk Raspbian
tags: [telegram, raspbian]
comments: true
author: ahmadi
category: raspberry
---

Biasanya saat ada oprekan yang lagi *nanggung* atau ada artikel yang udah kebelet saya buang dari *draft* atau ~~tiba-tiba termotivasi buat nulis skripsi~~ (ah lupakan yang ini) terpaksa saya memboyong *notebook* Dell biru 12" milik istri saya ke tempat kerja. 

Mencari celah waktu demi sekedar menambah satu-dua kata pada draf artikel atau menjalankan dua-tiga bait perintah di `terminal` dalam sibuknya (halah) rutinitas pekerjaan sehari-hari seorang buruh berlabel "analis kimia".

Karena saya harus berganti kendaraan dari motor ke sepedah menuju ke tepian sungai Musi yang tidak lain tidak bukan merupakan tempat kerja saya, si imut Dell mini pun terasa berat juga akhirnya. Oleh karena hal ini saya terpikir buat meninggalkan komputer pribadi di tempat kerja. Ah atau sekalian aja bikin area kerja (ada gak sih istilah bahasa Indonesianya?) komputer sendiri.

Saya pun ber-angan-angan membuat meja kerja seperti milik Takaki. Iya si *nelangsa* dari "5 centimetres per second". Aneh memang mungkin karena kisahnya yang terlalu pilu dan ilustrasi kebangetan detil dari om Makoto sampai ke area kerja komputernya pun saya ingat.

![](/img/tur-takaki.jpg) 

Hmm.. Tapi cuma sebatas angan-angan sih akhirnya. Alih-alih monitor layar lebar dan langsing seperti yang digunakan Takaki, saya hanya punya monitor gendut 16" kurang dikit dari negeri yang banyak penari dan penyanyi luar biasa berbakatnya. 

😭

![](/img/tur-nyamnyung.jpg) 

Sebagai *PC*-nya pun saya hanya menggunakan *SBC* Raspberry itu pun generasi ke-2 yang belum punya kartu jaringan nirkabel. 

😭😭

![](/img/tur-raspi.jpg) 

Sebagai kesing buat melindungi dari kemungkinan terpapar percikan air saya menggunakan bahan daur-ulang demi mengurangi sampah yang sudah kelewat banyak kita produksi setiap harinya. **Go Green bray!**

![](/img/tur-kesing.jpg) 

Walau kisah cinta saya tak sepilu masbro Takaki tapi meja kerja komputer saya jelas jauh lebih menyayat hati.

😭😭😭

`...`

Ehem. Ok. Bahasan kita kali ini yaitu memasang Telegram Desktop pada Raspberry dengan sistem operasi Raspbian stretch.

Walau sudah amat sangat banyak memiliki pengguna bahkan gosipnya sudah [banyak tawaran](https://www.bloomberg.com/news/articles/2017-12-12/cryptic-russian-crusader-says-his-5-billion-app-can-t-be-bought) ke Om Durov buat jual Telegram tapi entah kenapa pengembang Raspbian belum memasukkan paket aplikasi perpesanan sejuta fitur ini ke repo sistem operasi yang digunakan oleh komputer pribadi mengharukan saya tadi.

Beruntung ada yang memberi [informasi](https://www.raspberrypi.org/forums/viewtopic.php?t=167038#p1246183) bahwa kita bisa menggunakan paket dari repo `stretch backports` walau hal ini [amat sangat tidak disarankan](https://www.raspbian.org/RaspbianFAQ#Can_I_mix_packages_from_the_Debian_repositories_with_Raspbian.3F). Tapi kita enggak punya opsi lain karena menggunakan Telegram Web di Raspi juga bukan ide jenius.

Jadi yuk kita langsung tambahkan repo tersebut ke `sourcelist` kita!

```shell
/etc/apt/sources.list

deb http://ftp.de.debian.org/debian stretch-backports main 
```

Kebetulan lokasi saya dekat dengan Jerman jadi saya langsung *kopas* saja contoh dari halaman web paket milik Debian. 

😳

```shell
# apt-get update
```

Abaikan peringatan soal keyring atau sesuaikan dengan selera kamu, saya abaikan karena berencana pakai repo ini sekali saja. 

```shell
# apt install telegram-desktop
```

Abaikan lagi verifikasi key di sini.

Selesai deh, kita pun sudah bisa *ber-telegram-ria* di Raspberry Pi dengan lancar membahana.

![](/img/tur-ss.jpg)

***Referensi :***

<https://infinitemirai.wordpress.com/2013/11/28/five-centimeters-per-second-five-centimeters-per-second/>