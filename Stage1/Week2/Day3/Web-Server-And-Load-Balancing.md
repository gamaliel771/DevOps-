# Web Server And Load Balancing

![image](https://user-images.githubusercontent.com/78194305/187933112-4aa61651-ce63-45a0-b81b-4bb5788dec54.png)
## Pengertian Web Server
Pengertian Web Server menurut pemahaman saya yaitu sebuah peragkat lunak yang memberikan layanan berupa data yang berfungsi untuk menerima permintaan client berupa HTTP/HTTPS atau yang biasa kita pakai contohnya seperti halaman halaman web pada browser (chrome,mozila,dll)

## Membuat 3 buah server (server gateway, server aplikasi1, server aplikasi2)
Untuk task kali ini saya akan menggunakan multipass yang berfungsi untuk server nantinya

Multipass dirancang untuk pengembang yang menginginkan lingkungan Ubuntu baru dengan satu perintah. Pada dasarnya alat ini dirancang untuk menyederhanakan penginstalan berbagai versi Ubuntu pada mesin virtual yang berjalan di sistem virtualisasi Linux, Windows, dan macOS.
## Install multipass
```
sudo snap install multipass
```
![image](https://user-images.githubusercontent.com/78194305/187934079-33d013f1-e6c7-497b-b738-0f2f35b2bf06.png)

Kemudian saya akan membuat server baru menggunakan multipass
```
multipass launch --name server1
```
Untuk melihat list server gunakan
```
multipass list
```
![image](https://user-images.githubusercontent.com/78194305/187935066-684f8e4e-2b1d-4024-9b8e-b86a76dbfd1d.png)

Kemudian kalian bisa langsung lanjut membuat servernya

Saya akan membuat 2 server lagi bernama server gateway dan server 2
![image](https://user-images.githubusercontent.com/78194305/187937900-a256ed0d-71aa-4ce6-8e07-8616557b7c52.png)

## Instal web server nginx pada server gateway

Langkah awal saya akan masuk pada server gateway dengan menggunakan perintah
```
multipass shell server-gateway
```
![image](https://user-images.githubusercontent.com/78194305/187938209-e7da2b0e-f0f6-42e5-a6bd-7f20916d8eae.png)

selanjutnya saya akan menginstall nginx terlebih dahulu
```
sudo apt update; sudo apt upgrade
```
```
sudo apt install nginx
```
![image](https://user-images.githubusercontent.com/78194305/187940362-bbf3ea50-c781-4399-9abe-9af1a91f95c8.png)

Untuk cek status nginx gunakan perintah
```
sudo systemctl status nginx
```
![image](https://user-images.githubusercontent.com/78194305/187940652-48907e0b-6732-469f-8599-32b5f7c0920f.png)

kemudian saya akan cek pada web browser
![image](https://user-images.githubusercontent.com/78194305/187941111-bb6f4952-e3bc-4ef4-a8e3-e15d3024565d.png)

# Membuat Konfigurasi Revese Proxy




