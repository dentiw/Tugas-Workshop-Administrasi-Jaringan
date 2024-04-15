<div align="center">
  <h1>Tugas 4 </h1>
 <h2>  Workshop Administrasi Jaringan</h2>
<strong>konfigurasi Bind9 </strong>

<img src="Logo_PENS.png" alt="Alt teks">

<br><br>

<p>Oleh:</p>
<li>Denti Widayati (3122500003)</li>




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


<h2>KONFIGURASI NTP SERVER</h2>

<h3>1. Install NTP (Network Time Protocol)</h3>
<p>menggunakan perintah : 
<b>sudo apt-get install systemd-timesyncd</b>

<img src="gbr1.png" alt="Alt teks">


<h3>2. Konfigurasi NTP ke timezone lokal (Asia/Jakarta)</h3>
<p> sudo timedatectl set-timezone Asia/Jakarta

<img src="gbr2.png" alt="Alt teks">

<h3>3.Konfigurasi RTC (Real Time Clock) ke timezone lokal (Asia/Jakarta) dan mengaktifkan RTC</h3>

<img src="gbr3.png" alt="Alt teks">


<h3>4.Konfigurasi NTP ke server terdeka</h3>
<b>sudo nano /etc/systemd/timesyncd.conf ubah bagian NTP= menjadi NTP=0.id.pool.ntp.org</b>

<img src="gbr4.png" alt="Alt teks">

<p></p>

<h3>5.Restart NTP dan cek status NTP</h3>
<p>sudo systemctl restart systemd-timesyncd</p>
<p>sudo systemctl status systemd-timesyncd</p>

<img src="gbr5.png" alt="Alt teks">


<h3>6. Lakukan pengecekan waktu</h3>
<p>bash timedatectl</p> 
<img src="gbr6.png" alt="Alt teks">


<h2>Konfigurasi Web Server (apache2) dan PHP fpm</h2>


<h3>1. Install apache2 dan php-fpm</h3>
sudo apt-get install apache2 -y

<img src="gbr7.png" alt="Alt teks">

<h3>2. Konfigurasi apache2</h3>

<p>Lakukan konfigurasi security apache2

sudo nano /etc/apache2/conf-enabled/security.conf

Ubah bagian ServerTokens menjadi Prod</p>

<img src="gbr8.png" alt="Alt teks">


<h3>3.Lakukan konfigurasi directory apache2</h3>

<b>sudo nano /etc/apache2/mods-enabled/dir.com</b>

<img src="gbr9.png" alt="Alt teks">

<img src="gbr9.1.png" alt="Alt teks">

<h3>4.Tambahkan virtual host yang sudah disiapkan berdasarkan Canonical Name (CNAME) yang sudah dibuat (kelompok9.local) </h3>
<p>menggunakan perintah : sudo nano /etc/apache2/apache2.conf

<img src="gbr10.png" alt="Alt teks">

<img src="gbr10.2.png" alt="Alt teks">

<h3>5. Ubah Kontak email admin menjadi email webmaster@kelompok9.local</h3>
<p>menggunakan perintah</p>
<b>sudo nano /etc/apache2/sites-available/000-default.conf</b>
<p>Ubah bagian webmaster@localhost menjadi webmaster@kelompok9.local</p>
<img src="gbr10.1.png" alt="Alt teks">


<h3>6.Restart apache2 dan cek status apache2 </h3>
<p>sudo systemctl restart apache2 sudo systemctl status apach</p>

<img src="gbr11.png" alt="Alt teks">


<h3>7.  Lakukan Pengujian di browser</h3>
<p>menggunakan perintah : 
<b>Buka browser dan ketikkan alamat www.kelompok9.local</b>

<img src="gbr12.jpg" alt="Alt teks">


<h3>8. Install PHP dan extensi mbstring serta lakukan pengujian</h3>
<p>menggunakan perintah : 
<b>Fungsi mbstring digunakan untuk memanipulasi string atau text non ASCII sudo apt -y install php8.2 php8.2-mbstring php-pear php -v</b>
<img src="gbr15.png" alt="Alt teks">
<img src="gbr14.png" alt="Alt teks">
<img src="gbr13.png" alt="Alt teks">
Buat file php_info.php di /var/www/html sudo nano /var/www/html/php_info.php

Isi file php_info.php dengan kode berikut <?php phpinfo(); ?>

Buka browser dan ketikkan alamat www.kelompok9.local/php_info.php
<img src="gbr16.png" alt="Alt teks">


<h3>9. Install PHP-FPM</h3>
<p>Php fpm adalah FastCGI Process Manager untuk PHP berfungsi sebagai server untuk PHP sudo apt -y install php-fpm </p>

<img src="gbr17.png" alt="Alt teks">


<h3>10. Konfigurasi PHP-FPM di apache2</h3>
<p>menggunakan perintah : 
<b>sudo systemctl restart named</b>
nano /etc/apache2/sites-available/default-ssl.conf Berfungsi untuk mengarahkan apache2 ke php-fpm tambahkan di dalam tag VirtualHost *:443> VirtualHost
<img src="gbr18.png" alt="Alt teks">


<p>a2enmod proxy_fcgi setenvif Ini berfungsi untuk mengaktifkan modul proxy_fcgi dan setenvif</p>
<p>a2enconf php8.2-fpm Ini berfungsi untuk mengaktifkan konfigurasi php8.2-fpm</p>
<p>systemctl restart php8.2-fpm apache2 Ini berfungsi untuk merestart php8.2-fpm dan apache2</p>


<img src="gbr19.png" alt="Alt teks">

<h2>Konfigurasi Database Server (MariaDB)</h2>



<h3>1. Install MariaDB</h3>
<p>menggunakan perintah : 
<b>sudo apt -y install mariadb-server</b>

<img src="gbr20.png" alt="Alt teks">


<h3>2. Konfigurasi MariaDB</h3>
<p>menggunakan perintah : 
<b>sudo /etc/mysql/mariadb.conf.d/50-server.cnf ubah line 95 menjadi

character-set-server = utf8mb4
collation-server = utf8mb4_general_ci</b>

<img src="gbr21.png" alt="Alt teks">

sudo systemctl restart mariadb


<h3>3. Inisial Konfigurasi dan testing database MariaDB Server</h3>
<p>menggunakan perintah : 
<b>sudo mysql_secure_installation</b>

<img src="gbr22.png" alt="Alt teks">
<img src="gbr23.png" alt="Alt teks">


<h3>4. Login ke MariaDB</h3>
<p>menggunakan perintah : 
<b>sudo mysql -u root -p</b>

<img src="gbr24.png" alt="Alt teks">
<img src="gbr25.png" alt="Alt teks">


<h3>5. Uji Coba Database</h3>
<p>menggunakan perintah : 
<b>show grants for 'root'@'localhost';</b>

<img src="gbr28.png" alt="Alt teks">


<p>Tampilkan user,host dan password dari db mysql dan tabel user
<b>select user,host,password from mysql.user;</b>

<img src="gbr27.png" alt="Alt teks">

<p>Tampilkan database yang ada
<b>show databases;</b>

<img src="gbr26.png" alt="Alt teks">

<p>buat database baru
<b>show databases;</b>

<img src="gbr33.png" alt="Alt teks">

<p>buat tabel baru</p>
<b>use test;

create table test.test_table (id int, name varchar(50), address varchar(50), primary key (id));</b>

<img src="gbr32.png" alt="Alt teks">
<p>tambahkan data ke tabel</p>
<b>insert into test_table values (1, 'test', 'test address');</b>
<img src="gbr31.png" alt="Alt teks">
<p>ampilkan data dari tabel</p>
<b>select * from test_table;</b>
<img src="gbr30.png" alt="Alt teks">
<p>keluar dari database</p>
<b>exit</b>
<img src="gbr29.png" alt="Alt teks">




<h2>Install phpmyadmin</h2>

<h3>1. Install phpmyadmin</h3>
<p>menggunakan perintah : 
<b>sudo apt -y install phpmyadmin Konfigurasi installasi</b>
Pilih web server yang digunakan, pada contoh ini menggunakan apache2

<img src="4.png" alt="Alt teks">
Pilih configure database for phpmyadmin dengan dbconfig-common
<img src="3.png" alt="Alt teks">
Masukkan password root phpmyadmin dan konfirmasi password root phpmyadmin
<img src="2.png" alt="Alt teks">

<img src="1.png" alt="Alt teks">

<h3>2. Konfigurasi phpmyadmin pada apache2</h3>
<p>menggunakan perintah : 
<b>sudo nano /etc/apache2/apache2.conf</b>

<img src="5.png" alt="Alt teks">

<h3>3. Restart apache2</h3>
<p>menggunakan perintah : 
<b>sudo systemctl restart apache2</b>

<img src="6.png" alt="Alt teks">

<h3>4. Akses phpmyadmin</h3>
<p>menggunakan perintah : 
<b>Buka browser dan akses phpmyadmin dengan alamat http://kelompok9.local/phpmyadmin</b>

<img src="9.png" alt="Alt teks">

Masukkan username dan password root mysql yang telah diatur sebelumnya 
<img src="8.png" alt="Alt teks">

<h3>5. menambahkan privilege user phpmyadmin</h3>

login ke mysql mysql -u root -p
tambahkan privilege user phpmyadmin

<img src="7.png" alt="Alt teks">



<h2>Konfigurasi Mail Server</h2>



<h3>1. Install Postfix
</h3>

apt -y install postfix sasl2-bin

<img src="rm1.png" alt="Alt teks">
<img src="rm2.png" alt="Alt teks">
<img src="rm3.png" alt="Alt teks">
<img src="rm4.png" alt="Alt teks">
<img src="rm5.png" alt="Alt teks">
<img src="rm6.png" alt="Alt teks">
<img src="rm7.png" alt="Alt teks">
<img src="rm8.png" alt="Alt teks">
<img src="rm9.png" alt="Alt teks">
<img src="rm10.png" alt="Alt teks"><img src="rm11.png" alt="Alt teks">
<img src="rm12.png" alt="Alt teks">
<img src="rm13.png" alt="Alt teks">
<img src="rm14.png" alt="Alt teks">
<img src="rm15.png" alt="Alt teks">
<img src="rm16.png" alt="Alt teks">
<img src="rm17.png" alt="Alt teks">
<img src="rm18.png" alt="Alt teks">
<img src="rm19.png" alt="Alt teks">
<img src="rm20.png" alt="Alt teks">
<img src="rm21.png" alt="Alt teks">
<img src="rm33.png" alt="Alt teks">
<h3>4. Perbarui database aliases postfix</h3>
<p>digunakan untuk memperbarui basis data alias alamat email dalam sistem. Dalam sistem pengiriman email pada Unix dan Linux, file aliases digunakan untuk menentukan alamat mana yang harus dikirimkan ke mana. Perintah newaliases digunakan untuk memperbarui file aliases.db setelah mengubah atau menambahkan entri dalam file aliases.</p>
<b>sudo newaliases</b>
<img src="rm23.png" alt="Alt teks">
5. Restart postfix
<p>systemctl restart postfix
<img src="rm22.png" alt="Alt teks">
6. Menambahkan konfigurasi anti spam
<b>buka file main.cf sudo nano /etc/postfix/main.cf</b>
<img src="rm24.png" alt="Alt teks">
7. Install Dovecot
<img src="rm25.png" alt="Alt teks">
<img src="rm26.png" alt="Alt teks">
8. Konfigurasi Dovecot
Edit file /etc/dovecot/dovecot.conf sudo nano /etc/dovecot/dovecot.conf uncomment baris 30
<img src="rm27.png" alt="Alt teks">
Edit file /etc/dovecot/conf.d/10-auth.conf sudo nano /etc/dovecot/conf.d/10-auth.conf uncomment baris 10 dan setting ke no

ubah di baris 100 menjadi disable_plaintext_auth = plain login
<img src="rm28.png" alt="Alt teks">
<img src="rm29.png" alt="Alt teks">
<img src="rm30.png" alt="Alt teks">
<img src="rm31.png" alt="Alt teks">
<p>11. Testing</p>
<img src="rm32.png" alt="Alt teks">


<h2>Konfigurasi Roundcuber</h2>


<h3>1. Buat Database yang akan digunakan oleh Roundcube</h3>
<p>menggunakan perintah : 
<b>Masuk ke MySQL mysql -u root -p
Buat Database CREATE DATABASE roundcubemail;
Buat User CREATE USER 'roundcube'@'localhost' IDENTIFIED BY 'password';
Berikan Hak Akses grant all privileges on roundcube.* to roundcube@'localhost' identified by 'password'; </b>

<img src="h1.png" alt="Alt teks">
<img src="h2.png" alt="Alt teks">

<h3>2. Install Roundcube</h3>
<p>menggunakan perintah : 
<b>sudo apt-get install -y roundcube roundcube-mysql</b>

<img src="h3.png" alt="Alt teks">

<h3>3. Konfigurasi Roundcube</h3>
<p>menggunakan perintah : 
<p>Masuk ke direktori konfigurasi cd /usr/share/dbconfig-common/data/roundcube/install/</p>
<p>import database mysql -u roundcube -D roundcube -p < mysql kemudian masukkan password yang telah dibuat sebelumnya</p>
<p>Konfigurasi database sudo nano /etc/roundcube/debian-db.php</p>
<p>sesuaikan credential database dengan yang telah dibuat sebelumnya - Konfigurasi Roundcube ```sudo nano /etc/roundcube/config.inc.php``` - ubah line 27 ``` $config['imap_host'] = ["tls://mail.kelompok9.local:143"];``` - ubah line 31 ``` $config['smtp_host'] = 'tls://mail.kelompok9.local:587'; ``` - ubah line 39 ``` $config['smtp_pass'] = '%p'; ``` - ubah line 46 ``` $config['product_name'] = 'Server Mail PENS'; ``` - tambah pada baris paling akhir ``` $config['smtp_auth_type'] = 'LOGIN'; // specify SMTP HELO host $config['smtp_helo_host'] = 'mail.kelompok9.local';</p>

<img src="h4.png" alt="Alt teks">
<img src="h5.png" alt="Alt teks">









