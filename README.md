# Assessment 3: Customer Segmentation (Clustering) 👥

Proyek ini bertujuan untuk mengelompokkan pelanggan kartu kredit berdasarkan perilaku penggunaan mereka untuk strategi pemasaran yang lebih baik.

## 📊 Deskripsi Dataset
Dataset berisi informasi penggunaan kartu kredit pelanggan, meliputi:
* `BALANCE`: Saldo akun.
* `PURCHASES`: Total pembelian.
* `CREDIT_LIMIT`: Batas kredit.
* `PAYMENTS`: Total pembayaran yang dilakukan.
* Dan fitur perilaku lainnya.

## 🛠️ Pipeline Clustering
1.  **Data Cleaning:** Mengisi missing values pada `MINIMUM_PAYMENTS` dan `CREDIT_LIMIT`.
2.  **Preprocessing:** Standarisasi data (`StandardScaler`) agar fitur dengan nilai besar tidak mendominasi.
3.  **Dimensionality Reduction:** Menggunakan **PCA** untuk visualisasi 2D.
4.  **Modeling Comparison:** Membandingkan K-Means, Hierarchical Clustering, dan DBSCAN.

## 🔍 Evaluasi & Pemilihan Model
Perbandingan dilakukan menggunakan **Silhouette Score**:

| Model | Silhouette Score | Keterangan |
| :--- | :--- | :--- |
| **DBSCAN** | 0.4643 | Skor tertinggi, namun **GAGAL** karena hanya mendeteksi 1 cluster besar (noise). Tidak *actionable*. |
| Hierarchical | 0.1547 | Skor terendah. |
| **K-Means (K=4)** | **0.1976** | **DIPILIH**. Skor moderat namun memberikan segmentasi bisnis yang paling jelas. |

## 💡 Interpretasi Cluster (Profil Pelanggan)
Berdasarkan model K-Means (K=4), ditemukan 4 tipe pelanggan:
1.  **Cluster 0 (Active Users):** Penggunaan wajar, saldo terkontrol.
2.  **Cluster 1 (The Whales/VIP):** Pembelian sangat tinggi (>7000), limit kredit besar.
3.  **Cluster 2 (Credit Hungry):** Saldo hutang sangat tinggi, pembelian rendah. Berisiko.
4.  **Cluster 3 (Low Spenders):** Jarang menggunakan kartu, limit kecil.

## 📂 Visualisasi
Notebook menyertakan visualisasi PCA Scatter Plot dan Elbow Method untuk penentuan K optimal.
