# Minggu 5 - Block Cipher

## Mode Operasi Block Cipher

Untuk kerahasiaan, integritas, dan keaslian. macam:

1. ECB
2. CBC
3. OFB
4. CFB
5. ...
6. ...

## 1. ECB
AES dan DES => ECB

Kelemahan: 
- tidak bisa encrypt gambar,
- 1 plaintext untuk 1 ciphertext. sehingga, dapat mudah ditebak dan dibuat *codebook*nya.

metode:
Dienkripsi secara individual
contoh:
plaintext: 10100010001110101001
dipecah jadi blok 4 bit

1010 0010 0011 ....

per bloks di-XOR dengan kuncinya. (Kunci diketahui)

lalu, digeser 1 bit ke kiri.

## 2. CBC

Feedback pada sebuah bloks. langkah:

1. plaintext XOR Initialization Vector (IV)
2. Di enkripsi dengan key
3. key digeser ke kanan 3x
4. hasil dari enkripsi ini dijadikan IV untuk round selanjutnya

## 3. CFB

langkah:

1. plaintext = m = 11010100 dengan m1 = 11, m2 = 01, m3 = 01, r = 2 bit, m4 = 00, IV = 00000000, k = 01011101

2. e1 = IV XOR k
3. c1 = 2 bit awal e1 XOR m1
4. IV2 = e1 geser ke kiri 2 bit, 2 bit belakang kan kosong, jadi diisi 0.
5. ulangi step 2.

## 4. OFB

plaintext = m = 11010100 dengan m1 = 11, m2 = 01, m3 = 01, r = 2 bit, m4 = 00, IV = 00000000, k = 01011101
langkah:

1. e1 = IV XOR k
2. c1 = 2 bit awal e1 XOR m1
3. e2 = c1 XOR k
4. dan seterusnya ('.' ) whoaa~

## 5. CTR (Counter Mode)

cipher text tidak dipecah.

## 6 Galois Counter Mode

## Exhaustive Key Search Revisited
mencari kunci dan mencocokkannya dengan ciphertext.
brute force search. hanya ganti istilah

# meningkatkan keamanan di block cipher

## Double encryption
kunci meningkat 2x lipat, tapi kemanan tidak terlalu ngaruh.

## Triple encryption
kunci meningkat 3x lipat, tapi kemanan meningkat 2x lipat.

## key Whittening
memperpanjang kunci tanpa menyebabkan overhead
