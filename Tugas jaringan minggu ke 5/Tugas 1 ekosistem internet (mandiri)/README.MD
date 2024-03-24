<div align="center">
  <h1>Tugas 4 </h1>
 <h2>  Workshop Administrasi Jaringan</h2>
<strong>Ekosistem Internet </strong>

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

  <h2>Ekosistem Internet</h2>

  <p> ekosistem internet menurut saya adalah</p>

  Ekosistem internet adalah istilah yang digunakan untuk menggambarkan seluruh lingkungan online yang melibatkan berbagai entitas, teknologi, infrastruktur, dan pengguna yang saling terhubung. Secara lengkap, ekosistem internet mencakup berbagai komponen yang saling bekerja sama untuk mendukung konektivitas, pengiriman data, dan penyediaan layanan online. Berikut adalah penjelasan lengkap tentang ekosistem internet:

<h3>Entitas Utama:</h3>

Pengguna: Pengguna internet adalah bagian paling penting dari ekosistem ini. Mereka terdiri dari individu, organisasi, perusahaan, dan lembaga yang menggunakan internet untuk berbagai tujuan seperti komunikasi, belanja online, pendidikan, bisnis, hiburan, dan lainnya.
Penyedia Layanan Internet (ISP): ISP adalah entitas yang menyediakan akses internet kepada pengguna. Mereka dapat berupa perusahaan telekomunikasi besar, penyedia layanan kabel, penyedia layanan nirkabel, atau penyedia layanan satelit.

<h3>Teknologi dan Infrastruktur:</h3>

Jaringan Telekomunikasi: Infrastruktur jaringan yang menghubungkan berbagai perangkat dan komputer di seluruh dunia. Ini termasuk kabel serat optik, kabel tembaga, jaringan nirkabel, dan infrastruktur satelit.
Server dan Data Center: Server dan pusat data adalah komponen penting dalam ekosistem internet yang menyimpan dan mengelola data online, aplikasi, situs web, dan layanan lainnya.
Protokol dan Standar: Protokol komunikasi seperti TCP/IP, HTTP, DNS, dan lainnya merupakan aturan dan standar yang memungkinkan perangkat dan sistem berkomunikasi dan beroperasi secara efisien di internet.

<h3>Entitas Lainnya:</h3>

ICANN (Internet Corporation for Assigned Names and Numbers): ICANN bertanggung jawab atas pengelolaan sistem domain dan pengalokasian alamat IP di internet.
PANDI (Pengelola Nama Domain Internet Indonesia): PANDI adalah badan yang mengelola domain berakhiran .id untuk Indonesia.
IXP (Internet Exchange Point): IXP adalah titik pertukaran internet di mana penyedia layanan internet (ISP) bertukar data secara langsung, mempercepat pertukaran data lokal tanpa harus melalui jaringan global.
Badan Standar dan Organisasi: Badan seperti IETF (Internet Engineering Task Force) bertanggung jawab atas pengembangan standar dan protokol teknis untuk internet.

<h3>Proses dan Interaksi:</h3>

DNS (Domain Name System): DNS adalah sistem yang menerjemahkan nama domain menjadi alamat IP, memungkinkan pengguna untuk mengakses situs web dengan menggunakan nama domain.
Routing dan Protokol Jaringan: Sistem routing memastikan pengiriman data yang efisien melalui jaringan internet dengan menggunakan protokol seperti BGP (Border Gateway Protocol), OSPF (Open Shortest Path First), dan lainnya.
Pengaturan Peering dan Koneksi ISP: ISP melakukan peering untuk bertukar data secara langsung, dan mereka memiliki berbagai jenis hubungan seperti provider-customer, transit, dan settlement-free.

<h3>Layanan dan Konten:</h3>

Layanan Online: Berbagai layanan online termasuk email, media sosial, streaming video, e-commerce, e-learning, cloud computing, dan lainnya yang disediakan oleh penyedia layanan dan perusahaan teknologi.
Konten Digital: Konten digital seperti artikel, video, musik, gambar, aplikasi, dan lainnya tersedia secara online dan diakses oleh pengguna melalui internet.

<h3>Pendidikan dan Pembangunan Kapasitas:</h3>

Pendidikan Internet: Program dan sumber daya yang memungkinkan pengguna untuk memahami cara menggunakan internet secara efektif dan aman.
Pembangunan Kapasitas: Pengembangan infrastruktur, teknologi, dan keterampilan yang diperlukan untuk memperluas akses dan meningkatkan pemanfaatan internet di berbagai wilayah dan komunitas.
Secara keseluruhan, ekosistem internet adalah lingkungan yang kompleks dan dinamis yang melibatkan berbagai entitas, teknologi, dan proses untuk menyediakan konektivitas, layanan, dan konten kepada pengguna di seluruh dunia. Interaksi antara berbagai komponen ini menciptakan infrastruktur yang memungkinkan internet menjadi jaringan global yang sangat penting dalam era digital saat ini.

<br><br><br><br><br><br>


<h2>berikut adalah penjelasan detail tentang cara kerja iterative dan recursive dari DNS Query ketika mengakses situs web "example.com":</h2>

1. Permintaan Awal:
Saat pengguna memasukkan URL "example.com" ke dalam browser web, permintaan tersebut dikirimkan ke resolver DNS lokal yang terhubung ke jaringan internet.

2. Langkah Iterative:
Resolver DNS lokal membuat kueri pertama ke salah satu dari 13 root server global. Ini adalah langkah iteratif pertama.

> Root server merespons dengan informasi tentang server TLD (Top-Level Domain) yang bertanggung jawab atas ".com".
Langkah Recursive:

3. Resolver DNS lokal kemudian mengirimkan kueri ke server TLD yang bertanggung jawab atas ".com".

> Server TLD ".com" merespons dengan informasi tentang server DNS yang memiliki informasi tentang "example.com".

> Resolver DNS lokal kemudian mengirimkan kueri ke server DNS yang disediakan oleh registrar domain example.com.
Server DNS example.com merespons dengan alamat IP untuk example.com.

4. Resolusi Selesai:
Resolver DNS lokal menerima alamat IP dari server DNS example.com.

> Resolver DNS lokal meneruskan alamat IP ke browser.
> Browser menggunakan alamat IP tersebut untuk mengakses situs web example.com.


<h3>Analogi:</h3>
Untuk memberikan analogi yang lebih rinci tentang proses ini, bayangkan Anda mencoba mencari alamat rumah teman di kota yang tidak pernah Anda kunjungi sebelumnya.

a. Permintaan Awal: Anda memiliki nama teman (example.com) tetapi tidak tahu di mana dia tinggal (alamat IP).

b. Pertanyaan Pertama (Iterative): Anda meminta petunjuk pertama kepada seorang warga di kota tersebut. Mereka memberi tahu Anda untuk pergi ke pusat informasi kota (root server).

c. Pusat Informasi Kota (Root Server): Di pusat informasi kota, petugas memberi tahu Anda bahwa Anda harus mencari di bagian yang bertanggung jawab untuk wilayah tersebut (TLD server).

d. Wilayah (TLD Server): Anda pergi ke wilayah yang ditunjukkan oleh petugas, dan di sana Anda bertanya pada seseorang lagi. Mereka memberi tahu Anda untuk mencari di kantor polisi setempat (DNS server yang bertanggung jawab atas domain ".com").

e. Kantor Polisi (DNS Server .com): Di kantor polisi, petugas memberi tahu Anda bahwa Anda harus bertanya langsung ke keluarga teman Anda (DNS server yang bertanggung jawab atas domain example.com).

f. Rumah Teman (DNS Server example.com): Di rumah teman Anda, anggota keluarga memberi tahu Anda alamat lengkap teman Anda.
Kembali ke Anda: Anda kembali dengan alamat lengkap yang diberikan oleh keluarga teman .

g. Tiba di Rumah Teman: Anda mengunjungi teman Anda dengan menggunakan alamat yang Anda dapatkan dan tiba di rumahnya.


Dengan demikian, proses ini menggambarkan bagaimana DNS Query bekerja secara iterative dan recursive untuk menemukan alamat IP dari sebuah domain seperti example.com.
