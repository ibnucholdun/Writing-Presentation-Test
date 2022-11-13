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

React Context dengan `useReducer` adalah sebuah fitur yang memungkinkan kita untuk melakukan _data sharing_ antar komponen tanpa harus melewati _props_ secara langsung. React Context dengan `useReducer` dapat digunakan untuk menggantikan Redux, namun tidak disarankan untuk digunakan pada skala besar. 

- ### Membuat Context dengan useReducer
  
    Untuk membuat sebuah Context dengan `useReducer`, kita dapat menggunakan `React.createContext()`.
  
    ```jsx
    import React from 'react';
  
    const UserContext = React.createContext();
    ```
  
    Pada contoh di atas, kita telah membuat sebuah Context bernama `UserContext`. Context ini dapat digunakan untuk menyimpan data yang akan digunakan oleh komponen-komponen yang berada di dalamnya.

- ### Menggunakan Context dengan useReducer

  Untuk menggunakan Context dengan `useReducer`, kita dapat menggunakan `Context.Provider` dan `useContext`.

  ```jsx
  import React, { useContext } from 'react';
  import UserContext from './UserContext';

  const User = () => {
    const { user, setUser } = useContext(UserContext);

    return (
      <div>
        <h1>{user.name}</h1>
        <button onClick={() => setUser({ name: 'John Doe' })}>
          Change User
        </button>
      </div>
    );
  };

  export default User;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `User` yang akan menampilkan data user yang disimpan di Context. Komponen ini akan menggunakan `useContext` untuk mengakses data yang disimpan di Context.

  ```jsx
  import React, { useReducer } from 'react';
  import UserContext from './UserContext';
  import User from './User';

  const initialState = { name: 'John Doe' };

  const reducer = (state, action) => {
    switch (action.type) {
      case 'CHANGE_USER':
        return { name: 'John Doe' };
      default:
        return state;
    }
  };

  const App = () => {
    const [user, dispatch] = useReducer(reducer, initialState);

    return (
      <UserContext.Provider value={{ user, dispatch }}>
        <User />
      </UserContext.Provider>
    );
  };

  export default App;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `App` yang akan menyediakan data user yang disimpan di Context. Komponen ini akan menggunakan `useReducer` untuk menyediakan data yang disimpan di Context.

  ```jsx
  import React from 'react';
  import App from './App';

  const Root = () => {
    return <App />;
  };

  export default Root;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `Root` yang akan menggunakan Context. Komponen ini akan menggunakan `useContext` untuk mengakses data yang disimpan di Context.

  ```jsx
  import React from 'react';
  import Root from './Root';

  const index = () => {
    return <Root />;
  };

  export default index;
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `index` yang akan menggunakan Context. Komponen ini akan menggunakan `useContext` untuk mengakses data yang disimpan di Context.

## React Testing (jest & RTL)

React Testing adalah sebuah fitur yang memungkinkan kita untuk melakukan _testing_ pada komponen-komponen React. React Testing dapat digunakan untuk menguji komponen-komponen React secara _unit testing_ dan _integration testing_. react testing dapat menggunakan `jest` dan `react testing library`. Testing dapat dilakukan dengan menggunakan metode TDD (Test Driven Development)

TDD atau Test Driven Development adalah sebuah metode pengembangan perangkat lunak yang memungkinkan kita untuk melakukan _testing_ terlebih dahulu sebelum melakukan _coding_. TDD memungkinkan kita untuk melakukan _testing_ terhadap komponen-komponen React dengan menggunakan metode `describe`, `it`, `expect`, dan `beforeEach`.

- ### React testing menggunakan framework jest

  Untuk melakukan _testing_ pada komponen-komponen React, kita dapat menggunakan framework `jest`. Untuk melakukan _testing_ pada komponen-komponen React, kita dapat menggunakan metode `describe`, `it`, `expect`, dan `beforeEach`.

  ```jsx
  import React from 'react';
  import { render, screen } from '@testing-library/react';
  import App from './App';

  describe('App', () => {
    beforeEach(() => {
      render(<App />);
    });

    it('should render App', () => {
      expect(screen.getByText('Hello World')).toBeInTheDocument();
    });
  });
  ```

  Pada contoh di atas, kita telah membuat sebuah komponen bernama `App` yang akan melakukan _testing_ terhadap komponen `App`. Komponen ini akan menggunakan metode `describe`, `it`, `expect`, dan `beforeEach` untuk melakukan _testing_ terhadap komponen `App`.

- ### React testing menggunakan react testing library
  
    Untuk melakukan _testing_ pada komponen React menggunakan `react testing library`, kita dapat menggunakan `render()` untuk melakukan _rendering_ pada komponen React.
    
    ```jsx
    import React from 'react';
    import { render, screen } from '@testing-library/react';
    import App from './App';
    
    test('renders learn react link', () => {
      render(<App />);
      const linkElement = screen.getByText(/learn react/i);
      expect(linkElement).toBeInTheDocument();
    });
    ```
    
    Pada contoh di atas, kita telah membuat sebuah _test case_ yang akan melakukan _testing_ pada komponen `App`. Komponen ini akan melakukan _rendering_ pada komponen `App` dan melakukan _assertion_ pada komponen `App` dengan menggunakan `render()`.

