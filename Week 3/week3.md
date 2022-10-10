# <p align="center">Summary Writing Week 3</p>

## Table of contents

- [Javascript Intermediate - Array dan Multidimensional Array](#javascript-intermediate---array-dan-multidimensional-array)
- [Javascript Intermediate - Object](#javascript-intermediate---object)
- [Javascript Intermediate - Recursive dan Import Export Module](#javascript-intermediate---recursive-dan-import-export-module)
- [Javascript Intermediate - Asynchronous](#javascript-intermediate---asynchronous)
- [Javascript Intermediate - Web Storage](#javascript-intermediate---web-storage)

## Javascript Intermediate - Array dan Multidimensional Array

- ### Array

  Array adalah tipe data yang dapat menyimpan lebih dari satu nilai dalam satu variabel. Array dapat menyimpan berbagai tipe data, bahkan array lainnya, dalam satu array harus menimpan satu tipe data yang sama. Array juga dapat menyimpan fungsi. Array dapat diakses dengan menggunakan indeks. Indeks dimulai dari 0. Indeks juga dapat diakses dari belakang dengan menggunakan indeks negatif. Indeks -1 adalah indeks terakhir dari array.

  - #### Membuat Array
    ```javascript
    let arr = [1, 2, 3, 4, 5];
    let arr = new Array(1, 2, 3, 4, 5);
    ```
  - #### Mengakses Array
    ```javascript
    let arr = [1, 2, 3, 4, 5];
    console.log(arr[0]); // 1
    console.log(arr[4]); // 5
    console.log(arr[-1]); // undefined
    console.log(arr[-2]); // undefined
    console.log(arr[arr.length - 1]); // 5
    console.log(arr[arr.length - 2]); // 4
    ```
  - #### Mengubah Array

    ```javascript
    let arr = [1, 2, 3, 4, 5];
    arr[0] = 10;
    console.log(arr); // [10, 2, 3, 4, 5]
    ```

  - #### Array Properties

    Berikut adalah beberapa properti yang dapat digunakan pada array.

    - #### length
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      console.log(arr.length); // 5
      ```
    - #### constructor
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      console.log(arr.constructor); // [Function: Array]
      ```
    - #### prototype
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      console.log(arr.prototype); // undefined
      ```

  - #### Array Methode
    Berikut adalah beberapa methode yang dapat digunakan pada array.
    - #### push()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.push(6);
      console.log(arr); // [1, 2, 3, 4, 5, 6]
      ```
    - #### pop()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.pop();
      console.log(arr); // [1, 2, 3, 4]
      ```
    - #### unshift()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.unshift(0);
      console.log(arr); // [0, 1, 2, 3, 4, 5]
      ```
    - #### shift()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.shift();
      console.log(arr); // [2, 3, 4, 5]
      ```
    - #### splice()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.splice(2, 0, 10);
      console.log(arr); // [1, 2, 10, 3, 4, 5]
      ```
    - #### slice()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.slice(2, 4);
      console.log(arr2); // [3, 4]
      ```
    - #### join()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.join("-");
      console.log(arr2); // 1-2-3-4-5
      ```
    - #### concat()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.concat([6, 7, 8]);
      console.log(arr2); // [1, 2, 3, 4, 5, 6, 7, 8]
      ```
    - #### reverse()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.reverse();
      console.log(arr); // [5, 4, 3, 2, 1]
      ```
    - #### sort()
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.sort();
      console.log(arr); // [1, 2, 3, 4, 5]
      ```
  - #### Looping Pada Array
    Berikut adalah beberapa cara looping pada array.
    - #### for
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      for (let i = 0; i < arr.length; i++) {
        console.log(arr[i]);
      }
      ```
    - #### for of
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      for (let i of arr) {
        console.log(i);
      }
      ```
    - #### forEach
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      arr.forEach((i) => {
        console.log(i);
      });
      ```
    - #### map
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.map((i) => {
        return i * 2;
      });
      console.log(arr2); // [2, 4, 6, 8, 10]
      ```
    - #### filter
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.filter((i) => {
        return i % 2 == 0;
      });
      console.log(arr2); // [2, 4]
      ```
    - #### reduce
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.reduce((acc, cur) => {
        return acc + cur;
      });
      console.log(arr2); // 15
      ```
    - #### find
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.find((i) => {
        return i == 3;
      });
      console.log(arr2); // 3
      ```
    - #### findIndex
      ```javascript
      let arr = [1, 2, 3, 4, 5];
      let arr2 = arr.findIndex((i) => {
        return i == 3;
      });
      console.log(arr2); // 2
      ```

- ### Array Multidimensional
  Array multidimensional adalah array yang berisi array lainnya.
  - #### Membuat array multidimensional
    ```javascript
    let arr = [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9],
    ];
    ```
  - #### Mengakses array multidimensional
    ```javascript
    let arr = [
      [1, 2, 3],
      [4, 5, 6],
      [7, 8, 9],
    ];
    console.log(arr[0][0]); // 1
    console.log(arr[0][1]); // 2
    console.log(arr[0][2]); // 3
    console.log(arr[1][0]); // 4
    console.log(arr[1][1]); // 5
    ```
  - ### Looping pada array multidimensional
    Berikut adalah beberapa cara looping pada array multidimensional.
    - #### for
      ```javascript
      let arr = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ];
      for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr[i].length; j++) {
          console.log(arr[i][j]);
        }
      }
      ```
    - #### for of
      ```javascript
      let arr = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ];
      for (let i of arr) {
        for (let j of i) {
          console.log(j);
        }
      }
      ```
    - #### forEach
      ```javascript
      let arr = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ];
      arr.forEach((i) => {
        i.forEach((j) => {
          console.log(j);
        });
      });
      ```
    - #### map
      ```javascript
      let arr = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ];
      let arr2 = arr.map((i) => {
        return i.map((j) => {
          return j * 2;
        });
      });
      console.log(arr2);
      ```
    - #### filter
      ```javascript
      let arr = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ];
      let arr2 = arr.filter((i) => {
        return i.filter((j) => {
          return j % 2 == 0;
        });
      });
      console.log(arr2);
      ```
    - #### reduce
      ```javascript
      let arr = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9],
      ];
      let arr2 = arr.reduce((acc, cur) => {
        return acc.concat(cur);
      });
      console.log(arr2);
      ```

## Javascript Intermediate - Object

- ### Apa itu Object?
  Object adalah sebuah variabel yang berisi banyak nilai. Object juga disebut sebagai _collection of properties_. Object memiliki _key_ dan _value_. _Key_ adalah nama dari _value_ yang ada di dalam object. _Value_ adalah nilai dari _key_ yang ada di dalam object. Object dibuat dengan menggunakan kurung kurawal `{}`.
  ```javascript
  let obj = {
    key1: "value1",
    key2: "value2",
    key3: "value3",
  };
  ```
  - ### Membuat Object
    ```javascript
    let car = {
      type: "Fiat",
      model: "500",
      color: "white",
    };
    ```
  - ### Mengakses Object
    Terdapat dua cara untuk mengakses object, yaitu dengan menggunakan _dot notation_ dan _bracket notation_.
    - #### Dot Notation
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      console.log(car.type); // Fiat
      console.log(car.model); // 500
      console.log(car.color); // white
      ```
    - #### Bracket Notation
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      console.log(car["type"]); // Fiat
      console.log(car["model"]); // 500
      console.log(car["color"]); // white
      ```
  - ### Mengubah Object
    ```javascript
    let car = {
      type: "Fiat",
      model: "500",
      color: "white",
    };
    car.type = "Honda";
    car.model = "Civic";
    car.color = "black";
    console.log(car);
    ```
  - ### Menghapus Object
    ```javascript
    let car = {
      type: "Fiat",
      model: "500",
      color: "white",
    };
    delete car.type;
    delete car.model;
    delete car.color;
    console.log(car);
    ```
  - ### Nested Object
    Nested object adalah object yang berisi object lainnya.
    ```javascript
    let car = {
      type: "Fiat",
      model: "500",
      color: "white",
      owner: {
        name: "Ibnu",
        age: 20,
      },
    };
    console.log(car.owner.name); // Ibnu
    console.log(car.owner.age); // 20
    ```
  - ### Object Methode
    Object methode adalah sebuah fungsi yang ada di dalam object.
    ```javascript
    let car = {
      type: "Fiat",
      model: "500",
      color: "white",
      start: function () {
        console.log("The car has started");
      },
    };
    car.start(); // The car has started
    ```
  - ### Looping pada object
    Berikut adalah beberapa cara looping pada object.
    - #### for in
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      for (let i in car) {
        console.log(i);
      }
      ```
    - #### for of
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      for (let i of Object.keys(car)) {
        console.log(i);
      }
      ```
    - #### forEach
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      Object.keys(car).forEach((i) => {
        console.log(i);
      });
      ```
    - #### map
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      let car2 = Object.keys(car).map((i) => {
        return i;
      });
      console.log(car2);
      ```
    - #### filter
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      let car2 = Object.keys(car).filter((i) => {
        return i == "type";
      });
      console.log(car2);
      ```
    - #### reduce
      ```javascript
      let car = {
        type: "Fiat",
        model: "500",
        color: "white",
      };
      let car2 = Object.keys(car).reduce((acc, cur) => {
        return acc + cur;
      });
      console.log(car2);
      ```
  - ### Array of Object
    Array of object adalah array yang berisi object.
    ```javascript
    let cars = [
      {
        type: "Fiat",
        model: "500",
        color: "white",
      },
      {
        type: "Honda",
        model: "Civic",
        color: "black",
      },
    ];
    console.log(cars[0].type); // Fiat
    console.log(cars[0].model); // 500
    console.log(cars[0].color); // white
    console.log(cars[1].type); // Honda
    console.log(cars[1].model); // Civic
    console.log(cars[1].color); // black
    ```

## Javascript Intermediate - Recursive dan Import Export Module

- ### Apa itu Recursive?
  Recursive adalah sebuah fungsi yang memanggil dirinya sendiri.
  ```javascript
  function recursive() {
    recursive();
  }
  recursive();
  ```
- ### Recursive dengan kondisi

  ```javascript
  function recursive(num) {
    if (num === 0) {
      return;
    }
    console.log(num);
    recursive(num - 1);
  }
  recursive(5);
  ```

  - ### Import Export Module
    Import export module adalah sebuah cara untuk membagi kode menjadi beberapa file. Dengan menggunakan import export module, kita dapat membagi kode menjadi beberapa file sehingga kode menjadi lebih rapi dan mudah untuk di maintain. Berikut adalah cara menggunakan import export module.
    - #### Export
      ```javascript
      // file 1
      export const name = "Ibnu";
      export const age = 20;
      export const address = "Jakarta";
      ```
      ```javascript
      // file 2
      export default function () {
        console.log("Hello World");
      }
      ```
    - #### Import
      ```javascript
      // file 1
      import { name, age, address } from "./file1.js";
      console.log(name); // Ibnu
      console.log(age); // 20
      console.log(address); // Jakarta
      ```
      ```javascript
      // file 2
      import hello from "./file2.js";
      hello(); // Hello World
      ```
    - #### Import All
      ```javascript
      // file 1
      import * as file1 from "./file1.js";
      console.log(file1.name); // Ibnu
      console.log(file1.age); // 20
      console.log(file1.address); // Jakarta
      ```

## Javascript Intermediate - Asynchronous

- ### Apa itu Asynchronous?
  Asynchronous adalah sebuah proses dimana kita dapat menjalankan beberapa proses secara bersamaan tanpa harus menunggu proses sebelumnya selesai.
  ```javascript
  console.log("Hello");
  setTimeout(() => {
    console.log("World");
  }, 1000);
  console.log("!");
  ```
  Output:
  ```
  Hello
  !
  World
  ```
- ### Callback
  Callback adalah sebuah fungsi yang akan dijalankan setelah fungsi lain selesai dijalankan.
  ```javascript
  function hello(callback) {
    setTimeout(() => {
      console.log("Hello");
      callback();
    }, 1000);
  }
  function world() {
    console.log("World");
  }
  hello(world);
  ```
  Output:
  ```
  Hello
  World
  ```
- ### Promise
  Promise adalah sebuah fungsi yang akan dijalankan setelah fungsi lain selesai dijalankan. Promise memiliki 3 state yaitu pending, fulfilled, dan rejected.
  ```javascript
  function hello() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        console.log("Hello");
        resolve();
      }, 1000);
    });
  }
  function world() {
    console.log("World");
  }
  hello().then(world);
  ```
  Output:
  ```
  Hello
  World
  ```
- ### Async Await
  Async await adalah sebuah cara untuk menulis kode asynchronous yang lebih mudah dibaca.
  ```javascript
  function hello() {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        console.log("Hello");
        resolve();
      }, 1000);
    });
  }
  function world() {
    console.log("World");
  }
  async function main() {
    await hello();
    world();
  }
  main();
  ```
  Output:
  ```
  Hello
  World
  ```

## Javascript Intermediate - Web Storage

- ### Apa itu Web Storage?
  Web storage adalah sebuah cara untuk menyimpan data di browser. Web storage memiliki 2 jenis yaitu local storage dan session storage. Local storage akan menyimpan data di browser dan data tersebut akan tetap ada meskipun browser ditutup. Sedangkan session storage akan menyimpan data di browser dan data tersebut akan hilang jika browser ditutup.
  - #### Local Storage
    ```javascript
    localStorage.setItem("name", "Ibnu");
    localStorage.setItem("age", 20);
    localStorage.setItem("address", "Jakarta");
    console.log(localStorage.getItem("name")); // Ibnu
    console.log(localStorage.getItem("age")); // 20
    console.log(localStorage.getItem("address")); // Jakarta
    localStorage.removeItem("name");
    localStorage.removeItem("age");
    localStorage.removeItem("address");
    ```
  - #### Session Storage
    ```javascript
    sessionStorage.setItem("name", "Ibnu");
    sessionStorage.setItem("age", 20);
    sessionStorage.setItem("address", "Jakarta");
    console.log(sessionStorage.getItem("name")); // Ibnu
    console.log(sessionStorage.getItem("age")); // 20
    console.log(sessionStorage.getItem("address")); // Jakarta
    sessionStorage.removeItem("name");
    sessionStorage.removeItem("age");
    sessionStorage.removeItem("address");
    ```
- ### Apa itu Cookie?
  Cookie adalah sebuah cara untuk menyimpan data di browser. Cookie akan menyimpan data di browser dan data tersebut akan tetap ada meskipun browser ditutup.
- ### Apa perbedaan Web Storage dan Cookie?
  Perbedaan antara web storage dan cookie adalah web storage menyimpan data dalam bentuk key value, sedangkan cookie menyimpan data dalam bentuk string. Web storage hanya dapat menyimpan data dalam bentuk string, sedangkan cookie dapat menyimpan data dalam bentuk string, number, dan boolean. Web storage memiliki ukuran yang lebih besar dibandingkan cookie. Web storage memiliki waktu expired yang dapat diatur, sedangkan cookie memiliki waktu expired yang tidak dapat diatur. Web storage dapat diakses menggunakan javascript, sedangkan cookie tidak dapat diakses menggunakan javascript.
