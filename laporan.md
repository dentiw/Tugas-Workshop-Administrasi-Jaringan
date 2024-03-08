<div align="center">
  <h1>Tugas 3 </h1>
 <h2>  Workshop Administrasi Jaringan</h2>
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

  <h2>8.6 Cleaning The System</h2>

  <p>Meskipun kapasitas hard disk meningkat drastis selama beberapa tahun terakhir,mungkin memerlukan ruang kosong. Beberapa skrip mengotomatiskan proses pembersihan disk, namun harus saya akui bahwa saya lebih memilih untuk memeriksa sebelum menggunakan perintah rm


  <h3> 8.6.1	Disk space information </h3>

  <p>Hal pertama yang harus dilakukan tentu saja adalah mengetahui ruang yang terpakai di disk Anda. Beberapa alat tersedia untuk Anda, dimulai dengan terminal Anda:


  <h4>– Disk space in terminal mode –</h4>
  <p>Ruang disk dalam mode terminal. Ringkasan penggunaan ruang disk untuk setiap titik pemasangan sistem (disk dan partisi) dengan perintah df: </p>

  <img src="gbr1.png"> <br>

  <h4> –List your repertories sorted by decreasing size –</h4>
  <p> Buat daftar perbendaharaan Anda, diurutkan berdasarkan ukuran yang diperkecil. Lihat direktori Anda dalam jumlah besar berkat du dan sortir (satuannya adalah megabita)</p>

  <img src="gbr2.png"> <br>

  <h4>–Ncdu – </h4>
  <p>Penganalisis ruang disk dalam mode konsol. Untuk meluncurkannya, cukup ketik “ncdu” di terminal Anda. Untuk menginstal perangkat lunak ini (dalam mode administrator): </p>

   <img src="gbr3.png"> <br>

  <h4>– Baobab –</h4>
  <p>Penganalisis ruang disk dalam mode grafis, terintegrasi di Gnome tetapi tersedia di lingkungan lain dengan:</p>

  <img src="gbr4.png"> <br>

  <h3>8.6.Ł Cleaning the packages</h3>

  <p>Apt/aptitude/dpkg are the usual Debian package managers. When you install a package its archive- source/deb file is stored in your system (in the /var/cache/apt/archives/ folder) to enable a potential re- installation without Internet connection. To clean the “apt cache” use a simple command in administrator mode</p>

   <img src="gbr5.png"> <br>

  <p>Setelah cache dari paket yang diinstal dibersihkan, Anda juga dapat menghapus paket yang tidak berguna dari sistem Anda, serta file konfigurasi. Peringatan! Ingatlah untuk memeriksa dengan cermat daftar paket yang direncanakan untuk dihapus, sebelum menerima operasi:</p>
  
  <img src="gbr6.png"> <br>

  <p>Jika Anda telah mengupgrade sistem Anda, ada kemungkinan beberapa paket tidak lagi tersedia di repositori baru: paket tersebut sudah usang. Untuk membuat daftar dan menghapus paket-paket ini, gunakan apt dan ingatlah untuk memeriksa dengan cermat daftar paket yang direncanakan untuk dihapus:</p>

  <img src="gbr7.png"> <br>

  <p>Terakhir, untuk membuat daftar dan membersihkan file konfigurasi yang tetap ada meskipun aplikasi telah dihapus, Anda dapat menggunakan perintah berikut:</p>

  <img src="gbr8.png">
  <img src="gbr9.png"> <br>

  <p>Bagi yang lebih maniak, Anda dapat menginstal alat deborphan yang mencantumkan paket-paket yatim piatu di sistem Anda: paket-paket yang tidak bergantung pada paket lain. Peringatan! Ingatlah untuk memeriksa dengan cermat daftar paket yang direncanakan untuk dihapus, sebelum menerima operasi.</p>

  <img src="gbr10.png"> <br>

  <h3>8.6.3	Emptying the trash bins</h3 >

  <p>Tiga tempat sampah (atau keranjang sampah) yang berbeda harus dipertimbangkan:

  <p>Keranjang sampah pengguna : ~/.local/share/Trash/ . Anda dapat mengosongkannya dengan pengelola file sistem (bab.3.6.2.5), atau dengan terminal:</p>

  <img src="gbr11.png"> <br>

  <p>Keranjang sampah administrator : /root/.local/share/Trash/ . Untuk mengosongkannya dengan cara yang benar, gunakan terminal dalam mode administrator:</p>

  <img src="gbr12.png"> <br>

  <p>Keranjang sampah eksternal : terletak di disk eksternal Anda, biasanya diberi nama '/media/y- our_id/your_disk/.Trash_1000', dimana your_id sesuai dengan nama login Anda.</p>


  <h3>8.6.4	Purging application caches</h3>
  <p>Beberapa aplikasi menggunakan folder “cache”, tempat mereka menyimpan gambar, video, dan informasi lain-lain agar dapat berjalan lebih cepat. Biasanya data ini tidak memakan terlalu banyak ruang disk, namun jika (menggunakan alat yang dijelaskan di atas) Anda mendeteksi bahwa suatu folder menjadi terlalu tebal, jangan ragu untuk menghapusnya.</p>

  <img src="gbr13.png"> <br>

  <p>Setiap aplikasi mempunyai caranya sendiri untuk mengelola cache-nya sendiri: beberapa membersihkannya secara sistematis ketika ditutup, yang lain menyimpan datanya di folder /tmp, yang akan dibersihkan selama sesi logout, yang lain menyimpan semua informasinya dalam folder tertentu.</p>

  <p>Untuk Firefox, misalnya, Anda dapat membersihkan cache dari menu preferensi, dan bahkan mengotomatiskan tindakan ini setiap kali aplikasi ditutup.</p>

  <h3>8.6.5 Purging the thumbnails</h3>

  <p>Setiap kali Anda membuka folder yang berisi gambar atau video, thumbnail dibuat untuk mewakili file grafik tersebut. Thumbnail ini disimpan dalam folder tertentu untuk digunakan kembali, daripada dipaksa untuk menghitung ulang setiap kali Anda mengakses file semacam ini.</p>

  <p>Masalah muncul ketika Anda menghapus file grafik, karena thumbnail-nya disimpan di sistem, dan ini menyebabkan sejumlah ruang disk terbuang untuk menyimpan thumbnail yang sudah usang. Untuk membersihkannya, cukup dengan menghapus folder terkait:</p>

  <img src="gbr13.png"> <br>

  <p>Folder ini akan dibuat lagi, pada saat sistem perlu menyimpan thumbnail yang baru dibuat.</p>

  <br>

  <h2>8.7	Installing external “.deb” packages</h2>


  <p>Debian GNU/Linux menggunakan sistem repositori paket untuk mengelola perangkat lunak dengan lebih baik dan meningkatkan keamanan sistem Anda. Namun mungkin saja Anda memerlukan paket eksternal dengan format “.deb”.</p>


  <p>deb adalah kependekan dari “debian”, perusahaan induk. Untuk mendistribusikan perangkat lunaknya, Debian menggunakan format file arsip tertentu: “.deb”. Ini adalah format terkompresi, seperti “.zip” yang Anda gunakan untuk menyimpan data Anda. Arsip “.deb” ini dikenali oleh manajer paket Debian yang berbeda (APT dan antarmuka grafisnya Synaptic) sehingga dapat ditangani dengan lebih mudah.</p>

  <h3>8.7.1	Installation in graphic mode with GDebi</h3>

  <p>GDebi adalah utilitas grafis yang memungkinkan instalasi paket eksternal berformat “.deb”, sekaligus mengelola dependensinya.</p>

  <p>Untuk menginstalnya, cari “gdebi” di manajer paket favorit Anda (Synaptic, Discover, Software) atau lebih sederhana dari terminal dalam mode administrator menggunakan “su”</p>

  <img src="gbr14.jpg"> <br>

  <p>Saat Anda mengunduh paket eksternal Debian, klik kanan padanya dan pilih “Buka dengan gdebi”.</p>

  <img src="gbr15.png"> <br>

  <p>Di dalam menu, klik File > Buka dan masukkan jalur file “.deb”:</p>

  <img src="gbr16.png"> <br>

  <p>Kemudian klik "Instal Paket". Kata sandi Anda diminta untuk memvalidasi pemasangan.</p>

  <img src="gbr17.png"> <br>
  <img src="gbr18.png"> <br>

  <p>Untuk uninstallnya sangat mudah : cukup klik “Remove Package”.</p>

  <img src="gbr19.png"> <br>

  <h3>8.7.2 Installation in terminal mode with Dpkg</h3>

  <p>Dpkg adalah utilitas perangkat lunak yang menangani paket, seperti halnya apt, tetapi tanpa mengelola dependensi. Artinya jika Anda menggunakan dpkg untuk menginstal paket eksternal, Anda perlu menginstal paket “dependen” satu per satu dari terminal Anda. Dpkg terintegrasi di Debian secara default, dan harus digunakan dalam mode administratif.</p>


  <p>Pesan kesalahan akan memberi tahu Anda jika beberapa dependensi hilang. Kemudian cukup instal dengan cara klasik dengan apt

  Kemudian luncurkan kembali instalasi paket eksternal Anda. Untuk menghapus paket eksternal</p>

  <h2>Topologi</h2>

  <img src="gbr20.jpg"> <br>

  <p>Penjelasan :
  Gambar menunjukkan topologi jaringan sederhana dengan 10 perangkat yang terhubung. Kelebihan topologi ini adalah mudah dipasang dan efisien untuk transmisi data. Namun, topologi ini memiliki beberapa kekurangan, seperti rentan terhadap kerusakan dan akses jaringan yang lambat.
  </p>

</div>