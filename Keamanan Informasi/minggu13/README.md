# Minggu 14 - MACs

## Prinsip MAC

- Hanya 2 orang yang memiliki kunci.
- Skema simetris digunakan sebagai pembuat tanda, dikirim ke penerima, penerima membuat tanda dengan kunci yang sama. jika tanda sama, maka valid.
- Tidak ada anti-penyangkalan.
- Biasa digunakan pada protokol-protokol.
- Lebih cepat daripada tanda-tangan digital karena MAC menggunakan skema simetris.
-

## keunggulan MAC

- Keaslian pesan (memang dari yang bersangkutan). Dilihat dari tanda yang dibuat dari pesan dan kunci. Kunci bisa sama antara kedua belah pihak karena sudah ada kesepakatan.
- Keutuhan pesan.
- Checksum untuk mencek keaslian dan keutuhan pesan.
- Panjang MAC sudah fix.

## Hash MAC (HMAC)

Karena Hash tidak ada kunci, sedangkan MAC ada kunci, maka jika digabung, dilakukan dengan cara Kunci MAC di hash. Contoh penerapannya di TLS.

## MAC dari Block Ciphers

menggabungkan metode-metode enkripsi pada block cipher. Yang popular adalah menggunakan AES di CBC mode.
contoh: CBC-MAC
