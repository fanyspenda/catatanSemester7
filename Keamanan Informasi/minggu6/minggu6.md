# Minggu 6 - Public Key Cryptography

## Simetric cryptography revisited
- kunci sama.
  analoginya, ada brankas. ada 2 orang yang punya kunci untuk membukanya. jika salah seorang jahat, maka salahsatu yang lainnya akan rugi. (2 belah pihak bisa saling menipu)
- kunci harus disampaikan dalam jalur yang aman.
- terlalu banyak kunci jika banyak orang berkomunikasi.

- contoh: stream cipher dan block cipher

## Asymetric cryptography
sebelum tahun 76an, semuanya simetris, setelah itu, ada usulan untuk membuat enkripsi dimana ada 2 kunci, 1 kunci public, 1 kunci private.

kunci publik disebar, kunci private untuk pribadi.

## Mekanisme
- menghindari penyangkalan pesan (bikin pesan tapi gk ngaku).
- key distribution, menyediakan kunci public.
- Enkripsi = 1000 kali lebih lambat dari skema simetrik
- kenapa bisa mendekripsi dengan private key, meskipun cipher text dari public key? karena menggunakan matematika yang tidak lazim.

## Hybrid
karena ada kelemahan di mekanisme asimetrik, maka muncul gabungan Asimetrik dan simetrik.
nyebar kunci pake asimetrik, enkripsi pake simetrik.

## One Way Function
fungsi yang tidak bisa dibalik. metodenya:
- Kurfa eleptrik
- RSA, DL

## Key Length and Security Level
Simetrik = 64, 80, 128 bit
Kurva Eleptrik = 128, 160, 256 bit
RSA, DL = 700, 1024, 3072 bit

key awal = bisa dibobol beberapa jam/hari
key tengah = bisa dibobol kalo diserang oleh korporat besar
key kanan = bisa dibobol tapi butuh waktu lama (kecuali kalo ada kuantum komputer)

# Masuk ke Matematikanya
## GCD = FPB
contoh:
90 dan 30
90 = 2, 2, 3, 7
30 = 2, 3, 5

GCD = 2 x 3 = 6

kelemahan: ngehitungnya lama.

cara hitung yang lebih cepat adalah.....

## Eucledian Algorithm
caranya adalah:
GCD (angka terkecil, angka terbesar)
contoh: gcd(30, 84) 

= gcd(30, 24)

= gcd(24, 6)

= gcd(6, 0)

BOOOOM !!!

## Euler's phi
untuk mencari ada berapa banyak bilangan yang dapat diinverskan

## Euler phi fungsi 2/2 (lanjutan)
contoh:
modulus 899, cari faktor prima dari 899 = 29 x 31

= (29^1 - 29^(1-1))x(31^1 - 31^(1-1))

= (29 - 1) (31 - 1)

= 840
