# Modul 1 Jarkom 2020 - T04

Oleh:
  - Fachrizal Rahmat Hidayat - 05311840000005
  - Faza Murtadho            - 05311840000034
  
## Display Filter

1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

**Solusi**

```http.host contains "testing.mekanis.me"```
![01](https://user-images.githubusercontent.com/50489529/96352643-01e5d600-10ef-11eb-8ae5-37306bb8d02b.png)

Capture Filter

11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Solusi**

```port 21```

![11](https://user-images.githubusercontent.com/55182321/96349595-d527c380-10da-11eb-97af-3fcc35a03742.PNG)

Ketik port 21 pada capture filter, dan pilih di loopback

![11a](https://user-images.githubusercontent.com/55182321/96349666-28017b00-10db-11eb-96b4-ca939be54505.PNG)

Maka akan keluar seperti diatas.

12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

**Solusi**

```src port 80```

![12](https://user-images.githubusercontent.com/55182321/96349948-233dc680-10dd-11eb-97c0-1b53527f27ae.PNG)

Ketik src untuk "berasal" port 80

![12a](https://user-images.githubusercontent.com/55182321/96350011-71eb6080-10dd-11eb-95d0-ccd4f1315208.PNG)

Maka akan keluar seperti diatas jika ada yg berasal dari port 80

13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

**Solusi**

```dst port 443```

![13](https://user-images.githubusercontent.com/55182321/96350249-2934a700-10df-11eb-833a-bd8d50eaaec8.PNG)

Ketik dst untuk menampilkan paket yang menuju port 443

![13a](https://user-images.githubusercontent.com/55182321/96350281-6305ad80-10df-11eb-92b0-ccc61ddff38b.PNG)

Maka akan keluar seperti demikian

14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

**Solusi**

```src host 192.168.1.11```

![14](https://user-images.githubusercontent.com/55182321/96350353-b2e47480-10df-11eb-8c2f-b5edadf04800.PNG)

Untuk mengetahui IP sendiri, bisa dicari dengan menggunakan cmd lalu megetik ip config. Dalam kasus ini, ip saya adalah 192.168.1.11

![14b](https://user-images.githubusercontent.com/55182321/96350465-1ff80a00-10e0-11eb-8749-2c35a61d73b7.PNG)

Ketik pada capture filter

![14a](https://user-images.githubusercontent.com/55182321/96350428-f212c580-10df-11eb-94db-c2d9d6acd6ef.PNG)

Maka akan keluar seperti demikian

15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

**Solusi**

```dst host monta.if.its.ac.id```

![15](https://user-images.githubusercontent.com/55182321/96350537-909f2680-10e0-11eb-8d62-50e4ed02a0b4.PNG)

Ketik pada capture filter

![15a](https://user-images.githubusercontent.com/55182321/96350539-9137bd00-10e0-11eb-822a-6254a35419e0.PNG)

Maka akan keluar demikian
