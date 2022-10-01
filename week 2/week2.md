# <p align="center">Summary Writing Week 2</p>

## Table of contents

- [Javascript Dasar - Scope](#javascript-dasar---scope)
- [Javascript Dasar - Function](#javascript-dasar---function)
- [Javascript Dasar - Data Type Built-in (Prototype and Method)](#javascript-dasar---data-type-built-in---prototype-and-method)
- [Javascript Dasar - DOM - Introduction](#javascript-dasar---dom---introduction)
- [Javascript Dasar - DOM - Selecting Element](#javascript-dasar---dom---selecting-element)
- [Javascript Dasar - DOM - Traversing Element](#javascript-dasar---dom---traversing-element)
- [JavaScript Dasar - DOM - Manipulating Elements](#javascript-dasar---dom---manipulating-elements)
- [JavaScript Dasar - DOM - Manipulating Styles](#javascript-dasar---dom---manipulating-styles)
- [JavaScript Dasar - DOM - Events](#javascript-dasar---dom---events)
- [JavaScript Dasar - DOM - Forms](#javascript-dasar---dom---forms)

## Javascript Dasar - Scope

- ### Apa itu Scope?

  Scope adalah sebuah tempat dimana sebuah variabel dapat diakses. Scope dapat dibagi menjadi 2 yaitu Global Scope dan Local Scope.

- ### Apa itu Global Scope?

  Global Scope adalah sebuah scope yang dapat diakses dimana saja di dalam sebuah program. Variabel yang berada di dalam Global Scope dapat diakses di dalam function maupun di luar function.

- ### Apa itu Local Scope?

  Local Scope adalah sebuah scope yang hanya dapat diakses di dalam function. Variabel yang berada di dalam Local Scope tidak dapat diakses di luar function. Variabel yang berada di dalam Local Scope dapat diakses di dalam function lain yang berada di dalam function yang sama.

- ### Apa itu Hoisting?
  Hoisting adalah sebuah proses dimana sebuah variabel atau function akan diangkat ke atas. Sehingga variabel atau function dapat diakses sebelum deklarasi.

## Javascript Dasar - Function

- ### Apa itu Function?

  Function adalah sebuah blok kode yang berisi kumpulan algoritma tertentu yang dapat dipanggil kapan saja. Function dapat menerima parameter dan mengembalikan nilai. Function dapat dipanggil kapan saja dan berulang kali. Function dapat dipanggil di dalam function lain, sehingga dapat mempermudah dalam pengembangan program. Function dapat dideklarasikan dengan menggunakan keyword function.

- ### Apa itu Parameter dan Argument?

  Parameter adalah sebuah variabel yang digunakan untuk menerima nilai dari function yang dipanggil. Argument adalah sebuah nilai yang dikirimkan ke function saat dipanggil. Argument akan disimpan di dalam parameter. Jumlah parameter dan argument harus sama. Jika jumlah parameter dan argument tidak sama, maka akan terjadi error.

  - Contoh 1

    ```javascript
    function sayHello(name) {
      console.log(`Hello ${name}`);
    }

    sayHello("John");
    ```

  - Contoh Defaul Parameter

    ```javascript
    function sayHello(name = "John") {
      console.log(`Hello ${name}`);
    }

    sayHello();
    ```

- ### Apa itu Return?

  Return adalah sebuah keyword yang digunakan untuk mengembalikan nilai dari function. Return akan menghentikan eksekusi function. Jika tidak ada return, maka function akan mengembalikan nilai undefined.

- ### Jenis-jenis Function?

  Function dapat dibagi menjadi 2 yaitu Function Declaration dan Function Expression dan untuk di ES6 terdapat jenis Function baru yaitu Arrow Function.

  - Function Declaration

    Function Declaration adalah sebuah function yang dideklarasikan dengan menggunakan keyword function. Function Declaration dapat dipanggil sebelum dideklarasikan.
    Contoh:

    ```javascript
    function sayHello() {
      console.log("Hello World");
    }
    ```

  - Function Expression

    Function Expression adalah sebuah function yang dideklarasikan dengan menggunakan keyword function. Function Expression tidak dapat dipanggil sebelum dideklarasikan. Contoh:

    ```javascript
    const sayHello = function () {
      console.log("Hello World");
    };
    ```

  - Arrow Function

    Arrow Function adalah sebuah function yang dideklarasikan dengan menggunakan tanda panah (=>). Arrow Function tidak memiliki keyword this. Contoh:

    ```javascript
    const sayHello = () => {
      console.log("Hello World");
    };
    ```

## Javascript Dasar - Data Type Built-in - Prototype and Method

## Javascript Dasar - DOM - Introduction

## Javascript Dasar - DOM - Selecting Element

## Javascript Dasar - DOM - Traversing Element

## Javascript Dasar - DOM - Manipulating Elements

## Javascript Dasar - DOM - Manipulating Styles

## Javascript Dasar - DOM - Events

## Javascript Dasar - DOM - Forms
