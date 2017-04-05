---
layout: post
title: Blog Statis Dalam GitHub
tags: [Web]
comments: true
author: ahmadi
--- 

Beberapa waktu lalu istri membeli mainan edukasi (yang juga mengedukasi dompet 🙄) untuk anak. Mainan ini berupa boneka yang bisa berbicara. Serius berbicara! (`norak mode`) 
Beberapa fitur justru malah membuat orang tuanya yang belajar. Seperti selalu. 

Memang agak rancu rasanya saat membesarkan anak. Seringkali malah saya sendiri sebagai orang tua yang memperoleh pengajaran, bukan sebaliknya. Seperti seharusnya. 

Fitur paling sederhana saja sudah memberikan saya banyak pelajaran, yaitu fitur dongeng. 
Suatu hari terdengar dongeng tentang nabi **Idris**, manusia berilmu, pandai menulis katanya. Usut punya usut (berselancar menggunakan mesin pencari maksudnya) ternyata nabi **Idris/Enoch AS** adalah manusia pertama yang menulis. Hei! Ini enggak ada di pabrik bernama sekolah! Dulu katanya yang pertama menulis itu monyet jejadian mirip manusia atau sebaliknya sama saja.

Satu lagi manusia mulia dan berilmu, Sayyidina ‘Ali bin Abi Tholib ra yang mendapatkan gelar “`babul-ilmi`” berpesan:

قَيِّدُوا الْعِلْمَ بِالْكِتَابِ

“Ikatlah ilmu dengan kitab (yaitu, dengan menulisnya)”

`...`

Bahasan kita kali ini yaitu `menulis` atau bahasa okem nya nge-blog menggunakan *static site generator*. Sesuai tema serialisasi terbaru kita. 
Banyak sekali [keistimewaan](https://davidwalsh.name/introduction-static-site-generators) dari menulis blog berupa halaman web statis :
- kecepatan 
- kontrol versi 
- keamanan 
- enggak repot kelola server 

Dari empat poin di atas yang paling terasa adalah soal kecepatan, karena hanya berupa halaman web statis tanpa database dan sebagainya, halaman web kita menjadi ringan untuk dibuka oleh pembaca. Poin krusial.

Udah panjang nih intronya, sebenarnya saya masih mau banget cerita panjang lebar, tapi khawatir malah membosankan jadinya.

Buat kamu yang belum punya Blog statis Yuk kita buat satu secara instan.

Di sini kita akan melakukan *forking* repositori GitHub yang telah tersedia sehingga kita tidak perlu repot membangun dari `NOL`. 

**Fork Repository**

Kita akan mem-*fork* repo [beautiful jekyll](https://github.com/daattali/beautiful-jekyll) yang merupakan *parent* dari tema yang saya gunakan. Atau jika kamu kurang suka kamu bisa pilih yang lain [di sini](https://github.com/jekyll/jekyll/wiki/Themes). Atau bahakan kamu bisa mem-*fork* [repo saya](https://github.com/ahmadihamid/ahmadihamid.github.io) sekalian apalagi kalau kamu memang akan membuat web berbahasa Indonesia. Bahasa tercinta kita!
Buka halaman repo yang ingin di-fork kemudian klik tombol fork di pojok kanan atas.

**Ubah nama repo menjadi `<namakamu>.github.io`**

Setelah *forking* selesai kamu telah memiliki sebuah repositori yang persis dengan *parent*-nya. Ubah nama repo melalui `Setting` kemudian lakukan perubahan dari opsi `Rename`.

**Sesuaikan kustomisasi website**

Edit file `_config.yml` sesuai keterangan website kamu melaui icon pensil yang kan tampil ketika kamu membukafile tersebut. Pengembang [beautiful jekyll](https://github.com/daattali/beautiful-jekyll) menyertakan komentar dalam file `_config.yml` untuk membantu kita, baca dan ikuti secara perlahan. Sampai sini kamu sudah punya website statis sendiri yang dapat diakses dari alamat http://namakamu.github.io.

**Menulis posting**

Untuk posting artikel, kita lakukan dengan mebuat berkas `.md` di dalam direktori `_post`. Artikel ditulis menggunakan [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), jangan khawatir mengenai hali ini, karena `markdown` lebih mudah dipelajari dibandingkan `html`.

**Editor**

*Editor* yang biasa saya gunakan dalam mengetik artikel yaitu [Remarkable](http://remarkableapp.github.io/), karena memiliki fitur `WYSIWYG` (apa yang kamu lihat itu yang kamu dapat) alias *preview*. `Remarkable` juga menyediakan suatu berkas tutorial yang sangat membantu buat kamu yang baru belajar Markdown. Berkas ini dapat diakses dari menu `Help` - `Markdown Tutorial`.

![](/img/ps-renarkable.png) 

**Rangkuman**

Jangan berpikir bahwa langkah di atas rumit dan sulit. Mudah kok, hanya saja sayangnya saya enggak berbakat jadi guru. Berikut adalah video rangkuman langkah-langkah kita, yang saya ambil dari repo [beautiful jekyll](https://github.com/daattali/beautiful-jekyll#readme).

![Installation steps](/img/install-steps.gif)


Selamat menulis!
😘

**Referensi** :

<https://github.com/SinauDev/SinauDev.github.io>
<https://github.com/daattali/beautiful-jekyll>
<https://davidwalsh.name/introduction-static-site-generators>
<https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/>
