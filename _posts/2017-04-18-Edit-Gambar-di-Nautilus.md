---
layout: post
title: Nautilus Image Tools, Pengaya Modifikasi Gambar dalam Nautilus
tags: [GNU/Linux, Nautilus]
category: linux
comments: true
author: ahmadi
--- 

**Nautilus Image Tools** merupakan pengaya `Nautilus` untuk melakukan modifikasi pada berkas gambar langsung dari "contex menu". Pengaya ini sangat membantu meningkatkan produktifitas saya dalam menulis blog (apalagi demi menghadapi tantangan *ODOA*) karena kita tidak harus membuka aplikasi pengolah gambar semisal `GIMP` jika hanya untuk mengubah ukuran atau merotasi misalnya. 

Berikut adalah fitur-fitur yang ditawarkan oleh Nautilus Image Tools :

- *resize*, *rotate* atau *flip* gambar;
- konversi gambar;
- meningkatkan citra gambar;
- beberapa efek semisal *greyscale* dan *watermark*;
- dan beberapa fitur lain yang bisa kamu lihat di tangkapan layar berikut :

![](/img/f-ss.png) 

Seru kan?

😎

**Pemasangan**

Buat pengguna `ArchLinux` dapat memasang Nautilus Image Tools dari AUR.

```shell
$ yaourt -S nautilus-image-tools
```

Jangan lupa buat memulai ulang Nautilus agar pengaya baru kita dapat dimuat.

```shell
$ nautilus -q
```

Buat pengguna Ubuntu (jujur saya **belum** coba) dapat memasangnya dari [PPA](https://launchpad.net/~atareao/+archive/ubuntu/nautilus-extensions).

```shell
$ sudo add-apt-repository ppa:atareao/nautilus-extensions
$ sudo apt-get update
$ sudo apt-get install nautilus-image-tools
```

Sebagai tambahan buat kamu yang `idealis`, menjunjung tinggi performa di atas segalanya, bisa baca artikel milik Mimin Mentari mengenai optimasi gambar untuk web [di sini](https://rizaumami.github.io/2017/04/09/optimasi-gambar-untuk-blog/). Tapi kalau buat kamu itu buang-buang waktu dan jelas waktu kamu lebih mahal ketimbang harga kuota internet. Jangan memaksakan diri. 

Toh ini juga idealisme, dan sangat bisa diterapkan di tahun 2017.

😋

Tapi (lagi) tulisan Mimin tersebut **layak** dijadikan pembelajaran.

😘

---

Ada yang merasa kehilangan `mukaddimah` khas dari saya? Kalau ada Yuk *High Five*, karena saya juga kehilangan, ini hari ke-18 (setidaknya buat saya), dan kelihatannya saya mulai "*retak*". Sudah dua artikel diakhiri dengan kata "bersambung". Poin `ELO` saya pun terjun bebas. Member [@halamanbelakang](https://t.me/halamanbelakang) melarikan diri. Skripsi terkatung.

😳

Sampai ketemu di `filler` *ODOA* selanjutnya.

😳

---
