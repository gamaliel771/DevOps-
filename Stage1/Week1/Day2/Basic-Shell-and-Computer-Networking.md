## Basic Shell and Computer Networking

![image](https://user-images.githubusercontent.com/78194305/186144056-e253bdbb-8f96-4d4b-a44f-64c980bde44c.png)

Jaringan Komputer adalah dua atau lebih perangkat komputer yang saling terhubung atau terkoneksi antara satu dengan yang lain

## berikut ini daftar daftar perintah linux yang membantu untuk memanagement linux server

## sudo
sudo adalah suatu perintah untuk memungkin kalian untuk menjalankan program sebagai pengguna lain.

```
sudo apt update; sudo apt upgrade
```
![image](https://user-images.githubusercontent.com/78194305/186145516-a921225b-94f9-4e29-92c2-03838071ce32.png)

## mkdir
mkdir adalah perintah untuk membuat suatu directory.

```
mkdir Gama
```
![image](https://user-images.githubusercontent.com/78194305/186146051-c686eba7-58a3-4a18-816c-fdfef513b635.png)

## ls 
ls adalah perintah untuk melihat list apa saja yang ada di directory.

```
ls
```
![image](https://user-images.githubusercontent.com/78194305/186146332-2ff7f83f-7df2-448f-bb5d-55a08ead959b.png)

## cd
cd adalah perintah untuk masuk ke dalam directory.

```
cd
```
![image](https://user-images.githubusercontent.com/78194305/186146640-7e6d33b9-8544-4c43-8a2f-bb928d32dd81.png)

## ls -la
ls -la adalah perintah untuk melihat semua list file dan directory yang ada serta menampilkan semua file maupun directory yang tersembunyi.

```
ls -la
```
![image](https://user-images.githubusercontent.com/78194305/186146996-85d80039-872f-49d4-8856-3db2aac653e5.png)

## cd ..
cd .. adalah perintah untuk keluar dari directory.

```
cd ...
```
![image](https://user-images.githubusercontent.com/78194305/186147279-5036bb0e-9f0d-44f9-a24e-e44de46f802c.png)

## touch
touch adalah perintah untuk membuat suatu file. Sebagai contoh coba kalian buat suatu file dengan nama index.html.

```
touch index.html
```
![image](https://user-images.githubusercontent.com/78194305/186147659-43bf1390-3e98-411a-87b6-a91a26d2f80d.png)

## mv
mv adalah sebuah perintah untuk me-rename nama file, tetapi juga dapat digunakan untuk memindahkan suatu file ke directory tertentu.

```
mv
```
![image](https://user-images.githubusercontent.com/78194305/186148210-e5218cfd-4835-4bf2-8f53-a4f0fa3c5dbc.png)
![image](https://user-images.githubusercontent.com/78194305/186148552-da798a13-3fff-4890-ac29-9a85dbd4e444.png)

## mengubah IP Server

![image](https://user-images.githubusercontent.com/78194305/186149580-8c6709ce-8229-4191-8988-ac8576e667f2.png)

Ip yang saya gunakan sebelumnya adalah 10.0.2.1/24 , saya akan mengubahnya menjadi 192.168.100.20

```
sudo nano /etc/netplan/00-installer-config.yaml
```

![image](https://user-images.githubusercontent.com/78194305/186150223-aa12b524-d4f5-4613-b1ff-33b610381c93.png)

silahkan masukkan password root

![image](https://user-images.githubusercontent.com/78194305/186151514-1a82f692-c4d1-4f47-b85a-55233079b03d.png)

Selanjutnya tampilan akan berubah menjadi text editor pada addresses enp0s3 saya akan ubah menjadi 192.168.100.20/24

![image](https://user-images.githubusercontent.com/78194305/186152023-c2c10af6-c74e-49bb-a875-7e74d67dad32.png)

Kemudian untuk save dan exit kalian tekan ctrl+o (write out)lalu enter kemudian ctrl + x untuk exit

Selanjutnya untuk mengkonfirmasi customisasi IP yang sudah kalian buat tadi kalian bisa menggunakan perintah dibawah

```
sudo netplan apply
```
![image](https://user-images.githubusercontent.com/78194305/186152557-a1649b9f-7f25-4a0b-93c5-3201c4fdffc0.png)

Untuk memastikan lagi kalian bisa cek ip dengan megetikan ip a

```
ip a
```
![image](https://user-images.githubusercontent.com/78194305/186152768-70f9ec18-0584-4ece-8c45-aed040f0ce75.png)

## Install Web Server Apache2 secara manual

Localtunnel adalah sebuah tools yang memungkinkan kita untuk berbagi layanan website dari lokal komputer ke publik dengan url akses yang disediakan oleh localtunnel.

Sebelum di mulai saya akan meremote server yang baru di ubah ipnya terlebih dahulu

```
ssh gama777@10.0.2.20/24
```
![image](https://user-images.githubusercontent.com/78194305/186186638-c9ee6e50-b640-4fcf-a6e7-7628a6b840a4.png)

Selanjutnya untuk menginstall Apache2 kalian bisa gunakan command di bawah ini

```
sudo apt install apache2
```
![image](https://user-images.githubusercontent.com/78194305/186187072-6e3cfc9f-6f67-48c7-aad8-6d3f406e62bf.png)

Prosess penginstallan Apache2

pabila proses penginstalan sudah selesai kalian bisa mengcek status Apache2 dengan command di bawah ini

```
sudo systemctl status apache2
```
![image](https://user-images.githubusercontent.com/78194305/186187613-432f6982-2538-4854-bc87-1f9b3eaf4801.png)

Langkah selanjutnya kita coba cek melalui browser dengan mengetikan ip server




