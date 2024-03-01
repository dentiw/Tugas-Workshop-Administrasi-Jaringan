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

  <p>1. Tulis kembali dalam bahasa Indonesia dengan gaya tulisanmu sendiri tentang standar struktur direktori dari Debian (Gunakan referensi https://www.debianadmin.com/linux-directory-structure-overview.html)! Gambarkan struktur direktori dari hasil instalasimu ! (gambar bisa menggunakan Miro, draw.io atau lainnya)</p>

  <p><mark>Jawaban : </mark></p>

  <p> Direktori<br>
    Struktur direktori Unix dan Linux adalah struktur direktori seragam dimana semua direktori dikelompokkan di bawah sistem file root "/"</p>

  <td> <ol type="1">
  <li>  “/” Root <br>
    Struktur direktori dimulai dengan sistem file root "/", yang sebenarnya merupakan direktori root dari keseluruhan struktur. Partisi tempat / (direktori root) berada pada sistem yang kompatibel dengan UNIX atau UNIX. <br><br>

  <li> /boot <br>
    Direktori /boot berisi file boot loader, termasuk grub atau lilo, file konfigurasi kernel, initrd dan system.map. <br><br>


  <li> /sys <br>
    Berisi file terkait kernel, firmware, dan sistem. <br><br>

  <li> /sbin <br>
    Berisi biner sistem dan alat manajemen sistem yang penting, untuk pengoperasian dan kinerja sistem. <br><br>

  <li> /bin <br>
    Berisi biner dan utilitas penting bagi pengguna  yang diperlukan untuk mode pengguna tunggal. Contohnya termasuk cat, ls, cp, dll. <br><br>

  <li> /lib <br>
    Menyertakan file perpustakaan untuk semua binari yang disimpan di direktori /sbin dan /bin. <br><br>

  <li> /dev <br>
    Direktori /dev berisi file sistem dan driver  penting. <br><br>
 
  <li> /etc <br>
    /etc/directory berisi file konfigurasi sistem penting seperti /etc/hosts, /etc/resolv.conf, nsswitch.conf, file konfigurasi standar, dan file konfigurasi jaringan. Ini biasanya merupakan file konfigurasi aplikasi & sistem  khusus host. <br><br>

  <li> /home <br>
    Semua direktori home pengguna disimpan di  direktori ini kecuali direktori home root, yang disimpan di direktori /root. Direktori ini menyimpan file pengguna, pengaturan pribadi seperti profile dll. <br><br>

  <li> /media <br>
    Titik pemasangan umum untuk media yang dapat dipindahkan seperti CD-ROM, USB, dan floppies. <br><br>

  <li> /mnt <br>
    Titik pemasangan umum untuk sistem file sementara. Ini sangat berguna  ketika memecahkan masalah seperti CD-ROM di mana Anda perlu memasang sistem file root dan mengedit konfigurasi. <br><br>

  <li> /opt <br>
    Direktori yang jarang digunakan di Linux untuk paket perangkat lunak opsional. Ini biasanya digunakan pada sistem operasi UNIX, seperti Sun Solaris, di mana paket perangkat lunak diinstal. <br><br>

  <li> /usr <br>
    Subhierarki sistem file root, direktori data pengguna. Berisi utilitas dan aplikasi khusus. <br><br>

  <li> /usr/sbin <br>
    Berisi biner  yang tidak penting dan tidak penting untuk utilitas sistem dan jaringan. <br><br>

  <li> /usr/lib <br>
    File perpustakaan untuk binari di direktori /usr/bin dan /usr/sbin. <br><br>

  <li> /usr/share <br>
    Direktori data bersama yang tidak bergantung pada platform. <br><br>

  <li> /usr/local <br>
    Subhierarki di bawah direktori /usr yang berisi data spesifik sistem lokal, termasuk biner pengguna dan sistem serta pustakanya. <br><br>

  <li> /var <br>
    Direktori Sebagian besar diinstal sebagai sistem file terpisah di direktori root tempat semua konten variabel seperti log, file spool  printer, crontab, pekerjaan, mail, proses yang berjalan, file kunci, dll. <br><br>

  <li> /tmp <br>
      Sistem file sementara untuk menyimpan file sementara yang dibersihkan saat sistem di-restart. File sementara juga disimpan di direktori /var/tmp. <br><br>

<p><h3><mark>Berikut adalah gambar visual dari directory root<mark></h3></p>
     
 <img src="tgs1.jpg" alt="Alt teks">
 <br><br>

 <img src="tgs2.jpg" alt="Alt teks">
  <br><br>

  <img src="tgs3.jpg" alt="Alt teks">
  <br><br>

  <img src="tgs4.jpg" alt="Alt teks">
    <br><br>

  <img src="tgs5.jpg" alt="Alt teks">
  <br><br>

  <img src="tgs6.jpg" alt="Alt teks">
  <br><br>

  <img src="tgs7.jpg" alt="Alt teks">
  <br><br>

  <img src="tgs8.jpg" alt="Alt teks">
  <br><br>

  <img src="diagram1.png" alt="Alt teks">