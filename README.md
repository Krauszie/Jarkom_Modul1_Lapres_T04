# Modul 1 Jarkom 2020 - T04

Oleh:
  - Fachrizal Rahmat Hidayat - 05311840000005
  - Faza Murtadho            - 05311840000034
  
## Display Filter

1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

**Solusi**

Masukkan filter
```http.host contains "testing.mekanis.me"```
Kemudian tinggal di follow TCP Stream paket yang mengandung host [testing.mekanis.me]

![01](https://user-images.githubusercontent.com/50489529/96352776-43c34c00-10f0-11eb-8cf0-25b6003510ae.png)

Jadi webserver yang digunakan adalah **nginx/1.14.0.**


2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

**Solusi**

- Pada menu file, Export Objects HTTP
- Lalu akan ditampilkan list object HTTP
- Dengan text filter, masukan nama file yang dicari.

![02](https://user-images.githubusercontent.com/50489529/96352645-04e0c680-10ef-11eb-8549-f88aebf9088e.png)

Kemudian File tersebut dapat disimpan dengan nama bebas yang kemudian dapat dibuka dan dilihat isinya

![2](https://user-images.githubusercontent.com/50489529/96352646-06aa8a00-10ef-11eb-9657-7b89cf1c95ed.png)

3. Cari username dan password ketika login di "ppid.dpr.go.id"!

**Solusi**

Masukkan filter
```http.host contains "ppid.dpr.go.id" && frame contains "login" && http.request.method contains "POST"```

![03](https://user-images.githubusercontent.com/50489529/96352991-40c95b00-10f2-11eb-8521-70aa969d5986.jpg)

Kemudian dapat dilihat pada HTML form dan didapatkan

**Username: 10pemuda Password: guncangdunia**

4. Temukan paket dari web-web yang menggunakan basic authentication method!

**Solusi**

Masukkan filter
```http.authbasic```

![4](https://user-images.githubusercontent.com/50489529/96353084-1af08600-10f3-11eb-8c00-9ecf93319092.JPG)

Setelah di test ada 2 web yang menggunakan metode basic autentikasi, yaitu **testing.mekanisme.me** dan **aku.pengen.pw**

5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

**Solusi**

Masukkan filter
```http.host contains "aku.pengen.pw"```

![05](https://user-images.githubusercontent.com/50489529/96353174-f0eb9380-10f3-11eb-8757-c0ec0c7c6e28.png)

Kemudian dapat dilihat paketnya dan pada bagian Authorization Basicnya akan didapat **username: kakakgamtenk** dan **password: hartatahtabermuda**. Setelah itu dapat digunakan untuk mengakses website **aku.pengen.pw** dan menjawab pertanyaan yang jawabannya dapat dilihat di Modul 1

![5](https://user-images.githubusercontent.com/50489529/96353175-f34ded80-10f3-11eb-998e-2985facde213.jpg)

6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file "zipkey.txt" (passwordnya adalah isi dari file txt tersebut).

**Solusi**

7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"

**Solusi**

8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

**Solusi**

9. Cari username dan password ketika login FTP pada localhost!

**Solusi**

Masukkan filter
```ftp.request.command contains "USER" || ftp.request.command contains "PASS"```

![09](https://user-images.githubusercontent.com/50489529/96353339-217ffd00-10f5-11eb-8b49-aefb68c0c131.jpg)

Jadi didapatkan **Username: dhana** dan **Password: dhana123**

10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
**clue: "25 50 44 46"**

**Solusi**

Gunakan fitur find hex value kemudian masukkan clue maka akan didapatkan paket **290** yang kemudian dapat di follow TCP Streamnya 

![10](https://user-images.githubusercontent.com/50489529/96353770-52fac780-10f9-11eb-95d1-dadcd58fe0f8.png)

Kemudian dapat disimpan (dijadikan Raw dahulu)

![11](https://user-images.githubusercontent.com/50489529/96353772-568e4e80-10f9-11eb-90f5-a918297f09ef.png)

Terakhir dapat dibuka

![11](https://user-images.githubusercontent.com/50489529/96353805-a40abb80-10f9-11eb-9487-4f4bc8539949.jpg)




##Capture Filter

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
