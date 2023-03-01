_Convolutional Neural Network_ (_CNNs_) adalah jenis dari algoritma _deep learning_ yang digunakan untuk pengolahan data citra dan data sinyal. _CNNs_ menggunakan konsep konvolusi untuk mengidentifikasi pola dalam data masukan, seperti gambar atau sinyal audio.

_Convolutional Neural Network_ (_CNNs_) terdiri dari lapisan input, lapisan konvolusi, lapisan _pooling_, dan lapisan output. Lapisan konvolusi mengekstrak fitur dari data masukan dengan mengaplikasikan filter yang berbeda-beda pada data. Lapisan pooling mengurangi dimensi data dengan mengambil nilai maksimum atau rata-rata dari sekelompok data yang terkait. Lapisan _output_ mengolah fitur yang diekstrak dari lapisan konvolusi dan _pooling_ untuk menghasilkan _output_ yang benar.

_Convolutional Neural Network_ (_CNNs_) memiliki arsitektur yang berbeda dari _Neural Network_ biasa. _Neural Network_ biasa mengubah input dengan menempatkannya melalui serangkaian _hidden layer_. Setiap _hidden layer_ terdiri dari sekumpulan _neuron_, di mana setiap _layer_ terhubung secara penuh ke semua _neuron_ pada _layer_ sebelumnya. Akhirnya, ada _fully-connected layer_ – _output layer_ - yang menghasilkan prediksi.

Lapisan pada algoritma _CNNs_ memiliki _neuron_ yang diatur dalam 3 dimensi: _width_, _height_, dan _depth_. Dimensi _depth_ mengacu pada dimensi ketiga dari fungsi aktivasi, bukan kedalaman _neural network_ atau jumlah _total layer_ dalam jaringan.

Rumus matematis yang digunakan dalam _Convolutional Neural Network_ (_CNNs_) meliputi:
1. _Convolution Operation_: digunakan untuk mengekstrak fitur dari _input image_ dengan mengaplikasikan filter/kernel yang telah dipelajari. Rumusnya adalah:
   **f'(i,j) = sum(f(i+m,j+n) * w(m,n))**
   Dimana f adalah _input image_, w adalah kernel/filter yang telah dipelajari, dan f' adalah _output_ dari operasi konvolusi.
2. ReLU (_Rectified Linear Unit_) _Activation Function_: digunakan untuk menambah non-linearitas pada CNN. Rumusnya adalah: