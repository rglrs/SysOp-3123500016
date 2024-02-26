<div align="center">
  <h1 style="text-align: center;font-weight: bold">Praktikum 1<br>SysOp</h1>
  <h4 style="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h4>
</div>
<br />
<div align="center">
  <img src="pens.jpeg" alt="Logo PENS">
  <h3 style="text-align: center;">Disusun Oleh : </h3>
  <p style="text-align: center;">
    <strong>Roihanah Inayati Bashiroh (3123500005)</strong><br>
    <strong>Dio Ramadhan Widya Pamungkas (3123500011)</strong><br>
    <strong>Ragil Ridho Saputra (3122500016)</strong>
  </p>

  <h3 style="text-align: center;line-height: 1.5">Politeknik Elektronika Negeri Surabaya<br>Departemen Teknik
    Informatika Dan Komputer<br>Program Studi Teknik Informatika<br>2023/2024</h3>
  <hr>
  <hr>
</div>

## Daftar Isi
1. [Pendahuluan](#sistem-operasi)
2. [Soal](#soal)
3. [Referensi](#referensi)

# Sistem Operasi
Sistem operasi adalah perangkat lunak yang bertanggung jawab untuk mengelola sumber daya perangkat keras dan menyediakan
antarmuka bagi pengguna dan aplikasi untuk berinteraksi dengan komputer. Ini mengkoordinasikan tugas-tugas seperti
alokasi memori, penjadwalan CPU, manajemen file, dan penyediaan layanan jaringan, memungkinkan pengguna untuk
menjalankan program dengan efisien dan menjalankan fungsi-fungsi dasar seperti mengetik, menyimpan, dan mengakses data.

# Soal
# 1. Sebutkan dan jelaskan proses booting!
Proses booting adalah serangkaian langkah yang dilakukan oleh komputer ketika dinyalakan untuk mempersiapkan sistem agar siap digunakan. Proses ini meliputi:

1. *Menghidupkan Komputer*: Saat tombol daya ditekan, sumber daya listrik dialirkan ke komputer.
 
2. *Tes Awal (POST)*: Komputer melakukan Power-On Self-Test (POST) untuk memeriksa perangkat keras utama seperti RAM, prosesor, dan kartu grafis. Tujuannya adalah untuk memastikan bahwa semua perangkat keras berfungsi dengan baik sebelum memuat sistem operasi.

3. *Inisialisasi Perangkat Keras*: Setelah POST, komputer menginisialisasi perangkat keras seperti hard drive, keyboard, mouse, dan perangkat lainnya. Ini melibatkan pengenalan perangkat keras, pemuatan driver yang diperlukan, dan persiapan perangkat untuk digunakan.

4. *Pencarian Sektor Boot*: Komputer mencari sektor boot, area khusus di hard drive yang berisi instruksi awal untuk memuat sistem operasi.

5. *Memuat Sistem Operasi*: Setelah sektor boot ditemukan, sistem operasi dimuat ke dalam memori utama (RAM). Sistem operasi kemudian mengambil alih kendali dan mulai menjalankan program-program yang diperlukan untuk mengoperasikan komputer.

Proses booting memungkinkan komputer untuk memulai operasi normalnya dan siap digunakan oleh pengguna.

# 2. Bagaimana cara install Debian 12 di Virtualbox

1.Buka virtual box dan pilih tombol new untuk membuat virtual device
<img src="pictures/1.png">

2.Beri nama untuk project nya dan pilih iso debian yang ada di storage dan checklist kolom skip
<img src="pictures/2.png">

3.Atur berapa ram yang ingin di gunakan(sesuaikan dengan ram device) dan core cpu
<img src="pictures/3.png">

4.Jika sudah maka klik finish untuk menyelesaikan setup
<img src="pictures/4.png">

5.Akan terdapat pilihan proses booting nya debian pada halaman awal tadi
<img src="pictures/6.png">

6.Klik 2 kali dan akan memasuki proses penginstalan debian dan pilih graphic install dan akan memunculkan halaman tersebut dan pilih english
<img src="pictures/9.png">

7.Pilih yes pada bagian install the GRUB boot loader dan pilih continue
<img src="pictures/10.png">

8.Pilih Asia kemudian Indonesia sebagai lokasi kita dan klik continue
<img src="pictures/11.png">
<img src="pictures/12.png">

9.Saat konfigurasi lokal,pilih United States
<img src="pictures/13.png">

10.Pada bagian konfigurasi keyboard,pilih American English
<img src="pictures/14.png">

11.Tunggu instalasi sampai selesai,bila sudah selesai masukkan konfigurasi network untuk hostname dan untuk domain kita kosongkan
<img src="pictures/15.png">
<img src="pictures/17.png">
<img src="pictures/18.png">

12.Atur Password untuk masuk(yang mudah di ingat)
<img src="pictures/19.png">

13.Masukkan nama lengkap,username dan password(bedakan dari password sebelum nya) untuk setup user
<img src="pictures/20.png">
<img src="pictures/21.png">
<img src="pictures/23.png">

14.Pilih zona untuk jam,dan pilih Western(tergantung tempat)
<img src="pictures/24.png">

15.Untuk partition disk pilih manual dan pilih SCSI3 dan pilih yes pada create new empy partition table
<img src="pictures/25.png">
<img src="pictures/26.png">
<img src="pictures/27.png">

16.Pilih pri/log,kemudian create new partition,atur ke 20GB,pilih primary,kemudian pilih beginning dan bootable flag ubah ke on dan pilih done
<img src="pictures/28.png">
<img src="pictures/29.png">
<img src="pictures/30.png">
<img src="pictures/31.png">
<img src="pictures/33.png">
<img src="pictures/34.png">

17.Setelah di partisi menjadi beberapa bagian,kemudian pilih finish dan tunggu instalasi sampai selesai
<img src="pictures/41.png">
<img src="pictures/48.png">

18.Pilih no pada scan extra installation,pilih indonesia untuk debian archive dan pilih kebo.pens dan kosongkan http proxy
<img src="pictures/49.png">
<img src="pictures/50.png">
<img src="pictures/52.png">
<img src="pictures/53.png">

19.Tunggu konfigurasi sampai selesai
<img src="pictures/54.png">

20.Setelah selesai,pilih yes pada participate in the package,pada software selection biarkan default
<img src="pictures/55.png">
<img src="pictures/56.png">

21.Tunggu sampai proses installasi software selesai(membutuhkan waktu sedikit lama)
<img src="pictures/59.png">

22.Setelah selesai,pilih /dev/sda kemudian di halaman finish,klik continue dan debian sudah terinstall
<img src="pictures/61.png">
<img src="pictures/63.png">
<img src="pictures/65.png">

# Referensi

  [Debian Download](https://www.debian.org/download)

  [VirtualBox Download](https://www.virtualbox.org/wiki/Downloads)
