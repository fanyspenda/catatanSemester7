# DHKE (Diffie Hellman Key Exchange)
- DHKE untuk Pertukaran kunci (Bukan distribusi kunci)
- Elgamal untuk enkripsi
- ada 3 kunci, Kgabungan, k public, k private

## step:
1. pilih prima
2. integer alpha E {2,3, ..., p-2}
3. publish beta dan alpha

k public = (alpha ^ a) mod P
k gabungan AB = (alpha ^ a)^b mod P
k gabungan BA = (alpha ^ b)^a mod P

a = kunci private si A, random bebas
b = kunci private si B, random bebas

# Diskrit Logarithm Problem

Menemukan integer x dimana x = 1<=x<=n

- Finite Group (Z) adalah himpunan
- contoh: Zn dengan n = 10, berarti dari nilai ... sampai 10 (bisa dari negatif, kecuali diberi tanda mutlak |Z|n)
- beta = a * a * a... = a^x

- atau bisa dicari dengan rumus:
x = log alpha * beta mod P

## Penyerangan DLP
in generic algorithm
- Brute-Force
- Shanks baby step giant step
- pollard rho method
- pohling hellman

in non generic algorithm
- index calculus method

panjang kunci 532 (tidak lebih besar dari RSA, tapi masih lebih besar dari Simmetric)

# Elgamal
- ditemukan tahun 1985
- sebagai extension dari DHKE
- skema hampir sama dengan DHKE, tapi bisa enkripsi


## Mekanisme
- seperti DHKE
- 