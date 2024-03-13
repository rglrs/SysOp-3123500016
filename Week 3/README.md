## Daftar Isi

1. [PPT](#ppt)
2. [FLOPS dan IOPS](#flops-dan-iops)<br>
   [Install gcc, make, dan git](#install-gcc-make-dan-git)<br>
   [How to run FLOPS dan IOPS](#how-to-run-flops-dan-iops)<br>
   [Tabel Pengujian](#tabel-pengujian)<br>
   [Analisa](#analisa)
3. [Referensi](#referensi)

## PPT

[Link PPT](https://www.canva.com/design/DAF_Q_JAZRc/i6EOGG2lMCJPxMgpVESW0g/view?utm_content=DAF_Q_JAZRc&utm_campaign=designshare&utm_medium=link&utm_source=editor)

## FlOPS dan IOPS

### Install GCC, make, dan GIT

![App Screenshot](installmakegit.jpg)

### How to run FLOPS dan IOPS

![App Screenshot](runflopsiops.jpg)

1. Ragil<br>
   Percobaan FLOPS64 5 kali<br>
   ![App Screenshot](flopsragil.jpg)<br>
   Percobaan IOPS64 5 kali<br>
   ![App Screenshot](iopsragil.jpg)<br>
2. Hana<br>
   Percobaan FLOPS64 5 kali<br>
   ![App Screenshot](flopshana.jpg)<br>
   Percobaan IOPS64 5 kali<br>
   ![App Screenshot](iopshana.jpg)<br>
3. Dio<br>
   Percobaan FLOPS64 5 kali<br>
   ![App Screenshot](flopsdio.jpg)<br>
   Percobaan IOPS64 5 kali<br>
   ![App Screenshot](iopsdio.jpg)<br>

### Tabel Pengujian

| Nama Anggota | Max Single Core FLOPS | Max Single Core IOPS | Max CPU FLOPS | Max CPU IOPS |
| ------------ | --------------------- | -------------------- | ------------- | ------------ |
| Ragil        | 6.2                   | 5.5                  | 23.2          | 22           |
| Hana         | 6                     | 6.6                  | 12.1          | 13.2         |
| Dio          | 10.8                  | 10.1                 | 21.6          | 20.2         |

#### Analisa

Berdasarkan hasil pengujian kami, kinerja sistem dalam melakukan operasi floating point 64-bit menunjukkan variasi yang signifikan, dengan throughput CPU maksimum berkisar antara 9.98 hingga 23.22 Gigaflops. Sementara itu, operasi integer 64-bit menunjukkan fluktuasi yang lebih terkendali, dengan throughput CPU maksimum berkisar antara 12.72 hingga 13.22 Gigaiops. Meskipun throughput CPU maksimum pada operasi floating point biasanya lebih tinggi daripada operasi integer, perlu diperhatikan bahwa nilai throughput maksimum pada satu inti cenderung lebih rendah daripada throughput CPU maksimum, menyoroti adanya pembatasan kinerja yang bukan hanya berasal dari kemampuan pemrosesan inti tunggal. Oleh karena itu, dalam memilih sistem untuk aplikasi tertentu, penting untuk mempertimbangkan jenis operasi yang dominan dan memilih sistem dengan throughput yang sesuai dengan kebutuhan kinerja aplikasi tersebut.

### Kesimpulan

Berdasarkan hasil pengujian kelompok kami, kinerja sistem bervariasi tergantung pada jenis operasi yang dilakukan. Operasi floating point 64-bit menunjukkan fluktuasi yang signifikan dalam throughput CPU, sementara operasi integer 64-bit menunjukkan fluktuasi yang lebih kecil. Meskipun demikian, throughput CPU maksimum pada operasi floating point biasanya lebih tinggi daripada operasi integer. Ini menyoroti pentingnya mempertimbangkan jenis operasi yang dominan dalam aplikasi yang akan dijalankan, serta memilih sistem dengan throughput yang sesuai untuk memenuhi kebutuhan kinerja aplikasi tersebut.

## Referensi

- [What's Your Computer Actually Doing?](https://www.youtube.com/watch?v=Z5JC9Ve1sfI)
- [Fetch Decode Execute Cycle in more detail](https://www.youtube.com/watch?v=jFDMZpkUWCw)
- [FLOPS dan IOPS](https://github.com/ferryastika/flops-iops)
