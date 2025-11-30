# Assessment 2: Song Year Prediction 🎵

Proyek ini bertujuan untuk memprediksi tahun rilis sebuah lagu berdasarkan fitur audio (timbre) menggunakan algoritma Regresi.

## 📊 Deskripsi Dataset
* **Sumber:** YearPredictionMSD (Million Song Dataset).
* **Fitur:** 90 atribut audio (TimbreAverage dan TimbreCovariance).
* **Target:** Tahun rilis lagu (Continuous).

## 🛠️ Metodologi & Model
Kami membandingkan dua pendekatan model:

1.  **Linear Regression (Baseline):**
    * Model sederhana untuk melihat hubungan linear.
    * Memerlukan standarisasi data (`StandardScaler`).
2.  **LightGBM (Gradient Boosting):**
    * Model *state-of-the-art* untuk data tabular.
    * Konfigurasi: `num_boost_round=3000`, `learning_rate=0.05`.

## 📈 Perbandingan Hasil
Berikut adalah perbandingan performa pada data test:

| Model | MAE (Mean Absolute Error) | RMSE | R² Score |
| :--- | :--- | :--- | :--- |
| Linear Regression | 6.78 Tahun | 9.52 | 0.2360 |
| **LightGBM (Best)** | **6.05 Tahun** | **8.68** | **0.3658** |

**Kesimpulan:**
LightGBM dipilih sebagai model terbaik. Peningkatan iterasi ke 3000 terbukti signifikan menurukan error. Meskipun R² ~0.36 terlihat rendah, ini adalah skor yang kompetitif untuk dataset audio yang memiliki *noise* tinggi ini.

## 📂 File dalam Repository
* `midterm_regresi.ipynb`: Notebook utama berisi seluruh pipeline dari load data hingga visualisasi.
