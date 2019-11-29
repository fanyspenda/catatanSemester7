# Minggu 14 - Steganografi

- prisoner's problem
- misal, alice dan bob akan komunikasi, mereka mau kabur dari penjara. mereka sepakat lari jam 1. ada penjaga namanya Fred.
- gimana caranya bob dan alice merencanakan untuk kabur?
- metode 1: enkripsi => menjadi pesan yang tidak terbaca, Fred curiga.
- metode 2: mengubah pesan menjadi bentuk pesan yang lain. Fred nggak curiga. ini disebut **steganografi.**
- contoh: mengubah pesan dari gambar ke text, dari text ke suara, gambar ke gambar, dll.

## istilah
- embedded object = objek rahasianya
- cover object = objek penutup
- stego object = embedded object + cover object
- stego key = kunci untuk membuka stego object

## Tujuan
- untuk menghindari kecurigaan
- untuk menyembunyikan pesan (kalau enkripsi untuk membuat pesan tidak bisa dibaca)

## Teknik
- spatial domain
- transform domain

### Spatial Domain
- mengubah bit yang paling tidak berbobot (Least Significant Bit) dari cover text dengan pesan rahasianya dalam bentuk biner.

# Watermarking
- untuk memberikan perlindungan copyright
- menyediakan cara validasi data
- ada kriteria robustness (sulit dihapus) (jika gambar diubah, seperti kompres, crop, dll maka watermark akan hilang)
- watermark bisa dianggap digital signature, tapi beda tujuan.

## Watermark vs Digital Signature
- Watermark untuk melindungi hak cipta, DS untuk menjaga keaslian dan penyangkalan pesan.
- cover object watermark yang terpenting, DS hidden objectnya yang penting.
- watermark bersifat tidak dirahasiakan, DS bersifat rahasia.

## visible dan invisible watermarking
- visible = watermark bisa dilihat
- invisible = watermark tidak terlihat