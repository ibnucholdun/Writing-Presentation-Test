# <p align="center">Summary Writing Week 8</p>

## Table of contents

- [React Context](#react-context)
- [React Context with useReducer](#react-context-with-usereducer)
- [React Testing (jest & RTL)](#react-testing-jest--rtl)

## React Context

React Context adalah sebuah fitur yang memungkinkan kita untuk melakukan _data sharing_ antar komponen tanpa harus melewati _props_ secara langsung. React Context dapat digunakan untuk menggantikan Redux, namun tidak disarankan untuk digunakan pada skala besar.

- ### Membuat Context

  Untuk membuat sebuah Context, kita dapat menggunakan `React.createContext()`.

  ```jsx
  import React from 'react';

  const UserContext = React.createContext();
  ```

  Pada contoh di atas, kita telah membuat sebuah Context bernama `UserContext`. Context ini dapat digunakan untuk menyimpan data yang akan digunakan oleh komponen-komponen yang berada di dalamnya.

- ### Menggunakan Context

  Untuk menggunakan Context, kita dapat menggunakan `Context.Provider` dan `Context.Consumer`.

  ```jsx
  import React from 'react';
  import UserContext from './UserContext';

  const User = () => {
    return (
      <UserContext.Consumer>
        {({ user, setUser }) => (
          <div>
            <h1>{user.name}</h1>
            <button onClick={() => setUser({ name: 'John Doe' })}>
              Change User
            </button>
          </div>
        )}
      </UserContext.Consumer>
    );
  };

  export default User;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `User` yang akan menampilkan data user yang disimpan di Context. Komponen ini akan menggunakan `Context.Consumer` untuk mengakses data yang disimpan di Context.

  ```jsx
  import React, { useState } from 'react';
  import UserContext from './UserContext';
  import User from './User';

  const App = () => {
    const [user, setUser] = useState({ name: 'John Doe' });

    return (
      <UserContext.Provider value={{ user, setUser }}>
        <User />
      </UserContext.Provider>
    );
  };

  export default App;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `App` yang akan menyediakan data user yang disimpan di Context. Komponen ini akan menggunakan `Context.Provider` untuk menyediakan data yang disimpan di Context.

  ```jsx
  import React from 'react';
  import App from './App';

  const Root = () => {
    return <App />;
  };

  export default Root;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `Root` yang akan menggunakan Context. Komponen ini akan menggunakan `Context.Consumer` untuk mengakses data yang disimpan di Context.

  ```jsx
  import React from 'react';
  import Root from './Root';

  const index = () => {
    return <Root />;
  };

  export default index;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `index` yang akan menggunakan Context. Komponen ini akan menggunakan `Context.Consumer` untuk mengakses data yang disimpan di Context.

## React Context with useReducer

## React Testing (jest & RTL)

