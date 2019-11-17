---
title: "Dart Tipe Data String"
date: 2019-11-17T13:05:50+07:00
draft: false
banner: /img/post/dart_tipe_data_string.webp
jpg: /img/post/jpg/dart_tipe_data_string.jpg
categories:
  - dart
tags:
  - dart
  - basic
author: 
- saputrago  
---

### Apa itu tipe data String?
Tipe data String yaitu sekumpulan karakter. Pada tipe data ini biasanya mempresentasikan sebuah teks. 

String ini menggunakan unit kode UTF-16. String pada Dart bisa menyimpan data dari satu line sampai multiline(beberapa baris). Tipe data string dapat ditandai dengan:

1. Petik satu ganda `(' ')` atau petik dua ganda `(" ")` untuk satu line (baris). 
2. Petik satu triple `(''' ''')` atau petik dua triple `(""" """)` untuk menyimpan data multiline.

berikut ini adalah contoh semua String di Dart yang avalid:

```dart
'String single line petik satu';
"String single line petik dua";

'''
String 
multiline 
petik satu''';

"""
String 
multiline 
petik dua
""";

```

### Bagaimana cara membuat variabel dengan tipe data String?

Seperti yang pada tipe data integer dan lainya pembuatan variabel tidak jauh berbeda dengan yang lainya. Cara implementasi nya ada dua cara yaitu:

1. Dengan keyword `String`
contoh kode berikut:

```dart
void main() {
  String name = "Dart";
}
```
2. Dengan keyword  `var`

```dart
void main() {
  var name = "Dart";
}
```

Berikut contoh penerapan variabel tipe data String:

```dart
void main() {
  String str1 = 'ini adalah contoh string untuk satu baris dengan petik 1';
  var str2 = "ini adalah contoh string untuk satu baris dengan petik 2";

  String str3 = '''ini adalah contoh
   string untuk multiline/beberapa baris 
   dengan petik satu tiga''';
  var str4 = """ini adalah contoh
   string untuk multiline/beberapa baris 
   dengan petik dua tiga""";
  
  print(str1);
  print(str2);
  print(str3);
  print(str4);
}
```
dan akan menghasilkan output berikut:
```
ini adalah contoh string untuk satu baris dengan petik 1
ini adalah contoh string untuk satu baris dengan petik 2
ini adalah contoh
   string untuk multiline/beberapa baris 
   dengan petik satu tiga
ini adalah contoh
   string untuk multiline/beberapa baris 
   dengan petik dua tiga
```


## Interpolasi String
Interpolasi atau penggabungan yaitu proses membuat string baru dengan cara menambahkan nilai string satu ke string lain.

Pada proses ini dapat menggunakan keyword plus `+`. Ada beberapa proses untuk interpolasi ini, diantaranya sebagai berikut:

1. Menggunakan keyword `+`
```dart
void main() {
  var s1 = 'Dart';
  String s2 = 'is Fun';
  print(s1 + s2);  // interpolasi dengan variabel
  print('Hello' + 'World'); // interpolasi tanpa variabel
}
```
output:
```
Dart is Fun
Hello World
```

2. Tanpa keyword `+`
```dart
void main() {
  print('Dart ' 'is ' 'Fun');
  print('Hello ' 'World'); 
}
```
output:
```
Dart is Fun
Hello World
```Pada interpolasi ini penggabungan dengan variabel tidak berlaku akan menyebabkan error.

3. Interpolasi dalam String
```dart
void main() {
  var s1 = 'Dart ';
  var s2 = 'is Fun';

  print("Hasil interpolasi dari $s1 + $s2 menjadi ${s1+s2}");
}
```output:
```
Hasil interpolasi dari Dart  + is Fun menjadi Dart is Fun
```Pada kasus ini untuk menampilkan suatu variabel pada String kita perlu keyword `$` dan jika pada suatu variabel tersebut ada operasi maka gunakan keyword/sitkas ini `${}`.

## Property
Property | Deskripsi
---------|----------
[codeUnits](#codeunits)|Mengembalikan list unit kode UTF-16
[isEmpty](#isempty)|Mengembalikan **true** jika kosong, jika tidak **false**
[isNotEmpty](#isnotempty)|Mengembalikan **true** jika tidak kosong, jika tidak **false**
[length](#length)|Mengembalikan panjang karakter termasuk spasi, tab.

---
### codeUnits
```dart
void main() {
  String str = "Hello World";
  print("codeUnits: ${str.codeUnits}");
}
```
Akan menghasilkan output list karakter kode unit UTF-16. 

output:
```
codeUnits: [72, 101, 108, 108, 111, 32, 87, 111, 114, 108, 100]
```
---
### isEmpty
```dart
void main() {
  String str = "Hello World";
  String str1 = '';
  
  print("apakah nilainya kosong? ${str.isEmpty}");
  print("apakah nilainya kosong? ${str1.isEmpty}");
}
```
output:
```
apakah nilainya kosong? false
apakah nilainya kosong? true
```
Pada property ini jika panjang karakter dari string itu 0 atau kosong, seperti pada contoh diatas maka akan mengembalikan nilai **true**, jika tidak kosong **false**.

---
### isNotEmpty
```dart
void main() {
  String str = "Hello World";
  String str1 = '';
  
  print("apakah nilainya tidak kosong? ${str.isNotEmpty}");
  print("apakah nilainya tidak kosong? ${str1.isNotEmpty}");
}
```
output:
```
apakah nilainya tidak kosong? false
apakah nilainya tidak kosong? true
```
Pada properti ini penjelasannya cukup kebalikan dari properti `isEmpty`.

---
### length
```dart
void main() {
  String str = "Hello";
  String str1 = "Hello ";
  
  print("length variabel str ${str.length}");
  print("length variabel str ${str1.length}");
}
```
output:
```
length variabel str 5
length variabel str 6
```
Properti ini mengembalikan panjang dari suatu variabel string. Pada kasus ini sapasi ikut dihitung pada variabel `str1` ada spasinya dan panjangnya juga beda.

## Method
Method|Deskripsi
------|---------
[toLowerCase()](#tolowercase) | Mengubah karakter string jadi huruf kecil
[toUpperCase()](#touppercase) | Mengubah karakter string jadi huruf kapital
[trim()](#trim) | Menghapus spasi pada awal dan akhir kalimat
[replaceAll()](#replaceall) | Mengganti semua substring yang cocok dengan nilai yang diberikan
[spit()](#split) | Memisahkan string pada param yang ditentukan
[substring()](#split) | Mengembalikan substring dari string mulai startIndex, inklusif, endIndex, dan exklusif
toString() | Mengembalikan nilai ke String


--- 
### toLowerCase()
```dart
void main() {
  var s = "HELLO DART!";
  print(s.toLowerCase());
}
```
output:
```
hello dart!
```
Pada method ini text yang ada huruf kapitalnya akan dipaksa jadi huruf kecil.

---
### toUpperCase()
```dart
void main() {
  var s = "hello dart!";
  print(s.toUpperCase());
}
```
output:
```
HELLO DART!
```
Pada method ini merupakan kebalikan dari method `toLowerCase()`. Method ini berfungsi untuk menjadikan huruf kecil ke kapital semua.

---

### trim()
```dart
void main() {
  var s = "      dart is fun!       ";
  print(s.trim());
}
```
output:
```
dart is fun!
```
Pada method ini fungsinya untuk menghapus space pada awal dan akhir suatu kalimat / kata.

--- 
### replaceAll()
```dart
void main() {
  var s = "hai hai hai nama saya Dart!";
  print(s.replaceAll('a', 'o')); // replace karakter
  print(s.replaceAll('hai', 'helo')); // replace kata
}
```
output:
```
hoi hoi hoi nomo soyo Dort!
helo helo helo nama saya Dart!
```
Pada method ini berfungsi seperti find and replace.

---
### split()
```dart
void main() {
  var s = "halo nama saya Dart!";
  print(s.split('a')); 
}
```
output:
```
[h, lo n, m,  s, y,  D, rt!]
```
Pada method ini akan menghilangkan kata sesuai pada method `split()` dan akan dipisahkan sesuai 

---
### substring()
```dart
void main() {
  var s = "Hello World";
  print(s.substring(2));
  print(s.substring(2, 6));
}
```
output:
```
llo World
llo 
```
Pada method ini kita bisa menampilkan text dengan range sesuai kita. Untuk method `substring()` mempunyai 2 param yaitu startIndex dan endIndex `substring(startInidex, endIndex)`dari suatu teks. param index berisi nilai integer. Index selalu diawali dengan angka 0 bukan angka 1, jadi pada contoh diatas index ke 1 adalah karakter `e`.

Jika yang diisi cuma param startIndex maka akan ditampilkan yang mulai dari index tersebut. Lain jika startIndex dan endIndex diisi semua maka yang ditampilkan akan karakter range dari startIndex sampe endIndex.