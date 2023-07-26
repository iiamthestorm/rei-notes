# Pembukaan
- Bismillahirrohmanirrohim...
- Assalamu'alaikum wr wb......
- Yang terhormat ibu Ause Labellapansa, S.T., M.Kom., M.Cs sebagai dosen penguji,
	- Yang terhormat ibu Ana Yulianti, S.Kom., M.Kom sebagai dosen penguji,
	- dan Yang terhormat Ibu Nesi Syafitri N, S.Kom., M.Cs sebagai dosen pembimbing saya.
- Perkenalkan nama saya Reihan Maulana, disini izinkan saya untuk mempresentasikan hasil penelitian skripsi yang saya buat dengan "Pemanfaatan Augmentasi Data Dalam Klasifikasi Handwritten Digit Images Menggunakan Algoritma CNNs Berbasis Android"

# Latar Belakang
latar belakang dari penelitian ini adalah.........


# Deep Learning
![[Pasted image 20230315170219.png]]

_Deep learning_ merupakan subbidang _machine learning_ yang algoritmanya terinspirasi dari struktur otak manusia. Deep Learning memiliki kemampuan untuk mempelajari representasi data yang semakin kompleks dan abstrak melalui suatu jaringan neuron tiruan. Deep learning ini sendiri dapat menyelesaikan berbagai permasalahan yang sulit diselesaikan dengan algoritma machine learning lainnya.

Dalam penggunaannya, Deep Learning banyak digunakan pada aplikasi yang membutuhkan analisis data yang kompleks dan memerlukan pemahaman data yang lebih dalam, seperti:

1.  Pengenalan wajah dan pengenalan suara
2.  Deteksi objek pada gambar
3.  Penerjemahan bahasa alami
4.  Pengenalan tulisan tangan dan citra medis
5.  Sistem rekomendasi
6.  Pendeteksian spam dan cyber-security

Namun, penggunaan Deep Learning juga memiliki tantangan yang signifikan, seperti:

1.  Ketergantungan terhadap data yang sangat besar dan bervariasi untuk melatih model
2.  Kompleksitas arsitektur jaringan neuron

Itulah ulasan singkat tentang Deep Learning. Selanjutnya kita akan membahasa apa itu neural network, 

# Neural Network
![[Pasted image 20230315170325.png]]

Neural Network adalah sebuah model matematika yang terinspirasi dari cara kerja otak manusia. Model ini terdiri dari sejumlah besar neuron atau sel saraf buatan (artificial neurons) yang dihubungkan satu sama lain dalam sebuah jaringan. Neural Network dapat digunakan untuk mempelajari pola-pola kompleks dari data.

Konsep dasar dari Neural Network adalah bahwa setiap neuron menerima sinyal masukan, memproses sinyal tersebut, dan menghasilkan keluaran (output) yang kemudian dapat digunakan oleh neuron lain dalam jaringan. Jaringan Neural terdiri dari beberapa lapisan atau layer, dimana setiap layer terdiri dari sejumlah neuron. 

Ada beberapa jenis neural network, salah satunya adalah convolutional neural network yang akan saya bahas di slide selanjutnya

# Convolutional Neural Network
![[Pasted image 20230315170344.png]]

Convolutional Neural Network (CNN) adalah salah satu jenis neural network yang digunakan khususnya untuk memproses data spasial seperti gambar atau video. CNN memanfaatkan operasi konvolusi atau filter untuk mengidentifikasi fitur-fitur pada gambar. Operasi konvolusi pada CNN melibatkan filter atau kernel yang digeser (sliding) ke seluruh area gambar untuk menghasilkan sebuah feature map atau peta fitur.

Konsep dasar dari CNN adalah bahwa setiap layer pada CNN terdiri dari beberapa filter atau kernel yang dapat mempelajari fitur-fitur yang berbeda pada gambar. Setiap filter pada layer tersebut akan mencari pola-pola tertentu pada gambar dan menghasilkan feature map yang akan digunakan sebagai input untuk layer berikutnya.

Ada beberapa jenis layer pada CNN, diantaranya:
1. Convolutional Layer: layer yang terdiri dari beberapa filter atau kernel yang digunakan untuk menghasilkan feature map.
2. Pooling Layer: layer yang digunakan untuk mengurangi dimensi dari feature map dengan melakukan operasi penggabungan (pooling) pada beberapa area pada feature map.
3. Fully-Connected Layer: layer yang terhubung dengan seluruh neuron pada layer sebelumnya, dan biasanya digunakan pada akhir jaringan CNN untuk menghasilkan output klasifikasi.

Penerapan CNN dalam pengenalan gambar memiliki beberapa keunggulan, antara lain:
1.  Mampu mempelajari fitur-fitur pada gambar secara hierarkis dan otomatis.
2.  Robust terhadap variasi posisi, rotasi, dan ukuran objek pada gambar.
3.  Mampu memproses dan mempelajari data gambar dalam bentuk matriks piksel yang besar dan kompleks.

Namun, penggunaan CNN juga memiliki beberapa tantangan dan kelemahan, diantaranya:
1.  Memerlukan daya komputasi yang besar dan waktu pelatihan yang lama terutama untuk data gambar yang sangat besar dan kompleks.
2.  Memerlukan jumlah data yang cukup besar untuk memperoleh model yang akurat.


# Augmentasi Data
![[Pasted image 20230315170355.png]]

Teknik augmentasi data adalah teknik yang digunakan untuk menghasilkan data baru dari data yang ada dengan melakukan manipulasi atau modifikasi pada data tersebut. Beberapa contoh teknik augmentasi data pada gambar antara lain flipping, cropping, scaling, rotation. Dengan teknik augmentasi data, jumlah data yang tersedia untuk pelatihan model dapat ditingkatkan sehingga diharapkan model menjadi lebih akurat dan generalisasi dengan baik pada data yang belum pernah dilihat sebelumnya.
# Alur Desain Aplikasi
![[Pasted image 20230726224226.png]]
Alur Desain aplikasi adalah :
1.    Tahapan data preparasi digunakan untuk mengumpulkan data yang dibutuhkan. Langkah ini meliputi mengunggah dataset dari _Library TensorFlow_ ke platform _Google Colab_.

2.    Tahapan EDA yang sering disebut dengan _Explanatory Data Analysis_ merupakan merupakan proses pemeriksaan dan pembersihan agar data siap dipakai. EDA biasanya dilakukan sebagai tahap awal dalam proses analisis data untuk membantu memandu analisis dan pemodelan selanjutnya. Pemanfaatan Augmentasi Data akan dilakukan di tahap ini. Langkah ini dilakukan di platform _Google Colab_.

3.    Tahapan selanjutnya adalah pembuatan arsitektur model CNN dengan menentukan jumlah dari _convolutional layer_, _pooling layer_, _filter_ dan model _fully connected layer_ yang tersusun dari beberapa _layer_, setiap _layer_ memiliki beberapa _neuron_ yang saling berhubungan. Sistem memiliki 2 macam model yang akan dibuat, Pertama yaitu _Pre-Augmented model_ yang mana model ini dibuat tanpa menggunakan teknik Data Augmentasi. Kedua yaitu _Post-Augmented model_ yang mana model ini dibuat dengan menggunakan teknik Data Augmentasi. Langkah ini dilakukan di platform _Google Colab_.

4.    Tahapan selanjutnya adalah _Training_, _Training_ merupakan tahapan yang penting dari keberhasilan sebuah sistem yang dibangun. Jika hasil dari tahapan ini bagus, maka kemungkinan besar sistem bekerja dengan baik. Output yang dihasilkan dari tahapan proses ini adalah sebuah _model fitting_ yang merupakan ciri ciri dari klasifikasi _handwritten digit image_. _Model fitting_ ini akan digunakan sebagai validasi dan perbandingan bobot dalam proses _testing_. Langkah ini dilakukan di platform _Google Colab_.

5.    Tahapan selanjutnya adalah _Validating_. Tahapan ini bertujuan untuk mengetahui seberapa baik kinerja sistem dalam mengklasifikasikan _handwritten digit image_. Pada tahap _validation_, dilakukan proses validasi dengan melakukan perbandingan _model fitting_ yang didapat dari tahapan _training_ sebelumnya. Langkah ini dilakukan di platform _Google Colab_.

6.      Tahapan selanjutnya yaitu melakukan konversi pada model dan mengintegrasikannya ke dalam platform Android dengan menggunakan _Library TensorFlow Lite_ dan _Android Studio_ menggunakan bahasa pemrograman _Kotlin_.

7.      Tahapan terakhir adalah _Testing_. Pada tahapan ini, testing dilakukan dengan menggambar digit menggunakan jari pada aplikasi yang telah dibangun di perangkat android, kemudian hasil klasifikasi digit tersebut dievaluasi untuk menentukan tingkat akurasi model.

# Hasil dan Pembahasan
Evaluasi model dilakukan secara langsung dengan melakukan 10 kali pengujian pada 5 posisi yaitu atas (top), kiri (left), kanan (right), dan bawah (below) pada tiap digit melalui aplikasi yang telah diimplementasikan dengan model yang telah dibuat. Hasil dari setiap pengujian terdiri dari dua hal, yaitu Confidence dan hasil prediksi.

Confidence adalah ukuran tingkat kepercayaan model terhadap hasil prediksi tunggal. Confidence digunakan untuk memahami sejauh mana model yakin dengan prediksi tertentu. Sedangkan hasil prediksi adalah kondisi di mana model yang telah dilatih berhasil mengklasifikasikan atau memperkirakan nilai target.

## Atas (Top)
### Pre-Augmentasi
Model ini berhasil memprediksi digit 1 dan 3 dengan baik, terutama ketika Confidence >= 80. Namun, model ini mengalami kesulitan dalam memprediksi digit 0, 2, 4, 5, 6, 7, 8, dan 9 pada posisi atas.

### Post-Augmentasi
Model ini memiliki performa yang baik dalam memprediksi sebagian besar digit dengan confidence >= 80. Namun, digit 2 memiliki prediksi yang benar sebanyak 5 kali, namun dengan confidence < 80, yang mana jumlahnya lebih banyak daripada prediksi yang benar dengan confidence >= 80 sebanyak 4 kali.

## Bawah (Bottom)
### Pre-Augmentasi
Model pre-augmentasi berhasil memprediksi digit 1 dan 2 dibandingkan dengan digit lainnya dengan confidence lebih >= 80. Namun model pre-augmentasi mengalami kesulitan memprediksi pada beberapa digit seperti 0, 3, 4, 5, 6, 7, 8, dan 9. 

### Post-Augmentasi
Model post-augmentasi berhasil memprediksi semua digit dengan benar, terutama ketika confidence >= 80. Namun, hanya digit 2 yang memiliki rasio antara confidence >= 80 dan confidence < 80 pada prediksi benar yang sama, yaitu sebanyak 4 kali.

## Kiri (Left)
### Pre-Augmentasi
Model pre-augmentasi gagal memprediksi semua digit dengan benar. Pada prediksi benar, tingkat confidence < 80 lebih banyak dibandingkan confidence >= 80. 

### Post-Augmentasi
Model post-augmentasi berhasil memprediksi semua digit dengan benar, terutama ketika confidence >= 80. Namun, hanya digit 2 yang memiliki prediksi salah sebanyak 1 dengan confidence < 80. 

## Kanan (Right)
### Pre-Augmentasi
Model pre-augmentasi berhasil memprediksi digit 2 dan 4 namun gagal dalam memprediksi 0, 1, 3, 5, 6, 7, 8, 9. Digit 2 dan 4 memiliki jumlah hasil prediksi benar dan confidence >= 80 lebih banyak daripada prediksi benar dan confidence < 80.

### Post-Augmentasi
Model post-augmentasi berhasil memprediksi digit 0, 2, 3, 4, 5, 6, 7, 8 tetapi gagal dalam memprediksi digit 1 dan 9.

## Tengah (Middle)
### Pre-Augmentasi
Model pre-augmentasi cukup berhasil memprediksi semua digit dengan benar.

### Post-Augmentasi


# Penutup
Baik itu adalah presentasi singkat dari saya.