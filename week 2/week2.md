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

- ### Apa itu Prototype?

  Prototype adalah sebuah object yang berisi method-method yang dapat digunakan oleh object lain. Prototype dapat diakses dengan menggunakan tanda titik (.) setelah nama object. Contoh:

  ```javascript
  const name = "John";
  console.log(name.toUpperCase());
  ```

  Pada contoh di atas, method toUpperCase() merupakan method yang ada di dalam prototype String. Method toUpperCase() akan mengubah string menjadi huruf kapital.

- ### Apa itu Method?

  Method adalah sebuah function yang berada di dalam prototype. Method dapat digunakan untuk mengubah nilai dari object. Contoh:

  ```javascript
  const name = "John";
  console.log(name.toUpperCase());
  ```

  Pada contoh di atas, method toUpperCase() merupakan method yang ada di dalam prototype String. Method toUpperCase() akan mengubah string menjadi huruf kapital.

- ### Data Type Built-in - String
  - Protoype
    ```javascript
    const name = "John";
    console.log(name.length); // 4
    ```
  - Methode
    ````javascript
    const name = "Ibnu";
    console.log(name.toUpperCase()); // IBNU
    console.log(name.toLowerCase()); // ibnu
    console.log(name.charAt(0)); // I
    console.log(name.charAt(3)); // u
    console.log(name[0]); // I
    console.log(name[3]); // u
    console.log(name.charCodeAt(0)); // 73
    console.log(name.charCodeAt(3)); // 117
    console.log(name.concat(" ", "Choldun")); // Ibnu Choldun
    console.log(name.endsWith("u")); // true
    console.log(name.endsWith("n")); // false
    console.log(name.includes("b")); // true
    console.log(name.includes("c")); // false
    console.log(name.indexOf("b")); // 1
    console.log(name.indexOf("c")); // -1
    console.log(name.lastIndexOf("b")); // 1
    console.log(name.lastIndexOf("c")); // -1
    console.log(name.match(/b/g)); // ["b"]
    console.log(name.match(/c/g)); // null
    console.log(name.repeat(3)); // IbnuIbnuIbnu
    console.log(name.replace("b", "c")); // Icnu
    console.log(name.search("b")); // 1
    console.log(name.search("c")); // -1
    console.log(name.slice(0, 2)); // Ib
    console.log(name.slice(2, 4)); // nu
    console.log(name.split("")); // ["I", "b", "n", "u"]
    console.log(name.split("b")); // ["I", "nu"]
    console.log(name.startsWith("I")); // true
    console.log(name.startsWith("i")); // false
    console.log(name.substr(0, 2)); // Ib
    console.log(name.substr(2, 2)); // nu
    console.log(name.substring(0, 2)); // Ib
    console.log(name.substring(2, 4)); // nu
    console.log(name.trim()); // Ibnu
    console.log(name.trimStart()); // Ibnu
    console.log(name.trimEnd()); // Ibnu
    console.log(name.valueOf()); // Ibnu
        ```
    ````
- ### Data Type Built-in - Number
  - Protoype
    ```javascript
    const number = 10;
    console.log(number.toFixed(2)); // 10.00
    console.log(Number.MAX_VALUE); // 1.7976931348623157e+308
    console.log(Number.MIN_VALUE); // 5e-324
    console.log(Number.NEGATIVE_INFINITY); // -Infinity
    console.log(Number.POSITIVE_INFINITY); // Infinity
    console.log(Number.EPSILON); // 2.220446049250313e-16
    console.log(Number.NaN); // NaN
    console.log(Number.MIN_SAFE_INTEGER); // -9007199254740991
    console.log(Number.MAX_SAFE_INTEGER); // 9007199254740991
    ```
  - Methode
    ```javascript
    const number = 10;
    console.log(number.toFixed(2)); // 10.00
    console.log(number.toExponential(2)); // 1.00e+1
    console.log(number.toPrecision(2)); // 1.0e+1
    console.log(number.toString()); // 10
    console.log(number.toString(2)); // 1010
    console.log(number.toString(8)); // 12
    console.log(number.toString(16)); // a
    console.log(number.valueOf()); // 10
    console.log(Number.isFinite(10)); // true
    console.log(Number.isFinite(10 / 0)); // false
    console.log(Number.isInteger(10)); // true
    console.log(Number.isInteger(10.5)); // false
    console.log(Number.isNaN(10)); // false
    console.log(Number.isNaN(10 / 0)); // false
    console.log(Number.isNaN(10 / "a")); // true
    console.log(Number.isSafeInteger(10)); // true
    console.log(Number.isSafeInteger(10.5)); // false
    console.log(Number.isSafeInteger(9007199254740992)); // false
    console.log(Number.parseFloat("10.5")); // 10.5
    console.log(Number.parseInt("10.5")); // 10
    ```
- ### Data Type Built-in - Math

  - Protoype

    ```javascript
    console.log(Math.E); // 2.718281828459045
    console.log(Math.LN10); // 2.302585092994046
    console.log(Math.LN2); // 0.6931471805599453
    console.log(Math.LOG10E); // 0.4342944819032518
    console.log(Math.LOG2E); // 1.4426950408889634
    console.log(Math.PI); // 3.141592653589793
    console.log(Math.SQRT1_2); // 0.7071067811865476
    console.log(Math.SQRT2); // 1.4142135623730951
    ```

  - Methode
    ```javascript
    console.log(Math.abs(-10)); // 10
    console.log(Math.cbrt(8)); // 2
    console.log(Math.cos(1)); // 0.5403023058681398
    console.log(Math.floor(10.5)); // 10
    console.log(Math.log(10)); // 2.302585092994046
    console.log(Math.log10(10)); // 1
    console.log(Math.max(10, 20)); // 20
    console.log(Math.min(10, 20)); // 10
    console.log(Math.pow(2, 3)); // 8
    console.log(Math.random()); // 0.123456789
    console.log(Math.round(10.5)); // 11
    console.log(Math.sign(-10)); // -1
    console.log(Math.sin(1)); // 0.8414709848078965
    console.log(Math.sqrt(9)); // 3
    console.log(Math.tan(1)); // 1.5574077246549023
    ```

- ### Primitive dan non-primitive
  - Primitive
    - String
    - Number
    - Boolean
    - Null
    - Undefined
    - Symbol
  - Non-primitive
    - Object
    - Function
    - Array
    - Date
    - RegExp
    - Error

## Javascript Dasar - DOM - Introduction

- ### Apa itu Document Object Model (DOM)?

  Document Object Model (DOM) adalah sebuah interface yang memungkinkan kita untuk mengakses dan memanipulasi elemen HTML dan CSS. DOM menyediakan sebuah API yang memungkinkan kita untuk mengubah struktur halaman web, style, dan konten. DOM juga menyediakan sebuah API untuk membuat aplikasi yang interaktif dan menarik.

- ### Apa itu DOM Tree?

  DOM Tree adalah sebuah struktur data yang merepresentasikan struktur halaman web. DOM Tree terdiri dari node-node yang saling berhubungan. Setiap node memiliki tipe yang berbeda. Nodetipe element disebut element node. Node tipe text disebut text node. Node tipe comment disebut comment node. Node tipe document disebut document node. Node tipe attribute disebut attribute node.

- ### Apa itu DOM Node?

  DOM Node adalah sebuah objek yang merepresentasikan sebuah elemen HTML atau CSS. DOM Node memiliki properti dan metode yang dapat digunakan untuk mengakses dan memanipulasi elemen HTML atau CSS. DOM Node memiliki tipe yang berbeda. Tipe dari DOM Node dapat dilihat pada gambar di bawah ini.

- ### Apa manfaat DOM?
  - Memanipulasi elemen HTML dan CSS
  - Mengubah struktur halaman web
  - Mengubah style halaman web
  - Mengubah konten halaman web
  - Membuat aplikasi yang interaktif dan menarik

## Javascript Dasar - DOM - Selecting Element

- ### Cara mengakses DOM Node

  - Menggunakan ID
    ```javascript
    const title = document.getElementById("title");
    ```
  - Menggunakan Class
    ```javascript
    const title = document.getElementsByClassName("title");
    ```
  - Menggunakan Tag Name
    ```javascript
    const title = document.getElementsByTagName("h1");
    ```
  - Menggunakan Query Selector
    ```javascript
    const title = document.querySelector("#title");
    const title = document.querySelector(".title");
    const title = document.querySelector("h1");
    ```
  - Menggunakan Query Selector All
    ```javascript
    const title = document.querySelectorAll("#title");
    const title = document.querySelectorAll(".title");
    const title = document.querySelectorAll("h1");
    ```

- ### Cara mengakses DOM Node - Child

  - Menggunakan Child Nodes
    ```javascript
    const title = document.getElementById("title");
    const childNodes = title.childNodes;
    ```
  - Menggunakan Children
    ```javascript
    const title = document.getElementById("title");
    const children = title.children;
    ```
  - Menggunakan First Child
    ```javascript
    const title = document.getElementById("title");
    const firstChild = title.firstChild;
    ```
  - Menggunakan First Element Child
    ```javascript
    const title = document.getElementById("title");
    const firstElementChild = title.firstElementChild;
    ```
  - Menggunakan Last Child
    ```javascript
    const title = document.getElementById("title");
    const lastChild = title.lastChild;
    ```
  - Menggunakan Last Element Child
    ```javascript
    const title = document.getElementById("title");
    const lastElementChild = title.lastElementChild;
    ```

- ### Cara mengakses DOM Node - Parent

  - Menggunakan Parent Node
    ```javascript
    const title = document.getElementById("title");
    const parentNode = title.parentNode;
    ```
  - Menggunakan Parent Element
    ```javascript
    const title = document.getElementById("title");
    const parentElement = title.parentElement;
    ```

## Javascript Dasar - DOM - Traversing Element

- Menggunakan Next Sibling
  ```javascript
  const title = document.getElementById("title");
  const nextSibling = title.nextSibling;
  ```
- Menggunakan Next Element Sibling
  ```javascript
  const title = document.getElementById("title");
  const nextElementSibling = title.nextElementSibling;
  ```
- Menggunakan Previous Sibling
  ```javascript
  const title = document.getElementById("title");
  const previousSibling = title.previousSibling;
  ```
- Menggunakan Previous Element Sibling
  ```javascript
  const title = document.getElementById("title");
  const previousElementSibling = title.previousElementSibling;
  ```

## Javascript Dasar - DOM - Manipulating Elements

## Javascript Dasar - DOM - Manipulating Styles

## Javascript Dasar - DOM - Events

## Javascript Dasar - DOM - Forms
