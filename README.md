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
# 1. import dan definisi kelas

            def __init__(self):
                  self.daftar_mahasiswa = []
  • class Mahasiswa: Mendefinisikan kelas Mahasiswa yang akan digunakanuntuk mengelola data mahasiswa.

  • init: Merupakan metode konstruktor yang dipanggil saat objek dari kelas ini dibuat.

# 2. Method Tambahan

                  self.daftar_mahasiswa.append({'nama': nama, 'nim': nim, 'nilai': nilai})
            print(f"Data mahasiswa {nama} (NIM: {nim}) berhasil ditambahkan.")
  • tambah(self, nama, nim, nilai): Method ini digunakan untuk menambahkan data mahasiswa baru ke dalam daftar.

  • self.daftar_mahasiswa.append(...): Menambahkan dictionary yang berisi nama, nim, dan nilai mahasiswa ke dalamlist daftar_mahasiswa.

  • print(...): Menampilkan pesan konfirmasi bahwa data mahasiswa telah berhasil ditambahkan.
# 3. Method Tampilkan

                  if not self.daftar_mahasiswa:
          print("Daftar mahasiswa kosong.")
          return
        print("Daftar Mahasiswa:")
             for index, mahasiswa in enumerate(self.daftar_mahasiswa, start=1):
             print(f"{index}. Nama: {mahasiswa['nama']}, NIM: {mahasiswa['nim']}, Nilai: {mahasiswa['nilai']}")
  • tampilkan(self): Method ini digunakan untuk menampilkan semua data mahasiswa yang ada dalam daftar.

  • if not self.daftar_mahasiswa:: Memeriksa apakah daftar mahasiswa kosong. Jika kosong, program akan menampilkan pesan dan keluar dari method.

  • enumerate(...): Menggunakan fungsi enumerate untuk mendapatkan indeks dan data mahasiswa saat iterasi. Indeks dimulai dari 1.

  • print(...): Menampilkan informasi mahasiswa dalam format yang terstruktur.
# 4. Method menghapus

              for mahasiswa in self.daftar_mahasiswa:
       if mahasiswa['nama'] == nama:
          self.daftar_mahasiswa.remove(mahasiswa)
           print(f"Data mahasiswa {nama} berhasil dihapus.")
           return
      print(f"Data mahasiswa {nama} tidak ditemukan.")
  • hapus(self, nama): Method ini digunakan untuk menghapus data mahasiswa berdasarkan nama.

  • for mahasiswa in self.daftar_mahasiswa:: Melakukan iterasi melalui daftar mahasiswa.

  • if mahasiswa['nama'] == nama: Memeriksa apakah nama mahasiswa yang ingin dihapus ada dalam daftar.

  • self.daftar_mahasiswa.remove(mahasiswa): Menghapus mahasiswa dari daftar jika ditemukan.

  • print(...): Menampilkan pesan konfirmasi atau pesan bahwa mahasiswa tidak ditemukan.
# 5. Method Mengubah

                     for mahasiswa in self.daftar_mahasiswa:
         if mahasiswa['nama'] == nama:
             mahasiswa['nim'] = nim_baru
             mahasiswa['nilai'] = nilai_baru
             print(f"Data mahasiswa {nama} berhasil diubah menjadi NIM {nim_baru} dan nilai {nilai_baru}.")
             return
      print(f"Data mahasiswa {nama} tidak ditemukan.")
  • ubah(self, nama, nim_baru, nilai_baru): Method ini digunakan untuk mengubah data mahasiswa berdasarkan nama.

  • if mahasiswa['nama'] == nama:: Memeriksa apakah nama mahasiswa yang ingin diubah ada dalam daftar.

  • mahasiswa['nim'] = nim_baru dan mahasiswa['nilai'] = nilai_baru: Mengubah NIM dan nilai mahasiswa yang ditemukan.

  • print(...): Menampilkan pesan konfirmasi atau pesan bahwa mahasiswa tidak ditemukan.
# 6. Menu interaktif

                  mhs = Mahasiswa()

     while True:
               print("\nMenu:")
               print("1. Tambah Mahasiswa")
               print("2. Tampilkan Mahasiswa")
               print("3. Ubah Mahasiswa")
               print("4. Hapus Mahasiswa")
               print("5. Keluar")
    
               pilihan = input("Pilih menu (1-5): ")
    
               if pilihan
  Menu Interaktif :

  Program menampilkan menu dengan pilihan untuk menambah, menampilkan, mengubah, menghapus siswa, atau keluar dari program.
  Digunakan while True untuk terus menampilkan menu hingga pengguna memilih untuk keluar.

  Input Pengguna :

  Menggunakan input() untuk mendapatkan pilihan dari pengguna dan data siswa yang ingin ditambahkan, diubah, atau dihapus.
  Berdasarkan pilihan yang dimasukkan, program akan memanggil metode yang sesuai dari kelas Mahasiswa.
# Diagram Class
![image](https://github.com/user-attachments/assets/4ade2f77-cd11-48d9-b921-7b5e1a7b446d)
# Penjelasan Diagram class
# 1. Kelas Mahasiswa
 Deskripsi  :Kelas ini adalah inti dari manajemen data mahasiswa, bertanggung jawab untuk mengelola seluruh operasi pada data mahasiswa.

 Atribut
 
       • daftar_mahasiswa (private list):
          Menyimpan kumpulan data mahasiswa
          Bersifat privat untuk melindungi integritas data

Method

        • -__init__():

             Konstruktor kelas
             Menginisialisasi list kosong untuk menyimpan data mahasiswa
             
        • tambah(nama, nim, nilai):

             Menambahkan mahasiswa baru ke dalam daftar
             Menerima parameter nama, NIM, dan nilai
             Membuat entri baru dalam daftar mahasiswa
       
        • tampilkan():

            Menampilkan seluruh data mahasiswa yang tersimpan
            Menangani kasus daftar kosong
            Menampilkan informasi setiap mahasiswa termasuk nama, NIM, dan nilai
       
        •  hapus(nama):

            Menghapus data mahasiswa berdasarkan nama
            Mencari mahasiswa dengan nama tertentu
            Menghapus entri jika ditemukan
            Memberikan konfirmasi atau pesan kesalahan
            
        • ubah(nama, nim_baru, nilai_baru):

            Mengubah data mahasiswa yang sudah ada
            Mencari mahasiswa berdasarkan nama
            Memperbarui NIM dan nilai
            Memberikan konfirmasi perubahan
# 2. Kelas data mahasiswa
   Deskripsi: Kelas ini merupakan struktur data untuk menyimpan informasi individual setiap mahasiswa.

Atribut 

             • nama (string): Nama lengkap mahasiswa
             • nim (integer): Nomor Induk Mahasiswa
             • nilai (integer): Nilai akademik mahasiswa
# 3. Kelas main
    Deskripsi: Kelas yang bertanggung jawab untuk menjalankan program dan berinteraksi dengan pengguna.

Method

           • main():
                Fungsi utama untuk menjalankan program
                Membuat instance kelas Mahasiswa
                Memulai loop utama program
           • tampilkan_menu():
                 Menampilkan pilihan menu kepada pengguna
                 Memudahkan interaksi dan navigasi program
           • pilih_menu():
                 Memproses pilihan menu yang dipilih pengguna
                 Memanggil metode yang sesuai dari kelas Mahasiswa 
# Hubungan Antara Kelas
         Komposisi (Mahasiswa -- 0.. DataMahasiswa)
            • Kelas Mahasiswa mengandung beberapa objek DataMahasiswa
            • Hubungan komposisi berarti objek DataMahasiswa tidak dapat eksis tanpa Mahasiswa
            • Satu objek Mahasiswa dapat memiliki 0 atau lebih objek DataMahasiswa
         Asosiasi (Main ..> Mahasiswa)
            • Kelas Main menggunakan (uses) kelas Mahasiswa
            • Main bergantung pada fungsionalitas Mahasiswa untuk menjalankan program
