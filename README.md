# PRAKTIKUM 8 FARDHILAN GALANG PRIARTO
Progam Daftar Nilai Mahasiswa
Kode program ini digunakan untuk mengelola daftar nilai mahasiswa, dimana user dapat menambah, menampilkan, mengubah, atau menghapus data nilai mahasiswa.
# Algoritma
Berikut adalah algoritma dari program ini:
```
Membuat objek dari kelas DaftarNilai
Selama kondisi TRUE:
Meminta user memasukkan pilihan
Jika pilihan adalah T:
Menambahkan data nilai baru
Jika pilihan adalah L:
Menampilkan daftar nilai mahasiswa
Jika pilihan adalah H:
Menghapus data nilai mahasiswa
Jika pilihan adalah U:
Mengubah data nilai mahasiswa
Jika pilihan adalah Q:
Mengakhiri perulangan
Jika pilihan tidak dikenali:
Menampilkan pesan peringatan
Selesai
```
# CODE
```
class DaftarNilai:
    __listNilai=[]
    def tambah(self):
        print("\nTambah Data Nilai\n")
        nama=input("Masukkan Nama    : ")
        nim=input("Masukkan NIM     : ")
        tugas=int(input("Masukkan Nilai Tugas  : "))
        uas=int(input("Masukkan Nilai UAS    : "))
        uts=int(input("Masukkan Nilai UTS    : "))
        akhir=int((tugas+uas+uts)/3)
        data=[nama,nim,tugas,uas,uts,akhir]
        self.__listNilai.append(data)
        print("\nData berhasil ditambahkan\n")
    def tampil(self):
        print("\nDaftar Nilai Mahasiswa\n")
        print("===========================================================================================================")
        print("| No |   Nama    |    NIM    |Tugas|  UAS  |  UTS  |  Akhir  |")
        print("===========================================================================================================")
        no=1
        for item in self.__listNilai:
            print("| {0:2} |{1:10} |{2:10} | {3:5} | {4:5} | {5:5} | {6:7} |".format(no,item[0],item[1],item[2],item[3],item[4],item[5]))
            no+=1
        print("===========================================================================================================")
    def hapus(self):
        print("\nHapus Data Nilai\n")
        nama=input("Masukkan Nama : ")
        for item in self.__listNilai:
            if item[0]==nama:
                self.__listNilai.remove(item)
        print("\nData berhasil dihapus\n")
    def ubah(self):
        print("\nUbah Data Nilai\n")
        nama=input("Masukkan Nama : ")
        for item in self.__listNilai:
            if item[0]==nama:
                nim=input("Masukkan NIM     : ")
                tugas=int(input("Masukkan Nilai Tugas  : "))
                uas=int(input("Masukkan Nilai UAS    : "))
                uts=int(input("Masukkan Nilai UTS    : "))
                akhir=int((tugas+uas+uts)/3)
                item[1]=nim
                item[2]=tugas
                item[3]=uas
                item[4]=uts
                item[5]=akhir
        print("\nData berhasil diubah\n")

nilai=DaftarNilai()
while True:
    c=input("\nT)ambah,L)ihat,U)bah,H)apus,Q)uit: ")
    if(c.lower()=='t'):
        nilai.tambah()
    elif(c.lower()=='l'):
        nilai.tampil()
    elif(c.lower()=='h'):
        nilai.hapus()
    elif(c.lower()=='u'):
        nilai.ubah()
    elif(c.lower()=='q'):
        break
    else:
        print("\nPilih menu yang tersedia\n")
```
# OUTPUT
![image](https://user-images.githubusercontent.com/93815689/206897163-0aa56d59-baf8-45b1-adc4-f95e40e958d2.png)
![image](https://user-images.githubusercontent.com/93815689/206897176-7f75df0b-d8fa-4970-969f-0e7978741857.png)
![image](https://user-images.githubusercontent.com/93815689/206897197-c9d14657-bef3-45ab-8342-b5c998c3f399.png)
![image](https://user-images.githubusercontent.com/93815689/206897402-c284ba70-487e-4055-972e-cf400856b0ab.png)
