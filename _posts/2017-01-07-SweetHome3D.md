---
layout: post
title: SweetHome3D, Desain Sendiri Rumah Kamu
tags: [GNU/Linux]
comments: true
author: ahmadi
--- 

Saya bukanlah ahli di bidang desain, beberapa orang diberi karunia jiwa seni, yang lainnya logika analitis, dan sayangnya saya **bukan** keduanya.

Namun seringkali saya dihadapkan dengan persoalan yang seharusnya buat dua orang tadi. Semisal diminta membuat sebuah desain denah ruang di tempat kerja, sampai pengalaman ~~traumatis~~ diminta berpartisipasi lomba menyanyi sewaktu kecil.

Ya, inilah hebatnya negara kita, tanpa peduli minat/bakat, anak dipaksa serba bisa bagai dewa, skor baik di semua bidang adalah harga pas, gak boleh ditawar lagi. 

`...`

Yang akan kita bahas sekarang bukan soal bagaimana menyanyi walau anda seorang `Introvert` tapi **bagaimana membuat sebuah desain ruang atau bangunan walau anda bukan desainer**. Dan sebagai bonus walau anda `bokek` karena kita akan menggunakan aplikasi gratis [sweethome3d](http://www.sweethome3d.com/) di atas sistem operasi `GNU/Linux` yang juga gratis.

**Pemasangan Aplikasi**

Buat sistem operasi ArchLinux :
```shell
# pacman -S sweethome3d
```
Buat sistem operasi lain silakan merujuk ke [tautan ini.](http://www.sweethome3d.com/userGuide.jsp#Installation)   

Berikut adalah antar muka sweethome3d :
<img border="0" src="/img/sh3d-antarmuka.png" style="float:left; margin-right:10px"/>

- Panel 1 : daftar furnitur.
- Panel 2 : di sini tempat kita menggambar desain/cetak biru dengan menambahkan furnitur dari panel 1, atau toolbar di atasnya.
- Panel 3 : di sini kita mengatur ukuran dari furnitur yang ditambahkan.
- Panel 4 : tampilan 3D dari desain yang telah dibuat.

**Tutorial Singkat**

- Membuat dinding
<img border="0" src="/img/sh3d-tembok.png" style="float:left; margin-right:10px"/>
Untuk menggambar dinding, gunakan tombol *Create walls*, kemudian tentukan titik-titik tempat dinding dibangun pada `Panel 2`, tekan tombol `Escape` jika semua titik selesai dihubungkan.

- Menambahkan pintu, jendela, dan furnitur
Menambahkan pintu dan jendela dilakukan dengan memilihnya dari `Panel 1` kemudian menyeretnya ke dinding di `Panel 2`. Untuk furnitur kita dapat menempatkannya di posisi yang diinginkan. Kita mungkin perlu menyesuaikan ukuran dari 3 objek tersebut di `Panel 3` agar terlihat proporsoional.

- Ekspor Gambar
<img border="0" src="/img/sh3d-eksporgambar.png" style="float:left; margin-right:10px"/>
SweetHome3D memiliki fitur untuk membuat gambar 3D atau video dari desain yang kita buat melalui menu 3D view - Create photo. Kita dapat melakukan bebrapa konfigurasi seperti : pencahayaan, jam diambil gambar (berpengaruh ke efek cahaya matahari), dan kualitas gambar. Proses *rendering* dapat memakan waktu yang cukup lama, perlu kesabaran apalagi jika gambar dibuat dengan kualitas tinggi.
<img border="0" src="/img/sh3d-denah.bmp" style="float:left; margin-right:10px"/>

Selamat ~~menyanyi~~ mencoba.
😅

Referensi :
[http://www.sweethome3d.com/documentation.jsp](http://www.sweethome3d.com/documentation.jsp) 
[http://www.sweethome3d.com/userGuide.jsp](http://www.sweethome3d.com/userGuide.jsp) 
