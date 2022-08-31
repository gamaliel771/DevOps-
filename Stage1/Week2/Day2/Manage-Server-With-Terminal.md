# Terminal
![image](https://user-images.githubusercontent.com/78194305/187677190-45669e17-3a85-4af3-b916-0c5b15486248.png)

## apa itu terminal?

terminal adalah sebuah aplikasi command prompt yang berfungsi sebagai penghubung User dengan system komputer contoh dalam mengontrol file, membuat folder, ataupun membuat akses
## Keuntungan Menguasai Terminal
suatu yang sangat penting karena di DevOps kita sering kali melakukan remoting server berbasis CLI. Oleh karena itu penting nya mengusai terminal supaya kita dapat mengoprasikan OS berbasis CLI
# Memuat sebuah file bash sederhana yang bertugas untuk update dan upgrade sistem
pertama saya akan masuk ke server terlebih dahulu 
![image](https://user-images.githubusercontent.com/78194305/187677537-67e4b455-29fd-4b39-b352-13c0f3286f64.png)

Setelah connect ke server saya akan membuat direktori baru
![image](https://user-images.githubusercontent.com/78194305/187677916-9ffeed8c-1d28-4faa-b379-89c935224137.png)
![image](https://user-images.githubusercontent.com/78194305/187678158-5bd6a34c-c9df-4380-85ca-2d0eacdd6860.png)
![image](https://user-images.githubusercontent.com/78194305/187678531-afff1362-314d-403b-b188-9d8211fd2497.png)
![image](https://user-images.githubusercontent.com/78194305/187678610-90938c74-c8e2-4e60-b2bd-5b5103cb32dc.png)

# Membuat sebuah file bash sederhana yang bertugas untuk mencari file bernama sysctl.conf
![image](https://user-images.githubusercontent.com/78194305/187707172-4ed8ec83-dc1d-43d6-8527-4aea63ea9ee7.png)
![image](https://user-images.githubusercontent.com/78194305/187707463-5948d940-b764-4cbf-bdec-8417a5a283e6.png)
![image](https://user-images.githubusercontent.com/78194305/187707872-4a4ef8c9-0907-4d1a-b5d2-7fdd4e56824e.png)
![image](https://user-images.githubusercontent.com/78194305/187708026-402be0ce-8024-47a4-82d7-61f811ac7c53.png)
```
find -type f -name sysctl.conf
```
![image](https://user-images.githubusercontent.com/78194305/187708270-07b8f99f-7626-45de-b9f4-5f64233cf8a9.png)
![image](https://user-images.githubusercontent.com/78194305/187708638-73146f97-8f82-4b66-b596-eff7f1c4ece7.png)
## Membuat sebuah file bash serderhana yang bertugas untuk membuat firewall port 22, 80 dan 443
Lagkah pertama isntall ufw
```
sudo apt install ufw -y
```
Uncomplicated Firewall (UFW) adalah sebuah interface dari Linux iptables. iptables sendiri adalah tools yang sangat bagus untuk melakukan konfigurasi firewall di sistem operasi berbasis Linux.
![image](https://user-images.githubusercontent.com/78194305/187709264-dd7f6c56-76a1-4055-8d81-85915f7b75f3.png)
![image](https://user-images.githubusercontent.com/78194305/187709459-cda12b6e-dd2b-49f0-8be5-d67db4140e5f.png)
![image](https://user-images.githubusercontent.com/78194305/187709571-520ba79e-ff8e-488a-967d-bd99176b754a.png)
```
echo "file 22"

sudo ufw allow 22

echo "file 80"

sudo ufw allow 80

echo "file 443"

sudo ufw allow 443
```
![image](https://user-images.githubusercontent.com/78194305/187709866-97b74757-8ffa-487c-8ec0-7af8e662b64f.png)

Untuk mengeceknya kita bisa menggunakan
```
sudo ufw enable
```
```
sudo ufw status
```
![image](https://user-images.githubusercontent.com/78194305/187710242-efa51816-113a-4707-af2b-5ce2b78f1ad5.png)






