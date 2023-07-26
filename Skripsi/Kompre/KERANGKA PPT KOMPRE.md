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

Alur Desain aplikasi adalah :
1. Pertama, kita membuka Google Colab, kemudian menggantinya menjadi runtime dengan akselerator GPU. Dengan menggunakan akselerator GPU, proses training data dapat dilakukan dengan lebih cepat.
2. kemudian, kita panggil semua library yang diperlukan seperti TensorFlow, Numpy, Pandas, atau matplotlib.
3. Kemudian, dataset dimuat dari _library TensorFlow_ dengan menggunakan fungsi **`mnist.load_data()`** pada _sub-library_ **`keras.datasets`**.
4. Kemudian, kita akan membuat dua model menggunakan bahasa pemrograman Python, yaitu model pre-augmentasi dan model post-augmentasi. Model pre-augmentasi adalah model yang tidak menggunakan data augmentasi alias hanya mentraining data asli. Model post-augmentasi adalah model yang menggunakan data augmentasi, data augmentasi dapat digunakan dengan _library_ **TensorFlow** pada sub-library keras.preprocessing.image.ImageDataGenerator.
5. Setelah 2 model di training dan divalidasi, kita akan mulai mengkonversi model yang didapatkan dengan TensorFlow Lite. Hal ini dilakukan karena model yang biasanya dihasilkan setelah training tidak bisa dimuat ke dalam android, karena android memiliki keterbatasan dalam hal penyimpanan. 
6. Kemudian, kita akan membuat source code untuk menampung model tf.lite yang telah kita download dengan bahasa pemrograman kotlin di Android Studio. Disini kita mulai membuat Komponen View untuk menampilkan halaman yang nantinya kita bisa gunakan untuk menginputkan/menggambarkan digit melalui jari kita.





# Penutup
Baik itu adalah presentasi singkat dari saya, izinkan saya untuk mendemokan aplikasi yang saya buat.