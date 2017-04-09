---
layout: post
title: Bobot Terkecil dalam Menimbang 
tags: [Kimia Analisis]
comments: true
author: ahmadi
summary: "Menimbang merupakan keahlian yang pertama diajarkan pada para calon analis kimia. Petualangan menegangkan yang saya bayangkan saat membaca buku profil SMAKBO dengan kosa katanya yang super asing, Gravimetri katanya, Volumetri katanya, Proksimat, Spektrofotometri, Chromatografi, asing, asing, benar-benar asing dan terdengar luar biasa, saya merasa seperti Bilbo Baggins yang selalu hidup tentram di guanya dan kemudian datang para Kurcaci bercerita petualangan-petualangan hebat mereka satu-satu, tapi itu belum semua, yang terasing saya simpan di akhir buat bikin kamu kaget, yaitu “meniup kaca”. Ya petualangan yang tedengar hebat (dan memang hebat) itu ternyata dimulai dari menimbang menggunakan neraca analitik mekanik nan antik dengan jarum bergoyangnya yang dapat menggoyang takdir para analis muda!"
--- 

Akhirnya (lho kok langsung akhir?), saya memutuskan buat membahas soal `kimia analisis` untuk tantangan `ODOA` (satu hari satu artikel) kali ini, karena saya kesulitan menemukan blog berisi materi kimia analisis, pun ketemu satu-dua hanya membahas materi-materi sekolah. 
Berbeda dengan blog teknologi informasi atau dunia komputer yang biasanya berisi tips/trik atau `hacking` (bukan dalam artian bodoh tentunya). 
Entah kenapa, mungkin memang karena kimia analisis itu sendiri terlalu baku sehingga enggak banyak yang bisa `diulik`, misalnya saja ketika kita akan menggunakan pereaksi kimia dengan konsentrasi berbeda (lebih pekat/lebih encer) dengan prosedur maka **diwajibkan** dilakukan validasi. 
Atau jangan-jangan karena analis kimia itu pekerjaan bergaji kecil sehingga mereka enggak punya waktu buat ngulik dan kemudian mendokumentasikan ulikannya. 
Atau lagi saya kurang gaul. Semoga ada pembaca yang membuktikan `ke-kurang-gaul-an` saya ini dengan memberikan tautan blog berisi materi kimia analisis di bagian komentar. 
😁

Untuk memulai tema baru (lagi-lagi dan lagi) ini saya akan mulai dari hal fundamental atau mendasar yaitu `menimbang`. 
Sama seperti di sekolah dulu. Menimbang merupakan keahlian yang pertama diajarkan pada para calon analis kimia. 
Petualangan menegangkan yang saya bayangkan saat membaca buku profil `SMAKBO` dengan kosa katanya yang super asing, `Gravimetri` katanya, `Volumetri` katanya, `Proksimat`, `Spektrofotometri`, `Chromatografi`, asing, asing, benar-benar asing dan terdengar luar biasa, saya merasa seperti `Bilbo Baggins` (padahal manuskrip mbah Tolkien ini belum disulap jadi buku saat itu 😂) yang selalu hidup tentram di guanya dan kemudian datang para Kurcaci bercerita petualangan-petualangan hebat mereka satu-satu, tapi itu belum semua, yang terasing saya simpan di akhir buat bikin kamu kaget, yaitu **"meniup kaca"**. 
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

$$M~min~ = \frac{2*sd}{toleransi}$$

Jadi `perjalanan` panjang kita yang pertama adalah memperoleh Standar Deviasi (`sd`) atau simpangan baku dari alat melalui proses kalibrasi. Kemudian dilanjutkan ke `petualangan` memperoleh toleransi, yaitu ketetapan berdasar tingkat kepercayaan dari hasil penetapan ketidakpastian (`U`), saya biasanya menggunakan tingkat kepercayaan 95% sehinggga nilai U=5%, tapi saya kurang ingat ini merujuk ke mana. Maaf.

😔

**Contoh Kasus**

Suatu penetapan kadar Minyak dalam Amoniak dihitung berdasarkan persamaan  $ppm Minyak = \frac{B~residu~*10^6*1,004}{V~spl*0,682}$. Dengan Volume sampel (V~spl~) sebanyak 1000ml setelah diektrak dan didehidrasi, diperkirakan diperoleh kadar Minyak sebesar ∓ 1ppm. Pertanyaanya : Bolehkah kita menggunakan neraca dengan spesifikasi gambar di atas?

😨

**Sampai jumpa tahun depan!!**

---

Ok buat menjawab pertanyaan di atas kita butuh beberapa informasi tambahan, yaitu bobot residu yang akan ditimbang, simpangan baku dan ketidakpastian, untuk simpangan baku bisa kita misalkan sebesar kemampuan baca (0,01 baik pak Sartorius maupun bung Mettler milik kita tadi) dan untuk ketidak pastian kita gunakan sebesar 5% (dalam farmasi digunakan U=0,1%)

 $$mg Residu = \frac{ppm Minyak*V~spl*0,682*1000}{10^6*1,004}$$
 $$mg Residu = \frac{1*1000*0,682*100}{10^6*1,004}$$
 $$mg Residu = 0,68$$

Kemudian kita cari M~min~ neraca.

$$M~min~ = \frac{2*0,01}{0,05}$$
$$M~min~ = 0,4mg$$

Alhamdulillah ternyata kita belum butuh neraca super canggih dan pastinya super mahal.Dengan catatan kadar Minyak yg dianalisa tidak boleh lebih rendah dari 1ppm dan toleransi yang diberikan 5% alias derajat keyakinan 95%.

**Referensi** :

<https://t.me/halamanbelakang>
<http://www.mt.com/de/en/home/microsites/good_weighing_practice.html>
<http://ffebri188.blogspot.co.id/2015/11/throwback-kelas-10.html> ← Pinjem foto neracanya yah dek 😁
<https://almegasejahtera.files.wordpress.com/2011/03/minweight2009-vol-1-send.pps>