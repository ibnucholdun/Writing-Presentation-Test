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

## Bootstrap 5
