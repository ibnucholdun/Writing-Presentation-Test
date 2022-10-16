# <p align="center">Summary Writing Week 4</p>

## Table of contents

- [Javascript Intermediate - Asynchronous - Fetch](#javascript-intermediate---asynchronous---fetch)
- [Javascript Intermediate - Asynchronous - Async Await](#javascript-intermediate---asynchronous---async-await)
- [Git dan Github Lanjutan](#git-dan-github-lanjutan)
- [Responsive Web Design](#responsive-web-design)
- [Bootstrap 5](#bootstrap-5)

## Javascript Intermediate - Asynchronous - Fetch

- ### Fetch

  fetch() method mengembalikan sebuah Promise yang akan menyelesaikan dengan Response objek ketika permintaan selesai, atau dengan objek Error jika terjadi kesalahan. fetch dapat digunakan untuk mengambil data dari server, tetapi juga untuk mengirim data ke server.

  ```javascript
  fetch(url, [options]);
  ```

  - url : URL yang akan diakses
  - options : objek yang berisi properti tambahan untuk mengatur permintaan, seperti method, headers, body, dan mode.

- #### Contoh penggunaan fetch

  ```javascript
  fetch("https://jsonplaceholder.typicode.com/users")
    .then((response) => response.json())
    .then((data) => console.log(data));
  ```

  - response.json() : mengubah response menjadi json
  - data : data yang diambil dari server

  ```javascript
  fetch("https://jsonplaceholder.typicode.com/users", {
    method: "POST",
    body: JSON.stringify({
      name: "Ibnu Choldun",
      email: "ibnucholdun023@gmail.com",
    }),
    headers: {
      "Content-type": "application/json; charset=UTF-8",
    },
  })
    .then((response) => response.json())
    .then((data) => console.log(data));
  ```

  - method : method yang digunakan untuk mengakses url yang memiliki nilai beberapa method seperti GET, POST, PUT, DELETE, dan lain-lain. Default method adalah GET.
  - body : data yang dikirim ke server
  - headers : header yang digunakan untuk mengakses url

## Javascript Intermediate - Asynchronous - Async Await

## Git dan Github Lanjutan

## Responsive Web Design

## Bootstrap 5
