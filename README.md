
## Latihan 1
## Hasil Input
```Python
data_mahasiswa = []

while True:
    print("="*23)
    print("Masukkan Data Mahasiswa")
    print("="*23)
    nama = input("Nama: ")
    nim = input("NIM: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))

    nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

    data_mahasiswa.append({
        "nama": nama,
        "nim": nim,
        "tugas": tugas,
        "uts": uts,
        "uas": uas,
        "nilai_akhir": nilai_akhir
    })

    tambah_data = input("Tambah Data(y/t)? ")
    if tambah_data == 't':
        break

# Lebar kolom untuk setiap data
print("=" * 95)
print(f"{'No'.center(5)}|{'Nama'.center(15)}|{'NIM'.center(10)}|{'Nilai Tugas'.center(13)}|{'Nilai UTS'.center(10)}|{'Nilai UAS'.center(10)}|{'Nilai Akhir'.center(10)}")
print("=" * 95)

for i, mhs in enumerate(data_mahasiswa, start=1):
    print(f"{str(i).center(5)}|{mhs['nama'].center(15)}|{mhs['nim'].center(10)}|{str(mhs['tugas']).center(13)}|{str(mhs['uts']).center(10)}|{str(mhs['uas']).center(10)}|{format(mhs['nilai_akhir'], '.2f').center(10)}")

```
## Hasil Output
````Markdown
=======================
Masukkan Data Mahasiswa
=======================
Nama: Alya  
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? y
=======================
Masukkan Data Mahasiswa
=======================
Nama: aldi
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? y
=======================
Masukkan Data Mahasiswa
=======================
Nama: sela
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? y
=======================
Masukkan Data Mahasiswa
=======================
Nama: khusnul
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? y
=======================
Masukkan Data Mahasiswa
=======================
Nama: uswah
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? y
=======================
Masukkan Data Mahasiswa
=======================
Nama: veli
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? y
=======================
Masukkan Data Mahasiswa
=======================
Nama: agus
NIM: 3124
Nilai Tugas: 99
Nilai UTS: 99
Nilai UAS: 99
Tambah Data(y/t)? t
===============================================================================================
  No |      Nama     |   NIM    | Nilai Tugas |Nilai UTS |Nilai UAS |Nilai Akhir
===============================================================================================
  1  |      Alya     |   3124   |     99.0    |   99.0   |   99.0   |  99.00
  2  |      aldi     |   3124   |     99.0    |   99.0   |   99.0   |  99.00   
  3  |      sela     |   3124   |     99.0    |   99.0   |   99.0   |  99.00
  4  |    khusnul    |   3124   |     99.0    |   99.0   |   99.0   |  99.00
  5  |     uswah     |   3124   |     99.0    |   99.0   |   99.0   |  99.00
  6  |      veli     |   3124   |     99.0    |   99.0   |   99.0   |  99.00
  7  |      agus     |   3124   |     99.0    |   99.0   |   99.0   |  99.00
 
````
## Penjelasan Hasil Pemrograman Sederhana
## Analisis Kode Python untuk Input dan Perhitungan Nilai Mahasiswa

Kode di atas merupakan implementasi sederhana dalam Python untuk

1. Membuat input data mahasiswa: Pengguna secara berulang diminta untuk memasukkan nama, NIM, dan nilai-nilai tugas, UTS, serta UAS.
2. Menghitung nilai akhir: Nilai akhir dihitung berdasarkan bobot masing-masing komponen nilai (tugas, UTS, UAS).
3. Menyimpan data dalam list: Setiap data mahasiswa disimpan dalam bentuk dictionary (kamus) dan kemudian ditambahkan ke dalam list `data_mahasiswa`.
4. Menampilkan data: Setelah semua data dimasukkan, program akan menampilkan daftar nilai mahasiswa dalam bentuk tabel yang terformat.

Penjelasan Lebih Detail:

`data_mahasiswa = []`: Membuat list kosong untuk menyimpan data mahasiswa.
`while True:`: Looping tak terbatas untuk terus meminta input data hingga pengguna memilih untuk berhenti.
`input()`: Fungsi untuk mengambil input dari pengguna.
`float()`: Mengubah inputan nilai tugas, UTS, dan UAS menjadi tipe data float (bilangan desimal).
`.append()`: Menambahkan dictionary yang berisi data mahasiswa ke dalam list `data_mahasiswa`.
`f-string`: Digunakan untuk format output dengan cara yang lebih mudah dan fleksibel.
`:<15`: Menentukan lebar kolom untuk setiap data, misalnya `nama` akan memiliki lebar 15 karakter.
`.2f`: Memformat nilai akhir dengan 2 angka di belakang koma.




