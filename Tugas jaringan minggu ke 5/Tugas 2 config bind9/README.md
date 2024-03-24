<div align="center">
  <h1>Tugas 4 </h1>
 <h2>  Workshop Administrasi Jaringan</h2>
<strong>konfigurasi Bind9 </strong>

<img src="Logo_PENS.png" alt="Alt teks">

<br><br>

<p>Oleh:</p>
<li>Denti Widayati (3122500003)</li>
<li>Virginia Faiqoh (3122500022 )</li>



<br>

<p>  Dosen Pembimbing     :  Dr. Ferry Astika Saputra ST, M.Sc</p>

<br>
PROGRAM STUDI D3 TEKNIK INFORMATIKA
POLITEKNIK ELEKTRONIKA NEGERI 
SURABAYA
2023 / 2024



</div>



<br><br><br><br><br><br>


<div>


<h2>langkah-langkah untuk instalasi DNS sever menggunakan BIND9 pada Debian 12:</h2>

<h3>1. Install BIND 9</h3>
<p>menggunakan perintah : 
<b>sudo apt install bind9 bind9-doc</b>

<img src="install.png" alt="Alt teks">


<h3>2. Buka file named.conf</h3>
<p>menggunakan perintah : 
<b>sudo nano /etc/bind/named.conf</b>

<img src="dns-2.jpg" alt="Alt teks">

<h3>3. Edit file named.conf</h3>

<img src="config.png" alt="Alt teks">


<h3>4. . Buka file named.conf.options</h3>

<img src="gbr1.jpg" alt="Alt teks">

<p></p>

<h3>5. Edit file named.conf.options</h3>

<img src="named.conf.options.png" alt="Alt teks">


<h3>6. Buka file named.conf.local</h3>
<p>mengguakan perintah:</p> 
<b>sudo nano /etc/bind/named.conf.options</b>



<h3>7. Edit file named.conf.local</h3>

<img src="named.conf.local.png" alt="Alt teks">

<h3>8. Memeriksa kesalahan sintaks file named.conf</h3>

<p>menggunkan perintah </p>
<b>sudo named-checkconf /etc/bind/named.conf</b>


<h3>9. Buka file db.kelompok9.local</h3>
<p>menggunakan perintah : 

<b>sudo nano /var/lib/bind/db.kelompok9.local</b>


<h3>10. Edit file db.kelompok9.locall</h3>
<p>menggunakan perintah : 

<img src="gbr 1.jpg" alt="Alt teks">


<h3>11. Buka file db.kelompok9.local.inv</h3>
<p>menggunakan perintah</p>
<b>sudo nano /var/lib/bind/db.kelompok9.local.inv</b>


<h3>12. Edit file db.kelompok9.local.invl</h3>
<p></p>

<img src="gbr2.jpg" alt="Alt teks">


<h3>13. Memeriksa kesalahan sintaks file db.kelompok3.loca</h3>
<p>menggunakan perintah : 
<b>sudo named-checkzone kelompok9.local db.kelompok9.local</b>

<img src="02.png" alt="Alt teks">


<h3>14. Buka file resolv.conf</h3>
<p>menggunakan perintah : 
<b>sudo nano /etc/resolv.conf</b>


<h3>15. Edit file resolv.conf</h3>
<p> </p>

<img src="gbr 4.png" alt="Alt teks">


<h3>16. Merestart BIND DNS</h3>
<p>menggunakan perintah : 
<b>sudo systemctl restart named</b>


<h3>17. Memeriksa status BIND DNS</h3>
<p>menggunakan perintah : 
<b>sudo systemctl status named</b>

<img src="01.png" alt="Alt teks">


<h3>18. Melakukan query DNS domain kelompok9.local</h3>
<p>menggunakan perintah : 
<b>dig kelompok9.locald</b>

<img src="03.png" alt="Alt teks">


<h3>19. Melakukan reverse DNS lookup alamat IP 192.168.9.1</h3>
<p>menggunakan perintah : 
<b>dig -x 192.168.9.1</b>

<img src="04.png" alt="Alt teks">


<h3>20. Mencari server DNS domain</h3>
<p>menggunakan perintah : 
<b>nslookup ns</b>

<img src="gbr 5.png" alt="Alt teks">






