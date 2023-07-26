- jelaskan berapa banyak data tiap digit (Lihat Comment di Bab 3)
- siapa yang saya wawancarai (Lihat Comment di Bab 3)
- bandingkan dataset yg belum augmentasi dengan sudah augmentasi dengan data yg sama atau digit yang sama (Lihat Comment di Bab 3)
- buat step2 atau list step dalam pembuatan arsitektur cnn (Lihat Comment di Bab 3)
- buat step2 atau list step dalam menginput kan data/ data preparasi (Lihat Comment di Bab 3)


# Collab
- liat berapa pixel each digit (collab), contoh ; liat 1 citra berapa shape nya/pixel nya

## buat step2 atau list step dalam pembuatan arsitektur cnn (Lihat Comment di Bab 3)
1. **Import Libraries**: Langkah pertama adalah mengimpor library yang diperlukan untuk membangun dan melatih model CNN. Beberapa library yang umum digunakan adalah TensorFlow atau Keras, NumPy, dan lainnya.
2. **Pra-Pemrosesan Data**: Data harus dipersiapkan sebelum digunakan dalam model CNN. Langkah ini melibatkan normalisasi data, pembagian data menjadi set pelatihan dan set validasi, serta pengubahan format data menjadi bentuk yang dapat diterima oleh model CNN.
3. **Pembentukan Arsitektur Model**: Ini adalah langkah utama dalam membangun model CNN. Pada tahap ini, kita menentukan lapisan-lapisan yang akan digunakan dalam model, termasuk lapisan konvolusi, lapisan pooling, dan lapisan fully connected. Arsitektur model ini akan menentukan bagaimana informasi diproses dan bagaimana jaringan mempelajari representasi-fitur dari gambar.
4. **Inisialisasi Model**: Model CNN perlu diinisialisasi sebelum pelatihan dimulai. Inisialisasi ini termasuk penentuan fungsi aktivasi, optimizer, dan fungsi kerugian (loss function) yang akan digunakan dalam proses pelatihan.
5. **Pelatihan Model**: Pada tahap ini, model CNN akan dilatih menggunakan set pelatihan. Proses pelatihan ini melibatkan perhitungan gradien, penyesuaian bobot (weights) dan bias, serta iterasi berulang untuk mencapai bobot yang optimal.
6. **Evaluasi Model**: Setelah model selesai dilatih, langkah berikutnya adalah mengevaluasi kinerjanya menggunakan set validasi atau set pengujian. Evaluasi ini dilakukan untuk menilai sejauh mana model dapat melakukan prediksi dengan akurat pada data yang tidak digunakan dalam pelatihan.
7. **Penyempurnaan Model**: Jika hasil evaluasi belum memuaskan, langkah selanjutnya adalah menyempurnakan model dengan melakukan tuning parameter, mengubah arsitektur, atau menambahkan teknik regularisasi agar mendapatkan kinerja yang lebih baik.

## buat step2 atau list step dalam menginput kan data/ data preparasi 
