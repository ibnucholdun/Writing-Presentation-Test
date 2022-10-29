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
        <h1>Hello, Ibnu Choldun</h1>
      </div>
    );
  };

  export default App;
  ```

## React.js Basic - Props dan State

### Props

Props adalah sebuah object yang berisi data yang akan digunakan pada komponen. Props dapat diterima oleh komponen sebagai parameter. Props dapat diterima oleh functional component maupun class component. Props dapat digunakan pada JSX yang di return oleh functional component maupun class component. Props dapat digunakan untuk mengirimkan data dari parent component ke child component. props dapat ditulis meggunakan decturcturing object.

- contoh props

  ```javascript
  import React from "react";

  const App = (props) => {
    return (
      <div>
        <h1>Hello, {props.name}</h1>
      </div>
    );
  };

  export default App;
  ```

  ```javascript
  import React from "react";
  import App from "./App";

  const App = () => {
    return (
      <div>
        <App name="Ibnu Choldun" />
      </div>
    );
  };
  ```

- contoh props menggunakan decturcturing object

  ```javascript
  import React from "react";

  const App = ({ name }) => {
    return (
      <div>
        <h1>Hello, {name}</h1>
      </div>
    );
  };

  export default App;
  ```

  ```javascript
  import React from "react";
  import App from "./App";

  const App = () => {
    return (
      <div>
        <App name="Ibnu Choldun" />
      </div>
    );
  };
  ```

### State

State adalah sebuah object yang berisi data yang akan digunakan pada komponen. State dapat diterima oleh komponen sebagai parameter. State dapat diterima oleh class component. State dapat digunakan pada JSX yang di return oleh class component. State dapat digunakan untuk mengirimkan data dari parent component ke child component. State dapat ditulis meggunakan decturcturing object. State juga dapat digunakan pada functional component menggunakan hooks. State dapat digunakan untuk mengubah data pada komponen.

- contoh state

  ```javascript
  import React, { Component } from "react";

  class App extends Component {
    state = {
      name: "Ibnu Choldun",
    };

    render() {
      return (
        <div>
          <h1>Hello, {this.state.name}</h1>
        </div>
      );
    }
  }

  export default App;
  ```

- contoh state menggunakan decturcturing object

  ```javascript
  import React, { Component } from "react";

  class App extends Component {
    state = {
      name: "Ibnu Choldun",
    };

    render() {
      const { name } = this.state;
      return (
        <div>
          <h1>Hello, {name}</h1>
        </div>
      );
    }
  }

  export default App;
  ```

- contoh state menggunakan hooks

  ```javascript
  import React, { useState } from "react";

  const App = () => {
    const [name, setName] = useState("Ibnu Choldun");

    return (
      <div>
        <h1>Hello, {name}</h1>
      </div>
    );
  };

  export default App;
  ```

## React.js Basic - Styling

### Styling pada React.js

Styling pada React.js dapat dilakukan dengan menggunakan CSS, CSS Module, CSS in JS, dan Styled Component. Styling pada React.js dapat dilakukan dengan menggunakan inline styling, external styling, dan internal styling. Styling pada React.js dapat dilakukan dengan menggunakan class styling dan id styling. Styling pada React.js dapat dilakukan dengan menggunakan camelCase styling dan kebab-case styling. dan pemberian class styling pada React.js dapat dilakukan dengan menggunakan className.

- contoh styling pada React.js

  ```javascript
  import React from "react";

  const App = () => {
    return (
      <div>
        <h1 style={{ color: "red" }}>Hello, Ibnu Choldun</h1>
      </div>
    );
  };

  export default App;
  ```

  ```javascript
  import React from "react";
  import "./App.css";

  const App = () => {
    return (
      <div>
        <h1 className="text-red">Hello, Ibnu Choldun</h1>
      </div>
    );
  };

  export default App;
  ```

## React.js Basic - Handling Event

### Handling Event pada React.js

Handling event pada React.js dapat dilakukan dengan menggunakan event listener. Handling event pada React.js dapat dilakukan dengan menggunakan event listener pada JSX. Handling event pada React.js dapat dilakukan dengan menggunakan event listener pada class component dan functional component menggunakan hooks. jenis event pada react js adalah onClick, onChange, onSubmit, onKeyPress dan lain-lain.

- contoh handling event pada React.js

  ```javascript
  import React from "react";

  const App = () => {
    const handleClick = () => {
      console.log("Hello, Ibnu Choldun");
    };

    return (
      <div>
        <button onClick={handleClick}>Click Me</button>
      </div>
    );
  };

  export default App;
  ```

  ```javascript
  import React, { Component } from "react";

  class App extends Component {
    handleClick = () => {
      console.log("Hello, Ibnu Choldun");
    };

    render() {
      return (
        <div>
          <button onClick={this.handleClick}>Click Me</button>
        </div>
      );
    }
  }

  export default App;
  ```

- contoh handling event pada React.js menggunakan hooks

  ```javascript
  import React, { useState } from "react";

  const App = () => {
    const [name, setName] = useState("Ibnu Choldun");

    return (
      <div>
        <button onClick={() => setName("Ibnu Choldun 15")}>Click Me</button>
      </div>
    );
  };
  ```

## React.js Basic - Conditional Rendering

### Conditional Rendering pada React.js

- contoh conditional rendering pada ReactJs menggunakan if else

  ```javascript
  import React from "react";

  const App = () => {
    const name = "Ibnu Choldun";

    if (name === "Ibnu Choldun") {
      return <h1>Hello, Ibnu Choldun</h1>;
    } else {
      return <h1>Hello, Guest</h1>;
    }
  };

  export default App;
  ```

- contoh conditional rendering pada ReactJs menggunakan ternary operator

  ```javascript
  import React from "react";

  const App = () => {
    const name = "Ibnu Choldun";

    return (
      <div>
        {name === "Ibnu Choldun" ? (
          <h1>Hello, Ibnu Choldun</h1>
        ) : (
          <h1>Hello, Guest</h1>
        )}
      </div>
    );
  };

  export default App;
  ```

## React.js Basic - Life Cycle Method

### Life Cycle Method pada React.js

Life cycle method pada React.js adalah method yang akan dijalankan pada saat tertentu. Life cycle method pada React.js adalah method yang akan dijalankan pada saat mounting, updating, dan unmounting. Life cycle method pada React.js adalah method yang akan dijalankan pada saat mounting yaitu constructor, getDerivedStateFromProps, render, componentDidMount, dan getSnapshotBeforeUpdate. Life cycle method pada React.js adalah method yang akan dijalankan pada saat updating yaitu getDerivedStateFromProps, shouldComponentUpdate, render, getSnapshotBeforeUpdate, dan componentDidUpdate. Life cycle method pada React.js adalah method yang akan dijalankan pada saat unmounting yaitu componentWillUnmount.

- contoh life cycle method pada React.js

  ```javascript
  import React, { Component } from "react";

  class App extends Component {
    constructor(props) {
      super(props);
      console.log("constructor");
    }

    componentDidMount() {
      console.log("componentDidMount");
    }

    componentDidUpdate() {
      console.log("componentDidUpdate");
    }

    componentWillUnmount() {
      console.log("componentWillUnmount");
    }

    render() {
      console.log("render");
      return <h1>Hello, Ibnu Choldun</h1>;
    }
  }

  export default App;
  ```

## React.js Basic - Hooks

## React.js Basic - Forms
