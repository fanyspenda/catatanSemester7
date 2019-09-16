# Keamanan Informasi - minggu 1

## materi
- cryptology
- steganography
- secure application development

## Cryptology
1. cryptography  
   ilmu menyandikan suatu pesan
   1. symmectric ciphers  
   menggunakan kunci yang sama
      1. block ciphers
         mengenkripsi per blok
      2. stream ciphers
         mengenkripsi per bit
   1. asymmetric ciphers
   menggunakan kunci berbeda
   1. protocols
   implementasi algoritma cryptography
2. cryptanalysis
   membongkar pesan rahasia tanpa mengetahui kuncinya
   1. classical
   2. 

## Notasi
- x = data murni
- y = ciphertext (data yang sudah terenkripsi)
- K = key
- e() = enkripsi
- d() = dekripsi

## Panjang Kunci
1. 64 bit = lemah
2. 128 bit = kuat, tapi lemah jika quantum komputer ada
3. 256 bit = kuat, meski quantum komputer ada

## aritmatika modular
biasanya diterapkan dalam enkripsi
1. mencari sisa hasil bagi (modulus)
   contoh:
   17 mod 9 = 8 mod 9

   3 * 2 mod 5 = 6 mod 5 = 1 mod 5

   3/4 mod 5 = 3 * 4 ^-1 mod 5 <- invers
   = (3 + 5)*4^-1 mod 5 = 8/4 mod 5 = 2 mod 5

> **note**  
> invers hanya dimiliki jika pembagi dan yang dibagi hanya memiliki FPB 1

# caesar cipher
menggeser angka
a = 0, .... z=25

misal:
k = 7

data murni = attack = 0, 19, 19, 0, 2, ...
terenkripsi = haahjr = 7, 26, ....
