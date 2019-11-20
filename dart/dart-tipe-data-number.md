---
title: "Dart Tipe Data Number"
date: 2019-11-16T12:12:01+07:00
draft: false
banner: /img/post/dart_tipe_data_number.webp
jpg: /img/post/jpg/dart_tipe_data_number.jpg
categories:
  - dart
tags:
  - dart
  - basic
author: 
  - saputrago  
---

Sebelumnya sudah ada artikel tentang [pengenalan variabel dan tipe data](/dart/mengenal-tipe-data-dan-variable/), nah pada bagian ini akan diteruskan materinya yaitu tentang Tipe data Number.

Apa itu Number?

Number pada hal ini berarti sebuah tipe data yang nilainya sebuah angka. Pada basaha Dart ini tipe data Number dibedakan menjadi 2 yaitu:

1. **Int** (Integer)
2. **Double** (Float)

Berikut penjelan dari masing-masing tipe data Number:

## 1. Int
Int atau disebut juga Integer ini yaitu sebuah tipe data dari Number yang nilainya berbentuk bilangan bulat. Contoh seperti `12` , `3` dst. Jadi pada intinya pada integer ini nilainya harus bersifat angka dan tidak boleh ada koma. Pada integer ini jika di compile ke JavaScript nilai max nya mulai -2<sup>53</sup> sampai 2<sup>53</sup>. 

**Bagaimana cara membuat variabel dengan tipe data Integer?**
Pada tipe data integer ini kita membutuhkan keyword `int` untuk mengenali sebuah tipe data Integer. Sebagai contoh perhatikan contoh sintaks penerapan tipe data Integer pada Dart.

```dart
int nama_variabel
```

berikut contoh lengkap penerapan dari Integer ini:

```dart
void() {
  int angka = 12;
  print(angka);
}
```
dan hasilnya..
```txt
12
```

Oh ya jika teman ingin mencoba Dart tanpa perlu install ada tool yang sudah disediakan untuk menjalankan kode Dart secara online yaitu [DartPad](https://dartpad.dev).

## 2. Double
Tadi sudah dibahas tentang Integer, sekarang kita beralih ke tipe data double.

Tipe data **Double** yaitu tipe data yang nilainya berisi angka float/desimal. Pada tipe data double ini kita membutuhkan keyword untuk mendeklarasikan variabel yang tipenya double. Berikut contoh sintaks penerapanya:

```dart
double nama_variabel
```

untuk penerapan aslinya perhatikan kode berikut:
```dart
void main (){
  double numd = 12.34;
  print(numd);
}
```

maka akan menghasilkan output berikut:

```
12.34
```

Apakah nilai double harus berisi angka koma? Jawabanya **tidak** karena double bisa memuat tidak hanya float angka saja tapi juga angka bulat.

## Parsing 
Parsing ini memungkinkan kita merubah nilai variabel string ke angka. Tapi tidak semua nilai String bisa di parse ya, cuma string yang isinya cuma ada angka saja. Contoh `"80"`, `"23.45"`. Pada contoh tersebut nilai string bisa diparse. berikut contoh penerapanya.

```dart
void main() {
  print(num.parse("80"));
  print(num.parse("23.45"));
}
```

dan akan menghasilkan output berikut: 

```
80
23.45
```

Pada sintaks `num.parse()` itu sebagai sintaks atau keyqord untuk memparse sebuah string ke number/angka.

untuk contoh memparse yang salah, berikut contoh kodenya

```dart
void main (){
  print(num.parse("HAI"));
}
```
dan akan mengakibatkan error seperti berikut: 
`
Uncaught exception:
FormatException: HAI`

## Method
Di Dart pada type data Number sudah disediakan berbagai method baik Integer maupun Double untuk mempermudahkan kita.

Method |Deskripsi
-------|-------
[abs()](#abs) | Mengembalikan nilai absolut
[ceil()](#ceil) | Mengembalikan pembulatan besar ke **int**
[ceilToDouble()](#ceiltodouble) | Mengembalikan pembulatan besar ke **double**
[floor()](#floor) | Mengembalikan pembulatan kecil ke **int**
[floorToDouble()](#floortodouble) | Mengembalikan pembulatan kecil ke **double**
[round()](#round) | Mengembalikan pembulatan ke angka terdekat
[roundToDouble()](#roundtodouble) | Mengembalikan pembulatan ke angka terdekat ke **double**
[toString()](#method-tostring) | Mengembalikan nilai ke **String**
[toDouble()](#todouble) | Mengembalikan nilai ke **double**
[toInt()](#toint) | Mengembalikan nilai ke **int**
[truncate()](#truncate) | Mengembalikan nilai **int** dengan menghilangkan koma
[truncateToDouble()](#truncatetodouble) | Mengembalikan nilai ke **double**

---

### abs()
```dart
void main() {
  int n = -23;
  print(n.abs());
}
```
Jika nilainya netagatif akan dikembalikan ke nilai positif. Hasil output kode diatas:
```
23
```
---

### ceil()
```dart
void main (){
  double n1 = 23.2;
  double n2 = 54.9;
  print(n1.ceil());
  print(n2.ceil());
}
```
Jika nilainya double akan dibulatkan ke besar, misal `12,2` akan dibulatkan jadi `13`. Hasil dari kode diatas yaitu:
```
24
55
``` 
---

### ceilToDouble()
```dart
void main (){
  int n1 = 23;
  print(n1.ceilToDouble());
}
```
Nilai yang ingin dikonversi harus integer. Output dari kode diatas:

```
23
```
---

### floor()
```dart
void main (){
  double n = 23.9;
  double n1 = 23.2;
  print(n.floor());
  print(n1.floor());
}
```
Jika nilainya adalah double maka akan dibulatkan ke kecil, atau bisa juga dihilangkan komanya. Hasil output dari kode diatas:
```
23
23
```
---

### floorToDouble()
```dart
void main (){
  double n = 23.9;
  double n1 = 23.2;
  print(n.floor());
  print(n1.floor());
}
```
---

### round()
```dart
void main (){
  double n1 = 23.6;
  double n2 = 23.4;
  print(n1.round());
  print(n2.round());
}
```
Pada method `round()` ini, jika nilai koma double `< 5` maka akan dibulatkan ke bawah, sedangkan jika nilai koma double `>=` 5 akan dibulatkan ke atas. Hasil dari output kode diats adalah:

```
24
23
```
---
### roundToDouble()
```dart
void main (){
  double n = 45.6;
  print(n.roundToDouble());
}
```
pada method ini hampir sama dengan method `round()` cuma perbadaannya pada outputnya bertipe `double`. Hasil dari kode diatas:

```
46
```

---
### Method toString()
```dart
void main (){
  int n = 34;
  print(n.toString() + "sebagai String");
}
```
Pada method ini `toString` sebagai menkonversi nilai apapun ke `String`. Pada contoh kode diatas variabel `n` dikonversikan ke string makanya bisa ditambah dengan nilai string. Berikut hasilnya

```
34 sebagai String
```

--- 
### toDouble()
```dart
void main() {
  int n = 45;
  print(n.toDouble());
}
```
pada method ini nilai harus bertipe `int`, setelah itu nilai tersebut akan dikonversi ke double. 
Output:

```
45
```

--- 
### toInt()
```dart
void main() {
  double n = 86.6;
  print(n.toInt());
}
```
Pada contoh kode tersebut variabel `n` dikonversi ke `int` maka nilai koma dari variabel `n` akan dihangkan.

Output:
```
86
```

---
### truncate()
```dart
void main (){
  var n = 86.823;
  print(n.truncate());
}
```
Pada kasus ini method 'truncate()' berfungsi untuk meghilangkan koma dan akan mengembalikan nilai integer.

Output:
```
86
```

---
### truncateToDouble()
```dart
void main (){
  var n = 86.823;
  print(n.truncateToDouble());
}
```
Pada kasus ini method 'truncateToDouble()' berfungsi untuk meghilangkan koma dan akan mengembalikan nilai double.

Output:
```
86
```