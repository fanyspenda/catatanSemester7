# Keamanan Informasi - Stream Cipher

## Karakteristik
- cepat, kecil. (Biasanya digunakan pada embedded device seperti smartphone, arduino, dll)
- Meng-Encrypt per bit
- 1 gerbang XOR pada input maupun output
- bisa juga dicari dengan penjumlahan `mod 2`


## karakteristik Block cipher
- encrypt per blok (beberapa bit)
- biasanya digunakan pada protokol atau aplikasi internet

A | B | A XOR B
---|---|---
0 | 0 | 0
0 | 1 | 1
1 | 0 | 1
1 | 1 | 0

## time needed to send comparison
3DES < DES < AES < RC4

## Synchronous vs Asynchronous Stream cipher

## Syarat/Tantangan Stream Cipher
- Membuat kunci yang tidak bisa ditebak
- kunci harus bisa digenerate oleh penerima pesan
- praktis

## 1. RNG
- True RNG -> based random physic
- Pseudorandom NG

### True RNG
- tidak mudah ditebak tapi tidak bisa digenerate ulang oleh penerima

### Pseudorandom NG
- mudah ditebak tapi bisa digenerate ulang oleh penerima

### Cryptocalygraphy Secure RNG

## 2. One-Time Pad
- tidak mudah ditebak dan bisa digenerate oleh penerima.
- menyediakan kunci sesuai pesan yang dikirim dan hanya bisa digunakan 1 kali.
- kelemahan: tidak praktis(hanya bisa dipakai 1 kali, dan besar kunci = besar pesannya).

## 3. Linear Feedback shift register
- merupakan dasar dari memori.
- menggunakan gerbang logika XOR.
- tidak mudah ditebak, bisa digenerate oleh penerima, dan praktis.
- kelemahan: terdapat pola berulang (tergantung pada jumlah Shift Register)
- Initialitation Vector yang dikirimkan agar bisa digenerate di penerima

## 4. Trivium: LFSR but more complex
- ada kesepakatan di clock berapa akan berkomunikasi
- memiliki banyak Shift register