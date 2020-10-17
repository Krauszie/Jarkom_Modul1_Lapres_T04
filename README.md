# Modul 1 Jarkom 2020 - T04

Oleh:
  - Fachrizal Rahmat Hidayat - 05311840000005
  - Faza Murtadho            - 05311840000034
  
## Display Filter

1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

**Solusi**

tes

Capture Filter

11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

**Solusi**

```port 21```

![11](https://user-images.githubusercontent.com/55182321/96349595-d527c380-10da-11eb-97af-3fcc35a03742.PNG)

Ketik port 21 pada capture filter, dan pilih di loopback

![11a](https://user-images.githubusercontent.com/55182321/96349666-28017b00-10db-11eb-96b4-ca939be54505.PNG)

Maka akan keluar seperti diatas.

12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

```src port 80```

![12](https://user-images.githubusercontent.com/55182321/96349948-233dc680-10dd-11eb-97c0-1b53527f27ae.PNG)

Ketik src untuk "berasal" port 80

![12a](https://user-images.githubusercontent.com/55182321/96350011-71eb6080-10dd-11eb-95d0-ccd4f1315208.PNG)

Maka akan keluar seperti diatas jika ada yg berasal dari port 80
