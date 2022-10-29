# <p align="center">Summary Writing Week 6</p>

## Table of contents

- [React.js Basic - Intro to React.js, Virtual DOM, and JSX](#reactjs-basic---intro-to-reactjs-virtual-dom-and-jsx)
- [React.js Basic - Functional Component](#reactjs-basic---functional-component)
- [React.js Basic - Props dan State](#reactjs-basic---props-dan-state)
- [React.js Basic - Styling](#reactjs-basic---styling)
- [React.js Basic - Handling Event](#reactjs-basic---handling-event)
- [React.js Basic - Conditional Rendering](#reactjs-basic---conditional-rendering)
- [React.js Basic - Life Cycle Method](#reactjs-basic---life-cycle-method)
- [React.js Basic - Hooks](#reactjs-basic---hooks)
- [React.js Basic - Forms](#reactjs-basic---forms)

## React.js Basic - Intro to React.js, Virtual DOM, and JSX

### React.js

React.js adalah sebuah library javascript yang dibuat oleh Facebook untuk membangun user interface. React.js memanfaatkan konsep komponen untuk membangun user interface. React.js juga memanfaatkan virtual DOM untuk mempercepat proses rendering.

### Virtual DOM

Virtual DOM adalah sebuah konsep yang digunakan untuk mempercepat proses rendering. Virtual DOM adalah sebuah representasi dari DOM yang ada di browser. Virtual DOM dibuat menggunakan javascript. Virtual DOM dibuat untuk mempercepat proses rendering karena proses rendering pada DOM yang ada di browser membutuhkan waktu yang cukup lama. Virtual DOM dibuat untuk membandingkan perubahan yang terjadi pada DOM yang ada di browser dengan virtual DOM. Jika terdapat perubahan pada DOM yang ada di browser, maka virtual DOM akan melakukan perubahan pada virtual DOM sesuai dengan perubahan yang terjadi pada DOM yang ada di browser. Setelah itu, virtual DOM akan melakukan perubahan pada DOM yang ada di browser sesuai dengan perubahan yang terjadi pada virtual DOM.

### JSX (Javascript XML)

JSX adalah sebuah sintaksis yang digunakan untuk membangun user interface pada React.js. JSX adalah sebuah sintaksis yang mirip dengan HTML. JSX dibuat menggunakan javascript. JSX dibuat untuk mempermudah proses pembuatan user interface pada React.js.

- contoh JSX menggunakan functional component

  ```javascript
  import React from "react";

  const App = () => {
    return (
      <div>
        <h1>Hello World</h1>
      </div>
    );
  };

  export default App;
  ```

## React.js Basic - Functional Component

### Functional Component

Functional component adalah sebuah komponen yang dibuat menggunakan function baik menggunakan function declaration, function expression maupun arrow function. Pada functional component menjalankan proses rendering menggunakan return statement yang mengembalikan sebuah JSX. pada functional component dapat menerima props sebagai parameter yang kemudian dapat digunakan pada JSX yang di return.

- contoh functional component

  ```javascript
  import React from "react";

  const App = () => {
    return (
      <div>
        <h1>Hello, Ibnu CHolduhn</h1>
      </div>
    );
  };

  export default App;
  ```

## React.js Basic - Props dan State

## React.js Basic - Styling

## React.js Basic - Handling Event

## React.js Basic - Conditional Rendering

## React.js Basic - Life Cycle Method

## React.js Basic - Hooks

## React.js Basic - Forms
