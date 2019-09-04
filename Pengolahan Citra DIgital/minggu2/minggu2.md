# Minggu 2 PCD

## Image
- Image = sinyal 2 Dimensi

1. Analoog Image

- Gambar yang terus bersambung, seperti gambar yang diprint
- tidak bisa diproses di komputer
- dibuat dari device analog

2. Digital Image
   - Bitmap = jika dizoom, akan pecah, terdiri dari pixel
   - Vector = jika dizoom, tidak pecah, terdiri dari titik

## Image Operation
1. Point = output bergantung pada input value di koordinat yang sama
2. local = output bergantung pada sekitarnya
3. global = output value bergantung pada seluruh value yang ada pada pixel

## image acquisition
- mengatur image dari source cahaya hingga menjadi objek digital (citra)

## Image DIgitalization
- sampling
- Quantizing
- Resolution

### Sampling
Hanya sebagian informasi yang diambil (ada bagian yang hilang), tapi tidak memengaruhi citra aslinya.

> **Note**  
> - sistem ukuran citra adalah tinggi x lebar
> - koordinat citra mulai dari 0 (seperti array)
> - notasi pixel = f(tinggi, lebar)=nilai pixel
> - image = ada gambar aslinya
> - picture = tidak ada gambar aslinya

### Quantization
- kedalaman warna,
- bergantung pada bit warna,
- 1 bit = 2 warna, 2 bit = 4 warna,....,8 bit = 256 warna (2^n)

> **note: menghitung quantisasi pixel**  
> misal:  
> ada image 7 bit 4 kotak masing2 90, 110, 20, 56. ubah jadi 2 bit.  
> 2^7 - 2^2 = 2^5 = 32  
> artinya, jumlah warna dari 7 bit akan dibagi sebanyak 4x (sesuai jumlah warna bit tujuan) dan masing2 bagian terdiri dari 32 warna.  
> 0 - 31 -> 0  
> 32 - 63 -> 1  
> 64 - 95 -> 2  
> 96 - 127 -> 3  

## DPI
- Dot per inch
- 1 inch = 2,54 cm
- memengaruhi kualitas gambar
- tidak bisa diukur secara kasat mata, harus menggunakan lensa khusus
- printer jarum < inkjet < laserjet

> Note:  
> Resolusi -> berhubungan dgn DPI
> canvas Size/ukuran gambar -> Tinggi x Lebar

> Contoh Soal:  
> scanner dengan DPI 300 menscan gambar berukuran 3x4 inch. Maka, 
> 
> ``` 
> jumlah_pixel = (3(300) * 4(300)) = 1080000 px.
> ```
>   
> Jika ukuran file adalah 3 byte / pixel, maka:  
> ```
> ukuran file = (1080000 * 3) = 3MB
> ```

> format tugas  
> TugasPraktikum#2_kelas_NIM_Nama.zip