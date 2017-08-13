---
layout: post
title: Mengontrol Kodi lewat HDMI-CEC
tags: [raspberry, openwrt, lede]
comments: true
author: ahmadi
category: raspberry
---

Mengendalikan *media centre* `Raspberry Pi` atau kita spesifikkan saja `Kodi` menggunakan aplikasi Android semisal [Yatse](https://play.google.com/store/apps/details?id=org.leetzone.android.yatsewidgetfree) atau [Kore](https://play.google.com/store/apps/details?id=org.xbmc.kore) alias remot resmi Kodi memang cukup memudahkan. Tapi ternyata masih cukup mengganggu jika kita mesti mengambil ponsel kemudian menghubungkannya ke jaringan nirkabel rumah kita. Ditambah lagi di tangan kita sudah ada remot tv (jika kamu menggunakan tv sebagai monitor). Malas memang enggak ada batasnya. Kadang saya malas untuk malas dan amat ingin sesekali untuk rajin namun malas rasanya.

`...`

Beruntung ternyata kita masih memiliki alternatif untuk lebih menghemat energi yaitu kita bisa menggunakan pengendali jauh milik tv tersebut untuk juga mengendalikan mesin Raspberry Pi kita yaitu dengan memanfaatkan `HDMI-CEC.`

CEC (Consumer Electronics Control) memungkinkan kita untuk mengontrol perangkat lain melalui port HDMI. Fitur ini umumnya telah tersedia pada tv modern.

**Mengaktifkan HDMI-CEC pada TV**

Mungkin terdapat beberapa perbedaan letak atau istilah untuk konfigurasi HDMI-CEC atar merk TV, pada TV merk Sony milik saya opsi HDMI-CEC ini terletak di `SETTING` -> `Set-up` -> `HDMI Set-up`.

![](/img/cec-tv1.jpg)

![](/img/cec-tv2.jpg)

![](/img/cec-tv3.jpg)

Perangkat kamu dapat dilihat di `HDMI Device List` jika terdeteksi dengan baik. Satu catatan penting tentang ini yaitu versi kabel yang digunakan, yaitu minimal versi 1.3, saya agak ragu soal ini dan lupa pernah baca di mana, pada halaman [wiki](http://kodi.wiki/view/CEC) kodi `libCEC` merekomendasikan versi 1.4b.

🤔

Beberapa kabel HDMI "sembarang beli" yang saya miliki ternyata tidak dapat digunakan. Berikut ini adalah spesifikasi kabel milik saya yang bekerja dengan baik :

![](/img/cec-kabel.jpg)

**Mengaktifkan HDMI-CEC pada Kodi**

Konfigurasi CEC dapat ditemukan di `System` -> `Settings` -> `System` -> `Input Devices` -> `Peripherals` -> `CEC adapter` 

![](/img/cec-kodi.jpg)

Kita juga dapat pengatur keymap dengan menyunting berkas `remote.xml` jika mau. Kamu dapat merujuk ke [wiki](http://kodi.wiki/view/CEC#Settings_in_Kodi_for_CEC) untuk hal ini. Saya sendiri cukup menggunakan keymap bawaan.

**Nama Dagang**

Satu hal gila terjadi di sini. Walau merupakan teknologi yang kompatibel para pabrikan memberi nama dagang masing-masing buat HDMI-CEC mereka. Berikut adalah instilah HDMI-CEC dari beberapa produsen :

-    **Hitachi** - HDMI-CEC
-    **LG** - SimpLink
-    **Mitsubishi** - NetCommand for HDMI
-    **Onkyo** - RIHD (Remote Interactive over HDMI)
-    **Panasonic** - VIERA Link or HDAVI Control or EZ-Sync
-    **Philips** - EasyLink
-    **Pioneer** - Kuro Link
-    **Samsung** - Anynet+
-    **Sharp** - Aquos Link
-    **Sony** - BRAVIA Link or BRAVIA Sync
-    **Toshiba** - Regza Link or CE-Link

Pada TV Sony saya terdapat 2 port HDMI dan ternyata hanya port 1 (HDMI-MHL) yang mendukung teknologi CEC.

**Sekian. Selamat mencoba.**

**Referensi :**

<http://kodi.wiki/view/CEC>