### Tugas Praktikum 5
### Program Menghitung Nilai Mahasiswa Menggunakan Dictionary
```
Pada praktek kali ini, saya mencoba membuat program menentukan nilai mahasiswa dengan menggunakan Dictionary.

    Source Code dan Penjelasan

dataMhs = {}                                                                                     ## Membuat Dictionary kosong
print("==================================================================")
print("|      PROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN DICTIONARY      |")
print("==================================================================")

while True:                                                                                      ## LOOPING AKTIF
    c = input("\nA)dd, E)dit, S)earch, D)elete L)ist, Q)uit: ")                                  ## Membuat Menu

    ## MENU ADD
    if (c.lower() == 'a'):                                                                       ## MENU ADD
        print("\n=========================")
        print("| TAMBAH DATA MAHASISWA |")
        print("=========================")
        nama          = input("Masukkan Nama        : ")                                         ## Menginput Nama
        nim           = input("Masukkan NIM         : ")                                         ## Menginput NIM
        nilaiTugas    = int(input("Masukkan Nilai Tugas : "))                                    ## Menginput Nilai Tugas
        nilaiUts      = int(input("Masukkan Nilai UTS   : "))                                    ## Menginput Nilai UTS
        nilaiUas      = int(input("Masukkan Nilai UAS   : "))                                    ## Menginput Nilai UAS
        nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)              ## Menghitung Nilai Akhir
        dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir                          ## Menambahkan data yang sudah diinput ke Dictionary
        print("\nData Berhasil Ditambahkan!")

    ## MENU EDIT
    elif (c.lower() == 'e'):                                                                     ## Menu EDIT
        print("\n=======================")
        print("| EDIT DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukkan Nama: ")                                                          ## Cari nama yang akan diedit
        if nama in dataMhs.keys():                                                               ## Mengambil key dari Dictionary
            nim           = input("Masukkan NIM Baru         : ")                                ## Menginput NIM baru
            nilaiTugas    = int(input("Masukkan Nilai Tugas Baru : "))                           ## Menginput Nilai Tugas Baru
            nilaiUts      = int(input("Masukkan Nilai UTS Baru   : "))                           ## Menginput Nilai UTS Baru
            nilaiUas      = int(input("Masukkan Nilai UAS Baru   : "))                           ## Menginput Nilai UAS Baru
            nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)          ## Menghitung Nilai Akhir Baru
            dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir                      ## Mengupdate data ke Dictionary
            print("\nData Berhasil Di Update!")
        else:                                                                                    
            print("Data tidak ditemukan!")                                                       ## Jika nama tidak ditemukan maka muncul perintah tsb.

    ## MENU SEARCH
    elif (c.lower() == 's'):                                                                     ## Menu SEARCH
        print("\n=======================")
        print("| CARI DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukan Nama:  ")                                                          ## Masukkan nama yang akan dicari
        if nama in dataMhs.keys():                                                               ## Mengambil keys dari Dictionary
            print("\n                   DAFTAR NILAI MAHASISWA                   ")
            print("==============================================================")
            print("|     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==============================================================")
            print("| {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(nama, nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir)) ## Format tabel
            print("==============================================================")
        else:
            print("Datanya {0} Tidak Ada ".format(nama))                                        ## Jika data tidak ditemukan, akan muncul perintah tsb.

    ## MENU DELETE
    elif (c.lower() == 'd'):                                                                    ## Menu DELETE
        nama = input("Masukkan Nama:  ")                                                        ## Masukkan nama yang akan didelete
        if nama in dataMhs.keys():                                                              ## Mengambil keys dari Dictionary
            del dataMhs[nama]                                                                   ## Menghapus data yang dipilih
            print("Data Telah dihapus!")
        else:
            print("Data Mahasiswa Tidak Ada".format(nama))                                      ## Jika data tidak ditemukan, akan muncul perintah tsb.

    ## MENU LIST
    elif (c.lower() == 'l'):                                                                    ## Menu LIST
        if dataMhs.items():                                                                     ## Mengambil items dari Dictionary
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            i = 0
            for x in dataMhs.items():
                i += 1
                print("| {6:2} | {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))  ## Format tabel
            print("==================================================================")
        else:
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            print("|                          TIDAK ADA DATA!                       |")
            print("==================================================================")        ## Jika data masih kosong, akan muncul pesan tsb.

    ## MENU KELUAR PROGRAM
    elif (c.lower() == 'q'):                                                                   ## Menu QUIT
        print("\n Alfansha Abiftyo Hadyatama \n 311910321 \n TI.19.A.2")
        break                                                                                  ## Mengakhiri LOOPING

    else:
        print("Pilih menu yang tersedia: ")                                                    ## Jika menu yang dipilih tidak valid, akan muncul pesan tsb.
  ```      
### Flowchart
![flowchart](https://user-images.githubusercontent.com/56286071/72213297-ed9cf900-351e-11ea-9de2-5b272e1a76ca.png)


### Screenshot Input
Input(1)
<img width="960" alt="Input" src="https://user-images.githubusercontent.com/56286071/72205221-15ef0e00-34b3-11ea-9696-9447f74f2202.png">

Input(2)
<img width="960" alt="Input2" src="https://user-images.githubusercontent.com/56286071/72205277-a62d5300-34b3-11ea-81ff-191761bc3240.png">

Input(3)
<img width="960" alt="Input3" src="https://user-images.githubusercontent.com/56286071/72205304-25228b80-34b4-11ea-8507-8048cd9e6aea.png">

Input(4)
<img width="960" alt="Input4" src="https://user-images.githubusercontent.com/56286071/72205311-3b304c00-34b4-11ea-96d7-e1270f29e517.png">

Input(5)
<img width="960" alt="Input5" src="https://user-images.githubusercontent.com/56286071/72205319-4e431c00-34b4-11ea-8c12-60ec3d91ce69.png">

### Screenshot Output
-ADD & LIST
<img width="960" alt="Output Add dan List" src="https://user-images.githubusercontent.com/56286071/72205398-12f51d00-34b5-11ea-9c36-e37f197b93b2.png">

-SEARCH & EDIT
<img width="960" alt="Output Search dan Edit" src="https://user-images.githubusercontent.com/56286071/72205401-243e2980-34b5-11ea-8b37-8aae07d3f626.png">

-DELETE & QUIT
<img width="960" alt="Output Delete dan Quit" src="https://user-images.githubusercontent.com/56286071/72205408-33bd7280-34b5-11ea-8a1a-9897df83690b.png">
