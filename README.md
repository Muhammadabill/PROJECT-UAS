# Program Data Mahasiswa
Program ini adalah project sederhana untuk mengelola data mahasiswa menggunakan konsep modular dan OOP (Object-Oriented Programming). Program ini memungkinkan pengguna untuk menambahkan data mahasiswa, menampilkan data mahasiswa dalam bentuk tabel, serta memvalidasi input untuk memastikan data yang dimasukkan benar.
![400499318-c84b1d08-f2c1-4de7-adfc-e41fc129b276](https://github.com/user-attachments/assets/3fdaf322-bfbf-43f2-854b-a5892da6a7d8)

# Fitur Utama
1. Penambahan Bagian Deskripsi Fitur Utama: Sebelum meminta input dari pengguna, kita dapat menampilkan informasi tentang fitur-fitur utama yang dimiliki program ini, seperti:
- Memasukkan nama pelanggan dan tanggal pembelian.
- Menghitung total harga berdasarkan jumlah meja.
- Menampilkan hasil transaksi dalam format yang rapi.
2. Menambahkan Fitur Utama dalam Output: Fitur ini bisa ditampilkan di awal agar pengguna mengetahui apa yang bisa dilakukan oleh aplikasi ini.


# Struktur Program
1. ```Class Table```
Kelas ini bertanggung jawab untuk mengelola informasi terkait jumlah meja dan harga per unit meja.

```__init__(self, quantity)```: Konstruktor ini menerima argumen quantity (jumlah meja) dan menginisialisasi dua atribut:

```self.quantity```: Menyimpan jumlah meja yang diminta.
```self.price_per_unit```: Menyimpan harga per unit meja (diatur ke 10.000).
```total_price(self)```: Fungsi ini menghitung total harga berdasarkan jumlah meja yang diminta dan harga per unit. Fungsi ini mengembalikan hasil perkalian antara ```self.quantity``` dan ```self.price_per_unit.```
![Screenshot 2025-01-07 124710](https://github.com/user-attachments/assets/a58ca9b4-6fa4-49ec-adb3-b525d721651b)

2. ```Class View```
Kelas ini bertanggung jawab untuk menampilkan informasi kepada pengguna (output).

```display_table(customer_name, date, quantity, total_price)```: Fungsi statis ini menerima empat argumen:
```customer_name```: Nama pelanggan.
```date```: Tanggal yang diinput.
```quantity```: Jumlah meja yang dibeli.
```total_price```: Total harga dari meja.
Fungsi ini kemudian mencetak output dalam format yang telah ditentukan, berupa tabel yang menyajikan informasi transaksi seperti nama pelanggan, tanggal, jumlah meja, dan total harga.
![Screenshot 2025-01-07 124949](https://github.com/user-attachments/assets/2863934f-39f0-438a-bab0-4c9c45d1343f)

3. ```Class Process```
Kelas ini bertanggung jawab untuk memvalidasi input yang dimasukkan oleh pengguna.

```validate_input(input_value)```: Fungsi ini menerima argumen input_value yang merupakan input pengguna untuk jumlah meja. Fungsi ini mencoba mengkonversi input menjadi ```tipe data integer (int)```, dan jika input tersebut tidak valid (misalnya input bukan angka atau angka yang lebih kecil dari 1), maka fungsi ini akan mengeluarkan pesan error dan mengembalikan None.

```validate_date(input_date)```: Fungsi ini menerima argumen input_date yang merupakan input pengguna untuk tanggal. Fungsi ini mencoba mengkonversi input tanggal dalam format ```MM/YYYY (bulan/tahun)``` menjadi objek datetime. Jika format tidak sesuai, maka akan muncul pesan kesalahan dan fungsi ini akan mengembalikan None. Jika valid, fungsi ini mengembalikan tanggal dalam format yang lebih ramah pengguna (misalnya "Januari 2025").
![Screenshot 2025-01-07 125156](https://github.com/user-attachments/assets/e1f04089-c467-4228-abf3-f2cf8623806d)

4. ```Fungsi main()```
```Fungsi main()``` adalah fungsi utama yang menjalankan program ini. Berikut adalah langkah-langkah yang dilakukan di dalamnya:

Input dari pengguna:

Pengguna diminta untuk memasukkan nama pelanggan ```(customer_name)```.
Pengguna diminta untuk memasukkan jumlah meja ```(user_input)```.
Pengguna diminta untuk memasukkan tanggal dalam format ```MM/YYYY (date_input)```.
Validasi input:

Fungsi ```Process.validate_input(user_input)``` digunakan untuk memvalidasi apakah input untuk jumlah meja valid ```(angka positif)```.
Fungsi ```Process.validate_date(date_input)``` digunakan untuk memvalidasi apakah input untuk tanggal valid ```(dalam format yang tepat)```.
Proses data:

Jika validasi berhasil, objek Table dibuat menggunakan jumlah meja yang dimasukkan oleh pengguna, dan total harga dihitung menggunakan metode ```total_price()```.
Tampilkan hasil:

Hasil transaksi, yang mencakup nama pelanggan, tanggal, jumlah meja, dan total harga, ditampilkan dengan menggunakan metode ```View.display_table()```.
![Screenshot 2025-01-07 125459](https://github.com/user-attachments/assets/b0556fce-4fee-4017-a768-951f5bc9e8c1)


# Contoh Output
Tambah Table
```
Masukan nama pembeli
Masukan jumlah table
Masukan Tanggal
```
![Screenshot 2025-01-07 125706](https://github.com/user-attachments/assets/2d547cd8-c85c-45ff-807c-2de71c9d618a)

Tampilkan Table
```
+-------------------------------------------------+
|                     Hasil                       |
+-------------------------------------------------+
| Nama Pelanggan:                                 |
| Tanggal:                                        |
| Jumlah Table:                                   |
| Total Harga: Rp                                 |
+-------------------------------------------------+
```
![Screenshot 2025-01-07 125747](https://github.com/user-attachments/assets/f998fb3f-5f04-464a-a909-f1b384c35ad0)

# Teknologi Yang Digunakan
- Pyhton: Bahasa Pemrograman utama.
