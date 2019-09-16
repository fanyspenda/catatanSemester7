# SPK Minggu 3 - Analythical Hierarchy Process

## Analythical Hierarchy Process
pengambilan keputusan berdasarkan perbandingan antar kriteria dan perbandingan antar pilihan.

### Tahapan
1. menyusun hirarki/diagram masalah yang dihadapi
2. membuat perbandingan berpasangan antara kriteria dengan alternatif

| intensitas kepentingan | Keterangan                                 |
| ---------------------- | ------------------------------------------ |
| 1                      | kedua elemen sama penting                  |
| 3                      | Salahsatu elemen **sedikit** lebih penting |
| 5                      | Salahsatu elemen lebih penting             |
| 7                      | Salahsatu elemen **mutlak** lebih penting  |
| 9                      | Salahsatu elemen **mutlak** penting        |
| 2,4,6,8                | Nilai antar elemen yang berdekatan         |

misal A=kriteria, dan A1-A3 adalah elemen, maka:

| ... | A1  | A2  | A3  |
| --- | --- | --- | --- |
| A1  | 1   | ... | ... |
| A2  | ... | 1   | ... |
| A2  | ... | ... | 1   |

3. menentukan bobot prioritas
4. Menghitung Consistency Ratio
5. Menghitung perbandingan berpasangan yang bersesuaian
6. mengambil keputusan
   
## Bobot Prioritas
1. membagi setiap cell dengan jumlah ***kolom*** yang bersesuaian

Contoh: cell A1*A2(misal: kolomxbaris)=A1
2. Bobot prioritas adalah Jumlah tiap ***baris***, lalu dirata-rata.

## Consistency Ratio
1. mengalikan matrix dengan prioritas, lalu membaginya dengan priority weight. 
2. menghitung LambdaMax = jumlah perkalian pada step 1 dengan jumlah elemen.
3. Index Konsistensi = CI = (LambdaMax-N)/(N-1)
4. Rasio Konsistensi = CI/RI, jika rasio konsistensi <= 0.1, hasil = benar

| n   | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   | 11   |
| --- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| RC  | 0.00 | 0.00 | 0.58 | 0.90 | 1.12 | 1.24 | 1.32 | 1.41 | 1.45 | 1.49 | 1.51 |