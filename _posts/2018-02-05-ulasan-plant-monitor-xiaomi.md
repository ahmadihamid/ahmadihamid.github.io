---
layout: post
title: Review Xiaomi Plant Monitor
category: halamanbelakang
tags: [IoT, Plant Monitor, Review]
comments: true
author: ahmadi
---

Sesuai [janji saya sebelumnya](https://ahmadihamid.com/gaje/etan-ampret/) kali ini saya akan coba mengulas perangkat berkebun pintar buatan Xiaomi. Yaitu Xiaomi Plant Monitor.

Kalau kamu cari di mesin pencari atau malah langsung ke YouTube sebenernya buanyak yang udah me-*review* perangkat ini. Tapi tulisan ini saya usahakan ada sedikit info tambahan. Karena kayaknya belum ada ulasan yang dilakukan oleh seorang *gardener* sekaligus *chemist* sekaligus *computer geek*.

😎

*Wah parah! Sombong!*

😡

`...`

**Unboxing**

Amat sangat disayangkan saya enggak bisa *unboxing*. Karena emang gak ada *box*-nya.

🙄

Seperti biasa demi memangkas ongkos produksi yang ujung-ujungnya merampingkan harga. Xiaomi Plant Monitor hadir dengan bungkus plastik ala kadarnya. Plus secarik manual yang enggak bisa dibaca karena ukuran huruf yang terlalu kecil. Dan berbahasa Cina.

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/9" data-width="100%"></script>

**Menghubungkan Perangkat**

Xiaomi Plant Monitor mengirimkan data lewat Bluetooth Low Energy `4.1`. Data ini dapat dibaca menggunakan aplikasi Android [Flower Care](https://play.google.com/store/apps/details?id=com.huahuacaocao.flowercare).

Seperti yang sudah saya ceritakan sebelumnya. Saya mendapatkan perangkat yang ternyata khusus regional Cina. Jadi saya enggak bisa langsung menghubungkan perangkat begitu saja.

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/11" data-width="100%"></script>

Saya terpaksa teleport dahulu ke Cina menggunakan [fakegps](https://play.google.com/store/apps/details?id=com.blogspot.newapphorizons.fakegps).

🙄

Gilanya lagi. Tadinya saya kira cukup dengan memalsukan lokasi maka aplikasi sudah dapat digunakan. Ternyata alamat IP juga mesti regional Cina **Daratan**.

😩

Sengaja saya cetak tebal kata daratan karena sebelumnya saya lalai dengan kalimat "China Mainland" dan langsung pakai VPN Hong-Kong, yang lebih mudah diperoleh layanan gratisnya. Yang ternyata masih belum dapat restu aplikasi.

Singkat cerita setelah susah payah (mungkin karena kebijakan pemerintah setempat, VPN Cina langka gilak) berkelana mencari VPN Cina Daratan ketemu [ovpnspider.](https://play.google.com/store/apps/details?id=com.ovpnspider) 

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/12" data-width="100%"></script>

Lokasi sudah, alamat IP juga. Sekarang kita dapat menggunakan aplikasi Flower Care!

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/14" data-width="100%"></script>

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/17" data-width="100%"></script>

Setelah perangkat berhasil dipasangkan saya mendapat notifikasi untuk melakukan pembaruan `firmware.` Ada gosip tidak sedap soal ini. Ada yang bilang perangkat jadi tidak bisa dihubungkan menggunakan `openHAB.` Rencananya saya mau pantau kondisi tanaman [lewat Raspi](https://community.openhab.org/t/xiaomi-miflora-sensor-integration/17453). Kekhawatiran saya bertambah karena saya menggunakan versi Cina bukan versi internasional. Yang punya gosip tersendiri lagi yaitu konon perangkat akan di-brick oleh Xiaomi kalau kedapatan digunakan di luar Cina.

😰

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/19" data-width="100%"></script>

**Akurasi Pengukuran**

Kenyang dengan kabar buruk sekarang kita omongin kabar baik yuk!

Di sini saya menguji keakuratan pengukuran Xiaomi Plant Monitor. Walaupun cuma pada parameter kesuburan yang agak intensif.

**Kesuburan/Konduktivitas**

Seperti [bahasan kita dulu](https://ahmadihamid.com/halamanbelakang/meraba-2018/) soal cek kesuburan tanah, Xiaomi Plant Monitor juga memanfaatkan pengukuran konduktivitas (`µS/cm`) buat menentukan tingkat kesuburan tanah. Yang ternyata lumayan akurat. Berikut adalah hasil uji perbandingan dengan Konduktometer yang telah distandarisasi oleh badan standardisasi ternama.

🙈

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/21" data-width="100%"></script>

Itu pada larutan dengan konduktivitas tinggi. Selanjutnya saya coba menggunakan Air demineralisasi. Yang konduktivitasnya sangat rendah. Yang seharusnya menggunakan probe tertutup.

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/23" data-width="100%"></script>

Lumayan yah? Mengingat rentang tanah dikatakan subur lumayan lebar yaitu `500-3000` µS/cm. Dan sebagai catatan tambahan saya menggunakan 2 konduktometer yaitu masing-masing dengan probe khusus sesuai tinggi/rendahnya konduktivitas.

**Suhu**

Buat pengukuran suhu, saya coba mengukur suhu ruangan.

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/25" data-width="100%"></script>

**Ntapz!**

Sayangnya saya bingung buat mengukur intensitas cahaya dan *moisture*.

😳

Tapi berikut adalah pembacaan *moisture* ketika kering dan terbenam di dalam air.

<script async src="https://telegram.org/js/telegram-widget.js?1" data-telegram-post="nocan/27" data-width="100%"></script>

Kabar baik kedua yaitu ternyata kita hanya perlu menggunakan `fakegps` dan `vpn` saat pertama menghubungkan perangkat. Selanjutnya kita enggak harus memalsukan lokasi dan alamat IP ketika menggunakan aplikasi Flower Care. 

Okeh. Itu aja. Semoga bermanfaat. Teliti sebelum membeli. Hindari *seller* `oon.` Dan jangan lupa gabung [@halamanbelakang](https://t.me/halamanbelakang/).

**Assalamualaikum!**
 
😘

**Referensi**

<https://t.me/halamanbelakang/>

