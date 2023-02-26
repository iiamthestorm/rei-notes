## Tinjauan Umum Objek Penelitian
![[Pasted image 20230217155907.png]]

Penelitian ini bertujuan untuk mengevaluasi pengaruh pemanfaatan teknik augmentasi data pada akurasi klasifikasi handwritten digit image menggunakan platform android. Objek penelitian dari skripsi ini adalah hasil akurasi dari pemanfaatan augmentasi data dalam klasifikasi handwritten digit image.

Dalam konteks penelitian ini, permasalahan yang ingin dijawab adalah apakah teknik augmentasi data dapat meningkatkan akurasi klasifikasi handwritten digit image. Untuk menjawab permasalahan tersebut, dilakukan perbandingan hasil akurasi yang diperoleh menggunakan augmentasi data dengan hasil akurasi yang diperoleh tanpa pemanfaatan teknik augmentasi data.

Dengan melakukan penelitian ini diharapkan dapat memberikan gambaran yang lebih jelas tentang dampak pemanfaatan teknik augmentasi data pada akurasi klasifikasi handwritten digit image.

Data yang digunakan dalam penelitian ini adalah data gambar MNIST (Modified National Institute of Standards and Technology). Dataset ini adalah kumpulan data gambar yang terdiri dari angka-angka tulisan tangan (handwritten digits) dari 0 hingga 9. Dataset ini sering digunakan sebagai bahan latihan dalam masalah klasifikasi gambar. Setiap gambar dalam dataset MNIST adalah gambar hitam-putih berukuran 28x28 piksel yang ditulis tangan oleh berbagai penulis.

## Kondisi Saat Ini (Analisa Sistem yang Sedang Berjalan)
![[Pasted image 20230220172618.png]]
Saat ini, penggunaan teknologi semakin meluas dan berdampak besar pada berbagai bidang, termasuk bidang pengenalan karakter tulisan tangan. Klasifikasi handwritten digit images merupakan salah satu aplikasi dari pengenalan karakter tulisan tangan yang telah banyak dikembangkan dan digunakan pada platform Android. Algoritma Convolutional Neural Networks (CNNs) menjadi salah satu algoritma yang populer digunakan dalam proses klasifikasi tersebut. Meskipun begitu, terdapat masalah dalam akurasi klasifikasi handwritten digit images yang memerlukan perbaikan.

Rendahnya akurasi klasifikasi handwritten digit images menjadi masalah serius yang perlu dipecahkan. Hal ini disebabkan oleh berbagai faktor, termasuk variasi bentuk tulisan tangan dan perbedaan sudut pandang saat mengambil gambar. Oleh karena itu, penelitian ini berusaha untuk meningkatkan akurasi klasifikasi dengan memanfaatkan teknik augmentasi data. Teknik augmentasi data merupakan teknik yang dapat digunakan untuk menghasilkan data training baru dari data yang ada dengan melakukan berbagai macam transformasi pada gambar asli, seperti rotasi, pemotongan, dan pengubahan ukuran. 

## Alat dan Bahan Penelitian yang Digunakan
![[Pasted image 20230220182455.png]]
1. Processor Intel Core i5/AMD Ryzen 5 atau lebih.
2. Random Access Memory (RAM) 8GB atau lebih.
3. Solid State Drive (SSD) Minimal 256GB atau lebih.
4. Smartphone Realme c25 atau jenis lainnya.
5. Mouse.
6. Keyboard.
Berikut ini adalah spesifikasi software yang digunakan dalam proses penelitian ini:
1. Sistem Operasi Windows 11 Pro.
2. Web Browser Google Chrome.
3. Google Colaboratory.
4. Bahasa Pemrograman Python.
5. Deep Learning Library seperti TensorFlow.
6. Android Studio Electric Eel 2022.1.1.



## Teknik Pengumpulan Data
Adapun teknik pengumpulan data yang diperlukan oleh peneliti meliputi beberapa metodologi sebagai berikut:
1. Wawancara untuk pengumpulan informasi yang berkatian tentang penelitian kepada narasumber yang mengetahui tentang handwritten images.
2. Studi Pustaka dengan membaca literature buku, jurnal, makalah maupun artikel berkaitan dengan penelitian.
3. Sumber data yang dijadikan bahan penelitian oleh penulis bersumber dari dataset MNIST (_Modified National Institute of Standards and Technology_). Dataset ini adalah kumpulan data gambar yang terdiri dari angka-angka tulisan tangan (_handwritten digits_) dari 0 hingga 9. Dataset ini sering digunakan sebagai bahan latihan dalam masalah klasifikasi gambar. Setiap gambar dalam dataset MNIST adalah gambar hitam-putih berukuran 28x28 piksel yang ditulis tangan oleh berbagai penulis.
## Desain Sistem
Bab ini akan memberikan penjelasan tentang Langkah atau tahapan dan perancangan aplikasi penelitian agar prosesnya dapat terlihat lebih terstruktur sehingga proses penelitian dapat dipahami dengan baik. 

Penelitian ini dirancang untuk melakukan pemanfaatan teknik augmentasi data pada klasifikasi handwritten digit images menggunakan metode Convolutional Neural Network (CNN) berbasis Android.

Beberapa pertanyaan akan timbul ketika membangun sebuah sistem, seperti contoh "sistem apa yang akan dibangun?", "Bagaimana alur proses dari sistem tersebut?", "Bagaimana cara kerja dari sistem tersebut?". Oleh karena itu, diperlukan perancangan sistem, sehingga sistem akan tergambar lebih jelas dan mudah dipahami.

Sistem yang akan dibangun dalam penelitian ini meliputi beberapa tahap yaitu:
1. Tahapan data preparation digunakan untuk mengumpulkan data yang dibutuhkan.
2. Tahapan EDA yang sering disebut dengan Explanatory Data Analysis merupakan merupakan proses pemeriksaan dan pembersihan agar data siap dipakai. EDA biasanya dilakukan sebagai tahap awal dalam proses analisis data untuk membantu memandu analisis dan pemodelan selanjutnya. Pemanfaatan Augmentasi Data akan dilakukan di tahap ini.
3. Tahapan selanjutnya membuat pemodelan sistem dengan menentukan jumlah dari convolutional layer, pooling layer, filter dan model fully connected layer yang tersusun dari beberapa layer, setiap layer memiliki beberapa neuron yang saling berhubungan. Sistem memiliki 2 macam model yang akan dibuat, Pertama yaitu Pre-Augmented model yang mana model ini dibuat tanpa menggunakan teknik Data Augmentasi. Kedua yaitu Post-Augmented model yang mana model ini dibuat dengan menggunakan teknik Data Augmentasi.
4. Tahapan selanjutnya adalah Training, Training merupakan tahapan yang penting dari keberhasilan sebuah sistem yang dibangun. Jika hasil dari tahapan ini bagus, maka kemungkinan besar sistem bekerja dengan baik. Output yang dihasilkan dari tahapan proses ini adalah sebuah model fitting yang merupakan ciri ciri dari klasifikasi handwritten digit image. Model fitting ini akan digunakan sebagai validasi dan perbandingan bobot dalam proses testing.
5. Tahapan selanjutnya adalah Testing. Tahapan ini bertujuan untuk mengetahui seberapa baik kinerja sistem dalam mengklasifikasikan handwritten digit images. Pada tahap testing, dilakukan proses validasi dengan melakukan perbandingan model fitting yang didapat dari tahapan training sebelumnya.
6. Tahapan terakhir yaitu melakukan konversi pada model dan mengintegrasikannya ke dalam platform Android. 

Desain arsitektur sistem yang akan dibangun pada penelitian ini digambarkan seperti gambari 3.1. berikut:
![[Digit Classifier Diagram.png]]

Proses pada desain arsitektur sistem pada penelitian ini dimulai dari membuat source code untuk mengimplementasikan Convolutional Neural Network (CNN) dan mengimpor Framework Tensorflow yang dibuat menggunakan infrastruktur Google Colaboratory dengan bahasa pemrograman Python dan disimpan dalam bentuk file Jupyter Notebooks (.ipynb) dan kemudian disimpan ke Github. Selanjutnya dataset pelatihan tersebut diambil dari TensorFlow library nya sendiri dan disimpan ke dalam tempat penyimpanan sementara pada Google Colaboratory. 

Sistem ini dirancang dengan menggunakan arsitektur jaringan Convolutional Neural Network (CNN) dan terdiri dari dua model, yaitu pre-augmented model dan post-augmented model. Pre-augmented model tidak menggunakan teknik augmentasi data, sementara post-augmented model menggunakan teknik augmentasi data. Hal ini dilakukan untuk membandingkan kinerja kedua model dalam mengenali objek pada dataset yang sama, serta memperlihatkan apakah teknik augmentasi data dapat meningkatkan performa model dalam mengenali objek.

Perancangan Pre-Augmented model yang akan dibangun pada penelitian ini digambarkan secara sederhana, seperti gambar berikut :

![[Pre-Augmented Model.drawio.png]]
Gambar 3.2 Desain Pre-Augmented Model

Sedangkan perancangan Post-Augmented model yang akan dibangun pada penelitian ini digambarkan seperti gambar berikut :
![[Post-Augmented Model.png]]

Gambar 3.3 Desain Post-Augmented Model

Dari gambar desain di atas, terlihat bahwa kedua model memiliki arsitektur yang sama. Perbedaan utama antara keduanya terletak pada tahap augmentasi data yang dilakukan setelah tahap pre-processing pada model post-augmented. Dalam model pre-augmented, tahap augmentasi data tidak dilakukan sehingga data input langsung digunakan untuk training. Sedangkan pada model post-augmented, data input akan melalui tahap augmentasi terlebih dahulu sebelum digunakan untuk training.

### Input Image
Langkah pertama dalam melakukan penelitihan ini yaitu input data dengan melakukan pembagian data yang berisi 2 macam gambar, yaitu:
1. Data training, yang digunakan untuk proses learning.
2. Data testing, yang digunakan untuk validasi ketika proses learning berlangsung.

Dataset yang digunakan untuk klasifikasi handwritten digit image terdiri dari dataset training dan validation. Kedua dataset tersebut akan digunakan untuk melatih algoritma CNN sehingga dapat memperoleh model yang akurat. Seluruh dataset yang digunakan untuk pelatihan menggunakan gambar grayscale (satu saluran warna) dengan ukuran 28x28 piksel yang mana sudah sesuai untuk dimasukkan ke model. 

Dataset ini diakses melalui library tensorflow public dataset yang menyediakan akses ke berbagai macam dataset populer untuk keperluan pengembangan dan riset di bidang deep learning yang selanjutnya akan dimasukkan ke Google Colaboratory.