---
layout: post
title: Menambah Dukungan MathJax dalam Blog Jekyll 
tags: [Web, Jekyll]
comments: true
author: ahmadi
ext-js: "https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-MML-AM_CHTML"
summary: "Pada kesempatan kali ini saya dipaksa belajar menambahkan dukungan MathJax pada Jekyll karena ternyata dukungan ini tidak diberikan secara bawaan. MathJax merupakan skrip JavaScript yang berfungsi untuk menampilkan tulisan berupa LaTeX, MathML, AsciiMath pada peramban. Sederhananya buat menulis rumus Matematika dalam halaman web."
--- 

> Menulis membantu diri sendiri. Tetap ada walau mati.

Menulis dengan tema `kimia analisis` sepertinya merupakan ide bagus sekaligus buruk. Buruk karena ternyata malah enggak ada yang memberi komentar 😭. *Blunder*. Tapi berkat menulis topik baru lagi-lagi saya belajar hal baru. Ditambah lagi menulis blog dalam lingkungan web statis seperti ini memang `memaksa` banyak belajar. Kadang sepertinya malah buang-buang waktu dan `kotra-produktif`. 
Ah! Toh menulis memang bukan buat membuat orang belajar apalagi pamer kepintaran, menulis malah menjadi sarana belajar tersendiri buat saya yang malas belajar ini. Ya walau niat awal saya menggunakan Jekyll untuk `nge-blog` biar terlihat *geek*. Tau *geek* kan? Yang seperti digambar ini lho :

![](/img/ps4-bebegik.jpg) 

😋

Pada kesempatan kali ini saya dipaksa belajar menambahkan dukungan MathJax pada Jekyll karena ternyata dukungan ini tidak diberikan secara bawaan. MathJax merupakan skrip JavaScript yang berfungsi untuk menampilkan tulisan berupa `LaTeX`, `MathML`, `AsciiMath` pada peramban. Sederhananya buat menulis rumus Matematika dalam halaman web.

Sebenarnya pada dua postingan di belakang yaitu pada seri Catatan Kimia saya masih menggunakan html untuk menampilkan MathJax. Cara yang malas yaitu dengan melakukan eksport ke HTML melalui menu `File` - `Export HTML (Styled)`. Kemudian karena tetap ingin memperoleh berkas yang `mudah ditulis dan mudah dibaca` sesuai filosofi dari `Markdown` saya akhirnya menggabungkan keduanya yaitu `HTML` dan `MD`. Hasilnya? Kurang bagus! Dan jauh dari filosofi Markdown. Berikut adalah berkas hasi penggabungan tersebut :

```shell
---
layout: post
title: Bobot Terkecil dalam Menimbang
tags: [Kimia Analisis]
comments: true
author: ahmadi
summary: "Menimbang merupakan keahlian yang pertama diajarkan pada para calon analis kimia. Petualangan menegangkan yang saya bayangkan saat membaca buku profil SMAKBO dengan kosa katanya yang super asing, Gravimetri katanya, Volumetri katanya, Proksimat, Spektrofotometri, Chromatografi, asing, asing, benar-benar asing dan terdengar luar biasa, saya merasa seperti Bilbo Baggins yang selalu hidup tentram di guanya dan kemudian datang para Kurcaci bercerita petualangan-petualangan hebat mereka satu-satu, tapi itu belum semua, yang terasing saya simpan di akhir buat bikin kamu kaget, yaitu"
--- 

Akhirnya (lho kok langsung akhir?), saya memutuskan buat membahas soal `kimia analisis` untuk tantangan `ODOA` (satu hari satu artikel) kali ini, karena saya kesulitan menemukan blog berisi materi kimia analisis, pun ketemu satu-dua hanya membahas materi-materi sekolah. 

Berbeda dengan blog teknologi informasi atau dunia komputer yang biasanya berisi tips/trik atau `hacking` (bukan dalam artian bodoh tentunya). 

Entah kenapa, mungkin memang karena kimia analisis itu sendiri terlalu baku sehingga enggak banyak yang bisa `diulik`, misalnya saja ketika kita akan menggunakan pereaksi kimia dengan konsentrasi berbeda (lebih pekat/lebih encer) dengan prosedur maka **diwajibkan** dilakukan validasi. 

Atau jangan-jangan karena analis kimia itu pekerjaan bergaji kecil sehingga mereka enggak punya waktu buat ngulik dan kemudian mendokumentasikan ulikannya. 

Atau lagi saya kurang gaul. Semoga ada pembaca yang membuktikan `ke-kurang-gaul-an` saya ini dengan memberikan tautan blog berisi materi kimia analisis di bagian komentar. 

😁

Untuk memulai tema baru (lagi-lagi dan lagi) ini saya akan mulai dari hal fundamental atau mendasar yaitu `menimbang`. 

Sama seperti di sekolah dulu. Menimbang merupakan keahlian yang pertama diajarkan pada para calon analis kimia. 
Petualangan menegangkan yang saya bayangkan saat membaca buku profil `SMAKBO` dengan kosa katanya yang super asing, `Gravimetri` katanya, `Volumetri` katanya, `Proksimat`, `Spektrofotometri`, `Chromatografi`, asing, asing, benar-benar asing dan terdengar luar biasa, saya merasa seperti `Bilbo Baggins` (padahal manuskrip mbah Tolkien ini belum disulap jadi buku saat itu 😂) yang selalu hidup tentram di gua-nya dan kemudian datang para Kurcaci bercerita petualangan-petualangan hebat mereka satu-satu, tapi itu belum semua, yang terasing saya simpan di akhir buat bikin kamu kaget, yaitu **"meniup kaca"**. 

Ya petualangan yang tedengar hebat (dan memang hebat) itu ternyata dimulai dari **menimbang** menggunakan neraca analitik mekanik nan antik dengan jarum bergoyangnya yang dapat menggoyang takdir para analis muda!

![](/img/ak-neraca-analitik.jpg) 

`...`

Bahasan kita kali ini adalah "**bobot terkecil dalam menimbang**".

Beberapa hari lalu saya mengikuti sebuah presentasi dari [Mettler Toledo](http://www.mt.com/id/id/home.html) di tempat saya bekerja. Topiknya adalah [GWP](http://www.mt.com/de/en/home/microsites/good_weighing_practice.html) (*Good Weighing Practice*) yaitu suatu metoda terstandar dari Mettler Toledo dalam hal pengoperasian, kalibrasi, dan pemilihan alat timbang.
Di sini saya baru tersadar bahwa **bobot minimal ≠ kemampuan baca** dari timbangan. Bodoh memang. Mungkin saya sibuk memperhatikan teman kelas saya saat guru saya mengajarkan hal ini. `YKWIM`.

**Kemampuan Baca**

Kemampuan baca atau disebut juga *Readablility, Resolution, Scale Division, Scale Interval, Increment, Digit, d*, adalah perubahan terkecil yang mampu di deteksi timbangan dan ini (sayangnya) tidak menunjukkan bobot terkecil yang boleh kita timbang menggunakan neraca/timbangan tersebut. 
Di bawah ini adalah contoh nilai `d` yang tertera pada neraca :

![](/img/ak-d-mt.jpg) 

![](/img/ak-d-sarto.jpg) 

Hoo..Sartorius terlihat lebih teliti dalam menulis nilai `d` beliau membedakan nilai `d` berdasarkan bobot timbang. Yaa.. atau tuan Mettler Toledo lebih stabil dalam membaca, beliau istiqomah memberi nilai `d` di tiap bobot penimbangan. Ruarr Biasa. Maksudnya saya luar biasa enggak tau apa-apa.

😒

**Bobot Minimal**

Untuk mengetahui bobot minimal yang dapat ditimbang pada suatu neraca membutuhkan sebuat perjalanan panjang yang enggak mungkin saya bahas (karena saya enggak tahu 😎) secara mendetil. Berikut adalah persamaan untuk memperoleh nilai bobot minimal :

<html>
  <head>
    <meta content="text/html; charset=utf-8" http-equiv="content-type">
    <title> Bobot Terkecil dalam Menimbang </title>
    <link href="http://cdnjs.cloudflare.com/ajax/libs/highlight.js/8.1/styles/github.min.css"
      rel="stylesheet">
    <style type="text/css">
   body,table tr{background-color:#fff}table tr td,table tr th{border:1px solid #ccc;text-align:left;padding:6px 13px;margin:0}pre code,table,table tr{padding:0}hr,pre code{background:0 0}body{font:16px Helvetica,Arial,sans-serif;line-height:1.4;color:#333;word-wrap:break-word;padding:10px 15px}strong,table tr th{font-weight:700}h1{font-size:2em;margin:.67em 0;text-align:center}h2{font-size:1.75em}h3{font-size:1.5em}h4{font-size:1.25em}h1,h2,h3,h4,h5,h6{font-weight:700;position:relative;margin-top:15px;margin-bottom:15px;line-height:1.1}h1,h2{border-bottom:1px solid #eee}hr{height:0;margin:15px 0;overflow:hidden;border:0;border-bottom:1px solid #ddd}a{color:#4183C4}a.absent{color:#c00}ol,ul{padding-left:15px;margin-left:5px}ol{list-style-type:lower-roman}table tr{border-top:1px solid #ccc;margin:0}table tr:nth-child(2n){background-color:#aaa}table tr td :first-child,table tr th :first-child{margin-top:0}table tr td:last-child,table tr th :last-child{margin-bottom:0}img{max-width:100%}blockquote{padding:0 15px;border-left:4px solid #ccc}code,tt{margin:0 2px;padding:0 5px;white-space:nowrap;border:1px solid #eaeaea;background-color:#f8f8f8;border-radius:3px}pre code{margin:0;white-space:pre;border:none}.highlight pre,pre{background-color:#f8f8f8;border:1px solid #ccc;font-size:13px;line-height:19px;overflow:auto;padding:6px 10px;border-radius:3px}
  </style>
  </head>
  <body><br>
    <p> <mathjax> $$M~min~ = \frac{2*sd}{toleransi}$$ </mathjax> </p>
    <p> Jadi <code> perjalanan</code> panjang kita yang pertama adalah
      memperoleh Standar Deviasi ( <code> sd</code> ) atau simpangan baku dari
      alat melalui proses kalibrasi. Kemudian dilanjutkan ke <code> petualangan</code>
      memperoleh toleransi, yaitu ketetapan berdasar tingkat kepercayaan dari
      hasil penetapan ketidakpastian ( <code> U</code> ), saya biasanya
      menggunakan tingkat kepercayaan 95% sehinggga nilai U=5%, tapi saya kurang
      ingat ini merujuk ke mana. Maaf. </p>
    <p> 😔 </p>
    <p> <strong> Contoh Kasus </strong> </p>
    <p> Suatu penetapan kadar Minyak dalam Amoniak dihitung berdasarkan
      persamaan <mathjax> $ppm Minyak =
        \frac{B~residu~*10^6*1,004}{V~spl*0,682}$ </mathjax> . Dengan Volume
      sampel (V <sub> spl </sub> ) sebanyak 1000ml setelah diektrak dan
      didehidrasi, diperkirakan diperoleh kadar Minyak sebesar ∓ 1ppm.
      Pertanyaanya : Bolehkah kita menggunakan neraca dengan spesifikasi gambar
      di atas? </p>
    <p> 😨 </p>
    <br>
    <p> <strong> Sampai jumpa tahun depan!! </strong> </p>
    <br>
    <hr>
    <p> Ok buat menjawab pertanyaan di atas kita butuh beberapa informasi
      tambahan, yaitu bobot residu yang akan ditimbang, simpangan baku dan
      ketidakpastian, untuk simpangan baku bisa kita misalkan sebesar kemampuan
      baca (0,01 baik pak Sartorius maupun bung Mettler milik kita tadi) dan
      untuk ketidak pastian kita gunakan sebesar 5% (dalam farmasi digunakan
      U=0,1%) </p>
    <p> <mathjax> $$mg Residu = \frac{ppm
        Minyak*V~spl*0,682*1000}{10^6*1,004}$$ </mathjax> <br>
      <mathjax> $$mg Residu = \frac{1*1000*0,682*100}{10^6*1,004}$$ </mathjax>
      <br>
      <mathjax> $$mg Residu = 0,68$$ </mathjax> </p>
    <p> Kemudian kita cari M <sub> min </sub> neraca. </p>
    <p> <mathjax> $$M~min~ = \frac{2*0,01}{0,05}$$ </mathjax> <br>
      <mathjax> $$M~min~ = 0,4mg$$ </mathjax> </p>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/highlight.js/8.1/highlight.min.js"></script>
    <script>hljs.initHighlightingOnLoad();
  </script>
    <script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-MML-AM_CHTML'>
  </script>
    <script type="text/javascript">
   MathJax.Hub.Config({"showProcessingMessages" : false,"messageStyle" : "none","tex2jax": { inlineMath: [ [ "$", "$" ] ] }});
  </script>
  </body>
</html>


Alhamdulillah ternyata kita belum butuh neraca super canggih dan pastinya super mahal.Dengan catatan kadar Minyak yg dianalisa tidak boleh lebih rendah dari 1ppm dan toleransi yang diberikan 5% alias derajat keyakinan 95%.

**Referensi** :

<https://t.me/halamanbelakang>
<http://www.mt.com/de/en/home/microsites/good_weighing_practice.html>
<http://ffebri188.blogspot.co.id/2015/11/throwback-kelas-10.html> ← Pinjem foto neracanya yah dek 😁
<https://almegasejahtera.files.wordpress.com/2011/03/minweight2009-vol-1-send.pps>

```

Enggak enak dilihat kan? Apalagi dibaca. 
Solusi `darurat` alias sementara. Yang penting produksi jalan. 

Sedangkan buat solusi jangka panjangnya (terimakasih pada [Dean Attali](https://github.com/daattali/beautiful-jekyll/issues/195)) kita dapat menggunkan opsi `js` atau `ext-js` dalam parameter YAML postingan kita. Sehingga kita dapat kembali menulis sepenuhnya dalam Markdown. Berikut adalah contoh penggunaan MathJax :

```shell
---
layout: post
title: tes mathjax
tags: [Kimia Analisis]
comments: true
author: ahmadi
summary: ""
ext-js: "https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-MML-AM_CHTML"
--- 

###TESTING

Yuk kita turunkan rumus $$∆E*ab$$ ini :

\[L*		:\] tingkat kecerahan suatu sampel
\(a*		:\) perbedaan merah dan hijau (merah:`+`; hijau:` -` )
$$b*		:$$ perbedaan kuning dan biru (kuning :`+`; biru:`-`)
$$∆E*ab 	:$$ total perbedaan warna 

$$∆E*ab = \sqrt{(∆L*)^2+(∆a*)^2+(∆b*)^2}$$

$$(∆E*ab)^2 = (∆L*)^2+(∆a*)^2+(∆b*)^2$$

Sehingga $ ∆E*ab, ∆L*, ∆a* & ∆b* $  merupakan [Pythagorean Quadruple](https://en.m.wikipedia.org/wiki/Pythagorean_quadruple) yaitu tupel dari bilangan bulat dengan persamaan $a^2 + b^2 + c^2 = d^2$ dimana $$ a ,  b , dan  c $$ merupakan sisi dari sebuah kubus dengan $d$ sebagai diagonal ruangnya.

###EOT

```

Dan dibawah ini adalah hasilnya :

---

###TESTING

Yuk kita turunkan rumus $$∆E*ab$$ ini :

\[L*		:\] tingkat kecerahan suatu sampel
\(a*		:\) perbedaan merah dan hijau (merah:`+`; hijau:` -` )
$$b*		:$$ perbedaan kuning dan biru (kuning :`+`; biru:`-`)
$$∆E*ab 	:$$ total perbedaan warna 

$$∆E*ab = \sqrt{(∆L*)^2+(∆a*)^2+(∆b*)^2}$$

$$(∆E*ab)^2 = (∆L*)^2+(∆a*)^2+(∆b*)^2$$

Sehingga $ ∆E*ab, ∆L*, ∆a* & ∆b* $  merupakan [Pythagorean Quadruple](https://en.m.wikipedia.org/wiki/Pythagorean_quadruple) yaitu tupel dari bilangan bulat dengan persamaan $a^2 + b^2 + c^2 = d^2$ dimana $$ a ,  b , dan  c $$ merupakan sisi dari sebuah kubus dengan $d$ sebagai diagonal ruangnya.

###EOT

---

**Ternyata** (atau hanya di peramban saya) terjadi kegagalan dalam merender `\[...\]` dan `\(...\)` dimana seharusnya menampilkan rumus matematika dalam baris yang sama. Pun terjadi kegagalan saat menggunakan `$$...$$` malah menampilkan rumus dalam baris dimana seharusnya dihasilkan rumus dengan level block.

😒

Lagi-lagi, sementara `yang penting jalan`. Toh kita dapat menggunakan tombol `[ENTER]` untuk baris baru.

Selamat terpaksa!

**Referensi** :

<https://t.me/halamanbelakang>
<http://docs.mathjax.org/en/latest/start.html>
