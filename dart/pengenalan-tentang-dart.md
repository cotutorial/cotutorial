---
title: Pengenalan Tentang Dart
date: 2019-10-18T19:31:13+07:00
banner: /img/post/dart_pengenalan.webp
jpg: /img/post/jpg/dart_pengenalan.jpg
draft: false
categories:
  - dart
tags:
  - dart
  - intro
  - pengenalan
author: 
- saputrago  
description: Dart merupakan bahasa pemrograman general-pupose yang dirancang oleh Lars Bak dan Kasper Lund dan dikembangkan oleh Google.
---

## Apa itu Dart?
Dart merupakan bahasa pemrograman general-pupose yang dirancang oleh [Lars Bak](https://en.wikipedia.org/wiki/Lars_Bak_(computer_programmer)) dan [Kasper Lund](http://verdich.dk/kasper/) dan dikembangkan oleh [Google](https://google.com). Bahasa ini dirancang untuk mempermudahkan developer untuk mengembangkan app nya untuk disegala platform / multiplatform. 

Dart salah satu bahasa pemrograman yang ada yang menggunkan gaya pemrograman bersifat object oriented atau OOP. Dart senderi menggunakan gaya sintaks bahasa C yang yang dikompile ke dalam bahasa javascript. 

Dart diresmikan pada konverensi GOTO, Denmark 10-12 Oktober 2011. Dart pertama kali rilis Dart 1.0 pada tahun 14 November 2013. 

## Mengapa pilih Dart?

### 1. Optimasi UI
Ya betul, Dart memang dikembangkan dengan bahasa pemrograman yang dikhususkan untuk pembuatan antarmuka pengguna atau juga disebut UI. Dan pada bahasa ini sangat mudah dipelajari dengan sintaks yang familiar dengan bahasa pemrograman lainya.

### 2. Produktif Development
Di Dart mempunyai fitur yang namanya *Hot Reload* yang fungsinya untuk mereload / merefresh output secara instant tanpa mengulangi proses debug ulang saat proses aplikasi berjalan. Dan fitur ini sangat bermanfaat bagi para developer untuk memanfaatkan waktu semaksimal munkin karena tanpa harus debug ulang yang prosesnya bisa memakan waktu lumanyan.

### 3. Cepat di Semua Platform
Ya karena Dart bisa support di multiplatform misal di ARM, ARM 64 untuk Mobile, Desktop, dan Backend, atau kompile dengan JavaScript untuk Web. Dart ini mengkompile aplikasi sesuai dengan *engine* murni untuk starup instant. 

## Macam-macam Platform yang dibuat dengan Dart
Pada bahasa Dart memungkinkan Anda dapat menggunakan kode-kode sederhana ataupun aplikasi yang berfitur lengkap, baik pada platform mobile, web, command line script, dan aplikasi pada platform server.

Teknologi kompiler pada Dart sangat fleksibel tergantung Anda menargetkan ke sasaran platform apa. Dan berikut sasaran platform kopiler pada Dart:

## 1. Dart Native (VM JIT dan AOT)
Pada **Dart Native** ini untuk target platform/perangkat seperti mobile/seluler, desktop, server dan lainnya. 

Baru baru ini Google telah merilis teknologi baru yaitu [Flutter](https://flutter.dev) yang fungsinya untuk membuat aplikasi multi-platform dengan UI toolkit yang populer dengan menargetkan build secara native baik mobile ataupun desktop.

  - **Alur Kerja Dart VM JIT**
  Dart VM memiliki compiler just-in-time(JIT) yang mendukung interpretasi murni (seperti yang diperlukan pada IOS) dan optimasi runtime.

  - **Optimasi Kode / Dart AOT**
  Pada saat aplikasi digunakan untuk produksi, apakah Anda mempublikasikan aplikasimu ke Play Store/App Store, Anda dapat menggunakan kompiler AOT ini untuk kompile ke aplikasi ARM dan ARM 64. Aplikasi yang di kompile dari AOT sangat lancar dan cepat. 

## 2. Dart Web (JavaScript)
Pada **Dart Web** memungkinkan Anda menjalankan platform web yang didukung oleh JavaScript dengan Dart Web. Jadi pada Dart akan dikompile ke dalam bahasa JavaScript yang dimengerti oleh browser umumnya.

Dan sekarang [Flutter](https://flutter.dev/web) juga support ke web platform. 
  
  - **Alur Kerja Development yang Cepat (Dart Dev Compiler)** Dart dev Compiler atau *dartdevc* adalah kompiler Dart ke JavaScript yang dioptimalkan. Anda dapat menggunakan webdev, sebagai alat yang mendukung tugas seperti me **run**,**debug** dan development.  
  
  - **Code Produksi yang dioptimalkan (Kompiler Dart JS)** Dart Js atau `dart2js` yaitu suatu alat kompile pada bahasa Dart untuk mengkonversikan ke JavaScript.

## Memulai membuat program pertama dengan Dart

Pada bahasa Dart init sintaks hampir sama seperti dengan C++, C#, Java, dan JavaScript. Jika Anda sebelumnya sudah pernah mempelajari bahasa pemrograman lain, pasti tidak asing lagi dengan sintaks pada Dart. Berikut contoh kode sederhana  dan kode pertama dengan Dart:

```dart
main() {
  print("Hello, World!");
}
```

jika kode tersebut dijalankan maka akan mengasilkan output berikut:

```bash
Hello, World!
```

Untuk Anda yang ingin mencoba membuat program pertama dengan menggunakan Dart dan tanpa harus menginstalnya silahkan ke [Try Dart](https://dart.dev/#try-dart) untuk mencoba dengan bahasa Dart.

Sekian pembahasan tentang pengenalan Dart, jika Anda masih kebingungan silahkan komen di form bawah, Terimakasih telah berkunjung ke CoTutorial.