## use python 3.4.2
## script ini menggunakan fungsi function

## output berupa tabel yang diimport dari sebuah module texttable, modulenya bisa dilihat di sini https://pypi.python.org/pypi/texttable/0.8.4
```javascript
import texttable as tt
```
## fungsi dengan paramater 'nilai_mahasiswa' yang nantinya akan dipanggil saat dieksekusi
```javascript
def nilai_mahasiswa():
    nama = []
    nim = []
    nilai_tugas = []
    nilai_uts = []
    nilai_uas = []
    nilai_akhir = []

    x = [[]]

    jawab = "y"
```
## di sini texttable hanya ditulis 'tt' karena sebelumnya sudah dimainkan 'as'
```javascript
    tab = tt.Texttable()
```
## script untuk menambahkan data, di sini menggunakan fungsi 'append'
```javascript
    while (jawab == 'y'):
        nama.append(input("Masukkan Nama: "))
        nim.append(input("Masukkan Nim: "))
        tugas = int(input("Nilai Tugas: "))
        tugas = float(tugas)
        nilai_tugas.append(tugas)
        uts = int(input("Nilai UTS: "))
        uts = float(uts)
        nilai_uts.append(uts)
        uas = int(input("Nilai UAS: "))
        uas = float(uas)
        nilai_uas.append(uas)
        hasil = (tugas+uts+uas)/3
        nilai_akhir.append(hasil)
        jawab = input("Tambah data [y/n]?  ")
```
## fungsi untuk perulangan
```javascript
    for i in nama:
        idx = nama.index(i)
        x.append([idx+1,nama[idx],nim[idx],nilai_tugas[idx],nilai_uts[idx],nilai_uas[idx],nilai_akhir[idx]])
    tab.add_rows(x)
```
## fungsi agar tabel rata kiri
```javacript
    tab.set_cols_align(['l','l','l','r','r','r','r'])
```
## tampilan pada kolom tab (tab header)
```javascript
    tab.header(['No','Nama','Nim','Nilai Tugas', 'Nilai UTS', 'Nilai UAS','Nilai Akhir'])
```
## perintah untuk mengeksekusi tabel
```javascript
    print (tab.draw())
```
## untuk memanggil function yang telah dibuat di atas
```javascript
nilai_mahasiswa()
```

## Demikian penjelasan singkat dari saya, semoga bermanfaat. Selamat mencoba...
