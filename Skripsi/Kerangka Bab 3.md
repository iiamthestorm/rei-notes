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

Dataset ini diakses melalui library tensorflow public dataset yang menyediakan akses ke berbagai macam dataset populer untuk keperluan pengembangan dan riset di bidang deep learning yang selanjutnya akan dimasukkan ke Google Colaboratory. Dataset dipanggil menggunakan library TensorFlow dengan menggunakan fungsi `mnist.load_data()` pada sub-library `keras.datasets` dan akan dimasukkan ke variable seperti (train_images, train_labels), (test_images, test_labels). 

Setiap gambar/image pada dataset MNIST memiliki label atau kelas yang sesuai dengan digit yang digambarkan pada gambar tersebut. Data training pada dataset MNIST terdiri dari 60.000 gambar digit tulisan tangan yang telah diverifikasi dengan benar. Data validation pada dataset MNIST terdiri dari 10.000 gambar digit tulisan tangan yang berbeda dengan data training dan digunakan untuk menguji dan membandingkan hasil learning dengan dataset training di setiap epoch-nya.

Normalisasi data juga perlu dilakukan pada langkah ini. setiap piksel gambar pada data training dan validation akan dinormalisasi agar nilainya berada pada rentang antara 0 hingga 1. Hal ini dilakukan agar data dapat diproses dengan lebih efektif oleh algoritma CNN yang akan digunakan. Normalisasi juga dapat membantu mencegah terjadinya divergensi saat model dilatih, karena nilai yang terlalu besar dapat memperlambat konvergensi model. Dengan melakukan normalisasi, nilai piksel pada gambar akan memiliki skala yang sama sehingga memudahkan model dalam mempelajari pola-pola pada gambar.

### Data Augmentasi
Setelah normalisasi data, langkah kedua dalam melakukan penelitian ini adalah melakukan data augmentasi. Data augmentasi adalah teknik yang digunakan untuk memperluas jumlah data pelatihan dengan membuat variasi kecil pada data yang ada. 

Pada langkah ini, data augmentation akan dilakukan menggunakan library TensorFlow Keras .ImageDataGenerator. Dalam generator ini, objek datagen akan didefinisikan dan beberapa parameter augmentasi seperti rotasi gambar, pergeseran gambar/translasi, dan zoom in/out akan ditentukan. Dengan menggunakan generator ini, data latih dan data uji akan terus di-augmentasi secara acak saat pelatihan model, sehingga diharapkan dapat menghasilkan model yang lebih baik dalam menggeneralisasi data baru.

Setelah objek datagen didefinisikan, kita menggunakan method flow dari objek tersebut untuk menghasilkan augmented data dari dataset yang telah kita normalisasi. Hasilnya, kita akan mendapatkan dataset baru berisi data augmentasi yang siap digunakan.

Penting untuk diingat bahwa model yang menggunakan data augmentasi adalah post-augmented model, sementara pre-augmented model tidak melakukan data augmentasi. Setelah melakukan normalisasi pada data, langkah selanjutnya adalah membuat model CNN untuk pre-augmented model, sedangkan untuk post-augmented model, data akan dilakukan augmentasi terlebih dahulu sebelum diproses pada model CNN.

### Pembuatan Model CNN
Setelah dilakukan data augmentasi pada dataset, tergantung ingin membuat model pre-augmented atau model post-augmented, kita akan merancang struktur CNN.

Berdasarkan Kinerja CNN yang sangat baik dalam komputer vision, maka arsitektur yang akan dibangun pada penelitian ini terdiri dari dua tahap, yaitu feature learning dan classification. Input gambar pada model CNN menggunakan citra yang memiliki ukuran 28x28x1. Angka 1 tersebut merupakan citra yang hanya memiliki 1 channel yaitu grayscale. Citra masukan atau input kemudian diproses melalui proses convolution dan pooling yang dilakukan pada tahapan feature learning. 

Jumlah proses convolution pada rancangan ini memiliki dua lapisan convolution. Jumlah proses Pooling pada rancangan ini juga memiliki dua lapisan pooling. Setiap konvolusi memiliki jumlah filter yang berbeda tetapi memiliki ukuran kernel yang sama. Kemudian dilakukan proses flatten yang berfungsi untuk mengubah feature map dari hasil pooling layer menjadi bentuk vector. Proses ini disebut dengan proses fully Connected layer. Berikut adalah rancangan dari arsitektur CNN pada penelitian ini :
![[FlowChart CNN Architecture (3).png]]
Berdasarkan gambar di atas, dapat dijelaskan bahwa arsitektur CNN terdiri dari dua tahap utama, yaitu Feature Learning dan Classification. Feature learning merupakan teknik untuk memungkinkan sistem dapat secara otomatis mengekstraksi fitur-fitur dari sebuah gambar menjadi representasi numerik. Representasi ini kemudian digunakan dalam tahap Classification, di mana model menggunakan fitur-fitur tersebut untuk melakukan klasifikasi gambar ke dalam kelas atau subclass yang telah ditentukan sebelumnya. Dengan demikian, CNN memungkinkan penggunaan gambar sebagai input untuk melakukan klasifikasi secara otomatis. Jika gambar diatas diatas diubah kedalam bentuk arsitektur LeNet, maka dapat dilihat seperti gambar berikut:
![[CNN Architecture Diagram.png]]

Convolution pertama menggunakan filter sebanyak 32 dan kernel dengan matriks 3x3. Kemudian dilakukan pooling menggunakan ukuran 2x2 dengan pergeseran mask dua langkah. Kemudian Convolution kedua menggunakan filter sebanyak 64 dan kernel dengan matriks 3x3. Kemudian dilakukan pooling lagi menggunakan ukuran 2x2 dengan pergeseran mask dua langkah. 

Setelah proses Convolution dilakukan, output dari proses tersebut akan diubah menggunakan Flatten layer. Flatten layer melakukan perubahan output dari proses konvolusi dengan mengubah tensor multidimensi menjadi tensor satu dimensi untuk diproses lebih lanjut. Kemudian, proses klasifikasi dilakukan menggunakan Multi Layer Perceptron (MLP) yang terdiri dari satu lapisan tersembunyi dengan jumlah neuron yang telah ditentukan. Kelas dari citra kemudian diklasifikasikan berdasarkan nilai neuron pada lapisan tersembunyi dengan menggunakan fungsi aktivasi softmax.

### Training and Testing
Proses training dan testing merupakan bagian terpenting dari keberhasilan proses CNN, yang mana proses CNN dapat dikatakan berhasil jika proses training dan testing memiliki hasil yang akurat. 

Sebelum melakukan training dan testing, terdapat pemanggilan fungsi `compile` yang digunakan terlebih dahulu untuk mengkonfigurasi model CNN. 

Pada fungsi `compile`, kita menentukan optimizer yang digunakan (dalam hal ini 'adam'), loss function yang digunakan (dalam hal ini 'sparse_categorical_crossentropy'), serta metrics yang digunakan untuk mengukur kinerja model (dalam hal ini 'accuracy').

Setelah itu, proses training akan dilakukan dengan memanggil fungsi `fit` pada model. Jika ingin training model menggunakan data yang telah di augmentasi, data tersebut bisa didapat dari tahap augmentasi data pada materi sebelumnya, yaitu dengan memanggil objek datagen berupa variabel seperti (`train_generator`). Jumlah epoch yang digunakan untuk proses training adalah 5, serta data validasi yang digunakan adalah data testing yang telah diaugmentasi sebelumnya berupa variable (`test_generator`).

Untuk training model menggunakan data yang tidak diaugmentasi, data bisa langsung di panggil dari tahap Input Image sebelumnya. Kemudian langkah selanjutnya tetap sama seperti Jumlah epoch yang digunakan untuk proses training adalah 5 serta data validasi yang digunakan adalah data testing yang tidak diaugmentasi sebelumnya berupa variable (test_images, test_labels).
