# CNN
_Convolutional Neural Network_ (_CNNs_) adalah jenis dari algoritma _deep learning_ yang digunakan untuk pengolahan data citra dan data sinyal. _CNNs_ menggunakan konsep konvolusi untuk mengidentifikasi pola dalam data masukan, seperti gambar atau sinyal audio.

_Convolutional Neural Network_ (_CNNs_) garis besarnya terdiri dari lapisan input, lapisan konvolusi, lapisan _pooling_, dan lapisan output. Lapisan konvolusi mengekstrak fitur dari data masukan dengan mengaplikasikan filter yang berbeda-beda pada data. Lapisan pooling mengurangi dimensi data dengan mengambil nilai maksimum atau rata-rata dari sekelompok data yang terkait. Lapisan _output_ mengolah fitur yang diekstrak dari lapisan konvolusi dan _pooling_ untuk menghasilkan _output_ yang benar.

Lapisan pada algoritma _CNNs_ memiliki _neuron_ yang diatur dalam 3 dimensi: _width_, _height_, dan _depth_. Dimensi _depth_ mengacu pada dimensi ketiga dari fungsi aktivasi, bukan kedalaman _neural network_ atau jumlah _total layer_ dalam jaringan.
![[CNN Depth, Height & Width.png]]
Gambar 2.1 CNN Architecture Shape

Berikut penjelasan lebih dalam tentang lapisan Convolutional Neural Network:
1. Input Layer, Lapisan masukan berfungsi sebagai penampungan dari nilai piksel citra yang menjadi input atau masukan (Tandungan, 2019). Input menyesuaikan dengan ukuran dan channel warna dari citra. Seperti contoh, jika terdapat citra grayscale yang berukuran 28x28 dan hanya memiliki 1 channel warna, maka input yang dibutuhkan adalah sebuah piksel array yang memiliki ukuran 28x28x1.
2. Convolutional Layer, merupakan lapisan inti dari metode CNN (Tandungan, 2019). Layer ini terdiri dari beberapa filter (atau kernel) yang berfungsi untuk mengekstraksi fitur atau pola tertentu pada gambar. Layer ini bekerja dengan memproses citra masukan dengan menerapkan filter konvolusi pada seluruh bagian citra secara bergeser (sliding window) untuk menghasilkan representasi fitur. Proses konvolusi pada layer convolution dilakukan dengan mengalikan setiap nilai piksel pada filter dengan nilai piksel yang bersesuaian pada gambar input, kemudian menjumlahkan hasilnya.
   ![[Convolutional Layer Flow 1.png]]
3. Activation Layer, Lapisan aktivasi (activation layer) merupakan lapisan yang berfungsi untuk memasukkan feature map ke fungsi aktivasi (Tandungan, 2019). Fungsi aktivasi yang diterapkan pada keluaran dari lapisan sebelumnya akan menentukan apakah neuron di lapisan tersebut harus diberi "sinyal hijau" atau "sinyal merah". Fungsi aktivasi juga membantu dalam mempercepat konvergensi selama pelatihan model. Contoh fungsi aktivasi yang umum digunakan adalah ReLU (Rectified Linear Unit), sigmoid, dan tanh. Fungsi ReLU mengubah semua nilai negatif menjadi nol dan meninggalkan nilai positif. Fungsi sigmoid menghasilkan nilai output yang berada dalam rentang 0 dan 1. Fungsi tanh menghasilkan nilai output yang berada dalam rentang -1 dan 1. Pemilihan fungsi aktivasi tergantung pada jenis tugas yang akan diselesaikan dan karakteristik dari data yang digunakan. Lapisan Aktivasi biasanya ditempatkan setelah lapisan konvolusi atau lapisan densitas dalam arsitektur jaringan saraf tiruan.
4. Pooling Layer, Pooling layer adalah lapisan dalam jaringan saraf konvulsional (Convolutional Neural Network/CNN) yang berguna untuk mengurangi dimensi spasial (ukuran) dari representasi fitur. Tujuannya adalah untuk mengurangi jumlah parameter (Lorentius, dkk. 2019). Pooling juga bisa disebut subsampling atau downsampling yang berfungsi untuk mengurangi dimensi feature map dengan tanpa menghilangkan informasi penting yang terdapat di dalamnya. Proses pertama pada pooling layer yaitu menentukan ukuran downsampling yang akan digunakan pada feature map. Kemudian dilakukan proses pooling pada feature map. Ada dua jenis pooling layer yang umum digunakan dalam CNN, yaitu max pooling dan average pooling. Pada max pooling, nilai terbesar diambil dari setiap area sebagai nilai keluaran:
   ![[MaxPooling flow.png]]
   sedangkan pada average pooling, nilai rata-rata diambil sebagai nilai keluaran:
   ![[AveragePooling Flow.png]]
5. Fully Connected Layer, Fully Connected Layer adalah jenis lapisan dalam arsitektur jaringan saraf tiruan (neural network) yang menghubungkan setiap neuron di lapisan ini dengan semua neuron di lapisan sebelumnya. Lapisan ini juga dikenal sebagai Dense Layer atau Linear Layer (Lorentius, dkk. 2019). Pada lapisan ini, setiap neuron pada lapisan ini menerima masukan dari setiap neuron pada lapisan sebelumnya dan menghasilkan keluaran berdasarkan bobot dan bias yang ditentukan selama pelatihan. Oleh karena itu, lapisan ini dapat mempelajari hubungan non-linear antara masukan dan keluaran, dan menghasilkan representasi fitur. Fully Connected Layer sering digunakan sebagai lapisan output pada arsitektur jaringan saraf tiruan untuk melakukan klasifikasi. 
   ![[Fully Connected Layer flow.png]]

_CNNs_ telah digunakan dalam berbagai aplikasi seperti klasifikasi gambar, deteksi objek, dan pengenalan suara (LeCun dkk, 2015).
## daftar pustaka
1. Tandungan, Sofyan. (2019). “Pengenalan Convolutional Neural Network – Part 1”. [Daring]. Tersedia pada: http://sofyantandungan.com/pengenalanconvolutional-neural-network-part-1/
2. Lorentius, C.A dkk. (2019). Pengenalan Aksara Jawa dengan Menggunakan Metode Convolutional Neural Network. Jurnal Infra Vol.7, No.1.


# Google Colaboratory
Google Colaboratory (Colab) adalah sebuah layanan cloud computing gratis yang disediakan oleh Google. Layanan ini memungkinkan pengguna untuk membuat dan menjalankan notebook Jupyter di cloud, yang dapat digunakan untuk memprogram dengan Python dan bahasa pemrograman lainnya. Colab juga menyediakan akses ke sumber daya komputasi yang kuat, seperti unit pemrosesan grafis (GPU) dan unit pemrosesan tensor (TPU) yang dapat digunakan untuk pelatihan model deep learning.

Colab sangat berguna bagi para peneliti, pengembang, dan siswa yang ingin menjalankan kode mereka di lingkungan yang terpisah dari komputer lokal mereka. Dalam Colab, pengguna dapat mengimpor dan menginstal library Python, menyimpan dan membagikan notebook, dan mengakses data yang tersimpan di Google Drive. Colab juga menyediakan integrasi dengan layanan Google seperti BigQuery, Google Sheets, dan Google Cloud Storage, sehingga memudahkan pengguna untuk melakukan analisis data yang besar dan bekerja dengan data yang tersimpan di cloud.

Penggunaan Google Colaboratory memerlukan akun Google untuk dapat diakses dan digunakan semua fitur yang terdapat di dalamnya. Penggunaan Google Colaboratory sama seperti Jupyter Noteboook, yaitu melakukan tugas-tugas atau perintah-perintah yang berorientasi sel. Google Colaboratory dapat digunakan untuk membuat macam-macam sel dan digunakan untuk buku catatan. (Google Colaboratory Documentation ,2023).

## daftar pustaka
Google Colaboratory Documentation, 2023, Frequently Asked Questions, [https://research.google.com/colaboratory/faq.html](https://research.google.com/colaboratory/faq.html), 26 Februari 2023.
# Android Studio
Tampilan antarmuka pada Android Studio dapat dilihat pada gambar di bawah.
![[Antar Muka Android Studio.png]]
Dari gambar di atas, dilihat bahwa tampilan Android Studio memiliki beberapa area yaitu:
## daftar pustaka
Google. “Android Studio User Guide”. [Daring]. Tersedia pada: https://developer.android.com/studio/intro. [Diakses: 3-Mar-2021].