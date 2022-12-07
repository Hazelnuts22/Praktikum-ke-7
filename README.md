Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan :
    
    ◉ Fungsi tambah() untuk menambah data.
    ◉ Fungsi tampilkan() untuk menampilkan data.
    ◉ Fungsi hapus(nama) untuk menghapus data berdasarkan nama.
    ◉ Fungsi ubah(nama) untuk mengubah data berdasarkan nama.
    ◉ Buat Flowchart dan Penjelasan Programnya pada README.md.
    ◉ Commit dan push repository ke github.

**Code Program**

    s_nama = []
    s_nim = []
    s_tugas = []
    s_uts = []
    s_uas = []
    s_akhir = []


    def judul():
    print('==================================')
    print('|     Daftar Nilai Mahasiswa     |')
    print('==================================')


    def menu():
    system('cls')
    print('=====================================')
    print('Input Data Nilai Mahasiswa'.center(40))
    print('=====================================')
    print('|    a. Tambah Data                 |')
    print('|    b. Tampilkan Data Mahasiswa    |')
    print('|    c. Ubah Data Mahasiswa         |')
    print('|    d. Hapus Data Mahasiswa        |')
    print('|    e. Selesai                     |')
    print('=====================================')
    choose = input('Pilih Menu  : ')
    if choose == 'a':
        tambah()
    elif choose == 'b':
        tampilkan()
    elif choose == 'c':
        ubah()
    elif choose == 'd':
        hapus()
    elif choose == 'e':
        selesai()
    else:
        tidak = input('Menu Tidak Ada')
        system('cls')
        menu()


    def tambah():
    system('cls')
    judul()
    print('Tambah Data'.center(40))
    print('==================================')
    nama = input('Nama     : ')
    s_nama.append(nama)
    nim = input('NIM       : ')
    s_nim.append(nim)

    system('cls')
    judul()
    print('Tambah Data'.center(40))
    print('==================================')
    tugas = float(input('Nilai Tugas    : '))
    s_tugas.append(tugas)

    uts = float(input('Nilai UTS        : '))
    s_uts.append(uts)

    uas = float(input('Nilai UAS        : '))
    s_uas.append(uas)

    total = tugas * 0.30 + uts * 0.35 + uas * 0.35
    s_akhir.append(total)
    print('Data Tersimpan'.center(40))
    kembali = input('Kembali [Enter]')
    menu()


    def tampilkan():
    system('cls')
    judul()

    for i in range(len(s_nim)):
        print('%d. Nama         : %s' % (i + 0, s_nama[i]))
        print('    NIM          : %s' % s_nim[i])
        print('    Nilai Tugas  : %.2f' % s_tugas[i])
        print('    UTS          : %.2f' % s_uts[i])
        print('    UAS          : %.2f' % s_uas[i])
        print('    Nilai Akhir  : %.2f' % s_akhir[i])
        print('-----------------------------')
    kembali = input('Kembali Tekan [Enter]')
    menu()


    def ubah():
    rubah = input('Ubah Biodata Tekan [A]   : ')
    if rubah == 'A' or rubah == 'a':
        i = int(input('Masukkan Nomor Urut  : '))
        if (i > len(s_nim[i])):
            print('Nomor Urut Salah')
        else:
            namabaru = input('Nama      : ')
            s_nama[i] = namabaru
    kembali = input('Kembali Tekan [Enter]')
    menu()


    def hapus():
    system('cls')
    judul()
    print('Hapus Data'.center(40))
    print('=================================')
    i = int(input('Masukkan Nomor Urut  : '))

    if (i > len(s_nim[i])):
        tidak = input('NIM Tidak Ada')
        hapus()

    else:
        s_nim.remove(s_nim[i])
        s_nama.remove(s_nama[i])
        s_tugas.remove(s_tugas[i])
        s_uts.remove(s_uts[i])
        s_uas.remove(s_uas[i])
        s_akhir.remove(s_akhir[i])

    print('Data Berhasil Di Hapus')
    kembali = input('Kembali Tekan [Enter]')
    menu()

    def selesai():
    system('')


    menu()

**Program**

![Screenshot (42)](https://user-images.githubusercontent.com/115677959/206162835-bb6270cb-9907-4dce-bad8-05a83021c065.png)

![Screenshot (43)](https://user-images.githubusercontent.com/115677959/206162844-6b2a8e39-721c-4ea1-82ed-cd58be3ee7a5.png)

![Screenshot (44)](https://user-images.githubusercontent.com/115677959/206162849-4d8fb138-b2e8-4754-8d53-7c729a786242.png)

![Screenshot (45)](https://user-images.githubusercontent.com/115677959/206162856-ab6d8d7d-1537-43a1-8ef9-79f21ee0cb50.png)

![Screenshot (46)](https://user-images.githubusercontent.com/115677959/206162915-0ef5671d-0a78-45ea-b104-4069a1367400.png)

**Hasil Run Code**
  **Menambahkan Data**
 
  ![Screenshot (47)](https://user-images.githubusercontent.com/115677959/206163959-2e4aba81-5921-4876-929e-7a8132203b18.png)
  
   **Menampilkan Data**
    
   ![Screenshot (50)](https://user-images.githubusercontent.com/115677959/206168528-4ff17dd8-0e73-46a2-babe-1b1b27dc1d9b.png)
    
   **Hapus Data dan Selesai**
    
 ![Screenshot (52)](https://user-images.githubusercontent.com/115677959/206169124-7dd50327-7f0d-439b-8df4-83e9ba0b6989.png)

**Penjelasan Program**
     
     1. Definisikan dictionary terlebih dahulu data = {}.
     2. Membuat fungsi
        ◉ Fungsi tampilkan(), untuk menambahkan data def tampilkan()
        ◉Fungsi tambah(), untuk menampilkan data def tambah()
        ◉Fungsi hapus(nama), untuk menghapus nama pada data def hapus(nama)
        ◉Fungsi ubah(nama), untuk mengubah nama pada data def ubah(nama)
     3. Menggunakan Perulangan while True: dapat diartikan perulangan akan terus mengulang jika inputan benar dan masuk kedalam proses jika tidak maka perulangan berhenti atau lanjut ke proses selanjutnya. Gunakan statement if untuk memproses perintah yang di inginkan sesuai inputan.
     4. Untuk menambahkan data pilih "[1] Tambah" gunakan fungsi if gunakan perintah "1", lalu masukan nama, nim, tugas, uts, uas, nilaiakhir, nilai akhir didapat dari = ((tugas)*30/100 + (uts)*35/100 + (uas)*35/100.
     5. Lalu jika ingin memilih "[2] Lihat" gunakan fungsi 'elif' dan gunakan fungsi 'for x in data.items():' untuk melihat data pada tabel data yang kita inputkan, dengan perintah "2". Jika data tidak terdaftar maka akan tampil "TIDAK ADA DATA" atau = 0.
     6. Lalu untuk menampilan pilihan "[3] Ubah" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian input nama, nim, nilai tugas, nilai uts, nilai uas untuk mengubah data nama kemudian gunakan fungsi 'else' untuk menampilkan data nama yang kita ingin ubah tidak ada.
     7. Untuk menghapus data pilih "[4] Hapus" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian fungsi 'del.data[nama] jika nama yang kita hapus tidak ada dalam tabel maka gunakan fungsi 'else' untuk menampilkan "TIDAK ADA DATA".
     8. Untuk keluar maka gunakan fungsi else dan exit() atau gunakan perintah [5] Keluar.

**Flowchart**

![Flowchart](https://user-images.githubusercontent.com/115677959/206171316-8433d805-8a0a-4b32-9ad8-f6416cc51437.jpg)


