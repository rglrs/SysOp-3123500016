1. [Komposisi Motherboard](#Komposisi-Motherboard)
2. [Perbedaan Legacy&UEFI](#Perbedaan-Legacy&UEFI)

# Komposisi Motherboard
1. *Socket CPU*: Ada ZIF (Zero Insertion Force), LIF (Low Insertion Force), dan AMD Socket A.
<img src="pictures/cpu.jpeg">

2. *BIOS (Basic Input-Output System)*: Program dasar yang menghubungkan motherboard dengan sistem operasi.
<img src="pictures/bios.jpeg">

3. *North Bridge Controller*: Menghubungkan slot RAM, AGP, dan socket CPU.
<img src="pictures/southnorthbrigde.jpeg">

4. *South Bridge Controller*: Mengatur peripheral seperti USB, keyboard, IDE controller, dll.
<img src="pictures/southnorthbrigde.jpeg">

5. *Konektor Power Supply Unit*: Menyambungkan motherboard dengan power supply, AT atau ATX.
<img src="pictures/konektorpowersupply.jpeg">

6. *Slot RAM*: Tempat meletakkan RAM, saat ini menggunakan tipe DDR3.
<img src="pictures/socketram.jpeg">

7. *Slot PCI*: Tempat untuk Add-on Card seperti LAN, sound, dan TV Tuner.
<img src="pictures/pci.jpeg">

8. *Slot AGP (Accelerated Graphics Port)*: Untuk AGP Card yang menampilkan grafis.
<img src="pictures/slotagp.jpeg">

9. *Slot IDE dan SATA*: IDE untuk harddisk atau floppy disk, SATA untuk serial ATA.
<img src="pictures/sata.jpeg">

10. *CMOS (Complementary Metal Oxide Semiconductor)*: Baterai yang memberi daya pada memori untuk pengaturan konfigurasi.
<img src="pictures/cmos.jpeg">

# Perbedaan Legacy&UEFI

<img src="pictures/UEFI-vs-Legacy.png">
<img src="pictures/uefi dan legacy.drawio.png">
1. Definisi
Unified Extensible Firmware Interface (UEFI) adalah proses booting pada komputer modern dengan kemampuan lebih canggih dibanding sistem Legacy. UEFI menggunakan firmware URFI untuk menyimpan EFI Service Partitions saat proses booting berlangsung. 
Sementara, Legacy adalah proses booting komputer dengan firmware BIOS yang lebih lama dan tradisional. 
2. Waktu yang Dibutuhkan
UEFI membutuhkan waktu booting yang lebih cepat. Sedangkan, Legacy lebih lama. 
3. Dukungan untuk Penyimpanan
UEFI sudah menggunakan partisi GUID Partition Table (GTP), sehingga dapat mendukung perangkat penyimpanan hingga 9 zettabytes. 
Legacy yang masih menggunakan dukungan Master Boot Record (MBR) dapat mendukung perangkat penyimpanan komputer hanya 2 TB. 
4. Keamanan
UEFI dapat mencegah pemuatan aplikasi yang tak sah atau dicurigai. Selain itu juga dapat menghambat adanya kerja dua boot karena UEFI menganggap sistem operasi adalah aplikasi. 
ADVERTISEMENT
Namun, pada Legacy, tak ada keamanan yang disediakan saat booting berlangsung, sehingga ada kemungkinan aplikasi tak sah dimuat serta terjadi dual-boot.
