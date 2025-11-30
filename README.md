# Midterm Exam (UTS) - Machine Learning

Repository ini berisi penyelesaian tugas **Midterm (UTS) Machine Learning**. Proyek ini mencakup tiga domain utama pembelajaran mesin: Klasifikasi (Fraud Detection), Regresi (Prediksi Tahun Lagu), dan Clustering (Segmentasi Pelanggan).

## 📂 Struktur Proyek & Navigasi
Tugas ini dibagi menjadi 3 asesmen yang dikerjakan dalam branch/folder terpisah. Berikut ringkasannya:

| Assessment | Topik | Jenis Masalah | Branch/Link |
| :--- | :--- | :--- | :--- |
| **Assessment 1** | **Fraud Detection** | Classification | [Lihat Detail di Branch Assesment1](https://github.com/espressoD/Midterm-UTS-ML/tree/Assesment1) |
| **Assessment 2** | **Song Year Prediction** | Regression | [Lihat Detail di Branch Assesment2](https://github.com/espressoD/Midterm-UTS-ML/tree/Assesment2) |
| **Assessment 3** | **Customer Segmentation** | Clustering | [Lihat Detail di Branch Assesment3](https://github.com/espressoD/Midterm-UTS-ML/tree/Assesment3) |

## 📝 Ringkasan Pengerjaan

### 1. Fraud Detection (Klasifikasi)
Bertujuan untuk memprediksi transaksi penipuan. Tantangan utama adalah *imbalanced data*. Solusi menggunakan model *tree-based* dengan penanganan *class weight*.
* **Model Terbaik:** Random Forest / LightGBM.
* **Metrik Utama:** ROC-AUC.

### 2. Song Year Prediction (Regresi)
Bertujuan memprediksi tahun rilis lagu berdasarkan fitur audio (timbre).
* **Model Terbaik:** LightGBM (Gradient Boosting) mengungguli Linear Regression.
* **Metrik Utama:** RMSE & R² Score.

### 3. Customer Segmentation (Clustering)
Bertujuan mengelompokkan pengguna kartu kredit berdasarkan perilaku belanja.
* **Model Terpilih:** K-Means (K=4).
* **Metrik Validasi:** Silhouette Score & Interpretasi Bisnis.

---
*Dibuat untuk memenuhi tugas UTS Machine Learning 2025.*
