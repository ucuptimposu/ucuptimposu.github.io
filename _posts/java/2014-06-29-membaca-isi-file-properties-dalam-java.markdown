---
comments: true
date: 2014-06-29 14:23:25+00:00
layout: article
slug: membaca-isi-file-properties-dalam-java
title: Membaca Isi File Properties dalam  JAVA
categories: java
tags: [java]
ads: true
image:
  feature:
  teaser: java.jpg
---

Sering kita membutuhkan file Properties biasanya berisi konfigurasi atau log dalam mebuat program.  Kita bisa menggunakan class Properties untuk membaca isi file .. Misal  contoh kita akan membaca file konfigurasi database.





  1. buat file dulu contoh namanya `konfigurasi.ini` atau terserah anda namanya...bisa buatnya pake notepad atau yg lain



[![](http://i713.photobucket.com/albums/ww134/upamisterlobal/timposu/konfig_zpsf227ebd2.png)](http://i713.photobucket.com/albums/ww134/upamisterlobal/timposu/konfig_zpsf227ebd2.png)

tanda awalan `#` itu cuman komen jadi tdk akan ke baca baris kalimatnya,

jadi ada 3 variabel yang akan di load yaitu  `url` , `nama` ,  dan `password`

2.. nah entar di load pake class Properties yang ada di paket `java.util`


```java
java.util.Properties properti = new java.util.Properties();
properti.load(new FileInputStream("konfigurasi.ini"));

String url = properti.getProperty("url");
String user = properti.getProperty("user");
String pass = properti.getProperty("password");
```


Oh iya pastiin juga tempat file konfigurasi yang di load di class `FileInputStream` sesuai dengan lokasi file nya..

<center><script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script><!-- BOX--><ins class="adsbygoogle"  style="display:inline-block;width:300px;height:250px" data-ad-client="ca-pub-4504493660273886" data-ad-slot="1638134271"></ins><script>(adsbygoogle = window.adsbygoogle || []).push({});</script></center>
