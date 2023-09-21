# lapresJarKom1
1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

- Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
- Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
### jawaban
mula-mula buka file .pcapng yang telah disediakan pada modul soal

![Ss Soal1](images/Screenshot%202023-09-21%20102039.png)

kemudian filter tabel dengan menggunakan searchbar dengan bendera biru disampingnya dengan menuliskan "ftp" sehingga tabel wireshark akan menampilkan log dengan protocol FTP saja 

![Ss Soal1.1](images/Screenshot%202023-09-21%20103352.png)

untuk menyelesaikan soal a dan b,cari log yang bertuliskan request: STOR yang mana command STOR adalah command untuk mengunggah file pada protokol FTP

![Ss Soal1.2](images/Screenshot%202023-09-21%20104215.png)

lalu tekan log tersebut hingga muncul header yang berisi informasi dari  log tersebut

![Ss Soal1.3](images/Screenshot%202023-09-21%20104746.png)

lalu cari Sequence number(raw) dan Acknowledge number(raw) dari log STOR tersebut 

![Ss Soal1.4](images/Screenshot%202023-09-21%20104746.png)

pada gambar diatas telah terlihat berapa sequence number(raw) dan aknowledge number(raw) dari log STOR yang terekam.
untuk soal c dan d lakukan hal yang sama seperti yang dilakukan pada log STOR untuk mencari sequence number(raw) dan acknowledge number(raw) tapi lakukan pada log persis dibawah log STOR yang mana log tersebut merupakan log response dari request STOR pada log sebelumnya 

![Ss Soal1.5](images/Screenshot%202023-09-21%20105704.png)

![Ss Soal1.5](images/Screenshot%202023-09-21%20110334.png)

pada gambar terakhir terlihat Sequence number(raw) dan Acknowledge number(raw) dari log response dari request STOR  tersebut.Setelah mengetahui jawaban-jawaban yang dicari,kirim jawab tersebut ke netcat yang telah disediakan dengan bash(nc/ncat) 
```bash
ncat sekian.sekian sekian.sekian
```
lalu setelah submit jawaban jika benar akan mendapatkan flag dan flag tersebut dapat disubmit pada platform pratikum yang digunakan.

