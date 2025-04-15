# 📊 Prediksi dan Segmentasi Penjualan Produk Minuman dengan Machine Learning

Proyek ini bertujuan untuk membantu perusahaan minuman dalam memahami tren penjualan melalui analisis data historis dan penerapan algoritma Machine Learning. Proyek ini mencakup proses **clustering**, **klasifikasi**, serta evaluasi performa model dalam memprediksi kelompok pasar dan performa penjualan.

---

## 📌 Deskripsi Proyek

Perusahaan memiliki data penjualan dalam jumlah besar dengan banyak atribut seperti harga produk, kuantitas, diskon, wilayah, dan waktu pemesanan. Tantangannya adalah:

- Sulitnya mengolah data dalam jumlah besar
- Tidak adanya label yang jelas mengenai performa penjualan
- Perlunya prediksi performa penjualan untuk efisiensi produksi dan strategi pemasaran

Melalui Machine Learning, proyek ini mencoba **mengelompokkan data penjualan** menggunakan **K-Means Clustering**, kemudian memanfaatkan hasil tersebut untuk **melatih model klasifikasi** menggunakan **K-Nearest Neighbors (KNN)** dan **Naive Bayes**, sehingga dapat **memprediksi performa penjualan (tinggi/rendah)** secara otomatis.

---

## ⚙️ Instalasi & Dependensi

1. **Clone repositori ini:**

```bash
git clone https://github.com/yourusername/sales-segmentation-ml.git
cd sales-segmentation-ml
## ⚙️ Instalasi & Dependensi
```

2. **Aktifkan virtual environment:**

```bash
python -m venv venv
source venv/bin/activate  # atau venv\\Scripts\\activate di Windows
```

3. **Aktifkan virtual environment:**

```bash
pip install -r requirements.txt
```

---

## 🔁 Alur Proyek

Berikut adalah flow utama dari proyek:
- Import & Load Data
Data penjualan dimuat dari file CSV.
- Eksplorasi Data
  - Visualisasi distribusi dan korelasi antar fitur
  - Cek nilai outlier dan missing values
- Pra-Pemrosesan
  - One-Hot Encoding pada fitur kategorikal
  - Normalisasi fitur numerik
  - Menambahkan fitur baru seperti Revenue_per_Unit
  - Reduksi dimensi dengan PCA
  - Sampling data jika terlalu besar
- Clustering (K-Means)
  - Menentukan jumlah cluster optimal
  - Menyimpan label cluster ke dalam dataset sebagai target awal
- Data Splitting
Dataset dibagi menjadi 80% training dan 20% testing untuk klasifikasi.
- Klasifikasi
  - Melatih model KNN dan Naive Bayes
  - Evaluasi dengan akurasi, F1-score, precision, recall, dan confusion matrix
- Tuning Hyperparameter
  - Gunakan RandomizedSearchCV untuk mencari parameter optimal pada KNN
  - Ulangi proses evaluasi untuk model yang sudah dituning
- Analisis & Interpretasi
  - Bandingkan performa model sebelum dan sesudah tuning
  - Interpretasi karakteristik cluster
  - Rekomendasi strategi bisnis berdasarkan segmentasi
  
---
