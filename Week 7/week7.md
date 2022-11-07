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

## State Management - React Redux

## State Management - React Thunk
