_Convolutional Neural Network_ (_CNNs_) adalah jenis dari algoritma _deep learning_ yang digunakan untuk pengolahan data citra dan data sinyal. _CNNs_ menggunakan konsep konvolusi untuk mengidentifikasi pola dalam data masukan, seperti gambar atau sinyal audio.

_Convolutional Neural Network_ (_CNNs_) terdiri dari lapisan input, lapisan konvolusi, lapisan _pooling_, dan lapisan output. Lapisan konvolusi mengekstrak fitur dari data masukan dengan mengaplikasikan filter yang berbeda-beda pada data. Lapisan pooling mengurangi dimensi data dengan mengambil nilai maksimum atau rata-rata dari sekelompok data yang terkait. Lapisan _output_ mengolah fitur yang diekstrak dari lapisan konvolusi dan _pooling_ untuk menghasilkan _output_ yang benar.

_Convolutional Neural Network_ (_CNNs_) memiliki arsitektur yang berbeda dari _Neural Network_ biasa. _Neural Network_ biasa mengubah input dengan menempatkannya melalui serangkaian _hidden layer_. Setiap _hidden layer_ terdiri dari sekumpulan _neuron_, di mana setiap _layer_ terhubung secara penuh ke semua _neuron_ pada _layer_ sebelumnya. Akhirnya, ada _fully-connected layer_ – _output layer_ - yang menghasilkan prediksi.

Lapisan pada algoritma _CNNs_ memiliki _neuron_ yang diatur dalam 3 dimensi: _width_, _height_, dan _depth_. Dimensi _depth_ mengacu pada dimensi ketiga dari fungsi aktivasi, bukan kedalaman _neural network_ atau jumlah _total layer_ dalam jaringan.
![[CNN Depth, Height & Width.png]]
Gambar 2.1 CNN Architecture Shape


Convolutional Neural Network (CNN) memiliki beberapa lapisan atau layer utama sebagai berikut:
1. Input Layer, Lapisan masukan berfungsi sebagai penampungan dari nilai piksel citra yang menjadi input atau masukan (Tandungan, 2019). Input menyesuaikan dengan ukuran dan channel warna dari citra. Seperti contoh, jika terdapat citra grayscale yang berukuran 28x28 dan hanya memiliki 1 channel warna, maka input yang dibutuhkan adalah sebuah piksel array yang memiliki ukuran 28x28x1.
2. Convolutional Layer, merupakan lapisan inti dari metode CNN (Tandungan, 2019). Layer ini bekerja dengan memproses citra masukan dengan menerapkan filter konvolusi pada seluruh bagian citra secara bergeser (sliding window) untuk menghasilkan representasi fitur








Rumus matematis yang digunakan dalam _Convolutional Neural Network_ (_CNNs_) meliputi:
1. _Convolution Operation_: digunakan untuk mengekstrak fitur dari _input image_ dengan mengaplikasikan filter/kernel yang telah dipelajari. Rumusnya adalah:
   **f'(i,j) = sum(f(i+m,j+n) * w(m,n))**
   Dimana f adalah _input image_, w adalah kernel/filter yang telah dipelajari, dan f' adalah _output_ dari operasi konvolusi.
2. ReLU (_Rectified Linear Unit_) _Activation Function_: digunakan untuk menambah non-linearitas pada CNN. Rumusnya adalah:
   **f(x) = max(0,x)**
   Dimana x adalah _input_ dan f(x) adalah _output_ dari fungsi aktivasi ReLU.
3. _Pooling Operation_: digunakan untuk mengurangi dimensi spasial dari _feature_ map yang dihasilkan oleh operasi konvolusi. Ada dua jenis _pooling_ yang sering digunakan, yaitu _max pooling_ dan _average pooling_. Rumus _max pooling_ adalah:
   **f'(i,j) = max(f(i:i+n, j:j+n))**
   Dimana f adalah _feature map_ yang dihasilkan oleh operasi konvolusi, f' adalah _output_ dari operasi _pooling_, dan n adalah ukuran _pooling window_.

_CNNs_ telah digunakan dalam berbagai aplikasi seperti klasifikasi gambar, deteksi objek, dan pengenalan suara (LeCun dkk, 2015).