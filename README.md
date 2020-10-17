# Jarkom_Modul1_Lapres_B02

A.  **Display Filter**

1.  **Sebutkan webserver yang digunakan pada
    \"[testing.mekanis.me]{.ul}\"!**

> **wireshark filter expression: http.host == \"testing.mekanis.me\"**
>
> lalu klik follow http stream pada salah satu paket, dan akan muncul
> pop up seperti berikut.
>
> ![](.//media/image1.png)
>
> dari pop up tersebut didapat untuk host *testing.mekanis.me*
> menggunakan webserver **nginx**

2.  **Simpan gambar
    \"Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg\"!**

> ![](.//media/image2.png)
> ![](.//media/image3.png)
>
> hasil downloadnya
>
> ![](.//media/image4.jpg)

3.  **Cari username dan password ketika login di
    \"[ppid.dpr.go.id]{.ul}\"!**

> **wireshark filter expression: http.host contains \"ppid.dpr.go.id\"
> && http.request.method == POST**
>
> ![](.//media/image5.png)

4.  **Temukan paket dari web-web yang menggunakan basic authentication
    method!**

> **wireshark filter expression: http.authbasic**
>
> ![](.//media/image6.png)

5.  **Ikuti perintah di**
    **[[aku.pengen.pw]{.ul}](http://aku.pengen.pw/)! Username dan
    password bisa didapatkan dari file .*pcapng*!**

> **wireshark filter expression: http.host contains \"aku.pengen.pw\"**
>
> didapatkan
>
> ![](.//media/image7.png)
>
> **user: kakakgamtenk**
>
> **password: hartatahtabermuda**
>
> ![](.//media/image8.png)

6.  **Seseorang menyimpan file zip melalui FTP dengan nama
    \"Answer.zip\". Simpan dan Buka file \"Open This.pdf\" di
    Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file
    zipkey.txt (passwordnya adalah isi dari file txt tersebut).**

> Ctrl + F cari berdasarkan string Answer.txt
>
> ![](.//media/image9.png)
> Lalu follow TCP stream (ganti ke raw) dan save jadi .zip
>
> ![](.//media/image10.png)
>
> Untuk membuka file zipnya maka Ctrl + F string *zipkey.txt*
>
> ![](.//media/image11.png)
>
> Lalu didapatkan passwordnya dengan follow tcp stream
>
> ![](.//media/image12.png)
>
> **password zip : hey997400323051**
>
> ![](.//media/image13.png)

7.  **Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip,
    2.zip, \..., 500.zip. Salah satunya berisi pdf yang berisi puisi.
    Simpan dan Buka file pdf tersebut.\
    Your Super Mega Ultra Rare Hint = nama pdf-nya \"Yes.pdf\"**

> **wireshark filter expression: frame contains \"Yes.pdf\"**
>
> ![](.//media/image14.png)
>
> ![](.//media/image15.png)
>
> ![](.//media/image16.png)

8.  **Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan
    Microsoft FTP Service!**

> **Wireshark filter expression : ftp contains "Microsoft"**
>
> ![](.//media/image17.png)
>
> Sehingga diperoleh ip untuk Microsoft FTP Service 198.246.117.106
>
> **wireshark filter expression: ftp.request.command == RETR && ip.addr
> == 198.246.117.106**
>
> ![](.//media/image18.png)
>
> **Nama objectnya : Readme**

9.  **Cari username dan password ketika login FTP pada localhost!**

> **wireshark filter expression: ftp.request.command == USER \|\|
> ftp.request.command == PASS**
>
> **user : dhana**
>
> **pass : dhana123**
>
> ![](.//media/image19.png)

10. **Cari file .pdf di wireshark lalu download dan buka file
    tersebut!**

> **clue: \"25 50 44 46\"**
>
> Ctrl + F cari berdasarkan Hex value *25 50 44 46*
>
> ![](.//media/image20.png)
>
> Lalu follow tcp stream (ganti ke raw) dan save as .pdf
>
> ![](.//media/image21.png)
>
> Isi Pdfnya
>
> ![](.//media/image22.png)

B.  **Capture Filter**

11. **Filter sehingga wireshark hanya mengambil paket yang mengandung
    port 21!**

> **wireshark filter expression: port 21**
>
> ![](.//media/image23.png)

12. **Filter sehingga wireshark hanya mengambil paket yang berasal dari
    port 80!**

> **wireshark filter expression: src port 80**
>
> ![](.//media/image24.png)

13. **Filter sehingga wireshark hanya menampilkan paket yang menuju port
    443!**

> **wireshark filter expression: dst port 443**
>
> ![](.//media/image25.png)

14. **Filter sehingga wireshark hanya mengambil paket yang berasal dari
    ip kalian!**

> **Cek IP menggunakan "ipconfig" di cmd**
>
> ![](.//media/image26.png)
>
> **wireshark filter expression: src net 192.168.43.192**
>
> ![](.//media/image27.png)

15. **Filter sehingga wireshark hanya mengambil paket yang tujuannya ke
    monta.if.its.ac.id!**

> **wireshark filter expression: dst host monta.if.its.ac.id**
>
> ![](.//media/image28.png)
