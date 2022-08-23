# Tutorial Install Ubuntu Server 20.04 LTS Menggunakan Virtualbox
![ubuntu-server-logo](https://user-images.githubusercontent.com/78194305/186046844-12cadd9d-4547-4a00-8aae-8e9e876b8d24.png)

DevOps menurut pandangan saya yaitu gabungan antara Development dan Operation yang berarti menggabungkan proses development/pengembangan dari sebuah sistem/aplikasi dengan operation/operasional yang bertujuan untuk mempercepat pembuatan aplikasi dan meminimalisir adanya kesalahan pada saat deploying aplikasi.

Kali ini saya akan memberikan tutorial menginstall Ubuntu Server versi 20.04 LTS , LTS adalah kepanjangan dari Long Term Service, dengan kata lain kamu akan mendapat update selama 5 tahun penuh sebelum disarankan untuk melakukan upgrade ke versi yang lebih tinggi dan saya menggunakan VM (Virtual Machine) Virtual Box

Untuk bahan- bahan yang kalian butuhkan akan saya cantumkan link di bawah ini :

[Virtual Box](https://www.virtualbox.org/wiki/Downloads) (90MB–100MB)

[Ubuntu Server 20.04 LTS](https://ubuntu.com/download/server) (1.2GB)

Apabila file sudah di download, kalian install virtual box dan pilih lokasi untuk menyimpan file Virtual Boxnya

Berikut adalah langkah langkah menginstall Ubuntu Server 20.04 LTS

![Screenshot_20220822_195149](https://user-images.githubusercontent.com/78194305/186048540-6d3f74ca-7286-4916-8598-76de1b41f041.png)

Buka Aplikasi VirtualBox

![image](https://user-images.githubusercontent.com/78194305/186048703-c50cc4b0-8dfb-4f33-8cb7-0c5baeea473c.png)

Pilih New

![Screenshot_20220822_195702](https://user-images.githubusercontent.com/78194305/186048843-a27c0243-5777-41e6-9bdc-f7eb154e0847.png)

masukkan nama dan pilih lokasi folder selanjutnya pilih " next"

![Screenshot_20220822_200057](https://user-images.githubusercontent.com/78194305/186049279-0be58590-e0fa-4b32-8706-9334882b0307.png)

Sesuai Task untuk RAM nya 2GB (2048MB) lalu pilih “Next”


![image](https://user-images.githubusercontent.com/78194305/186049699-4b8a87dc-5d3b-4b00-abdd-c0e02b5dabed.png)


Pilih Create a virtual hard disk now lalu “Create”

![Screenshot_20220822_200534](https://user-images.githubusercontent.com/78194305/186049858-5ef62954-8914-4c1d-8595-a71dfc36d654.png)


Pilih VDI (Virtual Box Disk Image) lalu “Next”

![Screenshot_20220822_200534](https://user-images.githubusercontent.com/78194305/186049962-9926f3c6-4214-46b1-906f-376bbb8eab5c.png)

Pilih Dynamically allocated lalu “Next”

![Screenshot_20220822_200622](https://user-images.githubusercontent.com/78194305/186050035-e587faed-2a77-40bf-8f77-1958ebaaef52.png)

Atur kapasitas storage menjadi 10GB lalu “Create”

![Screenshot_20220822_203203](https://user-images.githubusercontent.com/78194305/186050219-fe762706-8943-435f-ac46-419e4d0aec19.png)

# Perbedaan NAT dan Bridge

NAT merupakan singkatan dari Network Address Translation adalah cara paling sederhana untuk mengakses jaringan eksternal dari virtual machine. Biasanya, itu tidak memerlukan konfigurasi pada jaringan host dan sistem guest. Ini adalah mode jaringan default di VirtualBox atau VMware.

BRIDGE merupakan jenis jaringan yang menggunakan driver perangkat pada sistem host kalian yang menyaring data dari physical network adapter kalian.


![Screenshot_20220822_204251](https://user-images.githubusercontent.com/78194305/186051488-bc4bb3a7-b532-48d7-9a9e-a6f4aa3c80c0.png)

Pilih file Ubuntu Server 20.04LTS yang sudah di downlad lalu “Start”

![Screenshot_20220822_204431](https://user-images.githubusercontent.com/78194305/186051622-8d1d1da0-4a82-43f0-8b26-8ef7f158dc7a.png)

tunggu hingga proses selesai

![Screenshot_20220822_204508](https://user-images.githubusercontent.com/78194305/186051768-fadd31dc-ffe4-403e-8c2a-8513cf808570.png)

Pada step ini kita diminta memilih bahasa , untuk bahasa yang saya pilih saya pakai bahasa inggris lalu “Enter”

![Screenshot_20220822_204529](https://user-images.githubusercontent.com/78194305/186051845-0386f9cb-1cd4-4a7b-ae93-7136e9c2b4d0.png)

Pilih Continue without updating lalu “Enter”

![Screenshot_20220822_204607](https://user-images.githubusercontent.com/78194305/186051987-779becae-e023-4c14-a592-5b565e93e2bf.png)

Pilih “Done” lalu “Enter”

![Screenshot_20220822_210249](https://user-images.githubusercontent.com/78194305/186052186-8c5a0bee-bc25-4d26-a0fb-0bc7275972bb.png)

tahap ini pilih done 

![Screenshot_20220822_204742](https://user-images.githubusercontent.com/78194305/186052592-adf5d422-4479-47a3-8a60-bea34b2bd648.png)

Pada step ini karena intruksinya menggunakan static kalian “Enter” enp0s3 lalu pilih edit ipv4

![Screenshot_20220822_205749](https://user-images.githubusercontent.com/78194305/186054074-d618f086-7ede-47a5-971e-2887309c9c1c.png)

Pilih “Manual”

![Screenshot_20220822_210121](https://user-images.githubusercontent.com/78194305/186054166-d8f21280-d43b-439b-88e0-3bbb9e8ea8d6.png)

Setelah memih metode manual IPv4 / static kalian perlu mengisi Subnet,Address,Gateway, dan Name Server lalu pilih “Save”

![Screenshot_20220822_210215](https://user-images.githubusercontent.com/78194305/186073171-6a49c1db-2577-4e77-8522-f66dc7a62076.png)

Setelah itu DHCPv4 akan berubah menjadi Static lalu pilih “Done”

![Screenshot_20220822_210249](https://user-images.githubusercontent.com/78194305/186100075-afae8d5e-3392-49b5-a62d-b78372d7fad1.png)

Pada step configure proxy langsung saja pilih “Done”

![Screenshot_20220822_210326](https://user-images.githubusercontent.com/78194305/186100228-d40db681-1a58-4352-8a8a-92b45ad964f9.png)

Untuk Storage configuration kalian pilih “Costum storage layout” lalu “Done”

![Screenshot_20220822_210428](https://user-images.githubusercontent.com/78194305/186100890-96d16f91-c8d2-4272-9af8-aa6e737348c2.png)

Pilih “free space” lalu pilih “Add GPT Partition”

Swap adalah ruang pada disk yang digunakan ketika jumlah memori RAM fisik penuh. Ketika sistem Linux kehabisan RAM, halaman yang tidak aktif akan dipindahkan dari RAM ke ruang swap.

![Screenshot_20220822_210505](https://user-images.githubusercontent.com/78194305/186101188-e67e2699-6e5f-4db9-94ff-75179662d267.png)

Pilih “Create”

![image](https://user-images.githubusercontent.com/78194305/186101422-84c879dd-2c19-48ae-a123-63ffbdc0b0d8.png)

Lalu kalian pilih “free space” > “Add GPT Partition”

![image](https://user-images.githubusercontent.com/78194305/186101956-70918d58-af9c-4e0a-b5c3-9c61e7c49407.png)


Untuk Size saya berikan Max / atau semua space yang tersisa “8.997GB” , Format pilih “ext4”, Mount “/’ , Lalu pilih “Create”

![Screenshot_20220822_210636](https://user-images.githubusercontent.com/78194305/186102061-cf5de252-1fbc-4c9a-acf1-a9fdf9bf43ef.png)

Kemudian pilih “Done”

![Screenshot_20220822_210701](https://user-images.githubusercontent.com/78194305/186102147-b0e7877a-8443-445b-863b-e7f0e55ebed0.png)

Pilih “Continue”

![Screenshot_20220822_210746](https://user-images.githubusercontent.com/78194305/186102251-7598b343-ae0d-4c20-98e3-e48727842d6b.png)

Kalian perlu mengisi beberapa kolom profile . Jika sudah pilih “Done”

![Screenshot_20220822_210804](https://user-images.githubusercontent.com/78194305/186102417-8def264a-702b-45d3-9045-66976f35babc.png)

Pada step ini bisa langsung di skip saja pilih “Done”

![Screenshot_20220822_210836](https://user-images.githubusercontent.com/78194305/186102546-4806c8b6-3f5f-4771-ba6e-3e216778805b.png)

Pada step SSH Setup kalian pilih “Install OpenSSH Server” lalu pilih done

![Screenshot_20220822_210953](https://user-images.githubusercontent.com/78194305/186102708-6c0e5e24-7baf-40b3-b4d7-2619d7b5c364.png)

Pada step ini kalian diminta untuk menginstal beberapa fitur . Apabila tidak ada yang ingin di install bisa langsung pilih “Done”

Sebagai tambahan saya akan mengintall docker pada step diatas

![Screenshot_20220822_211034](https://user-images.githubusercontent.com/78194305/186102892-67917434-f396-4401-b773-e67d39ce2a55.png)

Pilih “stable” dan “close”

![Screenshot_20220822_211057](https://user-images.githubusercontent.com/78194305/186103009-2959d9d9-5e9e-47ed-9d29-90797cba34f1.png)

pilih Done 

![Screenshot_20220822_211116](https://user-images.githubusercontent.com/78194305/186103291-e2833c1e-1749-45ef-924e-e199481b7dc4.png)

![Screenshot_20220822_220616](https://user-images.githubusercontent.com/78194305/186103539-379d0d19-f51e-4162-8c1a-1775a6a87bd5.png)


Proses instalasi biasanya memakan beberapa menit , apabila sudah selesai kalian bisa pilih “Reboot Now”

![Screenshot_20220822_220919](https://user-images.githubusercontent.com/78194305/186103738-b2bcaa39-9c4d-4144-89ff-872243e78410.png)

Setelah Server memasuki tampilan ini kalian perlu memasukan username dan password lalu enter

![Screenshot_20220822_221000](https://user-images.githubusercontent.com/78194305/186103944-fcf8bcea-b763-415b-a17f-28e83fad088c.png)

Tahap terakir adalah tes koneksi dengan ping 8.8.8.8.com (dns google)


















