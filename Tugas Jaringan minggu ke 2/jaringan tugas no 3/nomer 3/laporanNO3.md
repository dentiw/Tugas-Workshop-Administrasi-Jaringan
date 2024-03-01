<div align="center">
  <h1>Tugas 2</h1>
  <h2>Workshop Administrasi Jaringan</h2>
  <strong>DEBIAN</strong>

  <img src="Logo_PENS.png" alt="Alt teks">

  <br><br>
  <p>Oleh:</p>
<li>Denti Widayati (3122500003)</li>
<li>Virginia Faiqoh (3122500022 )</li>
<li>Adira Callysta (3122500025 )</li>

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

  <p>1. Ubahlah alamat IP dinamis menjadi statis</p>

  <p><mark>Jawaban : </mark></p>

  <p> Ada dua cara untuk melakukan setting network di debian yaitu melalui GUI (Network Manager) dan CLI (Menggunakan file /etc/network/interfaces)</p>

  Default gateway :

  <img src="gbr1.png" alt="Alt teks"> <br>

  <h3> A. Menggunakan Network Manager </h3>

  <td> <ol type="1">
  
  <li>Buka Network Manager dengan meng klik ikon setting di pojok kanan atas <br>

  <img src="gbr2.png" alt="Alt teks"> <br><br>

  <li> Setelah itu akan masuk ke halaman setting <br>

  <img src="gbr3.png" alt="Alt teks"> <br><br>

  <li> Pilih Interfaces yang sudah tersambung, lalu klik ikon setting pada interface tersebut<br>

  <img src="gbr4.png" alt="Alt teks"> <br><br>

  <li> Pilih menu IPV4 lalu klik manual. Kemudian, masukkan konfigurasi <br>- alamat IP
  Address : 10.0.2.100 <br>
  - Netmask : 255.255.255.0 <br>
  - DNS : 8.8.8.8 <br>
  Lalu Klik Apply<br>

  <img src="gbr5.png" alt="Alt teks"> <br><br>

  </td>
</div>

<div>

  <h3> B. Menggunakan Network Manager </h3>

  <td> <ol type="1">
  
  <li>Buka terminal, lalu ketikkan /etc/network/interfaces <br>

  <img src="gbr6.png" alt="Alt teks"> <br><br>

  <li>Isi file dibagian paling bawah sesuai dengan konfigurasi yang diinginkan. Setelah itu klik simpan dan keluar<br>

  <img src="gbr7.png" alt="Alt teks"> <br><br>

  <li>Ketikkan perintah sudo ifdown(nama interfaces) untuk mematikan interface <br>

  <img src="gbr8.png" alt="Alt teks"> <br><br>

  <li>Ketikkan perintah sudo ifup(nama interfaces) untuk mengaktifkan kembali interface dengan pengaturan yang baru <br>

  <img src="gbr9.png" alt="Alt teks"> <br><br>

  <li>Kemudian cek menggunakan perintah ~$ ip address <br>

  <img src="gbr10.png" alt="Alt teks"> <br><br>

  <li>Lakukan pengujian. disini pengujian dilakukan dengan meng ping google <br>

  <img src="gbr11.png" alt="Alt teks"> <br><br>

  </td>

</div>

Setelah melakukan salah satu cara di atas, pengaturan network di debian akan berubah sesuai dengan yang kita inginkan.