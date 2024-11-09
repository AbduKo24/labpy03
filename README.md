# labpy03

# Latihan 1
# Meminta pengguna memasukkan nilai n
import random

n = int(input("Masukkan nilai N: "))

# Looping untuk menghasilkan n bilangan acak
for i in range(1, n + 1):
    # Menghasilkan bilangan acak antara 1 dan 5
    bilangan_acak = random.uniform(1, 5)

    # Menampilkan data ke-i dan nilai bilangan acak
    print(f"data ke: {i} => {bilangan_acak}")
    print("Selesai")

# Output
Masukkan nilai N: 7
data ke: 1 => 3.958239291509731
Selesai
data ke: 2 => 2.447275721181781
Selesai
data ke: 3 => 3.241959970814829
Selesai
data ke: 4 => 3.344501125052031
Selesai
data ke: 5 => 2.396872131409517
Selesai
data ke: 6 => 1.1363144116576445
Selesai
data ke: 7 => 2.2238102472309116
Selesai


# Penjelasan Kerja 1 Dan Output

1. Input Nilai N
n = int(input("Masukkan nilai N: "))
Pada bagian ini, program meminta pengguna untuk memasukkan nilai n yang akan menentukan seberapa banyak data yang akan diproses.
Nilai ini kemudian disimpan dalam variabel n. Misalnya, jika pengguna memasukkan angka 7, maka n akan bernilai 7.
2. Looping untuk Menghasilkan Bilangan Acak
for i in range(1, n + 1):
Bagian ini menggunakan perulangan for yang akan dieksekusi sebanyak n kali. Fungsi range(1, n + 1) menghasilkan urutan
angka dari 1 hingga n, sehingga perulangan ini akan terjadi mulai dari i = 1 sampai i = n.
3. Menghasilkan Bilangan Acak
bilangan_acak = random.uniform(1, 5)
Di dalam perulangan, pada setiap iterasi, program akan menghasilkan sebuah bilangan acak yang nilainya berada
di antara 1 dan 5 menggunakan random.uniform(1, 5). Fungsi uniform(a, b) dari modul random menghasilkan bilangan float acak yang terdistribusi
secara merata antara a dan b (termasuk a dan b).
4. Menampilkan Data
print(f"data ke: {i} => {bilangan_acak}")
print("Selesai")
Setiap kali perulangan selesai, program mencetak informasi berupa nomor urut data (i) dan nilai bilangan acak yang dihasilkan pada iterasi tersebut. 
Selain itu, setelah mencetak nilai bilangan acak, program mencetak kata "Selesai" untuk memberi tanda bahwa proses untuk data tersebut sudah selesai.
5. Output
Misalnya, jika pengguna memasukkan 7 sebagai nilai n, maka program akan menghasilkan 7 bilangan acak, satu per satu, diikuti dengan kata "Selesai" setelah setiap data. 

# Latihan 2
# Inisialisasi laba per bulan
laba = 0
total_laba = 0

# Loop untuk bulan 1 sampai 8
for bulan in range(1, 9):
    # Menentukan laba berdasarkan bulan
    if bulan in [1, 2]:  # Bulan 1 dan 2
        laba = 0
    elif bulan in [3, 4]:  # Bulan 3 dan 4
        laba = 20000000.0
    elif bulan in [5, 6, 7]:  # Bulan 5, 6, dan 7
        laba = 70000000.0
    elif bulan == 8:  # Bulan 8
        laba = 500000000.0
    
    # Menampilkan laba per bulan
    print(f"laba bulan ke- {bulan} sebesar: {laba}")
    
    # Menambahkan laba ke total laba
    total_laba += laba

# Menampilkan total laba
print(f"Total laba adalah: {total_laba}")

# Output
laba bulan ke- 1 sebesar: 0
laba bulan ke- 2 sebesar: 0
laba bulan ke- 3 sebesar: 20000000.0
laba bulan ke- 4 sebesar: 20000000.0
laba bulan ke- 5 sebesar: 70000000.0
laba bulan ke- 6 sebesar: 70000000.0
laba bulan ke- 7 sebesar: 70000000.0
laba bulan ke- 8 sebesar: 500000000.0
Total laba adalah: 750000000.0


# Penjelasan Kerja 2 Dan Output
1. Inisialisasi Variabel
laba = 0
total_laba = 0

Pada bagian ini, dua variabel diinisialisasi:
    laba: Menyimpan laba untuk setiap bulan. Nilainya dimulai dengan 0 dan akan diperbarui di setiap iterasi.
    total_laba: Menyimpan jumlah total laba yang telah diakumulasi sepanjang 8 bulan. Dimulai dengan 0 dan akan bertambah setiap kali laba bulan tertentu ditambahkan.
2. Loop untuk Menghitung Laba Per Bulan

for bulan in range(1, 9):
    range(1, 9) menghasilkan urutan angka dari 1 sampai 8, yang berarti loop akan berjalan untuk setiap bulan dari bulan 1 hingga bulan 8.
    Variabel bulan akan mengambil nilai-nilai ini secara berurutan, yaitu 1, 2, 3, ..., 8.
3. Menentukan Laba Berdasarkan Bulan
if bulan in [1, 2]:  # Bulan 1 dan 2
    laba = 0
elif bulan in [3, 4]:  # Bulan 3 dan 4
    laba = 20000000.0
elif bulan in [5, 6, 7]:  # Bulan 5, 6, dan 7
    laba = 70000000.0
elif bulan == 8:  # Bulan 8
    laba = 500000000.0
    Bulan 1 dan 2: Pada bulan 1 dan 2, laba adalah 0 (belum ada laba).
    Bulan 3 dan 4: Pada bulan 3 dan 4, laba adalah 20,000,000 (20 juta).
    Bulan 5, 6, dan 7: Pada bulan 5, 6, dan 7, laba adalah 70,000,000 (70 juta).
    Bulan 8: Pada bulan 8, laba meningkat sangat besar menjadi 500,000,000 (500 juta).
4. Menampilkan Laba Per Bulan
print(f"laba bulan ke- {bulan} sebesar: {laba}")
Setiap kali iterasi berlangsung, program mencetak informasi mengenai laba pada bulan tersebut, dengan format:
laba bulan ke- <bulan> sebesar: <laba>
5. Menambahkan Laba ke Total Laba
total_laba += laba
Setiap kali laba bulan ini dihitung, laba tersebut ditambahkan ke dalam total_laba. Jadi, di akhir program, total_laba akan berisi jumlah total laba yang telah dihitung untuk seluruh 8 bulan.
6. Menampilkan Total Laba
print(f"Total laba adalah: {total_laba}")
Setelah loop selesai, program mencetak total laba yang terakumulasi dari bulan 1 hingga bulan 8.
# Latihan 3
def atm():
  saldo = 1000000000000

  while True:
    print("Saldo saat ini: Rp", saldo)
    print("1. Tarik Uang")
    print("2. Keluar")
    pilihan = int(input("Pilih menu (1/2): "))

    if pilihan == 1:
      jumlah_tarik = int(input("Masukkan jumlah penarikan: "))
      if jumlah_tarik <= saldo:
        saldo -= jumlah_tarik
        print("Penarikan berhasil!")
      else:
        print("Saldo tidak mencukupi!")
    elif pilihan == 2:
      print("Terima kasih telah menggunakan ATM!")
      break
    else:
      print("Pilihan tidak valid!")

atm()


# Output
Saldo saat ini: Rp 1000000000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 500000000
Penarikan berhasil!
Saldo saat ini: Rp 999500000000


# Penjelasan Kerja 3 Dan Output
Penjelasan Kode
1. Definisi Fungsi ATM
def atm():
    saldo = 1000000000000
    Fungsi atm() didefinisikan, yang berfungsi sebagai simulasi dari sebuah mesin ATM.
    Variabel saldo diinisialisasi dengan nilai 1000000000000 (1 triliun) yang akan menjadi saldo awal di ATM.
2. Looping Tak Terbatas (while True)
while True:
    Program menggunakan loop while True, yang berarti perulangan ini akan terus berjalan tanpa batas hingga ada perintah untuk keluar (misalnya, dengan break).
    Di dalam loop ini, pengguna dapat melakukan beberapa transaksi atau keluar dari program.
3. Menampilkan Informasi Saldo dan Menu
print("Saldo saat ini: Rp", saldo)
print("1. Tarik Uang")
print("2. Keluar")
    Program pertama kali menampilkan saldo saat ini.
    Setelah itu, menu pilihan ditampilkan:
        Tarik uang
        Keluar dari aplikasi ATM
4. Membaca Pilihan Pengguna
pilihan = int(input("Pilih menu (1/2): "))
    Program meminta input dari pengguna untuk memilih menu (1 untuk tarik uang atau 2 untuk keluar). Input ini kemudian diubah menjadi integer dengan int() dan disimpan dalam variabel pilihan.
5. Menangani Pilihan Tarik Uang (Pilihan 1)

if pilihan == 1:
    jumlah_tarik = int(input("Masukkan jumlah penarikan: "))
    if jumlah_tarik <= saldo:
        saldo -= jumlah_tarik
        print("Penarikan berhasil!")
    else:
        print("Saldo tidak mencukupi!")

    Jika pengguna memilih 1 (tarik uang), program akan meminta input lagi, yaitu jumlah uang yang ingin ditarik (jumlah_tarik).
    Program kemudian memeriksa apakah jumlah yang ingin ditarik lebih kecil atau sama dengan saldo yang tersedia:
        Jika ya, saldo akan dikurangi dengan jumlah penarikan (saldo -= jumlah_tarik), dan program menampilkan pesan bahwa penarikan berhasil.
        Jika tidak, program akan menampilkan pesan bahwa saldo tidak mencukupi untuk melakukan penarikan.

6. Menangani Pilihan Keluar (Pilihan 2)

elif pilihan == 2:
    print("Terima kasih telah menggunakan ATM!")
    break

    Jika pengguna memilih 2 (keluar), program akan menampilkan pesan "Terima kasih telah menggunakan ATM!" dan kemudian keluar dari loop dengan perintah break, yang menghentikan eksekusi fungsi.

7. Menangani Pilihan Tidak Valid

else:
    print("Pilihan tidak valid!")

    Jika pengguna memasukkan pilihan selain 1 atau 2, program akan menampilkan pesan bahwa pilihan yang dimasukkan tidak valid dan kembali meminta input pilihan.

8. Memanggil Fungsi

atm()

    Fungsi atm() dipanggil untuk memulai eksekusi program.
Output Program

Jika kita mengikuti langkah-langkah yang telah dijelaskan, dan memasukkan input tertentu, output yang dihasilkan adalah sebagai berikut.
Langkah 1: Menampilkan saldo dan menu
Saldo saat ini: Rp 1000000000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Langkah 2: Pengguna memilih untuk menarik uang
Masukkan jumlah penarikan: 500000000
Penarikan berhasil!
Saldo yang baru setelah penarikan:
Saldo saat ini: Rp 999500000000
Langkah 3: Menampilkan menu lagi setelah penarikan
Program akan mengulangi proses tersebut sampai pengguna memilih untuk keluar (menu pilihan 2).
Alur Eksekusi:
    Program dimulai dengan saldo 1 triliun.
    Menu ditampilkan dengan dua pilihan: tarik uang atau keluar.
    Jika pengguna memilih 1 (Tarik Uang), program meminta jumlah uang yang ingin ditarik.
    Jika jumlah uang yang ditarik kurang dari atau sama dengan saldo, saldo akan berkurang dan penarikan berhasil.
    Jika jumlah uang yang ditarik lebih besar dari saldo, maka penarikan gagal dan saldo tidak berubah.
    Program kemudian akan mengulangi langkah 2 hingga pengguna memilih 2 (Keluar), yang akan keluar dari loop dan mengakhiri program.

Kesimpulan:
Fungsi atm() ini membuat simulasi mesin ATM yang memungkinkan pengguna untuk melakukan penarikan uang 
selama saldo mencukupi, atau keluar dari aplikasi. Program ini terus berjalan dalam loop hingga pengguna memilih untuk keluar dengan menu pilihan 2.






    
