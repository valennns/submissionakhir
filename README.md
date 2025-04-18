🐾 Proyek Klasifikasi Gambar: Animal Faces Classification

Selamat datang di proyek klasifikasi gambar! Proyek ini bertujuan membangun model deep learning untuk mengklasifikasikan gambar wajah hewan ke dalam beberapa kategori menggunakan TensorFlow dan Keras. Dataset yang digunakan adalah Animal Faces Dataset, dan proyek ini mencakup tahap preprocessing, augmentasi data, pelatihan model CNN, konversi ke format TFLite, serta evaluasi hasil. 🚀

📑 Daftar Isi
📘 Ikhtisar Proyek
🗂️ Dataset
📦 Persyaratan
⚙️ Cara Menjalankan
▶️ Penggunaan
🏗️ Arsitektur Model
🏋️ Pelatihan dan Evaluasi
📊 Hasil
🤝 Kontribusi



📘 Ikhtisar Proyek

Proyek ini mengembangkan model Convolutional Neural Network (CNN) untuk mengklasifikasikan gambar wajah hewan ke dalam beberapa kelas. Model dilatih menggunakan teknik augmentasi data dan dijalankan pada Google Colab dengan GPU T4 untuk performa optimal. Model kemudian dikonversi ke format TFLite untuk inferensi ringan. ⚡



🗂️ Dataset

Dataset Animal Faces berisi gambar wajah hewan dari berbagai sumber seperti Flickr dan Pixabay. Dataset ini terdiri dari beberapa kelas wajah hewan (misalnya, kucing, anjing, dll.), yang disusun dalam direktori Dataset-Final/test/.

Struktur dataset:

Direktori test/ berisi subfolder untuk setiap kelas hewan.
Contoh nama file: flickr_cat_000817.jpg, pixabay_cat_001243.jpg.



📦 Persyaratan

Proyek ini menggunakan library berikut:

tensorflow
tensorflowjs
numpy
pandas
matplotlib
seaborn
scikit-learn
opencv-python
pillow
tqdm



⚙️ Cara Menjalankan

Untuk menjalankan proyek ini secara lokal atau di Colab:
1. Unduh dataset Animal Faces dan tempatkan dalam direktori Dataset-Final/.
2. Pastikan model yang telah dilatih (model_saya.h5) tersedia di direktori proyek.
3. Jalankan notebook notebook.ipynb di Google Colab (GPU direkomendasikan).
4. Ikuti langkah-langkah dalam notebook untuk memproses data, mengonversi model ke TFLite, dan melakukan inferensi.



▶️ Penggunaan

1. Unduh dataset dan model yang telah dilatih (model_saya.h5).
2. Jalankan notebook: notebook.ipynb.
3. kuti alur berikut:

Impor library dan preprocessing data.
Konversi model Keras ke format TFLite.
Lakukan inferensi pada data uji menggunakan model TFLite.

4. Hasil prediksi akan ditampilkan dalam format: Gambar: <nama_file>, Predicted class: <kelas>.



🏗️ Arsitektur Model

Model CNN dibangun menggunakan Keras dengan komponen utama:

1. Lapisan Conv2D untuk ekstraksi fitur.
2. Lapisan MaxPooling2D untuk reduksi dimensi.
3. Dropout untuk mencegah overfitting.
4. Flatten untuk meratakan output.
5. Lapisan Dense dengan aktivasi relu.
6. Output layer dengan aktivasi softmax untuk klasifikasi multikelas.

Detail teknis:

1. Ukuran input gambar: 150x150 piksel.
2. Loss function: categorical_crossentropy.
3. Optimizer: Adam.
4. Metrik evaluasi: accuracy.

Model disimpan sebagai model_saya.h5 dan dikonversi ke animal_faces_model.tflite untuk inferensi ringan.



🏋️ Pelatihan dan Evaluasi

1. Pelatihan: Model dilatih menggunakan dataset Animal Faces dengan augmentasi data (rotasi, pergeseran, zoom, dll.) untuk meningkatkan generalisasi.
2. Evaluasi: Model diuji pada direktori Dataset-Final/test/ menggunakan interpreter TFLite.
3. Hasil inferensi: Model memprediksi kelas untuk setiap gambar uji, dengan output berupa indeks kelas (misalnya, 0 untuk kucing, 1 untuk anjing, dll.).

Catatan: Detail akurasi pelatihan dan validasi tidak disertakan dalam notebook, tetapi inferensi TFLite menunjukkan performa yang konsisten.



📊 Hasil

Output Inferensi: Model TFLite berhasil memprediksi kelas untuk gambar dalam direktori uji, dengan hasil ditampilkan dalam format:

Gambar: flickr_cat_000817.jpg, Predicted class: 0
Gambar: pixabay_cat_001243.jpg, Predicted class: 0
...

Kinerja: Sebagian besar prediksi menunjukkan kelas 0, dengan beberapa prediksi kelas 1, mengindikasikan distribusi kelas yang mungkin tidak seimbang atau model yang sangat bias ke satu kelas.

Keterbatasan: Tidak ada metrik evaluasi kuantitatif (seperti akurasi atau F1-score) yang disediakan dalam notebook. Disarankan untuk menambahkan evaluasi tambahan seperti confusion matrix.



🤝 Kontribusi

Proyek ini merupakan bagian dari submission Dicoding:

Nama: Valencia Sutio
Email: mc172d5x1395@student.devacademy.id
ID Dicoding: MC172D5X1395

Kontribusi dan saran untuk perbaikan sangat dihargai! Silakan buka issue atau kirim pull request di repository ini. 🙌

