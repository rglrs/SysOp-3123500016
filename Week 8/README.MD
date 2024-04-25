## Daftar Isi

[1. Bash Tutorial](#1-bash-tutorial)

[2. Bash Variable](#bash---variable)

[3. Bash Loop File](#bash---loop-file)

[4. Bash Comments](#bash---comments)

[5. Bash Arrays](#bash---arrays)

[6. Bash Expansion](#bash---expansion)

[7. Bash Conditional Expression](#bash---conditional-expression)

[8. Bash Case Statement](#bash---case-statements)

[9. Bash Special Character](#bash---special-characters)

[10. Bash If elif else](#bash---if-elif-else)

[11. Bash Loops](#bash---loops)

[12. Bash Append Strinng](#bash---append-string)

[13. Bash Functions](#bash---functions)

[14. Bash Append Strings](#bash---append-string-1)

[15. Bash Operators](#bash---operators)

[16. Bash Number Comparation](#bash---numbers-comparasion)

[17. Bash Check Directory](#bash---check-directory)

[18. Bash File Name](#bash---file-name)

[19. Bash Split String](#bash---split-string)

[20. Bash String Length](#bash---string-length)

[21. Bash bashrc](#bash---bashrc)

[22. Bash Ternary Operator](#bash---ternary-operator)

[23. Bash Lowercase](#bash---lowercase)

[24. Bash Uppercase](#bash---uppercase)

[25. Bash Substring](#bash---substring)

[26. Bash Variable Set](#bash---variable-set)

[27. Bash Iterate Nos](#bash---iterate-nos)

## **Bash Tutorial**

**Apa itu Bash?**

Ada dua jenis mode bash

- Mode interaktif: Juga disebut penerjemah perintah, memungkinkan eksekusi perintah di terminal. Ini mengeksekusi perintah secara berurutan jika ada beberapa perintah.
  **Shell Types**

Ada berbagai jenis shell di OS Unix.

| Shell Type | Alias              | First Line  |
| ---------- | ------------------ | ----------- |
| sh         | Bourne Shell       | #!/bin/sh   |
| bash       | Bourne Again shell | #!/bin/bash |
| cshell     | C shell            | #!/bin/csh  |

**Apa perbedaan antara Bash dan shell**

Shell adalah penerjemah baris perintah, Ini adalah aplikasi untuk memberikan perintah ke berbagai sistem operasi seperti Linux, Unix, dan Mac.

Bash adalah versi shell yang disempurnakan, lapisan antara panggilan fungsi pengguna dan sistem operasi.

**Apakah bash bahasa pemrogramman?**

Bash menjalankan perintah dari terminal atau file. Ini adalah bahasa pemrograman yang beroperasi pada sistem operasi kernel Unix/Linux, berisi semua fitur untuk menulis kode lengkap.

Bash adalah tipe shell khusus yang menerima masukan dari perintah, menjalankan kode, dan memproses masukan, serta mengembalikan hasilnya.

Skrip Bash memiliki banyak kasus penggunaan, termasuk:

b. Menyinkronkan tugas untuk menyalin file

c. Menjalankan tugas cron untuk penjadwalan

## Bash - Variable

Deklarasikan variabel: Untuk membuat variabel, harus memberikan nilai pada variable tersebut.

VariableValue adalah nilai yang disimpan dalam variabel, dan dapat berupa string angka atau boolean. Simbol sama dengan (=) digunakan untuk memberikan nilai pada suatu variabel.

example: `AGE=25`

Variabel bernama AGE dibuat dan diberi nilai 25.

**Cara Mengakses Variabel di Bash**

Setelah mendeklarasikan dan menetapkan nilai ke variabel, Anda dapat mengaksesnya menggunakan simbol dolar ($) diikuti dengan nama variabel.

Syntax :

![App Screenshot](img/Variables/var3.png)

Output :

![App Screenshot](img/Variables/var4.png)

Kode di atas mendeklarasikan variabel bernama AGE dengan nilai 25 dan kemudian menggunakan echo untuk menampilkan nilai variabel AGE. Simbol dolar sebelum nama variabel sangat penting untuk mengakses nilainya.

Bagaimana Anda membuat variabel tidak dapat diperbarui?

Syntax :

![App Screenshot](img/Variables/var5.png)

AGE adalah sebuah batasan, menetapkan nilai baru akan menimbulkan kesalahan, dan pesan kesalahannya adalah AGE: bersifat hanya-baca.

Output :

![App Screenshot](img/Variables/var6.png)

**Variabel Bash tidak disetel**

Kata kunci yang tidak disetel membantu menghilangkan nilai dari variabel yang ditentukan. Variabel tetap dapat diakses tetapi mencetak nilai kosong.

Syntax :

![App Screenshot](img/Variables/var7.png)

output:

![App Screenshot](img/Variables/var8.png)

**Lingkup Variabel**

Setiap variabel yang dideklarasikan harus memiliki ruang lingkup, yang menentukan di mana variabel tersebut dapat digunakan dalam program.

Misalnya, jika suatu variabel dideklarasikan di dalam suatu fungsi, maka variabel tersebut hanya tersedia di dalam fungsi tersebut dan tidak dapat diakses di luar fungsi tersebut.

Cakupan variabel di Bash dapat didefinisikan dengan dua cara, yaitu:

- Variabel global
- Variabel lokal

**Variabel Global Bash**

Syntax :

![App Screenshot](img/Variables/var9.png)

Output: `Inside Function Age: 40
Script Age: 40`

**Bash variabel Lokal**

Variabel lokal dideklarasikan di dalam blok kode atau fungsi. Cakupan variabel-variabel ini hanya terlihat di dalam blok tempat variabel-variabel tersebut dideklarasikan.

Syntax :

![App Screenshot](img/Variables/var11.png)

Output :
`Local Variable Age: 25
Global Age: 40`

**Variable Typing**
Skrip Bash bukan bahasa yang diketik, namun Anda dapat mendeklarasikan variabel dengan tipe data menggunakan perintah mendeklarasikan Berdasarkan tipe variabel, ini memungkinkan tipe data.
variabel dideklarasikan dan diberi nilai.

Opsi berisi opsi untuk membuat tipe variabel

Array: Untuk membuat variabel array

mendeklarasikan -a variabel=

| Variable Type    | Syntax                | Description                                                      |
| ---------------- | --------------------- | ---------------------------------------------------------------- |
| Array            | `declare -a variable` | Declare an indexed array variable that stores strings            |
| Associated Array | `declare -A variable` | Declare an Associated Array                                      |
| Integer          | `declare -i variable` | Declare a numeric value to store in the variable                 |
| Readonly         | `declare -r variable` | Declare a readonly variable, cannot be changed or unset          |
| Export           | `declare -x variable` | Export the variable and make it available to all child processes |

**Shell Variable**

Variabel shell adalah variabel yang diatur oleh shell, bukan oleh pengguna. Ini diperlukan oleh shell agar dapat bekerja dengan lancar

| Variable     | Description                                                                        |
| ------------ | ---------------------------------------------------------------------------------- |
| PWD          | Current working directory                                                          |
| Set-Location | Change the working directory to new directory                                      |
| Rename-Item  | Rename a file                                                                      |
| IFS          | Internal Field Separator, by default is space, set by Shell, Used for string split |
| PATH         | Contains semicolon separated path of commands, Configured to lookup for commands   |
| UID          | Prints the User Identification number                                              |
| Home         | Home directory of the current user                                                 |

## Bash - Loop File

Terkadang, Anda ingin membaca konten file dengan pemrograman bash.

Bagaimana cara membaca file baris demi baris di bash Shell?

Syntax :

![App Screenshot](img/Loop%20File/lf1.png)

Output :

![App Screenshot](img/Loop%20File/lf2.png)

## Bash - Comments

- Komentar tunggal
- Komentar multi-baris

Komentar berguna bagi manusia, kode ditulis untuk scripting

**Komentar satu baris di bash shell**

Penting untuk menempatkan omentar satu baris pada baris terpisah untuk kejelasan.

Untuk komentar sebaris, gunakan simbol # di awal komentar. Komentar satu baris selalu dimulai dengan simbol #.

Syntax :

![App Screenshot](img/Comments/comm1.png)

Output :

![App Screenshot](img/Comments/comm2.png)

Komentar multi-baris melibatkan penggunaan lebih dari satu baris untuk komentar. Cara pertama untuk membuat komentar multi-baris adalah dengan memanfaatkan komentar satu baris yang setiap barisnya dimulai dengan simbol komentar satu baris.

Syntax :

![App Screenshot](img/Comments/comm3.png)

Output :

![App Screenshot](img/Comments/comm4.png)

## Bash - Arrays

Array di shell adalah variabel yang menyimpan lebih dari satu nilai.
Misalkan, Anda memiliki daftar nomor 1 2 3.. 10 dan ingin menyimpan nomor-nomor ini di Shell Script

Bagaimana cara mendeklarasikan dan membuat array?

Ada dua jenis array yang bisa kita buat

- array yang diindeks: elemen array disimpan dengan indeks mulai dari nol
- array terkait: array disimpan dengan pasangan nilai kunci

**Deklarasikan sebuah array**

Untuk membuat array, kita perlu mendeklarasikan sebuah array.

Sebuah indexed array dengan kata kunci mendeklarasikan dengan opsi -a atau A

Contoh array yang diindeks Dalam hal ini, nilai Array disimpan dengan indeks=0 dan seterusnya. ini dibuat dengan opsi deklarasi dan -a

Contoh array asosiatif Dalam hal ini, nilai Array disimpan dengan kunci. ini dibuat dengan opsi deklarasi dan -A

**Akses nilai array**
Array berisi indeks untuk mendapatkan elemen. Elemen array dapat diakses menggunakan sintaks di bawah ini.

    ${array_name[index]}

**Deklarasikan Array angka dan ulangi**

Array dapat berisi angka Contoh ini berisi array angka dan loop for untuk dicetak

Syntax :

![App Screenshot](img/Array/arr1.png)

Output :

![App Screenshot](img/Array/arr2.png)

**Deklarasikan Array string dan ulangi**
Array dapat berisi angka Contoh ini berisi array angka dan loop for untuk dicetak

Syntax :

![App Screenshot](img/Array/arr3.png)

Output :

![App Screenshot](img/Array/arr4.png)

**Akses elemen pertama array**

Dalam elemen Array, indeks elemen Pertama adalah nol, dan array[0] mengembalikan elemen pertama

Syntax :

![App Screenshot](img/Array/arr6.png)

Output :

![App Screenshot](img/Array/arr7.png)

**Ulangi atau ulangi elemen array**

For loop digunakan untuk mengulangi elemen.
Berikut adalah contoh contoh loop array untuk mencetak semua elemen

Syntax :

![App Screenshot](img/Array/arr8.png)

Output :

![App Screenshot](img/Array/arr9.png)

Cara lain untuk mencetak indeks dan elemen array menggunakan for loop

Syntax :

![App Screenshot](img/Array/arr10.png)

Output :

![App Screenshot](img/Array/arr11.png)

**Menambahkan elemen ke array**

Anda dapat menambahkan elemen di posisi indeks mana pun menggunakan sintaksis di bawah ini.

Contoh penambahan elemen awal dan akhir serta tengah
Syntax :

![App Screenshot](img/Array/arr12.png)

Output :

![App Screenshot](img/Array/arr13.png)

Contoh lembar contekan array

| Contoh                | Deskripsi                                                       |
| --------------------- | --------------------------------------------------------------- |
| declare -a array      | Mendeklarasikan sebuah array yang diindeks                      |
| declare -A array      | Mendeklarasikan sebuah array asosiatif                          |
| declare -a array=()   | Mendeklarasikan sebuah array yang diindeks dengan array kosong  |
| array=()              | Membuat sebuah array kosong, tanpa mendeklarasikannya           |
| array=(1 6 3)         | Menginisialisasi array dengan angka                             |
| array=(satu dua tiga) | Menginisialisasi array dengan string                            |
| array=(satu dua 1)    | Menginisialisasi array dengan data campuran                     |
| ${array[0]}           | Mendapatkan elemen pertama dari array                           |
| ${array[1]}           | Mendapatkan elemen kedua dari array                             |
| ${array[-1]}          | Mendapatkan elemen terakhir dari array                          |
| ${array[@]}           | Mendapatkan semua elemen dari array                             |
| ${array[*]}           | Mendapatkan semua elemen dari array                             |
| ${!array[*]}          | Mendapatkan semua indeks dari array                             |
| ${#array[*]}          | Panjang array                                                   |
| array[0]=12           | Menambahkan elemen ke array pada posisi pertama, yaitu indeks=0 |
| array[-1]=22          | Menambahkan elemen ke array pada posisi terakhir                |
| array+=(11)           | Menambahkan nilai ke array                                      |
| ${array[@]:k:i}       | Mendapatkan elemen indeks=1 dimulai dari indeks=k               |

## Bash - expansion

perintah dimasukkan ke OS untuk membuat panggilan sistem dan melakukan tindakan. perintah masukan pengguna di terminal untuk melakukan operasi seperti ls, cd, mkdir dll.

Cara lain, Beberapa perintah dapat ditempatkan dalam satu file, juru bahasa bash membaca perintah dan menjalankannya

Pilih Editor atau editor teks
Buat file dengan ekstensi .sh atau .bash
Tulis perintah dalam file
Simpan file sebagai `expansion.sh`

Syntax :

![App Screenshot](img/Expansion/ex1.png)

Output :

![App Screenshot](img/Expansion/ex2.png)

## Bash - Conditional Expression

in

Ada berbagai jenis ekspresi konisional di Bash

- Operator Perbandingan String
- Operator Perbandingan Numerik
- Operator File
- Operator Logis

**File Operators**

Bash menyediakan operator logika pada FIle dan direktori untuk menguji ekspresi kondisional. Ini memungkinkan Anda untuk memeriksa berbagai operasi seperti keberadaan, dan izin, ukuran. Ini digunakan ekspresi kondisional dalam pernyataan kondisional seperti if else dan case.

conditiona_expressions berisi opsi, dan jalur file, yang selalu mengembalikan nilai benar atau salah.

berikut adalah opsi yang disediakan

| Operator        | Deskripsi                                                                                                 |
| --------------- | --------------------------------------------------------------------------------------------------------- |
| -e file         | Mengembalikan nilai true jika file yang diberikan ada, di mana file bisa berupa file biasa atau direktori |
| -f file         | Mengembalikan nilai true jika file yang diberikan ada dan merupakan sebuah file (bukan direktori)         |
| -d file         | Mengembalikan nilai true jika file adalah sebuah direktori                                                |
| -r file         | Mengembalikan nilai true jika file ada dan memiliki izin baca                                             |
| -w file         | Mengembalikan nilai true jika file ada dan memiliki izin tulis                                            |
| -x file         | Mengembalikan nilai true jika file ada dan memiliki izin eksekusi                                         |
| -s file         | Mengembalikan nilai true jika file ada dan ukurannya tidak kosong                                         |
| -G file         | Mengembalikan nilai true jika file ada dan dimiliki oleh sebuah ID Grup yang cocok                        |
| -O file         | Mengembalikan nilai true jika file ada dan dimiliki oleh sebuah ID Pengguna yang cocok                    |
| -N file         | Mengembalikan nilai true jika file ada dan telah dimodifikasi sejak baca terakhir                         |
| -L file         | Mengembalikan nilai true jika file ada dan merupakan sebuah tautan simbolik                               |
| file1 -ot file2 | Mengembalikan nilai true jika file1 lebih tua dari file2, atau jika file2 ada dan file1 tidak ada         |
| file1 -ne file2 | Mengembalikan nilai true jika file1 lebih baru dari file2, file1 ada, dan file2 tidak ada                 |
| file1 -ef file2 | Mengembalikan nilai true jika file1 dan file2 menunjuk ke perangkat dan inode yang sama                   |

## Bash - Case Statements

Pernyataan case mirip dengan switch case dalam bahasa pemrograman lain.
Ini digunakan untuk membandingkan masukan yang diberikan dengan beberapa pola, dan perintah di dalam pola yang cocok dijalankan.

- ekspresi adalah variabel atau ekspresi yang valid untuk dievaluasi
- Ini berisi pola defiend di dalam case yang dievaluasi dengan membandingkan ekspresi, mencocokkan case fuound, mengeksekusi perintah di dalamnya.
- default case(\*)) untuk dieksekusi jika tidak ada pola yang cocok
- Setiap blok pola diakhiri dengan ;;
- case adalah kata awal dan esac adalah kata yang mengakhiri pernyataan case

Ini sebuah contoh

Syntax :

![App Screenshot](img/Case%20Statement/cs1.png)

Output:

![App Screenshot](img/Case%20Statement/cs2.png)

## Bash - Special Characters

Karakter khusus di bash dievaluasi dengan arti khusus dalam interpretasi suatu perintah. Karakter-karakter ini memiliki instruksi khusus, penggunaan karakter ini memiliki arti berbeda dalam konteks berbeda
**Blankspace(" "):**
Ini juga disebut spasi putih, berisi tab, spasi, kembali, baris baru. Ini memberitahu penerjemah bash untuk memisahkan perintah dan konten. Ini adalah pembatas untuk memisahkan perintah dan string.

**Expansion($)**

Simbol tanda dolar digunakan untuk berbagai jenis perluasan parameter perluasan, ($variabel, ${variabel}) Substitusi ($(ekspresi)) ekspresi artema ($((ekspresi)))

**Ambersand(&)**

Menambahkan & di akhir perintah memungkinkan Anda menjalankan perintah di latar belakang.


**Single quotes**

Single quotes (') are used to define a string without a special meaning. It means all the variables and expansion are not interepreted and print the same literal string

Syntax :

![App Screenshot](img/Special%20Characters/sc4.png)

Output :

![App Screenshot](img/Special%20Characters/sc3.png)

**Double qoutes**

Tanda kutip ganda (') digunakan untuk mendefinisikan string literal dengan arti khusus.

jika string berisi variabel dan sintaks perluasan, Ini diinterprestasikan dan diperluas, dengan nilai yang dievaluasi saat runtime.

jika string tidak ingin memperluas variabelnya, maka Anda dapat keluar dari \ sebelum simbol $ dolar

Syntax :

![App Screenshot](img/Special%20Characters/sc2.png)

Output :

![App Screenshot](img/Special%20Characters/sc1.png)

**Backslash Character( \ )**

Karakter garis miring terbalik digunakan untuk keluar dari karakter dalam string. ini digunakan dalam string yang dikutip ganda.

**Comment ( # )**

Simbol komentar digunakan untuk mengomentari sebaris kode. Baris komentar selalu dimulai dengan #.
Itu diabaikan oleh penerjemah bash.

## Bash - if elif else

Skrip Bash menyediakan ekspresi kondisional untuk mengeksekusi kode berbeda berdasarkan kondisi yang ditentukan.

**Pernyataan Bersyarat Bash Shell**
Terkadang, Anda mungkin perlu mengeksekusi beragam blok kode bergantung pada berbagai keputusan berdasarkan kondisi tertentu.

Skrip Bash memfasilitasi hal ini melalui pernyataan kondisional

**If Conditional Statements**

Pernyataan if di Bash digunakan untuk mengeksekusi blok kode ketika kondisi yang ditentukan benar.

example

Syntax :

![App Screenshot](img/If%20Elif%20Else/if1.png)

Output:

![App Screenshot](img/If%20Elif%20Else/if2.png)

**If-Else Conditional Statements**

Pernyataan kondisional if-else di Bash memungkinkan Anda mengeksekusi blok kode yang berbeda bergantung pada apakah suatu kondisi benar atau salah.

example

Syntax :

![App Screenshot](img/If%20Elif%20Else/if3.png)

Output :

![App Screenshot](img/If%20Elif%20Else/if4.png)

**If..Elif..Else Statements**

Gunakan pernyataan kondisional if..elif..else di Bash untuk mengeksekusi blok kode yang berbeda berdasarkan beberapa kondisi.

## Bash - Loops

Loop digunakan untuk mengeksekusi blok kode beberapa kali.

Misalkan Anda ingin menjalankan perintah berulang kali atau mencetak array.for loop digunakan di Bash

- for loop
- for index loop
- while loop
- until loop

**For Loop**

for loop digunakan untuk mengeksekusi kode beberapa kali berdasarkan

example

Syntax :

![App Screenshot](img/Loops/l1.png)

Output :

![App Screenshot](img/Loops/l2.png)

**For index loop**

untuk loop indeks mirip dengan bahasa C untuk loop indeks. Ini mengeksekusi kode beberapa kali berdasarkan kondisi benar, Ini dimulai dengan nilai awal dan iterasi berisi nilai yang akan bertambah 1.

example

Syntax :

![App Screenshot](img/Loops/l3.png)

Output :

![App Screenshot](img/Loops/l4.png)

**While Loop**

Perulangan while di Bash memungkinkan eksekusi kode berulang selama kondisi yang ditentukan benar. Jika kondisi menjadi salah, perulangan akan keluar.

example

Syntax :

![App Screenshot](img/Loops/l6.png)

Output :

![App Screenshot](img/Loops/l5.png)

**Until Loop**

Kata kunci sampai di Bash digunakan untuk mengeksekusi kode berulang kali hingga kondisi yang ditentukan menjadi benar, di mana loop keluar.

example

Syntax :

![App Screenshot](img/Loops/l7.png)

Output :

![App Screenshot](img/Loops/l4.png)

## Bash - Append String

**Bash Athematic expressions**

Ekspresi artema digunakan untuk melakukan operasi matematika

ekspresi adalah istilah yang digunakan dalam matematika untuk menunjukkan suatu operasi. Ini berisi operan dan operator untuk melakukan operasi matematika. `a<b` adalah ekspresi. Ini mungkin berisi operator biner atau unary Di bash, Ekspresi dibuat menggunakan tanda kurung (()) dengan operan dan operator sebagai argumen. ((a)) adalah ekspresi bash.

ekspresi adalah operasi matematika, Dapat berisi sub ekspresi yang dipisahkan dengan koma.

Syntax :

![App Screenshot](img/Append%20String/as1.png)

Output :

![App Screenshot](img/Append%20String/as2.png)

Ekspresi artema dibuat menggunakan operator di bawah ini

- Operator Artmatik
- Operator Perbandingan

Operator perbandingan digunakan untuk mengecek satu sama lain dengan membandingkan nilai Operator (<, <=, >, >=, ==, !=)

Syntax :

![App Screenshot](img/Append%20String/as3.png)

Output :

![App Screenshot](img/Append%20String/as4.png)

- Operator Logis
- Pernyataan bersyarat

**Bash Athematic Expansion**

Ekspansi sama dengan ekspresi, Ekspansi menghitung nilai ekspresi dan hasilnya diganti dengan nilai. Itu selalu diawali dengan tanda dolar.

Misalnya menghitung rata-rata dua angka, cetak hasilnya. Di sini digunakan sintaks ekspansi, Ini mengevaluasi ekspresi dan hasilnya diganti dengan output ekspresi.

Syntax :

![App Screenshot](img/Append%20String/as5.png)

Output :

![App Screenshot](img/Append%20String/as6.png)

## Bash - Functions

Fungsi adalah kode yang dapat digunakan kembali dan dikelompokkan dalam satu nama. Mendeklarasikan suatu fungsi Memanggil Fungsi Fungsi dengan argumen Cakupan variabel dalam Fungsi

**Bagaimana mendeklarasikan suatu Fungsi dan memanggilnya**

Definisi fungsi berisi beberapa baris kode yang akan dieksekusi.

Fungsi berisi nama fungsi yang diapit {}.

Itu dapat dideklarasikan dengan dua cara, yaitu

![App Screenshot](img/function/1.png)

**Cara meneruskan parameter ke suatu fungsi**

![App Screenshot](img/function/2.png)

Parameter dapat diakses menggunakan $1 $2 $3.. $n

![App Screenshot](img/function/3.png)

## Bash - Append String

**Simple variable append**

Mulailah dengan mendeklarasikan dua variabel string dalam skrip Bash, yang dapat dicetak ke konsol menggunakan echo dengan mengapit variabel dalam tanda kutip ganda.

Syntax :

![App Screenshot](img/Append%20String%202/aas1.png)

Output :

![App Screenshot](img/Append%20String%202/aas2.png)

Contoh lain melibatkan penggabungan string ke variabel yang sama dan mencetaknya ke konsol:

Syntax :

![App Screenshot](img/Append%20String%202/aas3.png)

Output :

![App Screenshot](img/Append%20String%202/aas4.png)

Operator aritmatika singkatan (+=) biasanya digunakan dalam aritmatika untuk menambahkan nilai ke suatu variabel. Ini juga dapat digunakan untuk string untuk menambahkan string ke variabel.

Misalnya.

- a+=1 setara dengan a=a+1 dalam hal angka.
- str+="test" akan menjadi str=str+"test" dalam kasus string.

Berikut adalah contoh kode

Syntax :

![App Screenshot](img/Append%20String%202/aas5.png)

Output :

![App Screenshot](img/Append%20String%202/aas6.png)

**Use printf command**

printf digunakan untuk memformat string dengan berbagai opsi pemformatan yang kompleks. Kita dapat menggunakan perintah printf untuk menggabungkan string. Formatnya adalah %s%s, yang menambahkan dua variabel string.

Syntax :

![App Screenshot](img/Append%20String%202/aas7.png)

Output :

![App Screenshot](img/Append%20String%202/aas8.png)

**Using here string**

Di sini string adalah sintaks khusus untuk meneruskan string ke perintah dalam skrip Bash. Mereka digunakan untuk meneruskan string input tanpa menggunakan sumber lain, seperti file. Ini memungkinkan meneruskan string ke perintah Bash apa pun dari file atau baris perintah.

Syntax :

![App Screenshot](img/Append%20String%202/aas9.png)

Output :

![App Screenshot](img/Append%20String%202/aas10.png)

## Bash - Operators

**Apa itu operator?**

Operator adalah simbol dalam pemrograman yang melakukan suatu operasi pada operan

Syntax :

![App Screenshot](img/Operators/1.png)

**Bash Arithmetic Operators**

Operator aritmatika di Bash menyediakan operasi aritmatika seperti operator penjumlahan, pembagian, pengurangan, dan perkalian pembagian.

| Operator | Title          | Description                                     | Example       |
| -------- | -------------- | ----------------------------------------------- | ------------- |
| +        | Addition       | Penambahan dua atau lebih operand               | p+q=50        |
| -        | Subtraction    | Pengurangan dua atau lebih operand              | q-p=10        |
| \*       | Multiplication | Perkalian dua atau lebih operand                | p\*q=600      |
| /        | Divide         | Menghasilkan hasil bagi setelah pembagian nilai | q/p=1.5       |
| %        | Modulus        | Mengembalikan sisa setelah pembagian nilai      | q%p=10        |
| -expr    | Unary Minus    | Balik dari sebuah ekspresi                      | -(10-7) is -3 |
| ~/       | Division Int   | Mengembalikan nilai pembagian int               | (10~/7) is 1  |
| ++       | Increment      | Menambahkan nilai sebesar 1                     | ++p=21        |
| --       | Decrement      | Mengurangi nilai sebesar 1                      | --q=29        |

Operator penugasan digunakan untuk menetapkan nilai ke suatu variabel. Operasi dasarnya sama dengan (=)
Selain itu, Ada operator penugasan lainnya.

misalnya, p adalah 20

| Operation           | Symbol | Description                           | Result                |
| ------------------- | ------ | ------------------------------------- | --------------------- |
| Add Assign          | +=     | Penambahan dan penugasan ke variabel  | ((p += 3)) adalah 23  |
| Substract Assign    | -=     | Pengurangan dan penugasan ke variabel | ((p -= 3)) adalah 17  |
| Multiplicate Assign | \*=    | Perkalian dan penugasan ke variabel   | ((p \*= 2)) adalah 40 |
| Division Assign     | /=     | Pembagian dan penugasan ke variabel   | ((p /= 5)) adalah 4   |

**Bitwise Operators**

| Operation      | Symbol | Description                               | Result                |
| -------------- | ------ | ----------------------------------------- | --------------------- |
| AND            | &      | Bitwise AND dari dua operand              | $op1 & $op2 adalah 0  |
| AND Equal      | &=     | Bitwise AND Equal dari dua operand        | $op1 & $op2 adalah 0  |
| OR             | \|     | Bitwise OR dari dua operand               | $op1 \| $op2 adalah 7 |
| XOR            | ^      | Bitwise XOR dari dua operand              | $op1 ^ $op2 adalah 7  |
| Left Shift     | <<     | Bitwise Left Shift dari dua operand       | $op1 & $op2 adalah 0  |
| Left Shift Eql | <<=    | Bitwise Left Shift Equal dari dua operand | $op1 \| $op2 adalah 7 |
| XOR            | ^      | Bitwise XOR dari dua operand              | $op1 ^ $op2 adalah 7  |
| XOR Equal      | ^=     | Bitwise XOR Equal dari dua operand        | $op1 ^ $op2 adalah 7  |

**Logical operators**

Operator ini digunakan untuk melakukan operasi logika pada variabel/ekspresi/data.

| Operation   | Symbol | Description                                                                                                                       | Result                |
| ----------- | ------ | --------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| Logical AND | &&     | Mengembalikan true (status keluaran=0) jika kedua operan adalah true, jika tidak, mengembalikan false (status keluaran bukan nol) | $op1 && $op2 adalah 0 |
| Logical OR  | \|\|   | Logical OR dari dua operan                                                                                                        | $op1 \| $op2 adalah 0 |
| Logical NOT | \!     | Membalikkan nilai kondisional.                                                                                                    | $op1 adalah 7         |

**String Comparision Operator**

| Operation  | Description                                               |
| ---------- | --------------------------------------------------------- |
| -z String  | Mengembalikan true jika string kosong, jika tidak, false. |
| -n String  | Mengembalikan true jika string tidak kosong.              |
| str1=str2  | Mengembalikan true jika str1 sama dengan str2.            |
| str1!=str2 | Mengembalikan true jika str1 tidak sama dengan str2.      |
| str1>str2  | Mengembalikan true jika str1 diurutkan sebelum str2.      |
| str1<str2  | Mengembalikan true jika str1 diurutkan setelah str2.      |

**Numerical Comparision Operator**

Berikut ini adalah operator Perbandingan.

menggunakan operator `-eq` dalam pernyataan kondisional `if` `fi`

Syntax :

![App Screenshot](img/Operators/op1.png)

example

Syntax :

![App Screenshot](img/Operators/op3.png)

Output :

![App Screenshot](img/Operators/op2.png)

**Other Operators**

| Operation   | Description                                                                                |
| ----------- | ------------------------------------------------------------------------------------------ |
| -v variable | Mengembalikan true jika sebuah variabel diatur nilainya, artinya nilai sudah diberikan.    |
| -o optname  | Mengembalikan true jika sebuah opsi shell (optname) diaktifkan.                            |
| -R variable | Mengembalikan true jika sebuah variabel diatur nilainya, dan itu adalah referensi bernama. |

## Bash - Numbers Comparasion

**Angka dapat berupa bilangan bulat atau angka mengambang.**

Cara Memeriksa apakah dua angka sama atau tidak di Bash
Program ini mengambil nilai masukan dan memeriksa apakah dua nilai sama atau tidak.

![App Screenshot](img/Number%20Comparison/nc1.png)

Beberapa skrip shell tidak mendukung (()), gunakan [[]] dengan operator Perbandingan

Berikut ini adalah operator Perbandingan.

- persamaan: sama

  Periksa apakah dua variabel sama

- ne : Tidak setara

  Periksa apakah dua variabel tidak sama

- lt : Kurang dari

  Periksa apakah variabel pertama lebih kecil dari variabel kedua

- le : Kurang dari sama

  Periksa apakah variabel pertama kurang dari sama dengan variabel kedua

- gt : Lebih besar dari

  Periksa apakah variabel pertama lebih besar dari variabel kedua

- ge: Lebih besar dari atau sama

  Bandingkan Periksa apakah variabel pertama lebih besar dari sama dengan variabel

kedua menggunakan operator -eq dalam pernyataan kondisional if fi

![App Screenshot](img/Number%20Comparison/nc2.png)

Anda juga dapat melakukannya dengan operator ternary.

      first=13
      second=15

      echo $(( first == second ? "equal": "not equal" ))

## Bash - Check Directory

**Skrip Bash Periksa apakah direktori tersebut ada**

Pada contoh di bawah, blok if digunakan untuk menguji ekspresi kondisional keberadaan direktori.

**Periksa apakah Direktori Ada dan Cetak Pesan**

Ekspresi kondisional menggunakan opsi `-d` untuk memeriksa apakah direktori tersebut ada.

**periksa direktori yang ada dan cetak pesannya**

Ekspresi kondisional berisi opsi `-d` dan jalur direktori. Opsi `-d` yang memeriksa apakah direktori ada atau tidak.

Example

Syntax :

![App Screenshot](img/Check%20Directory/cd1.png)

Output :

![App Screenshot](img/Check%20Directory/cd2.png)

Harap dicatat bahwa tambahkan spasi setelah [ dan sebelum -d.

Bagaimana cara mkdir hanya jika direktori belum ada?
Dalam contoh ini, menggunakan blok kondisional if-else.

Diperiksa apakah direktori tersebut ada menggunakan -d.
else blok akan memiliki kode untuk tidak ada dan membuat direktori menggunakan jalur direktori

example

Syntax :

![App Screenshot](img/Check%20Directory/cd3.png)

Output :

![App Screenshot](img/Check%20Directory/cd2.png)

**Periksa direktori yang ada menggunakan sintaks ternary**

Alternatifnya, ekspresi kondisional ternary digunakan sebagai pengganti ekspresi kondisional if.

![App Screenshot](img/Check%20Directory/cd4.png)

Periksa apakah ada beberapa direktori Terkadang, Kami ingin memeriksa apakah ada beberapa direktori.
Kita harus menggunakan pernyataan kondisional if dengan operator logika AND(&&).

**Periksa direktori ada dan dapat ditulis dan dieksekusi**

Dalam contoh ini, Kode memeriksa hal-hal di bawah ini

foldernya ada atau tidak
jika ada, Folder tersebut memiliki izin untuk menulis dan dieksekusi.
Terakhir, Cetak pesan string

Syntax :

![App Screenshot](img/Check%20Directory/cd6.png)

Output :

![App Screenshot](img/Check%20Directory/cd7.png)

**Periksa file atau direktori ada**

Terkadang, kami ingin memeriksa apakah file atau direktori tersebut ada. Opsi -e memeriksa file atau direktori untuk jalur yang diberikan ada atau tidak.

Syntax :

![App Screenshot](img/Check%20Directory/cd8.png)

Output :

![App Screenshot](img/Check%20Directory/cd9.png)

## Bash - File Name

File Name mencakup:

- Ekstrak nama file untuk path lengkap yang diberikan
- mendapatkan nama file lengkap
- Nama ekstensi

**Ekstrak nama file dengan ekstensi**

Untuk mendapatkan nama file beserta ekstensinya, perintah basename dapat digunakan untuk menghapus direktori dan hanya mengembalikan nama file untuk jalur tertentu, baik itu variabel atau string.

Misalnya, jika jalurnya adalah /home/john/run.sh, nama file yang dikembalikan adalah run.sh. Proses ini melibatkan pengambilan jalur lengkap dan hanya mengekstrak nama file dengan menghapus jalurnya. Nama file yang dihasilkan kemudian disimpan dalam variabel dan dicetak ke konsol.

nama dasar digunakan untuk menghapus direktori dan mengembalikan nama file untuk jalur yang diberikan. jalurnya adalah variabel atau string. Misalnya, jalurnya adalah /home/john/run.sh, dan nama file yang dikembalikan adalah run.sh. Dalam hal ini, jalur lengkap diberikan dan mengembalikan nama file dengan menghapus jalurnya.

Nama file disimpan ke variabel dan dicetak ke konsol.

Syntax :

![App Screenshot](img/File%20Name/fn1.png)

Output :

![App Screenshot](img/File%20Name/fn2.png)

**Ekstrak nama file tanpa ekstensi**

Untuk mendapatkan hanya nama file tanpa ekstensi, Anda dapat menggunakan sintaks ${filename%.\*}.

Misalnya, pertimbangkan jalur /home/john/run.sh, nama file yang dihasilkan adalah run.sh.

Awalnya, perintah nama dasar digunakan untuk menghilangkan direktori dan menghasilkan nama file untuk jalur yang ditentukan dan mengembalikan variabel, dan variabel ini kemudian digunakan bersama dengan sintaks ekspresi untuk menghapus ekstensi dari nama file.

Ekspresi ini secara efektif menghapus ekstensi dari nama file.

Syntax :

![App Screenshot](img/File%20Name/fn3.png)

Output :

![App Screenshot](img/File%20Name/fn4.png)

**Ekstrak ekstensi untuk jalur file**

Untuk mengisolasi ekstensi file dari jalur file yang diberikan, ${filename##\*.} dapat digunakan. Ekspresi ini hanya mengembalikan ekstensi file.

Misalnya, pertimbangkan jalur /home/john/run.sh ekstensi yang dihasilkan adalah sh.

Awalnya, perintah nama dasar digunakan untuk menghapus jalur direktori dan mengembalikan nama file untuk jalur yang ditentukan, dan nama file ini kemudian digunakan bersama dengan sintaks ekspresi untuk mengembalikan ekstensi saja.

Syntax :

![App Screenshot](img/File%20Name/fn5.png)

Output :

![App Screenshot](img/File%20Name/fn6.png)

Berikut adalah contoh komprehensif yang menunjukkan cara mendapatkan nama file dengan atau tanpa ekstensi file. Setelah menjalankan skrip di bawah ini, skrip tersebut akan dicetak

- file dengan ekstensi,
- hanya nama file tanpa ekstensi,
- dan ekstensinya saja.

Syntax :

![App Screenshot](img/File%20Name/fn7.png)

Output:

![App Screenshot](img/File%20Name/fn8.png)

## Bash - Split String

Dalam beberapa kasus, saat bekerja dengan skrip bash, timbul kebutuhan untuk memisahkan string berdasarkan pembatas dan mengekstrak beberapa string untuk diproses lebih lanjut atau disimpan dalam variabel.

Split String ini membahas tiga metode.

- Pisahkan string menggunakan perintah awk
- Gunakan variabel IFS
- Ekspansi Parameter dengan for loop

**Pisahkan string menggunakan perintah awk dalam skrip bash shell**

Perintah awk, utilitas Linux yang kompatibel dengan semua distribusi bash dan shell, digunakan untuk membagi string berdasarkan pembatas yang ditentukan.

Input diberikan menggunakan simbol pipa (|), dan contoh di bawah ini menunjukkan pemisahan string yang mengandung titik dua (:)

Syntax :

![App Screenshot](img/Split%20String/ss1.png)

Output :

![App Screenshot](img/Split%20String/ss2.png)

dibagi menggunakan variabel IFS
Di sini, string masukan terdiri dari elemen yang dipisahkan oleh tanda hubung. Variabel shell IFS (Internal Field Separator) diatur ke tanda hubung, dan string diiterasi menggunakan for loop.
Setiap elemen dicetak setelah tanda hubung dihilangkan.

Syntax :

![App Screenshot](img/Split%20String/ss3.png)

Output :

![App Screenshot](img/Split%20String/ss4.png)

**Gunakan ekspansi Parameter dan loop**

Perluasan parameter digunakan untuk mengubah nilai variabel berdasarkan opsi yang ditentukan. Dalam hal ini, variabel string diubah menjadi array. Array kemudian diiterasi menggunakan sintaks for loop, mencetak setiap elemen ke konsol:

![App Screenshot](img/Split%20String/ss5.png)

![App Screenshot](img/Split%20String/ss6.png)

## Bash - String Length

Panjang string ditentukan oleh jumlah karakter yang dikandungnya, dan umumnya mudah untuk memastikan panjangnya untuk teks normal.

String Length ini akan membahas berbagai metode untuk menghitung jumlah karakter dalam sebuah string dengan pengkodean UTF.

**Menggunakan Sintaks `${#variable}`**

Metode pertama melibatkan penggunaan sintaks ${#variable} untuk mendapatkan panjang variabel string.

Dalam hal ini, jumlah karakter dalam variabel string.

Syntax :

![App Screenshot](img//String%20Lenght/sl1.png)

Output :

![App Screenshot](img/String%20Lenght/sl2.png)

**Menggunakan Perintah wc -m**

Metode kedua melibatkan penggunaan perintah wc -m, baik secara langsung dengan string atau melalui variabel.

Syntax :

![App Screenshot](img/String%20Lenght/sl3.png)

Dalam contoh ini, echo -n "string" digunakan untuk mencetak string tanpa baris baru (opsi -n). | operator pipa mengarahkan output dari perintah sisi kiri ke perintah sisi kanan, dan wc -m menghitung jumlah karakter dalam sebuah string.

Output :

    12
    12
    12

![App Screenshot](img/String%20Lenght/sl4.png)

**Menggunakan Perintah expr Metode lain melibatkan penggunaan perintah expr untuk mencari panjang string.**

Syntax :

![App Screenshot](img/String%20Lenght/sl5.png)

Output :

![App Screenshot](img/String%20Lenght/sl6.png)

**menggunakan perintah awk Awk menyediakan cara lain untuk menghitung panjang string menggunakan ekspresi.**

Syntax :

![App Screenshot](img/String%20Lenght/sl7.png)

Output :

![App Screenshot](img/String%20Lenght/sl8.png)

## Bash - Bashrc

File .bashrc adalah file skrip bash yang dijalankan dalam kasus berikut

- menggunakan eksekusi skrip bash
- bash shell dibuka dan dimulai secara interaktif

File ini disembunyikan secara default karena file dimulai dengan . disembunyikan.

**Di mana file bashrc di Linux?**

File .bashrc adalah skrip yang dijalankan saat pengguna login. File ini terletak di direktori home pengguna.
Ini berisi variabel lingkungan dan preferensi pengguna yang akan dikonfigurasi dalam file ini.

**Bagaimana cara melihat file .bashrc?**

Anda dapat menggunakan editor Vi atau Nano untuk melihat file bashrc.

Berikut ini adalah sebuah perintah

Syntax :

    nano ~/.bashrc

Output :

![App Screenshot](img/bashrc/bash1.png)

**Di mana file bashrc berada?**

file bashrc terletak di dua tempat

- direktori home pengguna
- Direktori sistem

Dalam kasus direktori home pengguna, file ini disembunyikan secara default. Lokasinya adalah ~/.bashrc di mana ~ adalah pengguna saat ini yang login di direktori home.

Dalam kasus direktori Sistem, file ini terletak di /etc/bash.bashrc.

**Bagaimana cara memuat ulang pengaturan .bashrc tanpa keluar dan masuk kembali?**

jika Anda membuat perubahan apa pun pada file .bashrc, Perubahan tidak akan langsung terlihat. Anda harus menutup dan memulai kembali sesi bash untuk melakukan perubahan.

Bagaimana cara memuat ulang konfigurasi .bashrc tanpa login lagi? Jalankan perintah berikut di command prompt.

![App Screenshot](img/bashrc/bash2.png)

## Bash - Ternary Operator

Pemrograman Bash tidak memiliki dukungan untuk sintaks operator ternary.

Operator ternary ditulis dalam bahasa Java

    expression?value1:value2

Sintaksnya mirip dengan ekspresi kondisional if dan else. jika ekspresi benar, nilai1 dikembalikan, jika tidak, nilai2 dikembalikan.

**Cara menggunakan Operator ternary di Bash**

Ada beberapa cara kita dapat menulis sintaksis sebagai pengganti sintaksis operator ternary.

Cara pertama, gunakan if-else dengan sintaks ekspresi.

Syntax :

![App Screenshot](img/Tennary%20Operator/to1.png)

Output :

![App Screenshot](img/Tennary%20Operator/to2.png)

Cara kedua, gunakan ekspresi aritmatika menggunakan && dan || Sintaksnya adalah

    [expression1] && Expression2|| Expression3

jika ekspresi1 benar, Ekspresi2 dievaluasi, jika tidak, Ekspresi3 dievaluasi

example

Syntax :

![App Screenshot](img/Tennary%20Operator/to3.png)

Output :

![App Screenshot](img/Tennary%20Operator/to4.png)

Ada cara lain untuk menetapkan variabel, bukan ekspresi.

dengan menggunakan mari kita dapat menetapkan variabel berdasarkan hasil ekspresi kondisi

Syntax :

![App Screenshot](img/Tennary%20Operator/to5.png)

Output :

![App Screenshot](img/Tennary%20Operator/to6.png)

## Bash - Lowercase

Misalnya, jika string inputnya adalah “Selamat Datang Halo Dunia”, outputnya akan menjadi “selamat datang di dunia”.

Ada beberapa cara untuk mencapai hal ini, bergantung pada jenis dan versi Bash.

- menggunakan perintah tr

Perintah tr, kependekan dari penerjemah, adalah perintah Unix yang digunakan untuk mengubah karakter dari satu format ke format lainnya.

Sintaksnya adalah sebagai berikut:

berikut adalah sintaksnya.

    tr input_format output_format

**Berikut skrip bash shell yang menggunakan tr untuk mengubah string menjadi huruf kecil:**

Syntax :

![App Screenshot](img/Lowercase/lc1.png)

Output :

![App Screenshot](img/Lowercase/lc2.png)

Sebagai alternatif, Anda dapat menggunakan.

Syntax :

![App Screenshot](img/Lowercase/lc3.png)

Output :

![App Screenshot](img/Lowercase/lc4.png)

Catatan: tr berfungsi dengan ASCII dan tidak mendukung karakter UTF.

**- using the awk command**

To convert a string to lowercase using the awk command, the tolower function is combined with awk.

The result is then passed to the echo command using the pipe operator:

Syntax :

![App Screenshot](img/Lowercase/lc5.png)

Output :

![App Screenshot](img/Lowercase/lc6.png)

**Metode ini paling baik untuk karakter ASCII dan UTF.**

**Gunakan Perl di Bash Script Printing lc dengan Perl mengubah string menjadi huruf kecil.**

lc adalah alias untuk huruf kecil.

Syntax :

    echo "$message" | perl -ne 'print lc'

gunakan ekspansi Parameter Bash 4.0 memperkenalkan utilitas manipulasi string bawaan. Untuk mengubah string menjadi huruf kecil, cukup tambahkan dua koma pada string. Ini juga disebut sintaks perluasan parameter.
Sintaksnya adalah ${variable[options]}.

Misalnya,

Syntax :

![App Screenshot](img/Lowercase/lc9.png)

Output :

![App Screenshot](img/Lowercase/lc10.png)

Syntax :

![App Screenshot](img/Lowercase/lc11.png)

Output :

![App Screenshot](img/Lowercase/lc12.png)

Di sini, ${msg,,} menggunakan opsi ,, untuk mengonversi variabel menjadi huruf kecil.

## Bash - Uppercase

String huruf besar mengacu pada string yang berisi semua huruf dalam huruf besar.

Misalnya, jika string inputnya adalah “Selamat Datang Halo Dunia”, outputnya akan menjadi “SELAMAT DATANG DUNIA”.

Bergantung pada jenis dan versi bash, ada beberapa metode untuk mengonversi string menjadi huruf besar.

menggunakan perintah tr
Perintah tr, yang dikenal sebagai penerjemah, adalah perintah Unix yang digunakan untuk mengubah karakter dari satu format ke format lainnya.

Sintaksnya adalah sebagai berikut:

    tr input_format output_format

Berikut skrip shell untuk mengonversi ke huruf besar.

Syntax :

![App Screenshot](img/uppercase/uc1.png)

Output :

![App Screenshot](img/uppercase/uc2.png)

Cara lain untuk mengganti kode di atas

Syntax :

![App Screenshot](img/uppercase/uc3.png)

Output :

![App Screenshot](img/uppercase/uc5.png)

Catatan: tr berfungsi dengan ASCII dan tidak mendukung karakter UTF.

**- menggunakan perintah awk**

Untuk mengubah string menjadi huruf besar menggunakan perintah awk, fungsi toupper digabungkan dengan awk. Hasilnya kemudian diteruskan ke perintah echo menggunakan operator pipa:

Syntax :

![App Screenshot](img/uppercase/uc4.png)

Yang terbaik adalah bekerja dengan karakter ASCII dan UTF.

dalam versi bash 4.0 bash 4.0 menyediakan utilitas manipulasi string bawaan. Menambahkan dua tanda sirkumfleks (^) ke sebuah string akan membuat string menjadi string huruf besar.

Syntax :

![App Screenshot](img/uppercase/uc6.png)

Output :

![App Screenshot](img/uppercase/uc7.png)

**menggunakan Perl dalam skrip bash**

perintah print uc di Perl mengubah string menjadi huruf besar

    echo "$message" | perl -ne 'print uc'

Gunakan sintaks perluasan parameter Bash 4.0 menyediakan utilitas manipulasi string bawaan. Menambahkan dua tanda sirkumfleks (^) ke sebuah string menjadikannya string huruf besar, juga disebut sintaks perluasan parameter.
Sintaksnya adalah ${variable[options]}

variabel untuk dimodifikasi berdasarkan opsi. Opsi bersifat opsional yang berisi perluasan parameter

Syntax :

![App Screenshot](img/uppercase/uc8.png)

Output :

![App Screenshot](img/uppercase/uc9.png)

Sintaks perluasan parameter mengubah string menjadi huruf besar. ${message^^} berisi opsi ^^ untuk mengubah string pesan variabel menjadi huruf besar.

## Bash - Substring

Ada beberapa cara untuk melakukan pemeriksaan ini, masing-masing diuraikan di bawah ini untuk kejelasan.

**Menggunakan Operator Perbandingan untuk Memeriksa Substring ada atau tidak**

- Tentukan variabel string yang berisi teks
- Gunakan pernyataan if untuk membandingkan string dengan substring yang diinginkan menggunakan operator kesetaraan (==) dan wildcard (\*).
- Terakhir, cetak string jika substring ditemukan.

Syntax :

![App Screenshot](img/substring/sub1.png)

Output :

![App Screenshot](img/substring/sub2.png)

**Gunakan Ekspresi Reguler untuk Menemukan Substring**

Operator =~ memfasilitasi pencarian substring dalam string tertentu, digunakan dalam blok if.

Contoh kode:

![App Screenshot](img/substring/sub3.png)

**Gunakan perintah grep**

Perintah grep digunakan untuk mencari string tertentu, disalurkan ke string utama untuk perbandingan.

![App Screenshot](img/substring/sub5.png)

## Bash - Variable Set

- Check variable is set or not
- variable is empty or nonempty
- Check for the variable is an empty string or not

Berikut adalah beberapa contoh penggunaan variabel untuk harga variabel

| Variable declaration | Description                                             |
| -------------------- | ------------------------------------------------------- |
| price;               | Variabel tidak dideklarasikan dan tidak diunset         |
| price=;              | Variabel dideklarasikan tetapi tidak diunset            |
| price=3000           | Variabel dideklarasikan, diisi nilai, dan tidak diunset |
| price=(3000)         | Variabel dideklarasikan, diisi nilai, dan tidak diunset |
| unset price;         | Variabel tidak dideklarasikan dan diunset               |

**Bagaimana cara memeriksa apakah suatu variabel diatur dalam skrip bash?**

Misalnya variabelnya diset artinya,

- Itu dideklarasikan dan ditetapkan dengan kosong atau tidak kosong.
  Dalam contoh di bawah ini,
- variabel1 dideklarasikan tetapi kosong
- variabel2 tidak dideklarasikan dan tidak disetel.

Syntax :

![App Screenshot](img/Variable%20Set/vs1.png)

Output :

![App Screenshot](img/Variable%20Set/vs2.png)

Cara lain untuk memeriksa suatu variabel adalah dengan menyetel menggunakan opsi -v

Syntax :

![App Screenshot](img/Variable%20Set/vs3.png)

Output :

![App Screenshot](img/Variable%20Set/vs4.png)

**Bagaimana cara memeriksa apakah variabel tidak disetel di skrip bash?**

Misalnya variabelnya tidak disetel artinya

- Itu tidak ada dan tidak diumumkan.

Dalam contoh di bawah ini,

- variabel1 dideklarasikan tetapi kosong
- variabel2 tidak dideklarasikan dan tidak disetel.

Syntax :

![App Screenshot](img/Variable%20Set/vs5.png)

Output :

![App Screenshot](img/Variable%20Set/vs6.png)

**Cara mengecek variabel kosong atau tidak kosong**

Tutorial ini memeriksa pemeriksaan variabel dibandingkan dengan spasi dan membungkus ekspresi ini di dalam [[]].

Hal yang sama juga dapat ditulis menggunakan variabel dalam tanda kutip ganda yang dibungkus dalam tanda kurung tunggal[]

Syntax :

![App Screenshot](img/Variable%20Set/vs7.png)

Output :

![App Screenshot](img/Variable%20Set/vs8.png)

Opsi penggunaan -z lainnya untuk memeriksa variabel disetel dan kosong atau tidak kosong menggunakan kode di bawah ini

Syntax :

![App Screenshot](img/Variable%20Set/vs11.png)

Output :

![App Screenshot](img/Variable%20Set/vs12.png)

## Bash - Iterate Nos

Dalam contoh ini, Hasilkan urutan rentang angka dan simpan dalam variabel.

Terkadang, Kami ingin membuat nama file dengan nama yang berisi angka yang dihasilkan dari urutan atau rentang angka.

Hasilkan serangkaian angka dalam skrip bash
menggunakan alat seq seq menghasilkan urutan angka.

Syntax :

![App Screenshot](img/Iterate%20Nos/in1.png)

Output :

![App Screenshot](img/Iterate%20Nos/in2.png)

- menggunakan perulangan for

Syntax :

![App Screenshot](img/Iterate%20Nos/in3.png)

Output :

![App Screenshot](img/Iterate%20Nos/in4.png)

- while loop

Syntax :

![App Screenshot](img/Iterate%20Nos/in5.png)

Output :

![App Screenshot](img/Iterate%20Nos/in6.png)