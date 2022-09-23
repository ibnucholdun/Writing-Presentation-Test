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

## Algoritma dan struktur data

## Javascript Dasar
