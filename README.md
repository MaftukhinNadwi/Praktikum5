 # Pertemuan10
 <p> Nama   :   Maftukhin Jafar Nadwi <p>
 <p> NIM    :   312210704
 <p> Kelas  :   TI.22.C9 <p>

 ## Latihan 1
<p> berikut programnya <p>

 ```python
 kontak={'Ari': '081267888', 'Dina': '087677776'}
print("=======================")
print("      DAFTAR KONTAK    ")
print("=======================")    
print("# Nama   |   No Telpon")
print("=======================")
print("# Ari    | ",   kontak['Ari'])
print("# Dina   | ", kontak['Dina'])
print("Menampilkan kontaknya Ari")
print("Ari      | ", kontak['Ari'])  # menampilkan kontak Ari
print("Menambahkan kontak baru")
kontak['Riko']='087654544' # menambah kontak baru
print("=======================")
print("      DAFTAR KONTAK    ")
print("=======================") 
print("# Nama   |   No Telpon")
print("=======================")
print("# Ari    | ",   kontak['Ari'])
print("# Dina   | ", kontak['Dina'])
print("# Riko   | ", kontak['Riko'])
print("Mengubah kontak Dina")
kontak['Dina']= '088999776' # Mengubah kontak Dina
print("Dina     | ", kontak['Dina']) 
print("Menampilkan semua nama")
print(kontak.keys())  # Menampilkan semua nama
print("Menampilkan semua no")
print(kontak.values())  # Menampilkan semua No
print("Menampilkan daftar nama dan nomornya")
print(kontak.items())  # Menampilkan daftar kontak
print("Menghapus kontak Dina")
del kontak['Dina'] # Menghapus kontak Dina
print(kontak.items())
 ```

 <p> kemudian run, hasilnya seperti ini <p>

 ![Untitled01](https://user-images.githubusercontent.com/124107247/217941225-223ff075-03a6-4bb5-94df-5096a0ac789f.png)


 ## Praktikum 5

 <p> Berikut soalnya <p>

 ![1675976835483](https://user-images.githubusercontent.com/124107247/217939767-9f1a3616-a061-4c2b-b856-a80258e76dc1.jpg)


 <p>berikut programnya<p>

  ```python
  dataMahasiswa = {}
print("==================================================================")
print("|      PROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN DICTIONARY      |")
print("==================================================================")
while True:
    c = input("\nA)dd, E)dit, S)earch, D)elete L)ist, Q)uit: ")
```
<p> kemudian muncul menu pilihan seperti ini <p>

![a](https://user-images.githubusercontent.com/124107247/217941448-0efec203-4c26-4f1e-ba36-8a40b63a4e42.png)

## Menu ADD (menambahkan data)
<p> berikut program nya <p>

```python
    if (c.lower() == 'a'):
        print("\n=========================")
        print("| TAMBAH DATA MAHASISWA |")
        print("=========================")
        nama          = input("Masukkan Nama        : ")
        nim           = input("Masukkan NIM         : ")
        nilaiTugas    = int(input("Masukkan Nilai Tugas : "))
        nilaiUts      = int(input("Masukkan Nilai UTS   : "))
        nilaiUas      = int(input("Masukkan Nilai UAS   : "))
        nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
        dataMahasiswa[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
        print("\nData Berhasil Ditambahkan!")
```

<p> kemudian run, ketik huruf a. maka kita bisa menambahkan data. kemudian isi nama, nim, dan nilai nilainya.<p>
<p> berikut hasil run <p>

![Untitled10](https://user-images.githubusercontent.com/124107247/217942657-07d164d5-9643-40b6-b1ba-462ed2ce05c5.png)


## Menu EDIT (untuk mengubah data)
<p> berikut program nya <p>

```python
elif (c.lower() == 'e'):
        print("\n=======================")
        print("| EDIT DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukkan Nama: ")
        if nama in dataMahasiswa.keys():
            nim           = input("Masukkan NIM Baru         : ")
            nilaiTugas    = int(input("Masukkan Nilai Tugas Baru : "))
            nilaiUts      = int(input("Masukkan Nilai UTS Baru   : "))
            nilaiUas      = int(input("Masukkan Nilai UAS Baru   : "))
            nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
            dataMahasiswa[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
            print("\nData Berhasil Di Update!")
        else:
            print("Data tidak ditemukan!")
```

<p> kemudian ubah data yang datanya sudah diinputkan seperti ini <p>

![Untitled30](https://user-images.githubusercontent.com/124107247/217944656-79419968-2c2a-41f4-893a-ebc84c7e1d77.png)


## Menu SEARCH (untuk mencari data)
<p> berikut program nya <p>

```python
  elif (c.lower() == 's'):
        print("\n=======================")
        print("| CARI DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukan Nama:  ")
        if nama in dataMahasiswa.keys():
            print("\n                   DAFTAR NILAI MAHASISWA                   ")
            print("==============================================================")
            print("|     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==============================================================")
            print("| {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(nama, nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir))
            print("==============================================================")
        else:
            print("Datanya {0} Tidak Ada ".format(nama))
```
<p> kamudian ketik nama yang ingin dicari datanya seperti ini <p>

![Untitled40](https://user-images.githubusercontent.com/124107247/217945776-f2f10fcf-6ab4-427e-a240-aec24a48c788.png)


## Menu DELETE (Menghapus data)
<p> berikut program nya <p>

```python
  elif (c.lower() == 'd'):
        nama = input("Masukkan Nama:  ")
        if nama in dataMahasiswa.keys():
            del dataMahasiswa[nama]
            print("Data Telah dihapus!")
        else:
            print("Data Mahasiswa Tidak Ada".format(nama))
```
<p> kemudian ketik nama yang data nya akan diapus, seperti ini <p>

![Untitled50](https://user-images.githubusercontent.com/124107247/217945845-a52f7649-b681-4284-a8c3-aa36b8b0998c.png)


## Menu list (melihat data)
<p> berikut programnya <p>

```python
    elif (c.lower() == 'l'):
        if dataMahasiswa.items():
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            i = 0
            for x in dataMahasiswa.items():
                i += 1
                print("| {6:2} | {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
            print("==================================================================")
        else:
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            print("|                          TIDAK ADA DATA!                       |")
            print("==================================================================")
```

<p> untuk melihat data ketik l , seperti berikut <p>
![Untitled300](https://user-images.githubusercontent.com/124107247/217949671-d8837299-16d1-44a6-9938-256e453530e0.jpg)


## Menu Quit (mengkhiri program)
<p> berikut programnya <p>

```python
  elif (c.lower() == 'q'):
        print("\n Maftukhin Jafar Nadwi \n 312210704 \n TI.22.C9")
        break
    else:
        print("Pilih menu yang tersedia: ")
```

![Untitled60](https://user-images.githubusercontent.com/124107247/217947333-a3bc0dc8-4801-4dca-91b9-2fa1bb5b4e68.png)
<P>makasi<p>
