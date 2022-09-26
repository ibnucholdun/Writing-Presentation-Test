# <p align="center">Summary Writing & Presentation Week 1</p>

## Table of contents

- [Unix Command Line](#unix-command-line)
- [Git dan GitHub Dasar](#git-dan-github-dasar)
- [HTML](#html)
- [CSS](#css)
- [Algoritma dan struktur data](#algoritma-dan-struktur-data)
- [Javascript Dasar](#javascript-dasar)

## Unix Command Line

- ### Shell

  Agar bisa terhubung dengan komputer maka user akan memerlukan penerjemah. Maka dari itu user memerlukan yang namanya shell. Definisi shell secara harfiah sendiri adalah program yang digunakan untuk berkomunikasi atau memerintah sistem.

- ### Command Line Interface (CLI)

  Merupakan sebuah program yang memungkinkan user mengetik perintah atau command yang akan mmemerintahkan perangkat komputer untuk melakukan suatu tugas tertentu.

- ### File System Structure

  - **Root** : merupakan direktori yang paling atas atau direktori induk dari semua direktori yang ada di sistem operasi.
  - **Home** : merupakan direktori yang paling bawah atau direktori anak dari semua direktori yang ada di sistem operasi.
  - **Relative Path** : merupakan path yang ditulis berdasarkan lokasi direktori yang sedang aktif.
  - **Absolute Path** : merupakan path yang ditulis berdasarkan lokasi direktori yang paling atas.

- ### Command
  Dibawah ini merupakan beberapa command yang sering digunakan dalam CLI dengan menggunakan bash shell.
  - Command `pwd` (_Print Working Directory_) => untuk mengetahui lokasi direktori yang sedang aktif.
  - Command `mkdir` (_Make Directory_) => untuk membuat direktori baru
  - Command `ls` (_list_) => untuk melihat isi dari direktori yang sedang aktif
  - Command `cd` (_change directory_) => untuk berpindah directori
  - Command `touch` => untuk membuat file baru
  - Command `cat` (_concatenate_) => untuk melihat isi dari file
  - Command `nano` => untuk mengedit file
  - Command `cp` (_copy_) => untuk menyalin file atau direktori
  - Command `mv` (_move_) => untuk memindahkan file atau directori
  - Command `rm` (_remove_) => untuk menghapus file direktori
  - Command `rmdir` (_remove directory_) => untuk menghapus direktori
  - Command `clear` => untuk membersihkan layar terminal

## Git dan GitHub Dasar

- ### Git

  Git adalah salah satu sistem pengontrol versi (Version Control System)yang berfungsi untuk mencatat setiap perubahan pada file proyek yang dikerjakan secara mandiri ataupun secara berkolaborasi tim.

- ### GitHub

  GitHub adalah layanan web yang menyediakan layanan hosting untuk proyek yang menggunakan sistem pengontrol versi Git.

- ### Kenapa Git dan Github tools yang wajib digunakaan?

  - Git dan Github sangat berguna untuk mengembangkan sebuah proyek yang bersifat kolaboratif.
  - Git dan Github sangat berguna untuk mengembangkan sebuah proyek yang bersifat mandiri.
  - Git dan Github sangat berguna untuk mengembangkan sebuah proyek yang bersifat open source.
  - Git dan Github sangat berguna untuk mengembangkan sebuah proyek yang bersifat komersial.

- ### Perbedaan Git dan Github

| Git                                                | Github                                                 |
| -------------------------------------------------- | ------------------------------------------------------ |
| 1. Meng-install software di penyimpanan lokal      | 1. Host melalui layanan cloud                          |
| 2. Berfokus pada version control dan code sharing  | 2. Berfokus pada source code hosting terpusat          |
| 3. Akses secara offline                            | 3. Akses secara online                                 |
| 4. Menyediakan desktop interface bernama “Git GUI” | 4. Menggunakan nama desktop interface “GitHub Desktop” |
| 5. _Open sourced licensed_                         | 5. Pilihan bagi pengguna gratis dan pengguna berbayar  |

- ### Alur kerja dari Git dan Github

  - Git sendiri memiliki 3 status yaitu :
    - **Modified** : berarti file tersebut telah diubah atau di edit.
    - **Staged** : berarti file tersebut telah siap untuk disimpan ke database Git.
    - **Committed** : berarti file tersebut telah disimpan ke database Git.
  - GitHub sendiri memiliki 3 status yaitu :
    - **Working Directory** : berarti file tersebut telah diubah atau di edit.
    - **Staging Area** : berarti file tersebut telah siap untuk disimpan ke database Git.
    - **Git Directory** : berarti file tersebut telah disimpan ke database Git.

- ### Command pada git dan github

  dibawah ini merupakan beberapa command yang sering digunakan dalam git dan github.

  - Command `git init` => untuk membuat repository baru
  - Command `git remote add origin` => untuk menambahkan remote repository
  - Command `git add` => untuk menambahkan file baru
  - Command `git commit` => untuk menyimpan perubahan ke database
  - Command `git push` => untuk mengirim perubahan ke server
  - Command `git pull` => untuk mengambil/mendownload perubahan terbaru dari server
  - Command `git clone` => untuk membuat working directory yang diambil dari repository server
  - Command `git status` => untuk mengecek status repository lokal
  - Command `git log` => untuk melihat history commit yang sudah dilakukan
  - Command `git branch` => untuk melihat daftar branch yang ada
  - Command `git checkout` => untuk berpindah branch
  - Command `git merge` => untuk menggabungkan branch lain ke branch yang sedang aktif

## HTML

- ### Apa itu HTML?

  HTML adalah singkatan dari _Hyper Text Markup Language_, yaitu sebuah bahasa markup yang digunakan untuk membuat struktur sebuah halaman web. HTML bukanlah bahasa pemrograman, namun merupakan bahasa markup yang digunakan untuk menandai elemen-elemen yang ada pada sebuah halaman web.

- ### Apa fungsi HTML?

  - HTML digunakan untuk menentukan struktur dari sebuah halaman web.
  - HTML digunakan untuk menentukan tampilan dari sebuah halaman web.
  - HTML digunakan untuk menentukan konten dari sebuah halaman web.
  - HTML digunakan untuk menentukan aksi dari sebuah halaman web.

- ### Tools pendukung dalam menggunakan HTML

  - Text Editor (Visual Studio Code, Sublime Text, Atom, Notepad++, dll)
  - Browser (Google Chrome, Mozilla Firefox, Opera, dll)

- ### Struktur dasar HTML

  - **DOCTYPE** `<!DOCTYPE>`: digunakan untuk mendefinisikan tipe dokumen HTML yang digunakan.
  - **HTML** `<html>.....</html>`: digunakan untuk menandai bahwa dokumen HTML dimulai.
  - **HEAD** `<head>.....</head>`: digunakan untuk menandai bagian kepala dokumen HTML.
  - **BODY** `<body>.....</body>`: digunakan untuk menandai bagian isi dokumen HTML.

- ### Tag dasar HTML

  - **Heading** `<h1>.....</h1>`
  - **Paragraph** `<p>.....</p>`
  - **Image** `<img/>`
  - **Link** `<a>.....</a>`
  - **Order List** `<ol>.....</ol>`
  - **Unorder List** `<ul>.....</ul>`
  - **Table** `<table>.....</table>`
  - **Form** `<form>.....</form>`
  - **Input** `<input/>`
  - **Button** `<button>.....</button>`
  - **Div** `<div>.....</div>`
  - **Span** `<span>.....</span>`

- ### Tag Semantik HTML 5

  - **Header** `<header>.....</header>`
  - **Footer** `<footer>.....</footer>`
  - **Main** `<main>.....</main>`
  - **Section** `<section>.....</section>`
  - **Article** `<article>.....</article>`
  - **Aside** `<aside>.....</aside>`
  - **Nav** `<nav>.....</nav>`
  - **Figure** `<figure>.....</figure>`
  - **Figcaption** `<figcaption>.....</figcaption>`

- ### Deploy HTML

  Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang. Jika aplikasi kita HTML atau Web App kita perlu mendeploy ke server. Untuk melakukan hal tersebut kita bisa menggunakan layanan gratis yang bernama Netlify, selain netlify ada juga layanan gratis lainnya seperti Heroku, Firebase, dll.

## CSS

- ### Apa itu CSS?

  CSS adalah singkatan dari _Cascading Style Sheets_, yaitu sebuah bahasa yang digunakan untuk membuat tampilan dari sebuah halaman web lebih menarik. CSS sama seperti HTML bukanlah bahasa pemrograman.

- ### Apa fungsi CSS?

  - CSS digunakan untuk menentukan tampilan dari sebuah halaman web.
  - CSS digunakan untuk menentukan warna dari sebuah halaman web.
  - CSS digunakan untuk menentukan font dari sebuah halaman web.
  - CSS digunakan untuk menentukan ukuran dari sebuah halaman web.
  - CSS digunakan untuk menentukan posisi dari sebuah halaman web.
  - CSS digunakan untuk menentukan animasi dari sebuah halaman web.

- ### Cara menyisipkan CSS ke dalam HTML

  - Inline CSS
    ```html
    <h1 style="color: red;">Hello World</h1>
    ```
  - Internal CSS
    ```html
    <head>
      <style>
        h1 {
          color: red;
        }
      </style>
    </head>
    ```
  - External CSS
    ```html
    <head>
      <link rel="stylesheet" href="style.css" />
    </head>
    ```

- ### Menggunakan sintaks dasar dari CSS

  - **Selector** `h1 {.....}` : digunakan untuk menentukan elemen mana yang akan diberi style.
  - **Property** `color: red;` : digunakan untuk menentukan style apa yang akan diberikan.
  - **Value** `color: red;` : digunakan untuk menentukan nilai dari style yang diberikan.
  - **Comment** `/*.....*/` : digunakan untuk menambahkan komentar pada CSS.

- ### Metode responsive web design menggunakan CSS

  - **Media Query** : digunakan untuk menentukan style yang berbeda pada device yang berbeda.
  - **Flexbox** : digunakan untuk menentukan layout yang responsive.
  - **Grid** : digunakan untuk menentukan layout yang responsive.

- ### Menggunakan flexbox
  - **Flex Container** : digunakan untuk menentukan elemen mana yang akan menjadi flex container.
  - **Flex Item** : digunakan untuk menentukan elemen mana yang akan menjadi flex item.
  - **Flex Direction** : digunakan untuk menentukan arah dari flex container.
  - **Flex Wrap** : digunakan untuk menentukan apakah flex item akan berpindah baris atau tidak.
  - **Flex Flow** : digunakan untuk menentukan flex direction dan flex wrap.
  - **Justify Content** : digunakan untuk menentukan posisi dari flex item secara horizontal.
  - **Align Items** : digunakan untuk menentukan posisi dari flex item secara vertical.
  - **Align Content** : digunakan untuk menentukan posisi dari flex item secara vertical jika terdapat lebih dari satu baris.

## Algoritma dan struktur data

- ### Apa itu algoritma?

  Algoritma adalah sebuah langkah-langkah yang sistematis dan logis untuk menyelesaikan suatu masalah.

- ### Apa itu struktur data?

  Struktur data adalah sebuah cara untuk menyimpan atau mengolah agar mudah diakses.

- ### Apa sih manfaat dari Algoritma dan Struktur data?

  - **Algoritma** : memudahkan kita dalam menyelesaikan masalah
  - **Struktur data** : memudahkan kita dalam mengolah data.

- ### Apa saja sih ciri-ciri dari Algoritma?

  - **Input** : Memiliki 0 atau lebih inputan
  - **Output** : Memiliki 1 atau lebih output
  - **Definiteness (Pasti)** : Setiap langkah harus jelas dan pasti
  - **Finiteness (Ada batas)** : Memiliki titik berhenti (stop)
  - **Effectiveness (Efektif)** : Sebisa mungkin tepat sasaran dan efisien

- ### Apa saja jenis proses dari algoritma

  - **Sequence** : langkah-langkah yang dilakukan berurutan
  - **Selection** : langkah-langkah yang dilakukan berdasarkan kondisi
  - **Repetition** : langkah-langkah yang dilakukan berulang-ulang

- ### Apa saja penyajian dari algoritma

  - **Descriptif** : penjelasan secara umum
  - **Flowchart** : merupakan gambaran dari algoritma yang berupa diagram
  - **Pseudocode** : merupakan penulisan algoritma dalam bahasa yang lebih mudah dimengerti

- ### Contoh algoritma sederhana

  - **Algoritma mencari Luas Persegi Panjang secara desctiptif**

    ```
        1. Deklarasikan variabel panjang dan lebar
        2. Masukkan nilai panjang dan lebar persegi panjang
        3. Hitung luas persegi panjang dengan rumus panjang x lebar
        4. Tampilkan luas persegi panjang
    ```

  - **Algoritma mencari Luas Persegi Panjang secara flowchart**

    ![flowchart](https://user-images.githubusercontent.com/96803344/192274918-b4b4cd8e-4620-4f59-8ef7-380b224d1ce6.png)

  - **Algoritma mencari Luas Persegi Panjang secara pseudocode**

    ```pseudocode
    DEKLARASI
        VAR panjang, lebar, luas : integer

    ALGORITMA
        panjang <- 10
        lebar <- 5
        luas <- panjang * lebar

    DISPLAY luas
    ```

- ### Menerapkan algoritma ke dalam bahasa pemrograman javascript

  ```javascript
  let panjang = 10;
  let lebar = 5;
  let luas = panjang * lebar;
  console.log(luas);
  ```

## Javascript Dasar

- ### Apa itu Javascript?

  Javascript adalah bahasa pemrograman yang digunakan untuk membuat website menjadi lebih interaktif.

- ### Apa saja yang bisa dilakukan dengan Javascript?

  - **Mengubah tampilan website** : dengan javascript kita bisa mengubah tampilan website sesuai dengan keinginan kita.
  - **Membuat animasi** : dengan javascript kita bisa membuat animasi yang menarik.
  - **Membuat interaksi** : dengan javascript kita bisa membuat interaksi antara user dan website.
  - **Membuat game** : dengan javascript kita bisa membuat game yang menarik.

- ### Bagaimana cara menggunakan javascript?

  - **Inline** : menuliskan script langsung pada html
    ```html
    <button onclick="alert('Hello World!')">Click Me!</button>
    ```
  - **Internal** : menuliskan script pada file html

    ```html
    <script>
      alert("Hello World!");
    </script>
    ```

  - **External** : menuliskan script pada file javascript

        ```html
        <script src="script.js"></script>
        ```

- ### Tipe data pada javascript

  - **Number** : tipe data yang berupa angka

    contoh :

    ```javascript
    let angka = 10;
    ```

  - **String** : tipe data yang berupa teks

    contoh :

    ```javascript
    let kata = "Hello World!";
    ```

  - **Boolean** : tipe data yang berupa true atau false

    contoh :

    ```javascript
    let benar = true;
    let salah = false;
    ```

  - **Array** : tipe data yang berupa kumpulan data

    contoh :

    ```javascript
    let array = [1, 2, 3, 4, 5];
    ```

  - **Object** : tipe data yang berupa kumpulan data yang memiliki key dan value
    contoh :
    ```javascript
    let object = {
      nama: "John",
      umur: 20,
      pekerjaan: "Programmer",
    };
    ```

- ### Operator pada javascript

  - **Aritmatika** : operator yang digunakan untuk melakukan operasi matematika

    | Operator | Keterangan  |
    | -------- | ----------- |
    | +        | Penjumlahan |
    | -        | Pengurangan |
    | \*       | Perkalian   |
    | /        | Pembagian   |
    | %        | Modulus     |

  - **Perbandingan** : operator yang digunakan untuk membandingkan dua buah nilai

    | Operator | Keterangan                        |
    | -------- | --------------------------------- |
    | ==       | Sama dengan                       |
    | !=       | Tidak sama dengan                 |
    | >        | Lebih besar dari                  |
    | <        | Lebih kecil dari                  |
    | >=       | Lebih besar dari atau sama dengan |
    | <=       | Lebih kecil dari atau sama dengan |

  - **Logika** : operator yang digunakan untuk menggabungkan dua buah kondisi

    | Operator | Keterangan |
    | -------- | ---------- |
    | &&       | AND        |
    | \|\|     | OR         |
    | !        | NOT        |

- ### Kondisi pada javascript

  - **If** : kondisi yang digunakan untuk mengeksekusi kode jika kondisi bernilai true

    ```javascript
    if (kondisi) {
      // kode yang akan dieksekusi jika kondisi bernilai true
    }
    ```

  - **If else** : kondisi yang digunakan untuk mengeksekusi kode jika kondisi bernilai true dan mengeksekusi kode jika kondisi bernilai false

    ```javascript
    if (kondisi) {
      // kode yang akan dieksekusi jika kondisi bernilai true
    } else {
      // kode yang akan dieksekusi jika kondisi bernilai false
    }
    ```

  - **If else if** : kondisi yang digunakan untuk mengeksekusi kode jika kondisi bernilai true dan mengeksekusi kode jika kondisi bernilai false

    ```javascript
    if (kondisi1) {
      // kode yang akan dieksekusi jika kondisi1 bernilai true
    } else if (kondisi2) {
      // kode yang akan dieksekusi jika kondisi2 bernilai true
    } else {
      // kode yang akan dieksekusi jika kondisi1 dan kondisi2 bernilai false
    }
    ```

  - **Switch** : kondisi yang digunakan untuk mengeksekusi kode jika kondisi bernilai true

    ```javascript
    switch (kondisi) {
      case "kondisi1":
        // kode yang akan dieksekusi jika kondisi bernilai kondisi1
        break;
      case "kondisi2":
        // kode yang akan dieksekusi jika kondisi bernilai kondisi2
        break;
      default:
      // kode yang akan dieksekusi jika kondisi tidak bernilai kondisi1 dan kondisi2
    }
    ```

  - **Ternary** : kondisi yang digunakan untuk mengeksekusi kode jika kondisi bernilai true dan mengeksekusi kode jika kondisi bernilai false

    ```javascript
    kondisi ? kode1 : kode2;
    ```

- ### Perulangan pada javascript

  - **For** : Perulangan dimana kita tahu seberapa banyak nilai pasti untuk pengulangannya

    ```javascript
    for (let i = 0; i < 10; i++) {
      // kode yang akan dieksekusi berulang kali
    }
    ```

  - **While** : Perulangan dimana kita tidak tahu seberapa banyak nilai pasti untuk pengulangannya

    ```javascript
    let i = 0;
    while (i < 10) {
      // kode yang akan dieksekusi berulang kali
      i++;
    }
    ```

  - **Do while** : perulangan yang menjalankan pengulangan 1 kali sebelum dilakukan pengecekan kondisi
    ```javascript
    let i = 0;
    do {
      // kode yang akan dieksekusi berulang kali
      i++;
    } while (i < 10);
    ```
