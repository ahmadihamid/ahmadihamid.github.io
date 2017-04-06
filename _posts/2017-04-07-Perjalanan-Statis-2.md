---
layout: post
title: Web Dokumen Statis Buat Guru Mandiri
tags: [Web]
comments: true
author: ahmadi
--- 

Saya adalah guru yang buruk. Itu harga pas gak bisa ditawar lagi. Sewaktu kecil adik saya selalu menangis kalau diajari oleh kakaknya. Saat belajar bersama teman sebaya mereka pasti kecewa saat saya giliran menjelaskan suatu permasalahan. Algoritmanya enggak manusiawi. Analoginya bukan dari Bumi. Asing katanya. 

Oleh karena itu saya sangat hormat dan sayang pada guru. Semisal pada guru agama saya yang manis atau guru analisa fisika non instrumen yang imut dulu semasa sekolah. `YKWIM`. 
😋

`...`

Melanjutkan serial "Perjalanan Statis" kita, kali ini kita akan membuat halaman web statis yang dapat dimanfaatkan oleh seorang guru. Yaitu suatu halaman web statis yang memiliki layanan berbagai dokumen seperti slideshare

**Kenapa enggak pake yang sudah ada saja? **

Pertama, sesuai manfaat yang sudah kita bahas di seri sebelumnya (link), di poin pertama soal kecepatan kita akan mencoba melakukan uji banding halaman Web yang kita buat dengan Web profesional di atas.
Kedua, ya karena kita bisa. 
😎
Kalau ada yang gratis kenapa harus pakai yang "gratis". 
😉

**Buat repo Web Statis **

Jika kamu belum memiliki sebuah repo web statis silakan ikuti [materi kita sebelumnya ](https://ahmadihamid.com/Perjalanan-Statis-1/)  

**Pasang Pengaya VieweJS**

Selanjutnya kita akan memasang VieweJS untuk web statis kita. ViewerJS menggabungkan beberapa tools sumber terbuka yang dibangun di atas HTML dan Javascript, yang berfungsi untuk mebuka/me-render berkas dokumen pada halaman web.
Untuk Pemasangan kita cukup mengunduh berkas ViewerJS [ di sini](http://viewerjs.org/releases/ViewerJS-latest.zip)  dan mengekstraknya ke repo web statis kita. 

![](/img/ps-viwerjs.png) 

**Memanggil Dokumen**

Kita akan menggunakan skrip `iframe` untuk melakukan *embedding* dokumen ke halaman web, contoh halaman`+`skrip adalah sebagai berikut :

```shell
---
layout: page
title: Modul Pak Guru
comments: true
---

<div class="message">
  Modul yah bukan Modol. Ingat!
  
</div>

---

<iframe src = "/materi/ViewerJS/#../buku/Presentasi Transfer Knowledge.odp" title="Presentasi Transfer Knowledge" width='800' height='600'  allowfullscreen webkitallowfullscreen></iframe> 
```
Simpan sebagai `anjay.md` di direktori web kamu maka halaman akan dapat diakses di **`<namakamu>.github.io/anjay`**

**Otomasi**

Kalau kamu jeli ada sedikit kekurangan pada web kita yaitu kita harus menambahkan entry `iframe` setiap kali mengunggah modul baru.
😂
Untuk itu berikut adalah skrip yang melakakukannya dengan ikhlas buat kita :

```shell
#!/bin/bash
laman=kubu.md;

#cari dah hapus semua line berawalan <iframe
sed '/^<iframe/ d' $laman > $laman.tmp;

#masukin buku ke laman.tmp
for buku in buku/*
do
 echo '<iframe src = "/ViewerJS/#../'$buku'" width="389" height="550"  allowfullscreen webkitallowfullscreen></iframe>' >> $laman.tmp;
done

#update laman
cat $laman.tmp > $laman;
rm $laman.tmp;
```

Bukan skrip yang hebat. Cuma skrip dadakan. Kalau kamu jeli lagi belum ada `prompt` buat mengatur ukuran tampilan dokumen, dan masih harus melakukan `push` manual.
😳

**Pengujian**

Iseng kita bandingin performa halaman statis kita yuk!

-  https://www.scribd.com/document/344235167/Presentasi-Transfer-Knowledge

![](/img/ps-scribd.png) 

- https://www.academia.edu/32291160/Presentasi_Transfer_Knowledge

![](/img/ps-academia.png) 

- https://ahmadihamid.com/kubu/

![](/img/ps-modol.png) 

Walau ada yang aneh.. Yah kira-kira gitu lah. Web statis masih lebih gegas ketimbang web dinamis!

Selamat mengajar!
😘

> "bapakku"
>
> pak Ino guruku
>
> darahku dari tintamu 


**Referensi** :

http://viewerjs.org/instructions/