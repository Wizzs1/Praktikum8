Nama  : Wisnu Ikhwansyah saputra

Nim   : 312210305

Kelas : TI 22.A3

---

# Praktikum 8
## Latihan 1

*)Kode program menggunakan Lambda :
    
    import math

    a = lambda x: x ** 2
    print(a(46))

    b = lambda x,y: x**2 + y**2
    print(b(4,6))

    c = lambda *args : sum(args)/len(args)
    print(c(5,7,9,11,10))

    d = lambda s: "".join(set(s))
    print(d("Tertimpa"))
    
Outputnya :
    
<img width="184" alt="12" src="https://user-images.githubusercontent.com/110619093/206646300-cb0308e1-2563-4bab-8cf2-6f9c3d3f1d7c.png">

---

## Praktikum 8

Masukan input sebagai berikut :

    data = {}


    class Data():
        def __init__(self, nim, nama, tugas, uts, uas, akhir):
            while True:

                print("\n")
                print('=' * 43)
                print('             DATA MAHASISWA              ')
                print('=' * 43)
                print('Menu Utama Data Mahasiswa : \n')
                print('|1| Input Data Mahasiswa        ')
                print('|2| Tampilkan Data Mahasiswa    ')
                print('|3| Ubah Data Mahasiswa         ')
                print('|4| Hapus Data Mahasiswa        ')
                print('|5| Keluar                      \n')

                x = input("> PILIH MENU : ")

                print("\n")

                if x == '1':
                    self.TAMBAH()
                elif x == '2':
                    self.TAMPILKAN()
                elif x == '3':
                    self.UBAH()
                elif x == '4':
                    self.HAPUS()
                elif x == '5':
                    self.KELUAR()

                else:
                    exit()

       def TAMBAH(self):
            print("Tambah Data")
            self.nim = input('Nim Mahasiswa\t    : ')
            self.nama = input('Nama Mahasiswa\t    : ')
            self.tugas = int(input('Masukkan Nilai Tugas\t   : '))
            self.uts = int(input('Masukkan Nilai UTS\t   : '))
            self.uas = int(input('Masukkan Nilai UAS\t   : '))
            self.akhir = (self.tugas * 30 / 100) + (self.uts * 35 / 100) + (self.uas * 35 / 100)
            data[self.nim] = self.nama, self.tugas, self.uts, self.uas, self.akhir


    class mahasiswa(Data):

        def TAMPILKAN(self):
            if data.items():
                print(
                    '==================================================================================================================')
                print('|   NO  |    NIM         |     NAMA        |  TUGAS  |   UTS   |   UAS   |     AKHIR    |')
                print(
                    '==================================================================================================================')
                i = 0
                for a in data.items():
                    i += 1
                    print(
                        "|    {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |    {5:6.2f}    |".format(a[0][: 14],
                                                                                                                a[1][0],
                                                                                                                a[1][1],
                                                                                                                a[1][2],
                                                                                                                a[1][3],
                                                                                                                a[1][4],
                                                                                                                no=i))
                    print(
                        '===============================================================================================================')

        def UBAH(self):
            print("Ubah Data")
            self.nim = input("Masukkan Nim              : ")
            if self.nim in data.keys():
                self.nama = input("Masukkan Nama\t        : ")
                self.tugas = int(input("Nilai tugas\t   : "))
                self.uts = int(input("Nilai UTS\t       : "))
                self.uas = int(input("Nilai UAS\t       : "))
                self.akhir = (self.tugas * 30 / 100) + (self.uts * 35 / 100) + (self.uas * 35 / 100)
                data[self.nim] = self.nama, self.tugas, self.uts, self.uas, self.akhir
            else:
                print("MAAF, DATA TIDAK DITEMUKAN")

        def HAPUS(self):
            print("Hapus Data")
            self.nim = input("masukkan Nim  : ")

            if self.nim in data.keys():
                del data[self.nim]
            else:
                print("MAAF, DATA TIDAK DITEMUKAN")

        def KELUAR(self):
            print()
            print("---------------------------------------------------------------------------------")
            print("                           PROGRAM TELAH SELESAI                    ")
            print("---------------------------------------------------------------------------------")
           print(35 * '=')
            print("NAMA\t: Wisnu Ikhwansyah Saputra\nKELAS\t: TI.22.A3\nNIM\t: 312210305")
            print(35 * '=')


    datamhs = mahasiswa("nama", "nim", "uts", "uas", "tugas", "akhir")
    
    
Outputnya Memasukan Data :

<img width="268" alt="14" src="https://user-images.githubusercontent.com/110619093/206647432-1368b44e-c60c-4db8-a2a8-44dd13412a1b.png">

Output Melihat Data :

<img width="743" alt="15" src="https://user-images.githubusercontent.com/110619093/206647488-289a1c61-f780-42ff-99f5-401252f820f1.png">









