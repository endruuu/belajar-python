Kumpulan latihan soal untuk memperdalam pemahaman python

# Latihan 1

Tina diberi uang Rp 50.000,00 oleh ibunya untuk membeli buah dan sayuran. Sampai di pasar, Tina membeli Mangga 1kg seharga Rp. 25.000,00 Wortel ½ kg Rp. 15.000,00 dan Sawi 1 Ikat Rp. 15.000,00.  Tina mendapatkan diskon 10% dari hasil pembelian. Buatlah Program yang berisikan inputan dari buah dan sayuran yang dibeli Tina, kemudian tampilkan output harga hasil pembelian dan hasil pembelian setelah diskon dan sisa uang Tina

Penyelesaian :

```
mangga = int(input("Masukan harga Mangga: "))
wortel = int(input("Masukan harga Wortel: "))
sawi = int(input("Masukan harga Sawi: "))
uang = 50000
total_harga = mangga+wortel+sawi
diskon = int(total_harga*10/100)
harga_akhir = total_harga-diskon

print("Harga Mangga: ", mangga)
print("Harga Wortel: ", wortel)
print("Harga Sawi: ", sawi)
print("==========================")
print("Total Harga: ", total_harga)
print("Diskon: ", diskon)
print("Total Harga Setelah Diskon: ", harga_akhir)
print("Bayar: ", uang)
print("Sisa Uang: ", uang-harga_akhir)
```

# Latihan 2

Jalankan output dari program ini, jelaskan syntax errornya.

```
.im = "python"
P3MBU4T = "Guido van Rossum"
T@hun = 1991
Comp_any = "Youtube”
$python_is = True
54t3 = "Benar"
Print(.im, P3MBU4T, T@hun, Comp_any, $python_is, 54t3)
```

Penyelesaian:

```
im = "python" # Error karena penulisan variabel tidak boleh di awali dengan .
P3MBU4T = "Guido van Rossum"
Tahun = 1991 # Error karena penulisan variabel tidak boleh mengandung special character
Comp_any = "Youtube"
python_is = True # Error karena penulisan variabel harus diawali oleh Huruf
_54t3 = "Benar" # Erro karena penulisan variabel di awali dengan angka
print(im, P3MBU4T, Tahun, Comp_any, python_is, _54t3)
```

# Latihan 3

Buatlah pemerograman menampilkan bilangan terbesar dari tiga bilangan yang dimasukkan.

Penyelesaian :
Ada 2 cara untuk menyelesaikan soal tersebut
Cara 1 :

```
bil1 = int(input("Bilangan 1: "))
bil2 = int(input("Bilangan 2: "))
bil3 = int(input("Bilangan 3: "))

if bil1 > bil2 and bil1 > bil3:
    print(f"Angka {bil1} adalah terbesar")
elif bil2 > bil1 and bil2 > bil3:
    print(f"Angka {bil2} adalah terbesar")
else:
    print(f"Angka {bil3} adalah terbesar")
```
Cara 2 :

```
bil = list()
for i in range(3):
    bil.append(int(input(f"Masukan bilangan ke {i+1} = ")))
print(f"Bilangan terbesar {max(bil)}")
```

# Latihan 4

Buatlah program yang dapat menebak nilai yang yang tersimpan dalam komputer. Jika inputan user lebih kecil dari nilai yang tersimpan dalam komputer maka sistem akan menampilkan pesan ”Tebakan anda terlalu rendah”. Sedangkan jika inputan dari user lebih besar dari nilai yang tersimpan dalam komputer maka sistem akan menampilkan pesan “Tebakan anda terlalu tinggi”. Jika inputan user bernilai sama dengan nilai yang tersimpan dalam komputer amka sistem akan menampilkan pesan ”Tebakan anda tepat”

Penyelesaian :

```
print("Game Tebak Angka")
angka = 26
tebak = int(input("Masukan tebakan anda: "))

if tebak < angka:
    print("Tebakan anda terlalu rendah")
elif tebak > angka:
    print("Tebakan anda terlalu tinggi")
else:
    print("Tebakan anda tepat")
```

# Latihan 5

Buatlah program python login sederhana yang meminta input username dan password. yang mana jika username dan password nya adalah admin  dan root, maka akan menampilkan login berhasil. Jika tidak maka akan menampilkan login gagal. User memiliki kesempatan login sebanyak 3 kali, jika user sudah mencapai batas maksimum percobaan user tidak bisa login lagi dan program akan menampilkan anda telah mencapai batas percobaan login.

Penyelesaian :

```
print("Login")

attempt = 0
doLogin = True

while doLogin:
    username = input("Username: ")
    password = input("Password: ")

    if username == "admin" and password == "root":
        print("Login Berhasil")
        doLogin = False
    else:
        print("Username atau Password Salah!")
        attempt += 1

        if attempt >= 3:
            print("Sistem Terkunci, anda sudah mencapat batas percobaan login!!")
            doLogin = False
```

# Latihan 6

Buatlah program yang dapat menampilkan outputnya seperti berikut ini:
```
Terimakasih
erimakasih
rimakasih
imakasih
makasih
akasih
kasih
asih
sih
ih
h
```

Penyelesaian :

```
kalimat = "Terimakasih"
panjang = len(kalimat)

for i in range(panjang):
    for j in range(i, panjang):
        print(kalimat[j], end="")
    print("")
```

# Latihan 7 

Buatlah program perulangan yang menampilkan outputnya sebagai berikut:
```
0
3
6
9
12
15
18
```

Penyelesaian :

```
for i in range(0,19,3):
    print(i)
```    

# Latihan 8

Buatlah program yang dapat menampilan segitiga “*” terbalik seperti contoh berikut ini:
```
*****
****
***
**
*
```

Penyelesaian :

```
angka = int(input("Jumlah Angka: "))

for i in range(angka):
    for j in range(i, angka):
        print("*", end="")
    print("")
```

# Latihan 9

Buatlah program yang dapat menampilkan piramida dengan simbol ‘*’, Pada program tersebut, user dapat memasukkan tinggi piramida. Berikut ini output yang diinginkan.
```
Masukkan angka: 3
    *
  * * *
* * * * *
```

Penyelesaian :

```
angka = int(input("Masukan angka: "))

for i in range(angka):
    for j in range(i, angka):
        print(" ", end=" ")
    for k in range(0, 2 * i + 1):
        print("*", end=" ")
    print("")
```