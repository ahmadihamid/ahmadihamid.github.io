---
layout: post
title: Migrasi Windows ke SSD Baru (bagian ke-3/Tamat)
tags: [Windows, Recovery]
category: linux
comments: true
author: ahmadi
--- 

Buat bayar `hutang` pada kamu (iya kamu 😘) pun buat `kejar setoran` *ODOA* ijinkan saya menyudahi serial yang hampir terlupa bahkan dibatalkan yaitu bahasan kita soal migrasi sistem operasi Windows ke `SSD` baru.

Singkat cerita saya menyerah melakukan pemulihan sistem Windows dari sistem operasi GNU/Linux. Walau terlihat sedikit lagi berhasil. Cuma butuh sentuhan akhir. Mungkin. Tapi karena *level* energi sudah rendah saya memutuskan berhenti.

😒

Saya lewati satu-dua cerita gagal dalam recovery via Windows dan berikut adalah cerita berhasilnya yaitu menggunakan perangkat lunak dari [vendor merk SSD](http://www.samsung.com/semiconductor/minisite/ssd/downloads/software/Samsung_Data_Migration_Setup_v30.zip) yang saya gunakan atau lebih tepatnya buatan [Clonix](http://clonix.co.kr/main.php). 

Sayangnya saya lupa tempat menyimpan (atau tak sengaja terhapus) berkas *Screenshot* saat Clonix melakukan `sihirnya`. Sihir memang kata hiperbolis yang saya pilih, karena selesai melakukan *Cloning* **ternyata** si Clonix menulis ulang MBR buat saya, MBR yang tadinya berisi grub ditimpa bootloader yang langsung memanggil Windows (saya lupa namanya, BCD?). Semoga dia tidak menulis hal-hal aneh di sana. Jadi selesai proses cloning, sistem Windows saya langsung siap pakai. Saya terguncang.

😱

Berikut adalah tangkapan layar dari buku manual :

![](/img/kz3-clonix.png) 
 
Seperti yang kamu lihat digambar, kita bisa hanya memilih satu partisi untuk di-*clone*. Ini  yang saya lakukan, saya hanya memilih partisi `C:`. Sayangnya perangkat luak ini belum mendukung format partisi GNU/Linux. Jadi saya tidak bisa sekaligus melakukan *cloning* sistem *ArchLinux* saya di sini.

Tamat.

Referensi :

<https://t.me/halamanbelakang>
