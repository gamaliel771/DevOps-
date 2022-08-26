## Version Control System
![image](https://user-images.githubusercontent.com/78194305/186786125-88092836-03ca-45e1-9816-f4b7f2e71fc8.png)

Git merupakan software berbasis Version Control System (VCS) yang bertugas untuk mencatat perubahan seluruh file atau repository suatu project.

## Git Config

pertama yang harus kalian lakukan adalah menetapkan nama pengguna dan alamat email, untuk perintahnya kalian dapat menggunakan perintah dibawah ini.

```
git config --global user.name "your.github-user.name"
```
```
git config --global user.email "your.github-user.email"
```

Jika kalian sudah menjalankan perintah di atas, kalian bisa cek user.name dan user.email kalian sudah tepat atau belum dengan menggunakan perintah dibawah ini.

```
git config --list
```
![image](https://user-images.githubusercontent.com/78194305/186786870-18d7af58-d975-4ef8-806a-47aeb2011889.png)

## Membuat repository

Repository adalah suatu penyimpanan file project. dimana kamu bisa menyimpan apapun yang berkaitan dengan project kalian, seperti code, gambar, ataupun audio. repo sendiri bertempat di penyimpanan atau storage github atau repository local di komputer anda.

![Screenshot_20220826_064047](https://user-images.githubusercontent.com/78194305/186792306-f1216de9-9011-4be5-8344-82e55599e22a.png)

Copy yang sudah disediakan Github, jangan lupa untuk memilih bagian SSH karena kita menggunakan SSH untuk mengkoneksikan local kita dengan Github.

![Screenshot_20220826_064134](https://user-images.githubusercontent.com/78194305/186792345-fe45eb76-b355-4fb6-829f-22298b12e467.png)

![Screenshot_20220826_072935](https://user-images.githubusercontent.com/78194305/186792372-7f86e780-d251-4faa-bc55-d75983f715a7.png)

## Check remote
Untuk melihat remote yang kita gunakan kita bisa menggunakan perintah berikut:

```
git remote -v
```
![image](https://user-images.githubusercontent.com/78194305/186792503-7f9dab08-7133-480a-8f3d-0ab7706a28bb.png)

## Membuat 3 buah repository untuk masing-masing aplikasi (NodeJS, Python dan Go)



