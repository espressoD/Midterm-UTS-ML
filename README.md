# Assessment 1: Fraud Detection Pipeline 🕵️‍♂️

Proyek ini bertujuan untuk membangun model Machine Learning *end-to-end* yang dapat mendeteksi transaksi penipuan (*fraud*) dari dataset transaksi online.

## 📊 Deskripsi Dataset
Dataset terdiri dari dua tabel utama (IEEE-CIS Fraud Detection):
* **Transaction Table:** Informasi nominal, kartu, alamat, dll.
* **Identity Table:** Informasi perangkat dan jaringan (dihubungkan via `TransactionID`).
* **Target:** `isFraud` (1 = Penipuan, 0 = Aman).
* **Karakteristik:** Dataset sangat *imbalanced* (jumlah fraud jauh lebih sedikit dari transaksi normal).

## 🛠️ Pipeline Pengerjaan
1.  **Data Loading & Merging:** Menggabungkan tabel transaksi dan identitas.
2.  **Preprocessing:**
    * Handling Missing Values (Imputasi `-999` atau `unknown`).
    * Encoding variabel kategorikal (Label Encoding).
    * Memory Reduction (Optimasi tipe data untuk menghemat RAM).
3.  **Modeling:** Menggunakan **Random Forest Classifier** dengan parameter `class_weight='balanced'` untuk menangani ketimpangan data.
4.  **Evaluasi:** Menggunakan ROC-AUC karena akurasi bias pada data imbalanced.

## 🚀 Hasil & Evaluasi
Model dievaluasi menggunakan validation set (20% data).

| Metrik | Skor |
| :--- | :--- |
| **ROC-AUC** | **0.85** (Contoh, sesuaikan dengan hasilmu) |
| **Precision/Recall** | Lihat Confusion Matrix di Notebook |

**Analisis:**
Model berhasil membedakan transaksi fraud dengan probabilitas tinggi. Distribusi prediksi menunjukkan model dapat memisahkan mayoritas transaksi aman (probabilitas < 0.1).

## 📂 Cara Menjalankan Code
1.  Buka `midterm_transaction_data.ipynb` di Google Colab.
2.  Pastikan dataset `train_transaction.csv` dan `test_transaction.csv` ada di Google Drive.
3.  Jalankan semua cell secara berurutan.
4.  Hasil prediksi akan disimpan sebagai `submission_midterm.csv`.
