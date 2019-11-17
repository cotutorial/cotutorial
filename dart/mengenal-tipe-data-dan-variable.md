---
title: "Mengenal Tipe Data Dan Variable"
date: 2019-11-15T18:55:24+07:00
draft: false
banner: /img/post/tipe_data_&_variable.webp
jpg: /img/post/jpg/tipe_data_&_variable.jpg
categories:
  - dart
tags:
  - dart
  - variable
  - basic 
author: 
- saputrago  
---

### Apa itu sih Variabel dan Tipe Data?

Jika teman-teman sudah pernah belajar bahasa pemrograman apapun itu pasti tidak asing lagi mendengar kata ini. Jika teman lupa atau belum tahu itu, saya akan jelaskan tentang variabel dan tipe data ini.

**Variable** yaitu suatu simbol untuk menandakan dan menyimpan suatu nilai.

**Tipe Data** yaitu jenis nilai yang tersimpan pada suatu variabel.

Masih bingung dengan penjelasnya? berikut gambaran dari variabel dan tipe data.

```dart
String name = "MyName"
```
![Image Struktur Tipe Data dan Variable](/img/post/tipe_data_variable_struktur.png)

Pada gambar tersebut pada tipe data `String` yaitu sebagai **Tipe Data**, sedangkan `name` pada gambar tersebut sebagai nama variabel untuk mendefinisikan suatu nilai. Terus yang `"My Name"` itu apa? `"My Name"` sebagai nilai/isi suatu variabel tersebut.

## Variable
Seperti yang kita ketahui tadi variable yaitu suatu simbol untuk menandakan dan menyimpan suatu nilai. Mengapa kita kok perlu variable dalam suatu program? Misal saja jika kamu mempunya suatu barang dan kamu tidak tahu namanya dan kamu menyuruh temanmu mengambil barang itu apa yang terjadi? pasti bingung kan? tidak tahu apa maksudnya. Oleh karena itu kita perlu sebuah variabel dalam suatu penyimpana nilai dalam suatu kode.

#### Aturan dan Persyaratan dalam Pembuatan Variabel
Pada variabel juga ada persyaratannya, untuk menghindari kesalahan manusia. Adapun aturannya sebagai berikut:

1. Pengidentifikasi sebuah variabel tidak boleh sama seperti keyword pada dart contoh `class`, `if`, `else`, `int`, dll.
2. Pengidentifikasi variabel boleh ada angka, tapi tidak boleh pada awal kata, contoh `3nama`
3. Pengidentifikasi variabel tidak boleh pakai spasi dan karakter khusus kecuali tanda underscore (_).

## Tipe Data
**Tipe Data** adalah jenis nilai yang tersimpan pada suatu variabel. Yang berarti jenis atau tipe suatu variabel itu dinamakan tipe data. Adapun jenis-jenis tipe data pada Dart yaitu:

1. [Number](/dart/dart-tipe-data-number/)
    - [Integer (Int)](/dart/dart-tipe-data-number/#1-int)
    - [Double](/dart/dart-tipe-data-number/#2-double)
2. [String](/dart/dart-tipe-data-string/)
3. Boolean
4. List
5. Sets
6. Maps
7. Runes
8. Symbols
