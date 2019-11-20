---
title: "Dart List"
date: 2019-11-18T10:25:03+07:00
draft: false
banner: /img/post/dart_list.webp
jpg: /img/post/jpg/dart_list.jpg
categories:
  - dart
tags:
  - dart
  - basic 
author: 
- saputrago  
---

### Apa itu List?
List dalam pemrograman yaitu suatu kelompok nilai atau data yang disusun berdasarkan urutan index. Seperti bahasa pemrograman lainya Dart juga mempunyai list pada library nya, yang sudah disediakan pada Dart. List ini bisa disebut juga sebagai array. Pada list index dimulai dari `0` bukan dari `1`. Berikut contoh representasinya.

![List Representasi](/img/post/jpg/list_representasi.png)

Berdasarkan contoh tabel diatas List mempunyai index dan value nya. Pada tabel tersebut index pada colum pertama yang dimulai dari angka `0` dan value pada colum `2` yang berisi nilai dari index tersebut.  Untuk memanggil fungsi list pada flutter cukup dengan sintak `List()` atau `[]` pada variabel. 

List strukturnya hampir sama seperti tabel tersebut. Di dart mempunyai 2 macam list sebagai berikut:

## Fixed-length
Pada jenis list ini panjang list sudah titetapkan terlebih dahulu dan tidak bisa ditambah. Dan proses  pengisian valuenya pada saat runtime. Berikut contoh sintaksnya:

#### 1. Mendeklarasikan list
Adapun contoh sintaks untuk mendeklarasikan list berikut ini:
```dart
var nama_list = new List(jumlah_list)
```
Pada contoh sintaks diatas `List()` digunakan untuk menententukan jumlah panjang list tersebut.
#### 2. Inisialisasikan list element
Berikut contoh sintaks untuk menginisialisasikan suatu element pada list:
```dart
nama_list[index_list]=value
```

Berikut contoh lengkap imlementasi list fixed-length:
```dart
void main() {
  var lst = new List(3);
  lst[0] = 4;
  lst[1] = 6;
  lst[2] = 9;
  print(lst);
  print(lst[1]); 
  
  /* 
   * lst[1] itu digunakan untuk memanggil suatu element pada list, 
   * dengan 1 sebagai index 
   */
}
```

Pada contoh diatas, pada variabel `lst` itu nilainya berbentu list, yang jumlah element nya ditentukan yaitu 3. Maka pada line berikutnya ada kode `lst[0]` sampai `lst[2]` itu digunakan untuk menginisialisasikan nilai dari list tersebut. Mengapa kok sampai index ke 2 saja? ingat list dimulai dari 0.

## Growable list
**Growable list** ini dapat berubah panjangnya saat runtime. Sintaks untuk mendeklarasikan dan menginisialisasikan list di bawah ini:

```dart
var nama_list = [2, 4, 45];
/*
  *  untuk spesifik nilai pada element list
  */

var nama_list = List();
/*
  * untuk variabel yang element listnya kosong
  */
```

Untuk menginisialisasikan list ini sama seperti pada list tetap, tapi ingat jika list tersebut sudah mempunyai nilai maka nilainya akan digantikan dengan nilai yang baru, sesuai dengan penginisialisian tersebut.

Berikut contoh penggunaan Growable list:
```dart
void main() {
  var num_list = [1, 2, 3];
  num_list[1] = 90; // akan merubah nilai list pada index 1
  print(num_list);
}
```
Pada contoh diatas tersebut pada variabel `num_list` dengan index ke 1 diganti dengan 90. Maka outpunya seperti ini:
```
[1, 90, 3]
```

## Property
Property | Deskripsi
---------|----------
first | Mengembalikan elemen list pada index pertama
last | Mengembalikan elemen list pada index terakhir
length | Mengembalikan jumlah panjang elemen pada list
isEmpty | Mengembalikan nilai **true** jika elemen kosong, **false** jika tidak
isNotEmpty | Mengembalikan nilai **true** jika elemen list tersebut **tidak** kosong, **false** jika tidak
reversed | Mengembalikan semua elemen dengan membalik urutan dari index terakhir

Berikut contoh penggunaan property pada List:
```dart
void main() {
  var list = [3, 45, 6];
  
  // properti first
  print("Properti first ${list.first}");
  
  // properti last
  print("Properti last ${list.last}");
  
  // properti length
  print("Properti length ${list.length}");
  
  // properti last
  print("Properti last ${list.last}");
  
  // properti isEmpty
  print("Properti isEmpty ${list.isEmpty}");
  
  // properti isNotEmpty
  print("Properti isNotEmpty ${list.isNotEmpty}");
  
  // properti reversed
  print("Properti reversed ${list.reversed}");
}
```
Kode diaatas akan menghasilkan output berikut:
```
Properti first 3
Properti last 6
Properti length 3
Properti last 6
Properti isEmpty false
Properti isNotEmpty true
Properti reversed (6, 45, 3)
```

## Basic Operator
### 1. Add Element
Menambahkan suatu elemen dari list tersebut. Untuk method add element menggunakan sintaks `add()` function. Berikut contoh kodenya:
```dart
void main() {
  List l = [1, 2, 3];
  l.add(12);
  print(l);
}
```
output: 
```
[1, 2, 3, 12]
```
Atau juga kalau ingin menambahkan multiple element list, bisa menggunkan method `addAll()`. Berikut contoh kodenya:
```dart
void main() {
  List l = [1, 2, 3];
  l.addAll([6, 8]);
  print(l);
}
```
output:
```
[1, 2, 3, 12, 13]
```

### 2. Update Element
Mengedit atau mengupdate suatu element pada list. Berikut contoh kode:
```dart
void main() {
  List l = [1, 2, 3];
  print(l); // sebelum diupdate
  l[2] = 90;
  print(l); // sesudah di update
}
```
output:
```
[1, 2, 3]
[1, 2, 90]
```
Pada list yang belum diupdate list denggan index ke `2` nilainya `3` dan setelah diupdate dengan `l[2]=90` yang berarti list dengan index ke `2` samadengan `90`, maka list yang index ke `2` menjadi `90`.

### 3. Delete Element
Fungsi berikut digunakan untuk menghapus suatu elemen yang ada di list. Adapun sintaks method untuk mendelete elemen pada list yaitu `remove()` dan `removeAt()`. Berikut contoh-contohnya:

#### a. remove()
Pada fungsi ini menghapus suatu elemen dengan spesisfik value, contoh:
```dart
void main() {
  List l = [1, 8, 3];
  print(l); // sebelum di hapus
  l.remove(8);
  print(l); // sesudah di hapus
}
```
output:

```
1, 8, 3]
[1, 3]
```

Pada contoh diatas itu menghapus elemen list yang value nya 8 atau dalam kodenya `l.remove(8)`, jadi disini hapus suatu elemen harus spesisfik, tidak boleh asal yang tidak ada dalam elemen list.

#### b. removeAt()

Pada fungsi ini menghapus suatu elemen yang berdasarkan index. contoh:

```dart
void main() {
  List l = [1, 8, 3];
  print(l); // sebelum di hapus
  l.removeAt(2);
  print(l); // sesudah di hapus
}
```
Output:
```
[1, 8, 3]
[1, 8]
```