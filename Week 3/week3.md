# <p align="center">Summary Writing Week 2</p>

## Table of contents

- [Javascript Intermediate - Array dan Multidimensional Array](#javascript-intermediate---array-dan-multidimensional-array)
- [Javascript Intermediate - Object](#javascript-intermediate---object)
- [Javascript Intermediate - Recursive dan Import Export Module](#javascript-intermediate---recursive-dan-import-export-module)
- [Javascript Intermediate - Asynchronous](#javascript-intermediate---asynchronous)

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

## Javascript Intermediate - Recursive dan Import Export Module

## Javascript Intermediate - Asynchronous
