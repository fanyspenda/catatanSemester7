# Minggu 10 - Eliptic Curves

- Merupakan solusi buat orang yang pengen enkripsi seaman RSA, tapi dengan panjang kunci Simetrik.

> rumus:  
> y^2 = x^3 + ax +b

## Grup

- himpunan G
- a, b dan c bagian dari G
- syarat:
  - closure: a\*b, bagian dari G
  - asosiatif: a*(b*c) = (a*b)*c
  - element: a*e = e*a = a, e bagian dari G
  - element invers: a*a' = a'*a = e, a' bagian dari G
  - notasi: (G, \*)

## Field

himpunan F, ada dua operasi biner. Syaratnya:

- closure
- asosiatif
- distributif:
  - x (y+z) = (xy) + (xz)
  - z (x+y) = (zx) + (zy)
- notasi: (F, +, \*)

### Fp (Medan dengan menggunakan bil. prima)

- Fp (0,1,2,..., p-1)
- penjumlahan: jika a, b bagian dari Fp, maka a + b = r
  - r=(a+b) mod p, 0 <= r <= p-1
- perkalian: a, b bagian dari Fp, maka a\*b = s
  - s = (a+b) mod p, 0 <= s <= p-1

> contoh:  
> F23 = {0,1,2,...,22}  
> penjumlahan: 12 + 20 = 32 mod 23 = 9  
> perkalian: 8 \* 9 = 72 mod 23 = 3

## Galois Field (GF(p^n))

- p adalah bilangan prima, >= 1
- bila n = 1 -> GF(p) maka elementnya {0,1,2,...,p-1}

> contoh:  
> GF(3), maka:
> +|0|1|2|
> ---|---|---|---|
> 0|0|1|2|
> 1|1|2|0|
> 2|2|0|1|
> perkalian:
> \*|0|1|2|
> ---|---|---|---|
> 0|0|0|0|
> 1|0|1|2|
> 2|0|2|1|
> contoh soal: GF(3) = {0,1,2}  
> jika x^2 = 2 mod 2,  
> maka x^2 = 0  
> x = 0

## GF (2^m)

setiap element di dalam GF (2^m) adalah integer dalam representasi biner sepanjang maks m bit

jadi, setiap a bagian dari GF (2^m)  
a = alpha_m-1 X^(m-1) + ... + alpha_1 X + alpha_gamma

Contoh: 1101 dapat dnyatakan x^3 + x^2 + 1
