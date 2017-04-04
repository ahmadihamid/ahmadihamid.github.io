---
layout: post
title: Migrasi Windows ke SSD Baru (bagian ke-2)
tags: [Windows]
comments: true
author: ahmadi
--- 

Tetiba teringat pepatah kurang bijak namun kaya akan kejujuran :

> Pemain catur kehilangan 100 poin ELO setelah menikah.

Terdengar sedikit egois namun ternyata banyak benarnya. Bahkan kita bisa menambah klausa pada kata bijak di atas menjadi :

> ...berkurang 100 lagi saat kedatangan seorang anak.

Egois! Walau ada sedikit anomali yang saya alami yaitu justru ELO (bukan resmi) **naik** saat anak pertama saya - yang ditunggu-tunggu selama 3 tahun - lahir, dan kemudian anomali yang sama terjadi saat anak kedua - yang tak diduga-duga - diamanahkan pada saya dan istri. 

> Marsyad dan Hilya. Tak dapat dipercepat apalagi ditunda.

Tapi dari segi produktifitas masih jelas terlihat menurun. Saya mulai sulit menulis - saat membuat tulisan ini pun kakak merengek karena penasaran dengan Laptop dan ayahnya- dan berkarya -satu yang disayangkan banyak orang kecuali saya yaitu Olimpiade Nasional MIPA Perguruan Tinggi tingkat Nasional yang bertepatan dengan detik-detik kelahiran anak pertama. Malu rasanya pada diri sendiri yang dulu sombong bilang "Bisa!" saat muda.

`...`

Melajut bahasan *cloning* Windows sebelumnya, setelah "berhasil gagal" menggunakan `wimlib` saya masih berkeras menggunakan Linux untuk memulihkan Sistem Windows. Kali ini saya menggunakan `DCFL (DoD Computer Forensics Lab) dd replacement with hashing`. Saya masih kurang menjelajahi paket bernama aneh ini, yang saya tau `dcfldd` = `dd` dengan informasi `byte` yang telah berhasil diperoses. 

```shell
# dcfldd if=/dev/sdc1 of=/dev/sda2 bs=64 conv=noerror,sync
```

Kalau kamu belum tau/mau tau maksud dan tujuan perintah di atas kamu bisa menggunakan `man dd` sama saja soalnya. Selanjutnya kita memperbarui `grub.cfg` untuk menambahkan partisi baru Windows kita.

![](/img/kz2-dcfldd.jpg) 

Selesai `dcfldd` melakukan tugasnya, kemungkinan besar - karena ukuran partisi yang berbeda - partisi baru kita akan memiliki bagian tidak teralokasi. Gunakan `gparted` untuk mengisi bagian tersebut.

![](/img/kz2-gparted.jpg)

Semua terlihat baik, yuk kita mulai ulang komputer dengan percaya diri!
::kacanamata:


![](/img/kz2-bootgagal.jpg)

Ternyata eh ternyata.. "aku tidak mampu mengerti disk kamu" kata bootloader Sa7an (bukan typo). 
Sejujurnya saya juga enggak sanggup mengerti SSD bermerk nyamnyung ini. Saya enggak ngerti kenapa harganya mahal.
:::nangiss.
Sekilas menjelajah mesin pencari, konon ini akibat bootloader rusak dan seterusnya, saya juga sudah mencoba buat memulihkannya melalui *installer*, namun ternyata SSD tidak terdeteksi, butuh driver katanya. 
OK saya berhenti sampai di sini. Menyerah, ganti SSD dengan HDD lama, dan kemudian mencoba recovery lewat sistem Windows saja. Nantikan kelanjutannya di bagian ketiga dari seri kita yang sangat menegangkan ini.

Selamat ini adalah (kurang/lebih) "tutorial gagal" kedua yang kamu baca!

Referensi :

<http://dcfldd.sourceforge.net/>