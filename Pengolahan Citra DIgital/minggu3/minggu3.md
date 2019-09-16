# Minggu 3 - PCD

## Warna
1. Grayscale = hanya ada 1 warna pada 1 pixel
   ukuran citra = size * ukuran bit
2. True Color (Citra RGB) = ada RGB dalam 1 pixel
   ukuran citra = size * ukuran bit

## File Format
1. Raster/Bitmap
2. Vector

## RGB
- bersifat additive
- jika menggunakan 8 bit perchannel, maka memiliki (256^3) warna
- menggabungkan 2 warna RGB = CMY

## Image Element
1. Brightness,
   Intensitas cahaya, didapat dengan menghitung setiap rata-rata pada pixel
2. Kontras
   sebarang terang dan gelap, bisa diukur dengan *histogram*. kontras yang baik adalah kontras yang nilainya berkumpul di tengah.

> Note:
> - histogram kontras = bergeser, tapi tinggi sama,
> - histogram brighness = bergeser, tapi tinggi berubah
> 
3. Kontur
   keadaan yang ditimbulkan oleh perubahan intensitas pada pixel yang bertetangga
4.  Warna
   merupakan persepsi mata manusia yang melihat kombinasi gelombang cahaya yang berbeda
5. Bentuk 
   bentuk merupakan properti intrinsik objek tiga dimensi
6. Textur
   Distribusi spasial dari derahat keabuan

## Invers dan logaritmic Brightness
### invers
- membalikan citra dengan mengurangkan nilai maximal dengan nilai asli:
- misal, R = 255 - nilai channel R

### Logaritmic Brightness
- Membuat brightness yang bisa dikembalikan