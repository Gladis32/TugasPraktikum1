# Tugas Praktikum 1 { Pertemuan ke 6 } <img src=https://qph.fs.quoracdn.net/main-qimg-648763cc041459725b62108f4fdf5b91 width="110px" >
|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Gladis Toti Anggraini |31310566|TI.23.A5|Basis Data|

# Soal Latihan Praktikum 1
## 1. Tulis semua perintah-perintah SQL percobaan di atas beserta outputnya!
**1. Buat sebuah database dengan nama latihan2**

Untuk membuat database gunakan perintah sebagai berikut :

`CREATE DATABASE [nama_database]`

`CREATE DATABASE latihan2;`

lalu, setelah kita membuat database. kita masuk kedalam database tersebut dengan perintah sebagai berikut :

`USE latihan2;`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/membuat%20database%20dengan%20nama%20latihan2.png)

**2. Buat sebuah tabel dengan nama biodata (nama, alamat) didalam database latihan2!**

Untuk membuat Tabel gunakan perintah sebagai berikut :

`CREATE TABLE nama_tabel (
    nama_field1 tipe _data(ukuran), nama_field2 tipe_data(ukuran), ..., nama_fieldn tipe_data(ukuran)
    );`

`CREATE TABLE biodata (
    nama varchar (15),
    alamat text
    );`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/membuat%20sebuah%20tabel%20biodata.png)

**3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!**

Untuk menambahkan kolom "keterangan" dengan tipe data VARCHAR(15) sebagai kolom terakhir pada tabel "biodata", gunakan perintah sebagai berikut:

`ALTER TABLE biodata ADD COLUMN keterangan VARCHAR (15);`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/menambah%20sebuah%20kolom%20keterangan%20(varchar%2015).png)

**4.Tambahkan kolom id(int 11) di awal (sebagai kolom pertama)!**

Untuk menambahkan kolom pertama yaitu dengan perintah sebagai berikut :

`ALTER TABLE biodata ADD COLUMN id int(11) FIRST; `

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/menambahkan%20kolom%20id%20(int%2011)%20di%20awal.png)

**5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!**

Untuk menambahkan kolom setelah kolom lain yaitu dengan perintah `AFTER`

`ALTER TABLE biodata ADD COLUMN phone VARCHAR (15) AFTER alamat`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/menambahkan%20kolom%20dengan%20nama%20phone%20(varchar%2015)%20setelah%20alamat.png)

**6. Ubah tipe data kolom id menjadi char(11)!**

Untuk mengubah type data yaitu dengan perintah sebagai berikut :

`ALTER TABLE [nama_tabel] MODIFY nama_field tipe_data_baru(ukuran);`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Ubah%20tipe%20data%20kolom%20id%20menjadi%20char(11).png)

**7. Ubah nama kolom phone menjadi hp (varchar 20)!**

Untuk mengubah kolom yaitu dengan perintah sebgai berikut :

`ALTER TABLE [nama_tabel] CHANGE nama_field_lama nama_field_baru tipe_data(ukuran);`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Ubah%20nama%20kolom%20phone%20menjadi%20hp%20(varchar%2020).png)

**8. Tambahkan kolom email setelah kolom hp**

Untuk menambahkan kolom setelah kolom lain yaitu dengan perintah `AFTER`

`ALTER TABLE biodata ADD COLUMN email TEXT AFTER hp`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/menambahkan%20kolom%20email%20setelah%20kolom%20hp.png)

**9. Hapus kolom keterangan dari tabel!**

Untuk menghapus kolom dari tabel yaitu dengan perintah sebagai berikut :

`ALTER TABLE [nama_tabel] DROP nama_field;`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Hapus%20kolom%20keterangan%20dari%20tabel.png)

**10. Ganti nama tabel menjadi data_mahasiswa!**

Untuk mengganti nama tabel yaitu dengan perintah sebagai berikut :

`ALTER TABLE [nama_tabel] RENAME [nama_tabel_baru];`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Ganti%20nama%20tabel%20menjadi%20data_mahasiswa.png)

**11. Ganti nama field id menjadi nim!**

Untuk mengubah kolom yaitu dengan perintah sebgai berikut :

`ALTER TABLE [nama_tabel] CHANGE nama_field_lama nama_field_baru tipe_data(ukuran);`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Ganti%20nama%20field%20id%20menjadi%20nim.png)

**12. Jadikan nim sebagai PRIMARY KEY!**

Untuk menambahkan index atau key, gunakan perintah sebagai berikut :

tipe index :

- PRIMARY KEY
- UNIQUE KEY
- FULLTEXT

`ALTER TABLE [nama_tabel] ADD [INDEX|PRIMARY KEY] (nama_field);`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Jadikan%20nim%20sebagai%20PRIMARY%20KEY.png)

**13. Jadikan kolom email sebagai UNIQUE KEY!**

Perintah nya sama seperti diatas, hanya saja diganti menjadi `UNIQUE KEY`

![alt text](https://github.com/Gladis32/TugasPraktikum1/blob/main/ss/Jadikan%20kolom%20email%20sebagai%20UNIQUE%20KEY.png)

## 2. Apa Maksud Dari INT(11) ?

- INT(11) Adalah Nama Tipe Datanya Yaitu `Integer` dan Memiliki Panjang 11 Karakter.

## 3. Ketika Kita Melihat Struktur Tabel Dengan Perintah DESC , Ada Kolom Null yang Berisi Yes dan No. Apa Maksudnya ?

- Nilai `NULL` dalam database mewakili ketidakhadiran data untuk kolom tertentu. Kolom dengan nilai `NULL` menunjukkan bahwa tidak ada informasi yang tersedia untuk kolom tersebut dalam baris data terkait.
- Jika Null berisi `No`, maka data tersebut akan dilakukan pengisian atau penginputan. Sedangkan jika Null berisi `Yes`, maka data tersebut akan dikosongkan atau tidak dilakukan penginputan

### Sekian Tugas Praktikum Saya di Pertemuan kali ini. 

### Jika Masih Ada Yang Salah Saya Mohon Maaf.

### Wassalamualaikum wr.wb. 
