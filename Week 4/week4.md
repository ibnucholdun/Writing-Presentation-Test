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

- ### Async Await

  Async Await adalah cara untuk menulis kode asynchronous yang lebih mudah dibaca dan ditulis. Async Await merupakan syntactic sugar dari Promise. Async Await memungkinkan kita untuk menulis kode asynchronous seperti kode synchronous. Async Await sama seperti Promise, hanya saja Async Await lebih mudah dibaca dan ditulis.

  - #### Contoh penggunaan Async Await

    ```javascript
    async function getData() {
      const response = await fetch(
        "https://jsonplaceholder.typicode.com/users"
      );
      const data = await response.json();
      console.log(data);
    }
    ```

    - `async function getData()` : membuat function getData() menjadi asynchronous
    - `await fetch("https://jsonplaceholder.typicode.com/users")` : menunggu fetch selesai untuk kemudian menjalankan baris selanjutnya
    - `await response.json()` : menunggu response.json() selesai untuk kemudian menjalankan baris selanjutnya

## Git dan Github Lanjutan

- ### Git Branch

  Branch adalah sebuah cabang dari repository yang berfungsi untuk mengembangkan fitur-fitur baru tanpa mengganggu branch utama. Branch utama disebut dengan branch master. Branch master adalah branch yang berisi kode yang sudah stabil dan siap untuk di deploy.

  - #### Membuat Branch

    ```bash
    git branch nama-branch
    ```

    - `git branch` : menampilkan semua branch yang ada
    - `git branch nama-branch` : membuat branch baru dengan nama nama-branch

  - #### Mengganti / Berpindah Branch

    ```bash
    git checkout nama-branch
    ```

    - `git checkout nama-branch` : mengganti branch ke nama-branch
    - `git checkout -b nama-branch` : membuat branch baru dengan nama nama-branch dan langsung mengganti branch ke nama-branch

  - #### Menggabungkan Branch

    ```bash
    git merge nama-branch
    ```

    - `git merge nama-branch` : menggabungkan branch nama-branch ke branch yang sedang aktif
    - `git merge nama-branch --no-ff` : menggabungkan branch nama-branch ke branch yang sedang aktif tanpa menghapus branch nama-branch
    - `git merge nama-branch --squash` : menggabungkan branch nama-branch ke branch yang sedang aktif dengan menggabungkan semua commit menjadi satu commit baru
    - `git merge nama-branch --abort` : membatalkan merge branch nama-branch ke branch yang sedang aktif dan mengembalikan branch yang sedang aktif ke kondisi sebelum merge
    - `git merge --abort` : membatalkan merge branch ke branch yang sedang aktif dan mengembalikan branch yang sedang aktif ke kondisi sebelum merge
    - `git merge --continue` : melanjutkan merge branch ke branch yang sedang aktif setelah mengatasi konflik
    - `git merge --no-commit` : menggabungkan branch ke branch yang sedang aktif tanpa membuat commit

  - #### Menghapus Branch

    ```bash
    git branch -d nama-branch
    ```

    - `git branch -d nama-branch` : menghapus branch nama-branch
    - `git branch -D nama-branch` : menghapus branch nama-branch tanpa memeriksa apakah branch nama-branch sudah di merge atau belum ke branch yang sedang aktif
    - `git branch -m nama-branch` : mengganti nama branch yang sedang aktif menjadi nama-branch baru
    - `git branch -M nama-branch` : mengganti nama branch yang sedang aktif menjadi nama-branch baru tanpa memeriksa apakah branch yang sedang aktif sudah di merge atau belum ke branch master

### Pull Request

Pull Request adalah sebuah fitur yang ada di Github yang berfungsi untuk meminta perubahan kode yang ada di branch yang sedang aktif untuk di gabungkan ke branch master. Pull Request juga dapat digunakan untuk meminta perubahan kode yang ada di branch yang sedang aktif untuk di gabungkan ke branch lainnya.

- #### Membuat Pull Request

  - Buka repository Github
  - Pilih branch yang akan digabungkan ke branch master
  - Klik tombol Pull Request
  - Isi judul dan deskripsi pull request
  - Klik tombol Create Pull Request

- #### Menerima Pull Request

  - Buka repository Github
  - Pilih tab Pull Request
  - Pilih pull request yang akan diterima
  - Klik tombol Merge Pull Request
  - Klik tombol Confirm Merge

- #### Mengatasi Konflik

  Konflik adalah sebuah permasalahan yang terjadi ketika ada perubahan kode yang dilakukan oleh dua orang yang berbeda pada satu baris kode yang sama. Untuk mengatasi konflik, kita harus mengatasi perubahan kode yang dilakukan oleh kedua orang tersebut.

  - #### Mengatasi Konflik di Github

    - Buka repository Github
    - Pilih tab Pull Request
    - Pilih pull request yang akan diterima
    - Klik tombol Resolve Conflicts
    - Atur perubahan kode yang dilakukan oleh kedua orang tersebut
    - Klik tombol Mark as Resolved
    - Klik tombol Commit Merge

  - #### Mengatasi Konflik di Local

    - Buka repository lokal
    - Lakukan perubahan kode yang dilakukan oleh kedua orang tersebut
    - Lakukan commit perubahan kode
    - Push perubahan kode ke Github

### Kolaborasi

Kolaborasi adalah sebuah fitur yang ada di Github yang berfungsi untuk mengundang orang lain untuk berkolaborasi dalam sebuah repository. Kolaborasi dapat dilakukan dengan mengundang orang lain untuk menjadi contributor pada repository yang kita miliki.

- #### Mengundang Orang Lain

  - Buka repository Github
  - Pilih tab Settings
  - Pilih tab Collaborators
  - Ketik username orang yang akan diundang
  - Klik tombol Add Collaborator

- #### Menerima Undangan
  - Buka repository Github
  - Klik tombol Fork
  - Pilih akun Github yang akan dijadikan tempat fork repository
  - Klik tombol Fork Repository

## Responsive Web Design

Responsive Web Design adalah sebuah teknik yang digunakan untuk membuat sebuah website agar dapat menyesuaikan tampilan website sesuai dengan ukuran layar yang digunakan. Responsive Web Design dapat dilakukan dengan menggunakan CSS Media Query.

- #### CSS Media Query

  CSS Media Query adalah sebuah aturan CSS yang digunakan untuk menentukan tampilan website sesuai dengan ukuran layar yang digunakan.

  ```css
  @media screen (max-width: 600px) {
    /* CSS disini akan dijalankan ketika ukuran layar maksimal 600px */
  }
  ```

  - `@media screen` : aturan CSS Media Query
  - `(max-width: 600px)` : aturan CSS Media Query yang digunakan untuk menentukan ukuran layar maksimal 600px

  ```css
  @media screen (min-width: 600px) {
    /* CSS disini akan dijalankan ketika ukuran layar minimal 600px */
  }
  ```

  - `@media screen` : aturan CSS Media Query
  - `(min-width: 600px)` : aturan CSS Media Query yang digunakan untuk menentukan ukuran layar minimal 600px

    ```css
    @media screen (min-width: 600px) and (max-width: 900px) {
      /* CSS disini akan dijalankan ketika ukuran layar minimal 600px dan maksimal 900px */
    }
    ```

    - `@media screen` : aturan CSS Media Query
    - `(min-width: 600px) and (max-width: 900px)` : aturan CSS Media Query yang digunakan untuk menentukan ukuran layar minimal 600px dan maksimal 900px

- #### Macam-macam satuan relatif yang digunakan untuk responsive

  - #### `em`

    Satuan `em` adalah satuan yang digunakan untuk mengukur ukuran font. Satuan `em` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `rem`

    Satuan `rem` adalah satuan yang digunakan untuk mengukur ukuran font. Satuan `rem` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vw`

    Satuan `vw` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vw` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vh`

    Satuan `vh` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vh` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vmin`

    Satuan `vmin` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vmin` merupakan satuan yang paling umum digunakan untuk responsive.

  - #### `vmax`

    Satuan `vmax` adalah satuan yang digunakan untuk mengukur ukuran layar. Satuan `vmax` merupakan satuan yang paling umum digunakan untuk responsive.

## Bootstrap 5

Bootstrap 5 adalah sebuah framework CSS yang digunakan untuk mempermudah dalam membuat tampilan website. Bootstrap 5 dapat digunakan untuk membuat tampilan website yang responsive.

- ### Menggunakan Bootstrap 5

  - #### Menggunakan CDN

    Menggunakan CDN adalah cara yang paling mudah untuk menggunakan Bootstrap 5. CDN adalah sebuah jaringan yang berfungsi untuk menyediakan file-file yang dibutuhkan oleh website.

    ```html
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css"
      integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1"
      crossorigin="anonymous"
    />
    ```

- ### Layout Bootstrap 5

  - #### Container

    Container adalah sebuah elemen yang berfungsi untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="container">
      <!-- Isi disini -->
    </div>
    ```

  - #### Row

    Row adalah sebuah elemen yang berfungsi untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="row">
      <!-- Isi disini -->
    </div>
    ```

  - #### Column

    Column adalah sebuah elemen yang berfungsi untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="col">
      <!-- Isi disini -->
    </div>
    ```

- ### Breakpoint

  - #### xs
    Breakpoint `xs` adalah breakpoint yang digunakan untuk ukuran layar minimal 0px.
  - #### sm
    Breakpoint `sm` adalah breakpoint yang digunakan untuk ukuran layar minimal 576px.
  - #### md
    Breakpoint `md` adalah breakpoint yang digunakan untuk ukuran layar minimal 768px.
  - #### lg
    Breakpoint `lg` adalah breakpoint yang digunakan untuk ukuran layar minimal 992px.
  - #### xl
    Breakpoint `xl` adalah breakpoint yang digunakan untuk ukuran layar minimal 1200px.
  - #### xxl
    Breakpoint `xxl` adalah breakpoint yang digunakan untuk ukuran layar minimal 1400px.

- ### Grid System
  - #### Grid System 1

    Grid System 1 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="container">
      <div class="row">
        <div class="col">
          <!-- Isi disini -->
        </div>
        <div class="col">
          <!-- Isi disini -->
        </div>
        <div class="col">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```

  - #### Grid System 2

    Grid System 2 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="container">
      <div class="row">
        <div class="col-4">
          <!-- Isi disini -->
        </div>
        <div class="col-4">
          <!-- Isi disini -->
        </div>
        <div class="col-4">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```

  - #### Grid System 3

    Grid System 3 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="container">
      <div class="row">
        <div class="col-6">
          <!-- Isi disini -->
        </div>
        <div class="col-6">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```

  - #### Grid System 4

    Grid System 4 adalah sebuah sistem yang digunakan untuk mengatur tampilan website agar terlihat rapi.

    ```html
    <div class="container">
      <div class="row">
        <div class="col-8">
          <!-- Isi disini -->
        </div>
        <div class="col-4">
          <!-- Isi disini -->
        </div>
      </div>
    </div>
    ```
