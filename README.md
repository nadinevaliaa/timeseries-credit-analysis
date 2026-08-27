# **Evaluasi Model Prediktif untuk Peramalan Pencairan Kredit Menggunakan Time Series**

## Deskripsi Proyek
Proyek ini membandingkan performa tiga model prediktif berbasis deret waktu, yaitu ARIMA, ETS, dan Prophet, dalam meramalkan pencairan kredit bulanan. Data yang digunakan mencakup periode Februari 2022 hingga 2031 yang mencakup informasi tanggal realisasi dan nominal terima bersih dan menunjukkan karakteristik volatil dengan adanya outlier yang signifikan.

## Pipeline Analisis
Prosedur analisis yang diterapkan dalam proyek ini meliputi:
1. Identifikasi pola musiman dan tren pada data historis nominal pencairan.
2. Verifikasi data menggunakan Augmented Dickey-Fuller (ADF) Test serta observasi plot ACF dan PACF.
3. Penanganan *outlier* melalui teknik *Moving Average Imputation* untuk menstabilkan varians data nominal.
4. Implementasi dan komparasi model ARIMA, ETS (Error, Trend, Seasonal), dan Prophet.

## Keterangan Dataset
Dataset yang digunakan dalam analisis ini memiliki struktur sebagai berikut:
- **Tanggal Realisasi:** Tanggal pelaksanaan pencairan kredit.
- **Terima Bersih (RP):** Nominal bersih yang diterima dalam satuan Rupiah.

## Hasil dan Evaluasi
Berdasarkan pengujian, model **Prophet** menghasilkan kapabilitas terbaik dalam menangkap tren non-linear dan pola musiman tahunan dibandingkan model ARIMA dan ETS. Berikut adalah ringkasan metrik evaluasi model Prophet setelah tahap imputasi:

| Metrik Evaluasi | Nilai Akurasi |
| :--- | :--- |
| Root Mean Square Error (RMSE) | 4.483.520 |
| Mean Absolute Error (MAE) | 3.274.253 |
| Mean Absolute Percentage Error (MAPE) | 85,11% |

## Dependensi & Pustaka
Proyek ini dikembangkan menggunakan bahasa pemrograman **R** dengan dependensi pustaka sebagai berikut:
- `forecast`
- `prophet`
- `tseries`
- `tidyverse`
- `ggplot2`
