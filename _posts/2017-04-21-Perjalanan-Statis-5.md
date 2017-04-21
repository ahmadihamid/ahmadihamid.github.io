---
layout: post
title: Migrasi Diskusi pada Disqus 
tags: [Web, Jekyll, Disqus]
category: pemrograman
comments: true
author: ahmadi
--- 

Beberapa hari lalu tanpa sengaja saya menghilangkan sejumlah **besar** (padahal sedikit dan memang sedikit total jumlahnya) komentar pengaya `Disqus` di dalam AhmadiHamid.com. Semua kenangan indah bersama kamu (iya kamu) hilang. Lenyap. Hujan pun tak mampu [mengembalikannya](https://bluemeda.web.id/ditinggal-pas-lagi-sayang-sayangnya-part-2/). 

😨


> Hujan, katak berzikir akan datangnya, tumbuhan [bersyukur](http://www.compoundchem.com/2014/05/14/thesmellofrain/) karenanya, para munafik hilang dari Masjid [takut](https://www.facebook.com/xgaptek/posts/10212754121198813) bertemu dia.

Berbicara hujan. Entah sejak kapan saya suka hujan. Walau sewaktu kecil fisik saya lemah dan mudah sakit sehingga enggak bisa bareng teman sebaya menari ria di bawah guyuran hujan. Saya cuma bisa merindu cemburu di bawah payung atau atap teduh. Luar biasa banyak momen **berhak** dikenang yang terjadi saat hujan. 

😚

---

Kembali ke diskusi/komentar Disqus kita yang hilang.Ternyata hal ini terjadi *gegara* `tautan` dari artikel berubah akibat saya menambahkan kategori pada setiap artikel. Tautan yang semula **domain.anu/judul-artikel** berubah menjadi **domain.anu/kategori/judul-artikel**. Fitur yang sangat bermanfaat dari [Beautiful Jekyll](http://deanattali.com/beautiful-jekyll/).

Semula saya pasrah saja komentar dalam blog ini hilang. Mulai dari `nol` lagi gumam saya. Tapi setelah curhat di grup [PegeLinux](https://www.google.com/search?q=PegeLinux) ternyata Disqus memiliki fitur migrasi untuk memindahkan diskusi ke tautan baru bahkan ke domain baru. 
Terimakasih Disqus.

Terdapat tiga skenario yang mungkin terjadi untuk migrasi yaitu :

- **Migrasi Domain** : yaitu ketika kita berganti domain semisal dari `http://domainA.anu` > `http://domainB.anu`

- **Migrasi Path** : ini yang saya alami, seperti yang sudah saya lejaskan di atas.

- **Redirect Crawler** : jika kita sebelumnya telah menyiapkan `301 redirects`.

**Langkah Migrasi Path**

- Masuk ke menu migrasi : **https://[short-name-kamu].disqus.com/admin/discussions/migrate/**

- Pilih menu `Start URL mapper`

- Unduh berkas CSV dari URL map kita

![](/img/ps5-unduh.png) 

- Sunting berkas CSV tersebut, ada hal aneh terjadi di sini, berkas CSV yang diberikan berupa berkas terkompresi dengan ekstensi `.gz` tapi saya tidak bisa mengekstraknya, iseng saya rename dengan menghapus`.gz` ternyata bisa dibuka menggunakan `LibreOffice!`

![](/img/ps5-sunting.png) 

- Unggah URL map yang baru

![](/img/ps5-unggah.png) 

- Selesai. Di akhir konfirmasi migrasi terdapat pesan bahwa diskusi mungkin memakan waktu hingga 24 jam untuk dapat kembali. Tapi saya coba cek **5-10 menit** sudah berhasil muncul kembali.

![](/img/ps5-selesai.png) 

Semoga bermanfaat.

**Referensi** :

<https://t.me/halamanbelakang>

<https://help.disqus.com/customer/en/portal/articles/912757-url-mapper>
