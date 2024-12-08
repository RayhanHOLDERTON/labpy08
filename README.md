# labpy08
     nama : patur rahman hakim
     nim : 312410271
     kelas : TI.24.A2
     pertemuan ke 12
# Flowchart
![image](https://github.com/user-attachments/assets/0cce3733-af1f-4c9b-905c-3a3f153b565b)
# code program
      class Mahasiswa: def init (self): self.daftar_mahasiswa = []

      def tambah(self, nama, nim, nilai):
           self.daftar_mahasiswa.append({'nama': nama, 'nim': nim, 'nilai': nilai})
            print(f"Data mahasiswa {nama} (NIM: {nim}) berhasil ditambahkan.")

       def tampilkan(self):
          if not self.daftar_mahasiswa:
             print("Daftar mahasiswa kosong.")
             return
             print("Daftar Mahasiswa:")
             for index, mahasiswa in enumerate(self.daftar_mahasiswa, start=1):
             print(f"{index}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")

       def hapus(self, nama):
          for mahasiswa in self.daftar_mahasiswa:
             if mahasiswa['nama'] == nama:
                self.daftar_mahasiswa.remove(mahasiswa)
                print(f"Data mahasiswa {nama} berhasil dihapus.")
                return
          print(f"Data mahasiswa {nama} tidak ditemukan.")

      def ubah(self, nama, nim_baru, nilai_baru):
           for mahasiswa in self.daftar_mahasiswa:
              if mahasiswa['nama'] == nama:
                 mahasiswa['nim'] = nim_baru
                 mahasiswa['nilai'] = nilai_baru
                 print(f"Data mahasiswa {nama} berhasil diubah menjadi NIM {nim_baru} dan nilai {nilai_baru}.")
                 return
         print(f"Data mahasiswa {nama} tidak ditemukan.")

# contoh pengguna
     if name == "main": mhs = Mahasiswa()

    while True:
        print("\nMenu:")
        print("1. Tambah Mahasiswa")
        print("2. Tampilkan Mahasiswa")
        print("3. Ubah Mahasiswa")
        print("4. Hapus Mahasiswa")
        print("5. Keluar")
    
        pilihan = input("Pilih menu (1-5): ")
    
        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            nim = int(input("Masukkan NIM mahasiswa (angka): "))
            nilai = int(input("Masukkan nilai mahasiswa (angka): "))
            mhs.tambah(nama, nim, nilai)
    
        elif pilihan == '2':
            mhs.tampilkan()
    
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            nim_baru = int(input("Masukkan NIM baru (angka): "))
            nilai_baru = int(input("Masukkan nilai baru (angka): "))
            mhs.ubah(nama, nim_baru, nilai_baru)
    
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            mhs.hapus(nama)
    
        elif pilihan == '5':
            print("Keluar dari program.")
            break
    
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")
# penjelasan code program
1. import dan definisi kelas

            def __init__(self):
                  self.daftar_mahasiswa = []
class Mahasiswa: Mendefinisikan kelas Mahasiswa yang akan digunakanuntuk mengelola data mahasiswa.

init: Merupakan metode konstruktor yang dipanggil saat objek dari kelas ini dibuat.
2. Method Tambahan

                  self.daftar_mahasiswa.append({'nama': nama, 'nim': nim, 'nilai': nilai})
            print(f"Data mahasiswa {nama} (NIM: {nim}) berhasil ditambahkan.")
tambah(self, nama, nim, nilai): Method ini digunakan untuk menambahkan data mahasiswa baru ke dalam daftar.

self.daftar_mahasiswa.append(...): Menambahkan dictionary yang berisi nama, nim, dan nilai mahasiswa ke dalamlist daftar_mahasiswa.

print(...): Menampilkan pesan konfirmasi bahwa data mahasiswa telah berhasil ditambahkan.
3.Metode Tampilkan

                  if not self.daftar_mahasiswa:
          print("Daftar mahasiswa kosong.")
          return
        print("Daftar Mahasiswa:")
             for index, mahasiswa in enumerate(self.daftar_mahasiswa, start=1):
             print(f"{index}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
