# Praktikum Pertemuan 5

## Requirement Tools/Software
1. [Git Bash](https://git-scm.com/downloads)
2. Text Editor (notepad / notepad++ / dsb.)

## Git untuk Individu

### Praktik
1. Pastikan Sudah Mendaftarkan akun anda pada http://github.com
2. Configurasi pada device (komputer/laptop)

    Bagian ini digunakan jika kita hanya berurusan dengan diri kita sendiri. Pertama kita inisialisasi user dengan perintah berikut, buka terlebih dahulu gitbash yang telah terinstall:
    ```
    cd ~
    git config --global user.name "usernameanda"
    git config --global user.email "email@anda.sendiri"
    cat .gitconfig
    ```
    `Amati Output pada gitbash`
3. Inisialisasi Git pada suatu project/folder tuliskan perintah dibawah ini :
   
    ```
    mkdir nim-anda
    cd nim-anda
    git init
    touch coba.txt
    ls -la
    git add .
    ls -la ./git
    ```
    `Amati Output pada gitbash`
4. Setelah itu lakukan commit. Commit adalah aktivitas untuk menuliskan atau menggabungkan perubahan-perubahan yang telah dilakukan ke dalam repository. Istilah lain untuk commit adalah check-in atau ci), dengan perintah :
   
    ```
    git commit -m "coba commit"
    ```
    `Amati Output pada gitbash`
5. Perintah-perintah berikut ini akan banyak digunakan pada saat kita bekerja dengan source code. **Perintah “git status” dan “git diff“**

    - Perintah “**git status**” digunakan untuk melihat status dari working copy. Jika tidak ada perubahan, hasilnya adalah sebagai berikut:
        ```
        git status
        ```
        `Amati Output pada gitbash`
    - Lakukan perubahan pada file coba.txt menggunakan text editor lalu simpan, kita bisa melihat perubahan yang kita lakukan terhadap source code dengan perintah “**git diff**”. Berikut adalah hasilnya:
        ```
        git diff
        ```
        `Amati Output pada gitbash`
6. Lakukan Commit dengan perintah :
   ```
   git commit -m 'ubah file coba.txt'
   ```
   `Amati Output pada gitbash`
7. **Perintah “git add” dan “git rm”** 
   - Jika kita menambahkan file atau direktori ke proyek kita, kita bisa menggunakan “**git add .**” .Ikuti perintah berikut:
        ```
        touch README.md
        git status
        git add README.md
        git status
        git commit -m 'tambah file README.md'
        git status
        ```
        `Amati Output pada gitbash`
   - Jika ingin menghapus pelacakan git, gunakan “**git rm**”

        `Opsional (tidak dikerjakan)`

8. Perintah “**git log**”

   - Perintah ini digunakan untuk menampilkan catatan-catatan (logs) terhadap apa yang telah dilakukan terhadap source code:
   - Jika memerlukan lebih rinci lagi, bisa menggunakan “**git log –stat –summary**”.
  
        `Opsional (tidak harus dikerjakan)`

## Git Kolaborasi
Kolaborasi akan melibatkan lebih dari satu developer. Pada dasarnya ada beberapa
perintah yang sering digunakan pada saat berkolaborasi.

**Perintah “git clone“** 

Terdapat 2 metode untuk melakukan clone pada suatu repository yaitu dengan protocol **SSH** dan **HTTPS**
- Perintah ini digunakan untuk mengambil repository pada protocol **HTTPS**. Contoh jika akan mengambil dari remote host berikut ini adalah sebagai berikut:

    ```
    cd ~
    git clone https://github.com/G9Insane/Praktikum-SQA
    ls -la
    ```
    `Amati Output pada gitbash`

    ### **`Terkait Tugas`**

- Perintah ini digunakan untuk mengambil repository pada protocol **SSH**. 
Sebelum Melakukan clone kita harus membuat ssh key pada device yang kita gunakan (laptop/komputer). Ikuti instruksi dibawah ini :
    - Buka **Git Bash**. Tuliskan perintah berikut :
        ```
        ssh-keygen -t rsa -b 4096 -C "email@anda.com"
        ```
        **Output :**
        `Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]`
    - ***Tekan Enter*** pada keyboard untuk default directory ssh-key anda
      **Output :**
      `Enter passphrase (empty for no passphrase): [Type a passphrase]>`

  - **Jika tanpa password, langsung saja *Tekan Enter***
  
    **Output :**
    `Enter same passphrase again: [Type passphrase again]`

  - **Lalu konfirmasi dengan *Tekan Enter* kembali**
  - Selanjutnya copy isi file ssh-key dengan perintah :
    ```
    cat < ~/.ssh/id_rsa.pub
    ```
- Lalu Buka **https://github.com**
    - klik ikon pada pojok kanan atas
    - pilih menu **Settings**
    - pilih menu pada bagian kiri **SSH and GPG keys**
    - klik tombol **New SSH key**
    - Isi Form title **Bebas Sesuai Selera**
    - Paste pada kolom key (*Ctrl+V*)
    - Klik Add SSH key
    - Clone project pada protocol **SSH** dengan perintah

    ```
    cd ~
    git clone git@github.com:G9Insane/Praktikum-SQA.git
    ls -la
    ```
    `Amati Output pada gitbash`
## **Bingung?** tulis bagian yang ingin ditanyakan  [disini](https://github.com/G9Insane/Praktikum-SQA/issues/new)
[Next Latihan](https://github.com/G9Insane/Praktikum-SQA/tree/master/Pertemuan-5/Latihan-5.md)