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
Reverse proxy adalah konfigurasi standar yang digunakan untuk mengubah jalur traffic, misalkan aplikasi menggunakan port 3000 tetapi agar dapat di akses melalui port 80 maka harus menggunakan reverse proxy.

masuk ke folder nginx setelah itu buat suatu directory baru telebih dahulu.
```
cd /etc/nginx
```
![image](https://user-images.githubusercontent.com/78194305/188037320-c16468ee-8be2-4622-b1e1-a7752a29faef.png)

Setelah itu saya membuat direktori baru lalu masuk ke direktori baru
```
mkdir dumways
```
![image](https://user-images.githubusercontent.com/78194305/188037908-42900cd7-207d-4ac8-986c-bf13fe41e371.png)
```
sudo nano proxy.conf
```
```
server { 
    server_name mydomain.xyz; 
  
    location / { 
             proxy_pass http://10.145.77.200:3000;
    }
}
```
![image](https://user-images.githubusercontent.com/78194305/188040233-c6e54309-d6c1-474d-9302-1332f151de6f.png)

Keterangan : ip pada proxypass kalian isi dengan ip aplikasi1 dan port nodejs
Selanjutnya keluar dari directory week2, setelah itu masuk ke dalam file nginx.conf.
```
sudo nano nginx.conf
```
![image](https://user-images.githubusercontent.com/78194305/188040561-c6015ef1-b5b0-4a83-b47e-3753d5fd1e08.png)

Selanjutnya pergi ke-bagian include, setelah itu masukan lokasi dari directory yang bersi konfigutasi yang sudah kalian buat tadi.
![image](https://user-images.githubusercontent.com/78194305/188041131-53c87392-a24d-42ec-9b66-87b52f258b07.png)

Jika sudah sekarang kita tinggal melakukan restart/reload Nginx kita.
```
sudo systemctl restart nginx
```
![image](https://user-images.githubusercontent.com/78194305/188041277-ce017068-f603-493c-bcef-a5e677d0e879.png)

Sekarang kita akan membuat sebuah virtual host. Untuk membuat virtual host kita harus masuk ke local server kita setelah itu masuk ke dalam file /etc/hosts.

```
sudo nano /etc/hosts
```
![image](https://user-images.githubusercontent.com/78194305/188042896-65ea8952-4555-481b-a504-c1fdc0d556b9.png)

## Instal aplikasi nodejs pada server server1
```
git clone https://github.com/dumbwaysdev/dumbflix-frontend.git
```
![image](https://user-images.githubusercontent.com/78194305/188038461-f2aed6fa-9fa7-4620-a3f3-e21bf74c8269.png)
```
cd dumbflix-frontend
```
![image](https://user-images.githubusercontent.com/78194305/188038721-e6b04836-ade0-495d-9a21-25045f431566.png)
```
sudo apt update
sudo apt install nodejs npm
```
```
npm i
```
```
npm start
```
![image](https://user-images.githubusercontent.com/78194305/188043303-2b6f3b5a-1d06-43ab-82e8-0e71ac7f6c15.png)
![image](https://user-images.githubusercontent.com/78194305/188043784-d33fcce3-4cf6-49f1-851b-27b5576f815b.png)


Kemudian cek di web browser
```
dumbways.xyz
```





