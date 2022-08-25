## Apa itu Application?​

Aplikasi adalah perangkat lunak yang yang berisi fitur fitur yang dapat digunakan untuk keperluan tertentu

## Pada sesi ini kita akan mencoba untuk membuat beberapa aplikasi sederhana berbasis NodeJs, Golang & Python.

## Node.js

NodeJs adalah runtime untuk lingkungan JavaScript di luar peramban web yang dibangun di atas mesin JavaScript V8.

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```
![image](https://user-images.githubusercontent.com/78194305/186712000-1ad7cb24-da6e-4cc8-a550-26d37213f1a1.png)

nvm merupakan singkatan dari Node Version Manager. nvm adalah sebuah program yang akan membantu kita untuk menggunakan lebih dari satu versi Nodejs di dalam satu komputer.


```
nvm install 16
```

![image](https://user-images.githubusercontent.com/78194305/186712747-04c090ab-3646-43f3-b7b3-c3c27cb2c2e2.png)

Jika tahapan di atas sudah kalian lakukan, maka kalian sudah berhasil untuk melakukan instalasi node.js. Untuk melakukan pengecekan kalian bisa menggunakan perintah di bawah ini.

```
node -v
```
```
npm -v
```
![image](https://user-images.githubusercontent.com/78194305/186713132-88ea189a-fe0d-495e-be5b-d041680cca08.png)

Selanjutnya kita akan menjalankan perintah npm init gunanya untuk mengisiasi project, Hasil dari kalian menjalankan perintah akan membuat file baru dengan nama package.json, package.json ini berisikan isi informasi dari aplikasi yang akan kalian buat.

```
npm init -y
```
![image](https://user-images.githubusercontent.com/78194305/186713460-51430607-fa47-48e8-bfee-eff965082431.png)

Selanjutnya kita akan menginstall Express JS. Express JS adalah framework dari NodeJS yang dirancang secara fleksibel dan sederhana untuk membantu tahap pengembangan aplikasi back end. Menginstall express js dapat dilakukan menggunakan NPM dengan perintah berikut:

```
npm install express —-save
```

![image](https://user-images.githubusercontent.com/78194305/186713951-7f022c6e-a083-49e2-b4f6-c54cb54bd1ba.png)

Jika sudah buat file dengan nama index.js, lalu masukan script dibawah ini

```
nano index.js
```

![image](https://user-images.githubusercontent.com/78194305/186714327-ba00af43-b9fb-4445-9929-9c20dd455a44.png)

```
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```

![image](https://user-images.githubusercontent.com/78194305/186714747-02e7e726-4830-4389-bf28-97d6a6ff81bc.png)

Untuk save dan keluar kalian bisa tekan Ctrl+O > enter > Ctrl + X

sekarang kita akan coba untuk menjalankan aplikasi sederhana yang sudah kita buat. Untuk menjalankan dapat menggunakan perintah berikut ini.

```
node index.js
```

![image](https://user-images.githubusercontent.com/78194305/186716554-7d042cdf-319d-461c-b391-2d8539c4a8e6.png)


Sekarang coba 
akses web browser kalian setelah itu kalian coba akses dengan localhost:3000 / ip server :3000 contoh 192.168.100.20:3000

![image](https://user-images.githubusercontent.com/78194305/186716837-d6d9b650-f02c-45b5-9c4d-2ecdd97ca740.png)

## Golang Go

Go adalah bahasa pemrograman yang dibuat di Google pada tahun 2009 oleh Robert Griesemer, Rob Pike, dan Ken Thompson. bahasa pemrograman sumber terbuka yang mudah, sederhana, efisien.

```
wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su
```

![image](https://user-images.githubusercontent.com/78194305/186717158-b6a103e4-e5f3-4044-99df-8ac36f3b1456.png)

```
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit
```

![image](https://user-images.githubusercontent.com/78194305/186717975-341ad407-ddfa-4bc8-a0dc-f6ddffc431b2.png)

Selanjutnya masukkan path go pada .bashrc

```
sudo nano .bashrc
export PATH=$PATH:/usr/local/go/bin
```
![image](https://user-images.githubusercontent.com/78194305/186718660-4133288d-79b1-4ba4-a275-ae0e156eb76d.png)

Jika sudah sekarang dapat verifikasi go dengan cara berikut.

```
go version
```

![image](https://user-images.githubusercontent.com/78194305/186719024-d4fc003d-e9c2-4de1-80c7-72e4c5223fec.png)

Sekarang kita akan membuat aplikasi sederhana menggunakan go. Kalian dapat menjalankan beberapa perintah berikut ini.
Buat sebuah file dengan nama index.go.

```
nano index.go
```
masukkan skrip

```
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
```

![image](https://user-images.githubusercontent.com/78194305/186719455-da78adad-360b-404d-aacd-b48a0d102900.png)

```
go run index.go
```
![image](https://user-images.githubusercontent.com/78194305/186723441-3f0dfa5f-e2b6-418f-a620-6a711c3ae09d.png)

## Python
Python adalah Python merupakan bahasa pemrograman tingkat tinggi yang diracik oleh Guido van Rossum

Pertama-tama kita harus install terlebih dahulu Pyhton3. Untuk instalasi ikuti beberapa perintah di bawah ini.

```
sudo apt update; sudo apt upgrade
```

![image](https://user-images.githubusercontent.com/78194305/186723855-9a17b729-3c0e-4971-b370-06477b1c0a32.png)

Python3 sudah ada secara default, untuk melakukan pengecekan jalankan perintah berikut.

```
python3 — version
```
![image](https://user-images.githubusercontent.com/78194305/186724431-3b37d104-9f40-4c01-9466-073845ca541a.png)

Sekarang kita install package manager dari python3. Kalian dapat menggunakan perintah berikut ini.

![image](https://user-images.githubusercontent.com/78194305/186724606-aa9965cc-a993-4757-9d18-44ca1c997b27.png)

```
pip install flask
```
![image](https://user-images.githubusercontent.com/78194305/186724911-d82d7ddd-0a0c-4591-b647-04d3cbaf1e5f.png)

PIP adalah sebuah package management system yang biasa digunakan untuk mengatur dan menginstall package yang berisi modul-modul Python.

Sekarang kita akan membuat aplikasi sederhana menggunakan Python3.

```
nano index.py
```
![image](https://user-images.githubusercontent.com/78194305/186725145-46a62adb-0cb8-4e8d-a262-6387327c226f.png)

```
from flask import Flask
app = Flask(__name__)
@app.route(“/”)
def helloworld():
return “Hello World”
if __name__ == “__main__”:
app.run()
```

![image](https://user-images.githubusercontent.com/78194305/186725340-c33673b8-3aac-4394-b4ee-8c2d63b48171.png)

Jika sudah sekarang jalankan aplikasi dengan menggunakan perintah berikut ini.

```
python3 index.py
```
![image](https://user-images.githubusercontent.com/78194305/186725690-87497baf-a8e8-47fc-ae14-e5f489e4e783.png)

## Konfigurasi dengan PM2 dandapat di akses melalui web browser
Menginstal PM2 sangat sederhana, dan dapat dilakukan dalam satu baris kode.

```
npm install -g pm2
```
![image](https://user-images.githubusercontent.com/78194305/186726211-61e0c48d-27da-4aee-a9d9-1ac31705671d.png)

```
pm2 list
```
![image](https://user-images.githubusercontent.com/78194305/186726321-9a933e04-94be-4319-9867-5629e9a69b7f.png)

Pada pm2 kita dibutuhkan membuat ecosystem.config.js dan pakai perintah berikut.

```
pm2 ecosystem
```
![image](https://user-images.githubusercontent.com/78194305/186726537-d20beb63-c6d0-4277-bd20-f3179f2835cf.png)

![image](https://user-images.githubusercontent.com/78194305/186727205-6739b20c-53bc-4c65-bb59-7573f085cda7.png)


lalu untuk memulaikan PM2 kalian ketikan

```
pm2 start node.js
```

![image](https://user-images.githubusercontent.com/78194305/186727439-7f489136-fd81-4332-af98-613d63b5b6ab.png)

```
pm2 start python.py --interpreter python3
```

```
pm2 start golang.go
```











