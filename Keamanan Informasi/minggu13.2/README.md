# Minggu 13.2 Penyediaan Kunci

## Key Transport
satu pihak membuat kunci rahasia dan menyebarkannya ke pihak terkait.

## Key Agreement
Pihak terkait membuat kunci bersama- sama.

# ISSUE
- Kesegaran kunci (*Key freshness*)
  - diharapkan sebuah kunci itu selalu berubah-ubah. Misal: kunci berhasil diserang oleh hacker. jika perombakan kunci terjadi tiap 1 minggu. maka Hacker hanya bisa merusak data yang kita punya selama 1 minggu.
- membuat kunci baru (*Key Derivation*)
  - untuk menyegarkan kunci, berarti kita perlu membuat kunci baru secara berkala. Daripada membuat kunci baru, maka lebih baik membuat *kunci session* seperti pada DES di *Simetric cipher*.

## Distribusi Kunci Terpusat (Key Distribution Center)
Merupakan Skema Simetris.
1. pihak terpercaya membuat kunci.
2. KDC membagikan KEK.
3. Jika A ada yang mau berkomunikasi dengan B, maka A harus meminta izin ke KDC.
4. jika sudah diberi izin, maka KDC akan memberikan key session untuk A dan B.
5. lalu, A dan B memiliki kunci yang sama untuk berkomunikasi.

## Kelebihan KDC
- distribusi kunci lebih sedikit dari Asimetris (jumlah kunci pada Distribusi kunci asimetris adalah 2n, sedangkan KDC n)
- kesegaran kunci terjamin karena setiap ada permintaan untuk berkomunikasi, harus melalui pihak terpercaya dulu.

## Kekurangan KDC
- communication bottleneck, karena setiap komunikasi harus melalui moderator.
- single point of failure, jika moderator berhasil diserang, maka semua komunikasi akan diketahui, termasuk yang sudah berlalu (dilihat di log/database)

## Sertifikat digital
1. CA memberikan sertifikat pada A dan B
2. Sertifikat digenerate oleh masing-masing pihak
3. A memberikan sertifikat ke B dan sebaliknya
4. A dan B memverifikasi sertifikat
5. jika valid, maka baru membuat kunci bersama untuk komunikasi. 

- Setifikat memiliki rentang waktu.