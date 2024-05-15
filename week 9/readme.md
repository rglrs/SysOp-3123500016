## Daftar Isi

[1. Producer Consumer Semaphore](#producer-consumer-semaphore)

[2. Producer Consumer Wake-Sleep thread](#producer-consumer-wake-sleep-thread)

## Producer Consumer Semaphore

![App Screenshot](img/1.png)

Analisa: Program ini merupakan contoh implementasi dari masalah Producer-Consumer menggunakan semaphore dalam bahasa C. Dalam program ini, terdapat tiga opsi menu: "Producer", "Consumer", dan "Exit". Ketika opsi "Producer" dipilih, program akan menciptakan data dengan maksimum tiga data. Jika pengguna terus memilih opsi "Producer" tanpa memilih opsi lain lebih dari tiga kali, program akan menampilkan pesan "Buffer your full!!". Sebaliknya, jika opsi "Consumer" dipilih dan pengguna terus memilihnya tanpa memilih opsi lain lebih dari tiga kali, program akan menampilkan pesan "Buffer is empty!!". Opsi "Exit" digunakan untuk keluar dari program.

## Producer Consumer Wake-Sleep thread

![App Screenshot](img/2.png)

Analisa : Contoh program ini mengimplementasikan permasalahan Produsen Konsumen menggunakan semaphore dan thread dalam bahasa C++. Dalam skenario ini, thread digunakan untuk menjalankan produsen dan konsumen secara bersamaan. Dengan menggunakan konsep kunci gembok (mutex) dan variabel kondisi sebagai lampu lalu lintas, program menjamin bahwa hanya satu proses yang dapat mengakses sumber daya pada satu waktu tertentu. Ketika produsen menghasilkan barang, ia memberi tahu konsumen bahwa barang baru telah tersedia. Begitu pula ketika konsumen mengonsumsi barang, ia memberi tahu produsen bahwa barang tersebut telah diambil. Dengan demikian, program memastikan bahwa proses produksi dan konsumsi berjalan dengan aman dan terkoordinasi.

### Referensi

- [Producer Consumer Problem](https://www.geeksforgeeks.org/producer-consumer-problem-in-c/)