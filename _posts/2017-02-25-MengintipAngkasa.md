---
layout: post
title: Mengintip Angkasa, Murah Meriah Melacak Pesawat 
tags: [SDR, ADS-B, LEDE]
comments: true
author: ahmadi
summary: "Seperti tulisan yang sudah-sudah, saya bukan pakar di topik tulisan saya, ini adalah kisah pertualangan dengan si mungil rtl-sdr."
--- 

!!TULISAN INI DIBUAT DEMI KEPENTINGAN ILMU PENGETAHUAN SEMATA. SEGALA KERUSAKAN/PELANGGARAN TERKAIT TULISAN INI BUKAN TANGGUNGJAWAB PENULIS!!

`...`

Kehilangan adalah peristiwa yang pasti dialami manusia, setiap saat, bahkan dalam satuan detik, setidaknya satu yang pasti hilang yaitu jatah hidupnya di dunia, hal ini sepertinya merupakan pemicu nafsu manusia untuk memiliki banyak hal, demi menambal kekosongan akibat kehilangan tersebut, sayangnya seringkali bukan sesuatu yang ia butuhkan.

Sebagai manusia normal hal ini terjadi pada saya. Terkadang obrolan di grup telegram saja mampu menjebol kantong yang sudah terlajur tipis ini. Seperti beberapa waktu lalu saat ada sentilan mengenai [rtl-sdr](http://www.rtl-sdr.com/about-rtl-sdr/) di grup [PegelWRT](https://t.me/pegelwrt), sejurus kemudian barang dagangan lapak daring sudah masuk *wishlist*, `Innalillah`.

Seperti tulisan yang sudah-sudah, saya bukan pakar di topik tulisan saya, ini hanyalah kisah pertualangan saya dengan si mungil `rtl-sdr`.


`...`

**Kawin dengan HameLede**

<img border="0" src="/img/sdr-kawin.jpg" width="50%" style="float:left; margin-right:10px"/>

[Hame Mpr-A2](https://wiki.openwrt.org/toh/hame/mpr-a2) adalah pengisi kekosongan saya yang lain. Router portabel imut lengkap dengan baterai ini jadi pasangan `samara` dengan rtl-sdr. Dengan baterai *built-in* kita bebas menempatkannya di mana pun.

**Kebutuhan Perangkat Lunak**

Hame Mpr-A2 hanya memiliki 8MB rom sehingga di sini saya terpaksa mebuang LuCI demi ruang tambahan. 
Beruntung paket `rtl-sdr` dan `dump1090` sebagai dekoder [ADS-B](https://en.wikipedia.org/wiki/Automatic_dependent_surveillance-broadcast) telah tersedia di repo dan dapat langsung dipasang menggunakan `opkg` tanpa perlu repot melakukan *compile*.

```shell
# opkg install rtl-sdr dump1090
```
Karena `dump1090` tidak memiliki mode *daemon* kita akan membuat sebuah *script* untuk memanggilnya melalui `screen`.

```shell
#!/bin/sh /etc/rc.common

START=95

start() {
    screen -S dump1090 -d -m -L dump1090 --net >> /dev/null
}

stop() {
    screen -r dump1090 -X quit
}
```
Saya menyimpannya sebagai `dump1090daemon.sh` langsung di folder root. Sampai di sini kita boleh langsung menjalankan dump1090 dengan perintah :

```shell
~# ./dump1090daemon.sh start
```

Untuk membaca data yang berhasil diterima kita akan menggunakan [Virtual Radar Server](http://virtualradarserver.co.uk/Default.aspx). Sayangnya belum tersedia paket untuk sistem operasi `GNU/Linux`, kita terpaksa menjalakannya melalui `mono`. 

**Pemasangan mono**

```shell
# pacman -S mono
```

**Pemasangan Virtual Radar Server**

Unduh berkas Virtual Radar Server [di sini](http://virtualradarserver.co.uk/Download.aspx) dan pengaya Web Admin [di sini](http://virtualradarserver.co.uk/Download.aspx#panel-web-admin), kemudian ekstrak berkas tersebut, tempatkan folder `Plugins` di dalam folder Virtual Radar Server.

**Masalah pada mono 4**

Virtual Radar Server dibuat dengan *framework* .NET versi 3.5 sehingga kita perlu membuat konfigurasi berikut untuk menjalankannya di mono 4. Buat file dengan nama VirtualRadar.exe.config di folder Virtual Radar Server yang berisi :

```shell
<?xml version="1.0"?>
<configuration>
    <configSections>
    </configSections>
    <startup>
        <supportedRuntime version="v2.0.50727"/>
    </startup>
    <runtime>
        <assemblyBinding  xmlns="urn:schemas-microsoft-com:asm.v1">
            <dependentAssembly>
                <assemblyIdentity name="Mono.Data.Sqlite"
                                  publicKeyToken="0738eb9f132ed756"
                                  culture="neutral" />
                <bindingRedirect oldVersion="2.0.0.0"
                                 newVersion="4.0.0.0" />
            </dependentAssembly>
        </assemblyBinding>
    </runtime>
</configuration>
```

Jalankan Virtual Radar Server dengan perintah :

```shell
$ mono VirtualRadar.exe
```
Sesuaikan alamat IP pada tools-options-reciever

<img border="0" src="/img/sdr-ip.png" style="float:left; margin-right:10px"/>

Sampai di sini kita sudah bisa mengakses halaman web Virtual Radar Server di [http://127.0.0.1:8080/VirtualRadar/desktop.html](http://127.0.0.1:8080/VirtualRadar/desktop.html) 


<img border="0" src="/img/sdr-web.png" style="float:left; margin-right:10px"/>


Selamat mengintip.
😅

Referensi :

[http://virtualradarserver.co.uk](http://virtualradarserver.co.uk/) 

[http://blog.y3xz.com/blog/2014/04/24/feeding-data-to-flightradar24-dot-com](http://blog.y3xz.com/blog/2014/04/24/feeding-data-to-flightradar24-dot-com/) 
