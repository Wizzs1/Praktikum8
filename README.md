Nama  : Wisnu Ikhwansyah saputra

Nim   : 312210305

Kelas : TI 22.A3

---

# Praktikum 8

- Pertama kita menyatakan sebuah class Mahasiswa yang didalamnya terdapat atribut NIM, Nama, nilai tugas, nilai UTS dan nilai UAS.

  untuk mendeklarasikan sebuah class didalam OOP kita harus gunakan def__init__ dan juga self
  
        class mahasiswa:
        def __init__(self, nim, nama, tugas, uts, uas):
                self.nim = nim
                self.nama = nama
                self.tugas = tugas
                self.uts = uts
                self.uas = uas
         
- deklarasikan satu dictionary kosong sebagai tempat menyimpan data-data yang sudah kita input. Ada 5 list kosong yang nanti isinya yaitu NIM, Nama, nilai tugas, nilai UTS dan nilai UAS

        data = mahasiswa([],[],[],[],[])
        
- buat beberapa method untuk menambahkan, menampilkan, menghapus, mengubah data mahasiswa. Pertama membuat method tambah(), method ini berfungsi untuk menambahkan data. Dalam method ini kita menggunakan append() supaya data yang terakhir ditambahkan, ada di urutan list paling akhir.

        def tambah(self,nim,nama,tugas,uts,uas):
                data.nim.append(nim)
                data.nama.append(nama)
                data.tugas.append(tugas)
                data.uts.append(uts)
                data.uas.append(uas)
 
 - output ketika ingin Menambahkan Data
 
 <img width="293" alt="1" src="https://user-images.githubusercontent.com/110619093/206836650-3accd72a-82c9-4eb8-ad97-6b7b2190b36e.png">

 
- Membuat method lihat(), gunanya untuk menampilkan seluruh data yang sudah kita tambahkan tadi. Kalau sama sekali tidak ada data, maka akan muncul tulisan TIDAK ADA DATA

        def lihat(self):
                for i in range(len(data.nama)):
                print("|", i+1, "  |", end="")
                print('{0:<25}'.format(self.nama[i]), end="")
                print("|", self.nim[i], end="")
                print(" |", self.tugas[i], end="")
                print("    |", self.uts[i], end="")
                print("  |", self.uas[i], " | ", end="")
                print(f'{((self.tugas[i]*30/100) + (self.uts[i]*35/100) + (self.uas[i]*35/100)) :.2f}', " |")

- output ketika ingin melihat data

<img width="478" alt="2 1" src="https://user-images.githubusercontent.com/110619093/206836750-dc91741a-53d1-4945-ab55-deba8ec44ba7.png">


- Membuat method ubah() yang fungsinya untuk mengubah data. jika method ini dipanggil, maka data Nama, NIM, nilai tugas, nilai UTS, nilai UAS akan diubah sesuai dengan inputan dari user. Index ke - (no) akan dicari secara otomatis sesuai dengan nama yang ingin diubah oleh pengguna.

        def ubah(self,nim,nama,tugas,uts,uas):
                self.nim[no] = nim
                self.nama[no] = nama
                self.tugas[no] = tugas
                self.uts[no] = uts
                self.uas[no] = uas

- output jika ingin mengubah data

<img width="505" alt="3" src="https://user-images.githubusercontent.com/110619093/206837309-93e8f113-9c25-4cbd-bdec-ae952797ef0a.png">


- Terakhir kita buat method hapus(). Gunanya adalah menghapus data berdasarkan nama. Kita bisa menggunakan del untuk menghapus datanya. Seperti tadi, nomor index list yang akan dihapus disesuaikan dengan inputan dari user. Yaitu index nomor ke - (no).

         def hapus(self):
                del self.nim[no]
                del self.nama[no]
                del self.tugas[no]
                del self.uts[no]
                del self.uas[no]
                
-output jika ingin menghapus data

<img width="544" alt="4" src="https://user-images.githubusercontent.com/110619093/206837537-00de465a-81ce-4349-a112-5c61547f03fe.png">


- output jika keluar program

<img width="305" alt="5" src="https://user-images.githubusercontent.com/110619093/206837572-8e636d77-1a0c-4558-bbd5-13ed8d4100be.png">
