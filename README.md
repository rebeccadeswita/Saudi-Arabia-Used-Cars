# Saudi-Arabia-Used-Cars
# Capstone Project 3: Prediksi Harga Mobil Bekas di Arab Saudi (Syarah.com)

**Author**: Rebecca Deswita  
**Cohort**: JCDSOL_018_1_ONLINE  
**Period**: May 2025  

## Deskripsi Proyek

Proyek ini bertujuan membangun model prediktif menggunakan algoritma machine learning untuk memperkirakan harga wajar mobil bekas yang dijual melalui platform digital otomotif terbesar di Arab Saudi, yaitu [Syarah.com](https://syarah.com/). Model ini diharapkan dapat membantu menciptakan sistem penilaian harga yang lebih adil dan transparan bagi pembeli maupun penjual.

## Latar Belakang Bisnis

Pasar mobil bekas Arab Saudi mengalami tantangan utama berupa ketidakkonsistenan harga antar penjual, rendahnya transparansi kondisi kendaraan, serta kurangnya sistem penilaian harga otomatis. Syarah sebagai marketplace digital memiliki peluang besar untuk mengatasi tantangan ini melalui teknologi prediktif berbasis data.

## Tujuan

Mengembangkan model machine learning yang dapat memperkirakan harga mobil bekas secara akurat berdasarkan karakteristik kendaraan yang tersedia.

## Pendekatan Analitis

- **Data Preparation**: Pembersihan data, deteksi dan penghapusan outlier harga ekstrem, encoding fitur kategorikal.
- **Exploratory Data Analysis (EDA)**: Analisis korelasi dan distribusi fitur seperti `Year`, `Engine Size`, `Mileage`, `Gear Type`, `Region`, dll.
- **Modeling**: 
  - Algoritma yang digunakan: Linear Regression, Lasso, Ridge, KNN, Decision Tree, Random Forest, XGBoost, CatBoost, AdaBoost, Elastic Net, Gradient Boosting.
  - Model terbaik: **CatBoost** dengan performa:
    - RMSE: 33.106
    - MAE: 14.069
    - MAPE: 18.39%
- **Hyperparameter Tuning** dilakukan menggunakan `RandomizedSearchCV`.

## Evaluasi Model

Model dievaluasi menggunakan tiga metrik utama:
- **RMSE (Root Mean Squared Error)**: Menghukum kesalahan besar, cocok untuk mengukur deviasi harga absolut.
- **MAE (Mean Absolute Error)**: Lebih stabil terhadap outlier.
- **MAPE (Mean Absolute Percentage Error)**: Mengukur kesalahan relatif dalam bentuk persentase, mudah dipahami oleh tim bisnis.

## Kesimpulan & Rekomendasi

- Fitur paling penting dalam prediksi harga adalah: Tahun kendaraan (`Year`) dan ukuran mesin (`Engine_Size`).
- Model lebih akurat untuk mobil keluaran tahun terbaru dan rentang harga menengah ke atas.
- Perlu perhatian terhadap outlier mileage dan harga ekstrem agar tidak menurunkan akurasi model.

## Struktur File

- `Capstone Project_Module3_Machine Learning_Rebecca Deswita.ipynb`: Notebook utama yang berisi semua tahapan analisis.
- `catboost.pkl`: File model pickle
- `README.md`: Dokumentasi proyek (file ini).

## Tools & Library

- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-Learn
- CatBoost, XGBoost
- Jupyter Notebook

## Potensi Pengembangan Lanjutan

- Integrasi API untuk deployment model prediksi secara real-time
- Tambahan fitur eksternal seperti skor inspeksi kendaraan atau estimasi kondisi pasar
- Visualisasi interaktif di dashboard Tableau atau Streamlit

---

> **Catatan:** Proyek ini dikembangkan untuk keperluan Capstone Modul 3 dalam program Data Science Bootcamp.

