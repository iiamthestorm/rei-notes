## preface
Sebelum sistem yang dibangun dipublikasikan, beberapa tahapan harus dilakukan untuk memastikan bahwa aplikasi telah benar-benar siap tanpa kesalahan.

Pada bab ini, akan dibahas tentang hasil pengujian model. Evaluasi model dilakukan secara langsung dengan melakukan 10 kali pengujian pada 5 posisi yaitu atas (top), kiri (left), kanan (right), dan bawah (below) pada tiap digit secara manual melalui aplikasi yang telah diimplementasikan dengan model yang telah dibuat. Hasil dari setiap pengujian terdiri dari dua hal, yaitu Confidence dan Hasil Prediksi.

Confidence adalah ukuran tingkat kepercayaan model terhadap hasil prediksi tunggal. Confidence digunakan untuk memahami sejauh mana model yakin dengan prediksi tertentu. Sedangkan Hasil Prediksi adalah kondisi di mana model yang telah dilatih berhasil mengklasifikasikan atau memperkirakan nilai target. Dari hasil prediksi ini, metriks akurasi dapat digunakan untuk mengukur sejauh mana model berhasil dalam melakukan prediksi yang benar dari total hasil prediksi yang dilakukan. Akurasi menghitung jumlah prediksi yang benar dibandingkan dengan jumlah total data yang diprediksi.

## Performance Results for Digit 0
### Digit 0 - Top Position

| Pengujian             | Confidence Pre-Augmentasi | Hasil Prediksi Pre-Augmentasi | Confidence Post-Augmentasi | Hasil Prediksi Post-Augmentasi |
| --------------------- | ------------------------- | ----------------------------- | -------------------------- | ------------------------------ |
| 1                     | 95.5                      | 4 (salah)                     | 99.4                       | 0 (benar)                      |
| 2                     | 65.6                      | 4 (salah)                     | 94.4                       | 0 (benar)                      |
| 3                     | 89.3                      | 4 (salah)                     | 97.9                       | 0 (benar)                      |
| 4                     | 63.4                      | 8 (salah)                     | 88.0                       | 0 (benar)                      |
| 5                     | 68.7                      | 4 (salah)                     | 77.2                       | 0 (benar)                      |
| 6                     | 70.1                      | 8 (salah)                     | 99.6                       | 0 (benar)                      |
| 7                     | 68.1                      | 9 (salah)                     | 99.7                       | 0 (benar)                      |
| 8                     | 91.6                      | 4 (salah)                     | 99.9                       | 0 (benar)                      |
| 9                     | 93.9                      | 4 (salah)                     | 98.4                       | 0 (benar)                      |
| 10                    | 87.9                      | 4 (salah)                     | 99.8                       | 0 (benar)                      |
| Average of Confidence | 79.41                     | -                             | 95.43                      | -                              |
| Total Benar Prediksi  |                           | 0                             |                            | 10                             |

Berdasarkan hasil rata-rata confidence, model sebelum Pre-Augmentasi mencapai rata-rata confidence sekitar 79,41%, sementara model Post-Augmentasi mencapai rata-rata confidence sekitar 95,43% pada posisi "Atas".

Akurasi yang diperoleh dari model Pre-Augmentasi adalah sebesar 0%, sementara Akurasi yang diperoleh dari model Post-Augmentasi adalah sebesar 100%. 

### Digit 0 - Bottom Position

| Percobaan            | Akurasi Pre-Augmentasi | Hasil Prediksi Pre-Augmentasi | Akurasi Post-Augmentasi | Hasil Prediksi Post-Augmentasi |
| -------------------- | ---------------------- | ----------------------------- | ----------------------- | ------------------------------ |
| 1                    | 45.6                   | 6 (salah)                     | 63.8                    | 0 (benar)                      |
| 2                    | 41.1                   | 6 (salah)                     | 96.1                    | 0 (benar)                      |
| 3                    | 88.1                   | 6 (salah)                     | 93.2                    | 0 (benar)                      |
| 4                    | 44.8                   | 2 (salah)                     | 86.8                    | 0 (benar)                      |
| 5                    | 73.0                   | 2 (salah)                     | 97.7                    | 0 (benar)                      |
| 6                    | 85.5                   | 8 (salah)                     | 81.1                    | 0 (benar)                      |
| 7                    | 51.5                   | 6 (salah)                     | 77.4                    | 0 (benar)                      |
| 8                    | 97.9                   | 2 (salah)                     | 42.5                    | 0 (benar)                      |
| 9                    | 84.7                   | 2 (salah)                     | 88.4                    | 0 (benar)                      |
| 10                   | 73.2                   | 2 (salah)                     | 99.0                    | 0 (benar)                      |
| Average              | 68.54                  | -                             | 82.6                    | -                              |
| Total Benar Prediksi |                        | 0                             |                         | 10                             |

Berdasarkan hasil rata-rata akurasi, model sebelum augmentasi mencapai rata-rata akurasi sekitar 68,54%, sementara model setelah augmentasi mencapai rata-rata akurasi sekitar 82,6% pada posisi "Bawah".

Berdasarkan Total Benar Prediksi, model sebelum Pre-Augmentasi memperoleh Total Benar Prediksi sebanyak 0 (semua prediksi salah), sementara model Post-Augmentasi memperoleh Total Benar Prediksi sebanyak 10 (semua prediksi benar) pada posisi "Bawah".

### Digit 0 - Left Position

| Percobaan            | Akurasi Pre-Augmentasi | Hasil Prediksi Pre-Augmentasi | Akurasi Post-Augmentasi | Hasil Prediksi Post-Augmentasi |
| -------------------- | ---------------------- | ----------------------------- | ----------------------- | ------------------------------ |
| 1                    | 94.8                   | 7 (salah)                     | 71.1                    | 0 (benar)                      |
| 2                    | 42.8                   | 7 (salah)                     | 95.9                    | 0 (benar)                      |
| 3                    | 61.5                   | 1 (salah)                     | 52.2                    | 0 (benar)                      |
| 4                    | 93.9                   | 1 (salah)                     | 96.1                    | 0 (benar)                      |
| 5                    | 88.7                   | 1 (salah)                     | 73.2                    | 0 (benar)                      |
| 6                    | 90.3                   | 1 (salah)                     | 94.7                    | 0 (benar)                      |
| 7                    | 99.0                   | 1 (salah)                     | 58.5                    | 2 (salah)                      |
| 8                    | 54.0                   | 1 (salah)                     | 96.7                    | 0 (benar)                      |
| 9                    | 93.2                   | 1 (salah)                     | 88.2                    | 0 (benar)                      |
| 10                   | 54.4                   | 4 (salah)                     | 71.2                    | 0 (benar)                      |
| Average              | 77.26                  | -                             | 79.78                   | -                              |
| Total Benar Prediksi |                        | 0                             |                         | 9                              |

Berdasarkan hasil rata-rata akurasi, model sebelum augmentasi mencapai rata-rata akurasi sekitar 77,26%, sementara model setelah augmentasi mencapai rata-rata akurasi sekitar 79,78% pada posisi "Kiri".

Berdasarkan Total Benar Prediksi, model sebelum Pre-Augmentasi memperoleh Total Benar Prediksi sebanyak 0 (semua prediksi salah), sementara model Post-Augmentasi memperoleh Total Benar Prediksi sebanyak 9 pada posisi "Kiri".

### Digit 0 - Right Position

| Percobaan            | Akurasi Pre-Augmentasi | Hasil Prediksi Pre-Augmentasi | Akurasi Post-Augmentasi | Hasil Prediksi Post-Augmentasi |
| -------------------- | ---------------------- | ----------------------------- | ----------------------- | ------------------------------ |
| 1                    | 92.8                   | 1 (salah)                     | 92.5                    | 0 (benar)                      |
| 2                    | 98.6                   | 4 (salah)                     | 84.7                    | 0 (benar)                      |
| 3                    | 91.5                   | 1 (salah)                     | 96.9                    | 0 (benar)                      |
| 4                    | 94.1                   | 4 (salah)                     | 87.0                    | 0 (benar)                      |
| 5                    | 75.6                   | 1 (salah)                     | 99.8                    | 0 (benar)                      |
| 6                    | 83.2                   | 1 (salah)                     | 99.8                    | 0 (benar)                      |
| 7                    | 60.8                   | 1 (salah)                     | 97.9                    | 0 (benar)                      |
| 8                    | 99.4                   | 4 (salah)                     | 68.3                    | 6 (salah)                      |
| 9                    | 92.8                   | 1 (salah)                     | 93.6                    | 0 (benar)                      |
| 10                   | 99.7                   | 1 (salah)                     | 73.6                    | 0 (benar)                      |
| Average              | 88.85                  | -                             | 89.41                   | -                              |
| Total Benar Prediksi |                        | 0                             |                         | 9                              |

Berdasarkan hasil rata-rata akurasi, model sebelum augmentasi mencapai rata-rata akurasi sekitar 88,85%, sementara model setelah augmentasi mencapai rata-rata akurasi sekitar 89,41% pada posisi "Kanan".

Berdasarkan Total Benar Prediksi, model sebelum Pre-Augmentasi memperoleh Total Benar Prediksi sebanyak 0 (semua prediksi salah), sementara model Post-Augmentasi memperoleh Total Benar Prediksi sebanyak 9 pada posisi "Kanan".

### Digit 0 - Middle Position

| Percobaan            | Akurasi Pre-Augmentasi | Hasil Prediksi Pre-Augmentasi | Akurasi Post-Augmentasi | Hasil Prediksi Post-Augmentasi |
| -------------------- | ---------------------- | ----------------------------- | ----------------------- | ------------------------------ |
| 1                    | 99.9                   | 0 (benar)                     | 99.1                    | 0 (benar)                      |
| 2                    | 72.9                   | 0 (benar)                     | 97.4                    | 0 (benar)                      |
| 3                    | 95.9                   | 0 (benar)                     | 94.8                    | 0 (benar)                      |
| 4                    | 99.5                   | 0 (benar)                     | 85.5                    | 0 (benar)                      |
| 5                    | 99.1                   | 0 (benar)                     | 98.4                    | 0 (benar)                      |
| 6                    | 97.8                   | 0 (benar)                     | 97.5                    | 0 (benar)                      |
| 7                    | 51.6                   | 0 (benar)                     | 98.8                    | 0 (benar)                      |
| 8                    | 99.9                   | 0 (benar)                     | 95.2                    | 0 (benar)                      |
| 9                    | 98.6                   | 9 (salah)                     | 97.3                    | 0 (benar)                      |
| 10                   | 98.4                   | 0 (benar)                     | 80.1                    | 0 (benar)                      |
| Average              | 91.36                  | -                             | 94.41                   | -                              |
| Total Benar Prediksi |                        | 9                             |                         | 10                              |

Berdasarkan hasil rata-rata akurasi, model sebelum augmentasi mencapai rata-rata akurasi sekitar 91,36%, sementara model setelah augmentasi mencapai rata-rata akurasi sekitar 94,41% pada posisi "Tengah".

Berdasarkan Total Benar Prediksi, model sebelum Pre-Augmentasi memperoleh Total Benar Prediksi sebanyak 9, sementara model Post-Augmentasi memperoleh Total Benar Prediksi sebanyak 10 (semua prediksi benar) pada posisi "Tengah".

## Performance Results for Digit 1
### Digit 1 - Top Position

| Percobaan            | Akurasi Pre-Augmentasi | Hasil Prediksi Pre-Augmentasi | Akurasi Post-Augmentasi | Hasil Prediksi Post-Augmentasi |
| -------------------- | ---------------------- | ----------------------------- | ----------------------- | ------------------------------ |
| 1                    | 99.9                   | 0 (benar)                     | 99.1                    | 0 (benar)                      |
| 2                    | 72.9                   | 0 (benar)                     | 97.4                    | 0 (benar)                      |
| 3                    | 95.9                   | 0 (benar)                     | 94.8                    | 0 (benar)                      |
| 4                    | 99.5                   | 0 (benar)                     | 85.5                    | 0 (benar)                      |
| 5                    | 99.1                   | 0 (benar)                     | 98.4                    | 0 (benar)                      |
| 6                    | 97.8                   | 0 (benar)                     | 97.5                    | 0 (benar)                      |
| 7                    | 51.6                   | 0 (benar)                     | 98.8                    | 0 (benar)                      |
| 8                    | 99.9                   | 0 (benar)                     | 95.2                    | 0 (benar)                      |
| 9                    | 98.6                   | 9 (salah)                     | 97.3                    | 0 (benar)                      |
| 10                   | 98.4                   | 0 (benar)                     | 80.1                    | 0 (benar)                      |
| Average              | 91.36                  | -                             | 94.41                   | -                              |
| Total Benar Prediksi |                        | 9                             |                         | 10                             |










## dst


