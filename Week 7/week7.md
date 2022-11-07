# <p align="center">Summary Writing Week 7</p>

## Table of contents

- [React.js Lanjutan - PropTypes](#reactjs-lanjutan---proptypes)
- [React Router 6](#react-router-6)
- [State Management - React Redux ](#state-management---react-redux)
- [State Management - React Thunk](#state-management---react-thunk)

## React.js Lanjutan - PropTypes

PropTypes adalah salah satu fitur yang ada di React.js yang digunakan untuk memvalidasi tipe data props yang dikirimkan dari komponen induk ke komponen anak. Jika tipe data yang dikirimkan tidak sesuai dengan yang diharapkan, maka akan muncul pesan error di console. Cara penggunaannya cukup mudah, cukup import PropTypes dari package react lalu tambahkan properti propTypes pada komponen yang akan di validasi.

```javascript
import React from 'react';
import PropTypes from 'prop-types';

const MyComponent = (props) => {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  );
};

MyComponent.propTypes = {
  title: PropTypes.string,
  description: PropTypes.string,
};

export default MyComponent;
```

- proptypes untuk tipe data string

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.string,
  };
  ```

- proptypes untuk tipe data number

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.number,
  };
  ```

- proptypes untuk tipe data array

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.array,
  };
  ```

- proptypes untuk tipe data object

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.object,
  };
  ```

- proptypes untuk tipe data boolean

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.bool,
  };
  ```

- proptypes untuk tipe data function

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.func,
  };
  ```

- proptypes untuk multiple tipe data

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.oneOfType([PropTypes.string, PropTypes.number]),
  };
  ```

- proptypes untuk tipe data yang wajib diisi

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.string.isRequired,
  };
  ```

- proptypes array of object

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.arrayOf(
      PropTypes.shape({
        id: PropTypes.number,
        name: PropTypes.string,
      })
    ),
  };
  ```

- proptypes untuk array of string

  ```javascript
  MyComponent.propTypes = {
    title: PropTypes.arrayOf(PropTypes.string),
  };
  ```


## React Router 6

React Router adalah library yang digunakan untuk membuat routing di React.js. Routing adalah proses untuk mengatur alur navigasi di aplikasi web. React Router 6 merupakan versi terbaru dari React Router yang dirilis pada tanggal 18 Juni 2021. Pada versi terbaru ini, React Router 6 menghilangkan fitur yang sudah tidak digunakan lagi seperti Switch, Redirect, dan Link. Pada React Router 6, fitur tersebut digantikan dengan fitur baru yaitu Routes, Outlet, dan Link. Pada React Router 6, fitur Routes digunakan untuk mengatur alur navigasi, Outlet digunakan untuk menampilkan komponen sesuai dengan alur navigasi yang ditentukan, dan Link digunakan untuk membuat link navigasi. Berikut adalah contoh penggunaan Routes, Outlet, dan Link pada React Router 6.

```javascript
import React from 'react';
import { Routes, Route, Link } from 'react-router-dom';

const Home = () => {
  return (
    <div>
      <h1>Home</h1>
    </div>
  );
};

const About = () => {
  return (
    <div>
      <h1>About</h1>
    </div>
  );
};

const App = () => {
  return (
    <div>
      <nav>
        <ul>
          <li>
            <Link to="/">Home</Link>
          </li>
          <li>
            <Link to="about">About</Link>
          </li>
        </ul>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="about" element={<About />} />
      </Routes>
    </div>
  );
};

export default App;
```

- Dynamic Routing

  ```javascript
  import React from 'react';
  import { Routes, Route, Link } from 'react-router-dom';

  const Home = () => {
    return (
      <div>
        <h1>Home</h1>
      </div>
    );
  };

  const About = () => {
    return (
      <div>
        <h1>About</h1>
      </div>
    );
  };

  const Product = () => {
    return (
      <div>
        <h1>Product</h1>
      </div>
    );
  };

  const App = () => {
    return (
      <div>
        <nav>
          <ul>
            <li>
              <Link to="/">Home</Link>
            </li>
            <li>
              <Link to="about">About</Link>
            </li>
            <li>
              <Link to="product">Product</Link>
            </li>
          </ul>
        </nav>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="about" element={<About />} />
          <Route path="product" element={<Product />} />
        </Routes>
      </div>
    );
  };

  export default App;
  ```

- Nested Routing

  ```javascript
  import React from 'react';
  import { Routes, Route, Link } from 'react-router-dom';

  const Home = () => {
    return (
      <div>
        <h1>Home</h1>
      </div>
    );
  };

  const About = () => {
    return (
      <div>
        <h1>About</h1>
      </div>
    );
  };

  const Product = () => {
    return (
      <div>
        <h1>Product</h1>
      </div>
    );
  };

  const ProductDetail = () => {
    return (
      <div>
        <h1>Product Detail</h1>
      </div>
    );
  };

  const App = () => {
    return (
      <div>
        <nav>
          <ul>
            <li>
              <Link to="/">Home</Link>
            </li>
            <li>
              <Link to="about">About</Link>
            </li>
            <li>
              <Link to="product">Product</Link>
            </li>
          </ul>
        </nav>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="about" element={<About />} />
          <Route path="product" element={<Product />}>
            <Route path=":id" element={<ProductDetail />} />
          </Route>
        </Routes>
      </div>
    );
  };

  export default App;
  ```

## State Management - React Redux

## State Management - React Thunk
