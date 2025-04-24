# intel_Classification

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun model klasifikasi gambar Pemandangan Alam di seluruh dunia. menggunakan Convolutional Neural Network (CNN) yang dibuat dengan TensorFlow dan Keras.

Model dilatih pada dataset Data ini berisi sekitar 25ribu gambar dengan ukuran 150x150 yang terbagi dalam 6 kategori.
{'buildings' -> 0,
'forest' -> 1,
'glacier' -> 2,
'mountain' -> 3,
'sea' -> 4,
'street' -> 5 }
Data Latih, Uji dan Prediksi dipisahkan dalam setiap file zip. Ada sekitar 14 ribu gambar di Latih, 3 ribu di Uji dan 7 ribu di Prediksi.
Data ini awalnya dipublikasikan di https://datahack.analyticsvidhya.com oleh Intel untuk menjadi tuan rumah Tantangan klasifikasi gambar.Translated with DeepL.com (free version) dengan augmentasi data dan menggunakan callback `EarlyStopping` serta penyesuaian `class_weight` untuk mengatasi ketidakseimbangan data. Model kemudian dikonversi ke dalam tiga format:
- SavedModel (untuk TensorFlow Serving)
- TFLite (untuk aplikasi mobile atau embedded)
- TensorFlow.js (untuk aplikasi berbasis web)

## Cara Menjalankan
1. **Notebook** (`notebook.ipynb`) digunakan untuk training dan konversi model.
2. **Model SavedModel** bisa digunakan untuk inference menggunakan `keras.layers.TFSMLayer`.
3. **Model TFLite** dapat digunakan dalam aplikasi Android atau embedded system.
4. **Model TensorFlow.js** dapat digunakan pada aplikasi web.

### Contoh Inference di Notebook dapat dilihat pada file "Intel_Inference.ipynb".
