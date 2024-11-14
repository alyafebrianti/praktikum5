
## Latihan 1
## Hasil Input
```Python
data_mahasiswa = []

while True:
    print("\nMasukkan data mahasiswa:")
    nama = input("Nama: ")
    nim = input("NIM: ")
    tugas = float(input("Nilai Tugas: "))
    uts = float(input("Nilai UTS: "))
    uas = float(input("Nilai UAS: "))

    nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

    data_mahasiswa.append({
        'nama': nama,
        'nim': nim,
        'tugas': tugas,
        'uts': uts,
        'uas': uas,
        'nilai_akhir': nilai_akhir
    })

    tambah = input("\nTambah data lagi? (y/t): ").lower()
    if tambah == 't':
        break

print("\nDaftar Nilai Mahasiswa:")
print("="*80)
print(f"{'Nama':<15} {'NIM':<10} {'Tugas':<10} {'UTS':<10} {'UAS':<10} {'Nilai Akhir':<10}")
print("="*80)

for mhs in data_mahasiswa:
    print(f"{mhs['nama']:<15} {mhs['nim']:<10} {mhs['tugas']:<10} {mhs['uts']:<10} {mhs['uas']:<10} {mhs['nilai_akhir']:<10.2f}")

print("="*80)

```
## Hasil Output
````Markdown
Masukkan data mahasiswa:
Nama: Alya Febrianti
NIM: 312410692
Nilai Tugas: 90
Nilai UTS: 98
Nilai UAS: 100

Tambah data lagi? (y/t): t

Daftar Nilai Mahasiswa:
================================================================================
Nama            NIM        Tugas      UTS        UAS        Nilai Akhir
================================================================================
Alya Febrianti  312410692  90.0       98.0       100.0      96.30
================================================================================
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




