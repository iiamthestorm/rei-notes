- ~~Revisi Bu Ana
	- ~~daftar pustaka minimal 20
	- ~~explain desain sistem dari diagram kemudian baru text 
	- ~~Tinjauan Pustaka 
	- ~~Caption


## Diagram Tahapan data augmentasi
1. Pra-Pemrosesan Data:
    - Normalisasi: Setiap piksel gambar dikonversi menjadi skala nilai antara 0 hingga 1 dengan membagi dengan nilai maksimum piksel (255).
2. Penambahan Dimensi Warna:
    - Tambahkan dimensi warna pada gambar dalam dataset "train" dan "validate" menggunakan np.expand_dims. Ini bertujuan untuk memenuhi kebutuhan input data augmentation pada ImageDataGenerator.
3. Data Augmentasi:
    - Rotasi: Gambar-gambar dalam dataset dirotasi dengan sudut acak hingga 30 derajat.
    - Pergeseran Lebar dan Tinggi: Gambar-gambar digeser ke arah horizontal dan vertikal dengan jarak acak hingga 25% dari lebar dan tinggi gambar.
    - Pemotongan (Shear): Beberapa bagian gambar dipotong dan digeser untuk menghasilkan efek kemiringan hingga 25%.
    - Perbesaran (Zoom): Gambar-gambar dipotong dan diperbesar atau diperkecil hingga 20%.
4. Pembentukan Data Augmentasi:
    - Data augmentasi dihasilkan dari dataset "train" dan "validate" menggunakan ImageDataGenerator. Data augmentasi ini akan digunakan sebagai input dalam pelatihan dan evaluasi model.

Dengan demikian, data augmentasi dari gambar MNIST telah dibentuk sesuai dengan langkah-langkah di atas untuk meningkatkan variasi data pelatihan dan membantu model lebih tangguh dan handal dalam mengenali angka-angka dari gambar.

