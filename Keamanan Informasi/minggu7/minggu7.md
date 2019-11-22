# Public Key

- Kunci publik boleh diketahui orang,
- kunci privat tidak boleh

# RSA

salahsatu cara untuk pendistribusian kunci

- ditemukan tahun 1977
- menggunakan aritmethic modulo n (Zn)
- n = p \* q
- p dan q = bilangan besar prima
- kunci public = (n, e)
- kunci privat = d

kunci public = X^e mod n
kunci privat = Y^d mod n

## Metode

1. pilih 2 bilangan prima
2. hitung n = p\*q
3. hitung ⌀(n)=(p-1)\*(q-1)
4. pilih public exponent e={1,2,...,⌀(n)-1}
5. hitung kunci privat d\*e ≡ 1 mod ⌀(n)
6. return kunci publik = (⌀(n), e)

## Square and Multiply

menghitung perkalian berpangkat

# Speed-Up Techniques

## Miller Rabin test

untuk menentukan angka prima yang pantas untuk digunakan.

## Attack and Countermeasures

# Rangkuman RSA

RSA terdapat 4 algoritma:
jika untuk optimasi:

1. square and multiply
2. Chinese Reminder

Jika untuk penentuan bilangan prima:

1. Random
2. Fernati
3. Miller-Rabin
