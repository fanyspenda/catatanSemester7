# minggu 3 - Block Cipher

## DES Algorithm

- bekerja per 64 bit
- didevelop oleh IDM
- masuk standar NBS/NIST
- key hanya 56 bit
- 3DES dikembangkan
- kunci meningkat sehingga aman lagi

### cara kerja

1. confusion = mengaburkan relasi key dan cipher text
2. diffusion = membuat pengaruh 1 plaintext tersebar, sehingga tidak mudah ditebak

langkah diatas dapat dilakukan berulang kali agar semakin sulit untuk ditebak

### algoritma DES

input: 64 bit
key: 56 bit
output: 64 bit
ronde: 16

1. kunci diubah mejadi 16 subkey untuk dilakukan di tiap2 ronde.
2.
