---
layout: post
title: Upgrade Windows 7 ke 10 Gratis dan Halal 
category: linux
tags: [windows 10, gratis, upgrade]
comments: true
author: ahmadi
--- 

Dulu saat Microsoft menawarkan *upgrade* gratis ke Windows versi terbaru yaitu Windows "sepuluh" saya cuek aja. Wajar karena saya 99% menggunakan sistem operasi Linux. Ada Windows di laptop cuma karena bawaan. Dibuang sayang. Namun setelah bertahun berlalu saya pikir itu keputusan bodoh. Terlanjur dibuang sayang kenapa enggak diperbaharui sekalian. [Biar bisa makin lama disimpan.](https://support.microsoft.com/id-id/help/13853/windows-lifecycle-fact-sheet) 

29 Juli 2016 adalah tanggal resmi Microsoft mengakhiri promo *upgrade* Windows 10. Kiraan kebanyakan orang. Pun saya yang amat kaget saat baca-baca <https://pegelinux.id/> dimana [Om Onosramus](https://unomind.github.io/) bilang doi habis upgrade gratis ke Ten.

😱

Setelah sekilas berselancar di dunia maya, ternyata memang benar bahwa kita kembali bisa mendapatkan pembaruan ke Windows 10 tanpa uang sepeser pun. Yang entah sejak kapan dimulai. Dan entah kapan bakal usai. Bodo ah yang penting gratis, resmi, gak nyolong.

Proses *upgrade* sendiri sangat mudah. Tipikal Windows. Pengguna cukup mengunduh dan menjalankan program [Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10). 
Selanjutnya cukup mengikuti saja arahan dari program tersebut sembari terhubung ke internet.

Bagai gayung bersambut kebetulan saya juga harus segera menghabiskan kuota internet di periode ini. Saya memang enggak berlangganan Internet kabel "tanpa batas kuota tapi amat terbatas waktu" yang amat mahal. Saya cuma menggunakan layanan dari provider kartu sim. Yang itu pun saya kepayahan menghabiskannya. `120rb buat 3-4 bulan.` 
Kadang saya enggak habis pikir kebanyakan manusia di luar sana kok bisa setiap bulannya rela ngasih **lebih dari 1/2 gram emas** ke provider Internet kabel. Istri bukan, ~~simpanan bukan~~, tiap bulan dikasih emas.

🙄

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/59" data-width="100%"></script> 

**Proses Upgrade**

Tangkapan layar selama proses pembaruan :

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/43" data-width="100%"></script> 

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/53" data-width="100%"></script> 

**Menyelamatkan grub**

Bagian ini cuma buat pengguna Dual OS atau Multiboot. Dalam proses instalasi, Windows akan menghapus `grub` dari `mbr`. Seperti yang sudah diantisipasi. Padahal katanya Microsoft ❤️ Linux. Tapi kok masih belum mendukung multiboot. 

😌

Kita dapat memasang ulang grub setelah kita masuk ke sistem operasi Linux dari `grub rescue`.

```shell
grub rescue > ls
grub rescue > set root=(hd0,msdos4)
grub rescue > set prefix=(hd0,msdos4)/boot/grub
grub rescue > insmod normal
grub rescue > normal
```

Sesuaikan dengan partisi kamu.

Jika tak ada kesalahan, `booting` akan berjalan dan menu grub awal kita akan muncul kembali. Di sini saya enggak langsung masuk ke sistem operasi Linux dan *reinstall* grub. Tapi saya memilih `boot entry` windows buat melanjutkan proses instalasi. Khawatir grub akan terhapus lagi. Kalau mau coba kamu boleh langsung *reinstall* aja.

😘👍

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/58" data-width="100%"></script> 

Baru setelah Windows 10 terpasang sempurna kita masuk ke Linux dari grub rescue menggunakan rangkaian perintah tadi. Pasang ulang grub :

```shell
~ ❯ sudo grub-install —target=i386-pc /dev/sda
[sudo] password for annajm: 
Installing for i386-pc platform.
Installation finished. No error reported.
~ ❯ update-grub
Generating grub configuration file ...
Found linux image: /boot/vmlinuz-linux
Found initrd image: /boot/initramfs-linux.img
Found fallback initrd image(s) in /boot: initramfs-linux-fallback.img
Found Windows 10 on /dev/sda1
done
```

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/63" data-width="100%"></script> 

**Mematikan fitur fast startup**

Satu lagi tugas buat kamu *dual-booter*. Yaitu mematikan fitur fast startup windows 10. Karena fitur ini menyebabkan hardisk tidak bisa ditulis saat masuk ke Linux. Read-only.

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/61" data-width="100%"></script> 

<script async src="https://telegram.org/js/telegram-widget.js?4" data-telegram-post="nocan/62" data-width="100%"></script> 

Assalamualaykum!

😘

**Referensi**

<https://pegelinux.id/>

<https://t.me/halamanbelakang>