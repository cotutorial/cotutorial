---
title: "Documentation Contribution"
draft: false
page: true
noTimeEstimate: true 
---
Halo terimakasih Anda sudah berniat ingin contribusi di sini di CoTutorial. Saya akan membagikan dokumentasi tag markdown dan param yang digunakan pada CoTutorial. Di CoTutorial tag markdown ini tidak jauh seperti di guthub, gitlab, dll. 

# Params
Param ini sangatlah penting untuk sebuah artikel di CoTutorial. Ketika Anda ingin berkontribusi di CoTutorial harus tahu macam-macam param yang telah kami sediakan. Berikut macam-macam param untuk membuat sebuah artikel.

### 1. Title
Title ini berguna untuk menampilkan title pada web browser pada tab dan untuk title pada serach google. Berikut contoh sintaknya:

```md
title: "Hello World"
```

contoh output:
![Title Dokumentasi CoTutorial](/img/doc/title.jpg)

### 2. Date
Date ini digunakan untuk menampilkan tangggal berapa artike ini rilis. Berikut contoh format sintaksnya:
```md
date: 2019-11-18T08:30:58+07:00
```

contoh output:
![Date Dokumentasi CoTutorial](/img/doc/date.jpg)
### 3. Banner
Banner ini digunakan untuk gambar tiap artikel yang dipublish. Berikut contoh sintaks params:
```md
banner: https://example.com/image.jpg
```
contoh output:
![Banner Dokumentasi CoTutorial](/img/doc/banner.jpg)
### 4. Categories
Params categories ini untuk artikel itu kategorinya apa. Berikut contoh sintaks paramnya:
```md
categories:
  - dart
```
contoh output:
![Category Dokumentasi CoTutorial](/img/doc/categori.jpg)
### 5. Tag
Param tag untuk tag apa pada artike tersebut. Berikut contoh sintaks params:
```md
tags:
  - tags1
  - tags2
  - tags3
```
contoh output:
![Tags Dokumentasi CoTutorial](/img/doc/tag.jpg)
### 6. Author
Param author untuk artikel tersebut artikel berikut. Params author tersebut adalah username github anda. Berikut contoh sintaksnya:
```md
author: 
    - saputrago  
```
contoh output:
![Author Dokumentasi CoTutorial](/img/doc/author.jpg)

Berikut contoh lengkap param lengkap untuk sebuah artikel:

```md
---
title: "Hello World"
date: 2019-11-18T08:30:58+07:00
banner: https://example.com/image.jpg
categories:
  - dart
tags:
  - dart
author: 
- saputrago  
---
```

---

# Tag Markdown
---
## Heading 
Heading digunakan sebagai title, subtitle, dll. Membuat heading dengan markdown tidaklah sulit cukup dengan sintaks berikut, dengan macam-macam heading:

```md
# Heading 1
## Heading 2
### Heading 3
#### Heading 4 
```
output: 

# Heading 1
## Heading 2
### Heading 3
#### Heading 4 

---

## Image
Berikut contohnya:

```md
![Text Alternative Image](https://cotutorial.github.io/img/logo.svg)
```
output:
![Text Alternative Image](https://cotutorial.github.io/img/logo.svg)

---

## Highlight Code

1. Simple highlight
```md
`hello world`
```
output
`hello world`
2. Higlight Code spesifik bahasa


```md
	```html
	<html>
		<head>
			<title>Hello World</title
		</head>
	<body>
		Hello World
	</body>
	</html>
	```
```

output:

```html
<html>
    <head>
        <title>Hello World</title>
    </head>
    <body>
        Hello World
    </body>
</html>
```
---
## Table
```md
Row 1 | Row 2 | Row 3
------|-------|------
Hello| My Name | CoTutorial
I am | is | Fun
```

output

Row 1 | Row 2 | Row 3
------|-------|------
Hello| My Name | CoTutorial
I am | is | Fun

--- 
## Horizontal Rules
contoh sintak
```md
---
```
output

---

garis itu lah hasil dari tag `---`. Sekian dokumentasinya tag-tag markdown bisa anda pelajari, Ini adalah cuma sebagian dari tag markdown yaang lain bisa anda pelajari di berbagai website lainya untuk menambah wawasan, contoh website dokumentasi markdown: https://www.markdownguide.org/basic-syntax/