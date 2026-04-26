# UTS Machine Learning: Klasifikasi Buah Oranges vs Grapefruit

Repository ini berisi implementasi model Machine Learning untuk mengklasifikasikan jenis buah (Jeruk atau Anggur) berdasarkan karakteristik fisik menggunakan tiga algoritma berbeda.

## 📝 Deskripsi Masalah
Tujuan dari proyek ini adalah membangun model klasifikasi yang dapat membedakan antara buah **Orange** dan **Grapefruit** menggunakan dataset yang mencakup fitur diameter, berat, dan intensitas warna (RGB).

## 📊 Dataset
Dataset yang digunakan adalah [Oranges vs. Grapefruit](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit) dari Kaggle.
- **Fitur**: Diameter, Weight, Red, Green, Blue.
- **Target**: Name (Orange atau Grapefruit).

## 🛠️ Tahapan Pengerjaan (Metodologi)

Langkah-langkah yang dilakukan dalam pembuatan model ini adalah sebagai berikut:

### 1. Data Preparation & Loading
Mengimpor library yang dibutuhkan seperti `pandas`, `numpy`, dan `scikit-learn`, kemudian memuat dataset `citrus.csv`.

### 2. Preprocessing Data
* **Label Encoding**: Mengubah kolom target 'name' dari bentuk teks menjadi numerik (misal: 0 untuk Orange, 1 untuk Grapefruit).
* **Feature Selection**: Memisahkan fitur independen (X) dan label dependen (y).
* **Data Splitting**: Membagi dataset menjadi **80% Training Set** untuk melatih model dan **20% Test Set** untuk mengevaluasi performa model.
* **Feature Scaling**: Menggunakan `StandardScaler` untuk menyamakan skala fitur agar model seperti SVM dapat bekerja dengan optimal.

### 3. Modeling
Melakukan pelatihan menggunakan tiga algoritma perbandingan:
1.  **Decision Tree**: Membangun model berdasarkan aturan keputusan logis.
2.  **Naive Bayes**: Menggunakan pendekatan probabilitas sederhana berbasis teorema Bayes.
3.  **Support Vector Machine (SVM)**: Mencari *hyperplane* optimal untuk memisahkan kedua kelas data.

### 4. Evaluasi
Setiap model dievaluasi menggunakan metrik:
* **Accuracy Score**: Persentase prediksi yang benar secara keseluruhan.
* **Classification Report**: Detail mengenai Precision, Recall, dan F1-Score untuk masing-masing kelas.

## 🚀 Cara Menjalankan
1. Clone repository ini.
2. Pastikan file `citrus.csv` berada di direktori yang sama.
3. Jalankan file python atau notebook:
   ```bash
   python UTS_ML.py
