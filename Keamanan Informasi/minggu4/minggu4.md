# Minggu 4 Keamanan Informasi - Enkripsi AES

## AES
- penyeleksian Algoritma dari 1997 - 2001
- Asymetric Cipher
- 128 bit block size
- support 3 jenis key: 128, 192. 256 bit, dengan ronde 10, 12, 14.
- efisiensi software dan hardware
- kemanan relative tergantung algoritma yang digunakan
- menggunakan byte
- ditunjukkan dengan hexadecimal

## langkah enkripsi
1. input 128 bit,
2. dibagi jadi 16 bagian dimulai dari index ke-0
3. subtitusi dengan s-Box Enkripsi AES
4. shift row (baris 0 tidak geser, baris 1 geser kiri 1, dst)
5. mixColumn
6. XOR dengan kunci ronde

## Key Schedule
- misal, kunci 128 bit. dibagi 16 bit dan dikelompokkan menjadi 4 word
- 1 word = byte
- word pertama diXOR dengan fungsi G
- sisanya hanya XOR-XOR dari word lain

> note:  
> - untuk enkripsi dengan kunci 256 mendapat tambahan

## langkah Dekripsi
1. key add
2. invers mixColumn
3. invers shift row
4. byte s-Box dekripsi

# Medan Galois

- medan ini ada jika dia bilangan prima atau pangkatnya.
- berkisar di range 0 - 255 (256 bit)
- operator aritmatika, hasilnya tidak boleh kurang dari 0 atau lebih dari 255

## penjumlahan dan pengurangn dalam GF(2)
1. penjumlahan  = XOR
contoh: 10100 + **10011** = 00111

2. pengurangan = XOR
contoh: 10100 - 00111 = **10011**

Lho, kok sama?

Ternyata, penjumlahan = pengurangan.

3. Perkalian = perkalian (x + y)(lalala + uwu)

4. pembagian = a/b = a * b^-1


# Insight
1. kuat terhadap brute force
2. lemah jika ada komputer quantum

# PR
di buku pdf chapter 4