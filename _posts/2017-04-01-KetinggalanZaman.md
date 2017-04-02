---
layout: post
title: Migrasi Windows ke SSD Baru
tags: [Linux]
comments: true
author: ahmadi
summary: "Di sini saya akan menggunakan wimlib, sebenarnya tersedia banyak pilihan perangkat lunak untuk membuat wim image namun karena saya telah ketergantungan dengan sistem operasi Linux - dan melupakan banyak hal mengenai administrasi di sistem operasi Windows - saya langsung mencari paket yang tersedia untuk ArchLinux."
--- 

Saya hampir mustahil dapat dikatakan makhluk kekinian. Jika kebanyakan manusia berusaha sekuat tenaga [demi mengikuti perkembangan zaman](http://www.independent.co.uk/life-style/gadgets-and-tech/news/iphone-6s-chinese-men-try-to-sell-kidney-to-buy-new-handset-10501755.html), dan sisanya yang sedikit menjadi luar biasa, kemudian melampaui zaman itu sendiri. Saya sebagai manusia biasa enggak mampu menjadi opsi kedua, pun enggak mau di opsi satu. Saya lebih memilih meninggalkan zaman ke belakang atau setidaknya diam di tempat, semisal saya bangga mampu bertahan menggunakan ponsel symbian sampai akhir 2015! 

😎

>"biar miskin asal sombong "

Ya.. 
Bukan pencapaian yang luar biasa sih. Toh ayah saya tidak menggunakan ponsel sama sekali sampai saat tulisan ini dibuat.

Namun sepertinya seiring bertambah usia, bertambah bertemu manusia, idealisme memudar. Hati-hati! 
Hal ini terlihat dari beberapa waktu lalu saya `kelepasan` membeli SSD demi meningkatkan performa laptop yang sepertinya selalu menjerit, meraung, terseok-seok saat digunakan.

`...`

Sampai di sini saya akhiri intro bernuansa `"curcol"`.

😂

Bahasan kita kali ini adalah "**kloning windows saat migrasi dari HDD ke SSD**"

Di sini saya akan menggunakan [wimlib]( https://aur.archlinux.org/packages/wimlib/ ), sebenarnya tersedia banyak pilihan perangkat lunak untuk membuat [wim image](https://en.wikipedia.org/wiki/Windows_Imaging_Format)  namun karena saya telah ketergantungan dengan sistem operasi Linux - dan telah melupakan banyak hal mengenai administrasi di sistem operasi Windows - saya langsung mencari paket yang tersedia untuk `ArchLinux`.

---

**wimcapture**

Untuk membuat `wim image` saya menjalankan perintah [wimcapture] [lokasi mounting partisi windows] [lokasi penyimpanan file wim image] [opsi]  :

```shell
$ wimcapture /run/media/annajm/A47C19827C195102 bakaup.wim --boot --check
```

setelah menunggu 2 jam, berkas terkompresi `bakaup.wim` dengan ukuran  sebesar 12GB pun siap!


---

**wimapply**

Selanjutnya kita akan menggunakan `wimapply` untuk merestore sistem operasi Windows ke partisi di SSD baru kita :

```shell
# wimapply bakaup.wim /dev/sda2
```
kita butuh akses root di sini.

Selesai `wimapply` melakukan tugasnya kita harus memperbaharui `grub.cfg`

```shell
# grub-mkconfig -o /boot/grub/grub.cfg
```

---

**Mulai ulang sistem!**

<img border="0" src="/img/ketinggal-berubah_resize.jpg" style="float:left; margin-right:10px"/>

jreng jreng..
kecewa sungguh kecewa..
untuk ke-sekian kalinya patah hati saya dibuat `M$`

😭

"kamu berubah" [katanya](https://answers.microsoft.com/en-us/windows/forum/all/0xc000000e-boot-error/ef08ab00-e130-4301-bc80-79d5b414a81f).

**ALASAN!**

Aku gak berubah, ~~dasar kamu binatang jalang, dari kumpulannya yang terbuang!~~

`...`

Sekian tutorial kali ini, semoga bermanfaat.

`...`

---

Bingung? Kali pertama melihat tutorial berisi kegagalan?

Maaf deh kalo bikin kamu `kecele`.

😔

Pun buat `M$`, maaf kalo saya pake kata kasar, mungkin kita enggak cocok karena kamu terlalu baik untuk diriku yang ketinggalan zaman ini!

`Bersambung..`


Referensi :

[https://wimlib.net/](https://wimlib.net/) 
