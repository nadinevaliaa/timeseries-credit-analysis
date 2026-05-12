# **Analisis Komparatif Model Deret Waktu untuk Peramalan Pencairan Kredit**

Repositori ini menyajikan penelitian mengenai evaluasi performa model prediktif dalam meramalkan angka pencairan kredit bulanan. Studi ini membandingkan pendekatan statistik klasik dengan model berbasis struktur aditif untuk menangani data keuangan yang memiliki tingkat volatilitas tinggi.

## Deskripsi Proyek
Tujuan utama dari proyek ini adalah menentukan model terbaik dalam memprediksi pencairan kredit dengan mempertimbangkan gangguan data berupa *outlier* yang signifikan. Penelitian ini mencakup seluruh siklus pemrosesan data, mulai dari pengujian statistik formal hingga evaluasi metrik akurasi pasca-pembersihan data.

## Metodologi Penelitian
Prosedur analisis yang diterapkan dalam proyek ini meliputi:
1. **Analisis Eksploratif:** Identifikasi pola musiman dan tren pada data historis.
2. **Uji Stasioneritas:** Verifikasi data menggunakan Augmented Dickey-Fuller (ADF) Test serta observasi plot ACF dan PACF.
3. **Pra-pemrosesan Data:** Penanganan *outlier* melalui teknik *Moving Average Imputation* untuk menstabilkan varians.
4. **Pemodelan:** Implementasi dan komparasi model ARIMA, ETS (Error, Trend, Seasonal), dan Prophet.

## Hasil dan Evaluasi
Berdasarkan pengujian, model **Prophet** menghasilkan kapabilitas terbaik dalam menangkap tren non-linear dan pola musiman tahunan dibandingkan model ARIMA dan ETS. Berikut adalah ringkasan metrik evaluasi model Prophet setelah tahap imputasi:

| Metrik Evaluasi                       | Nilai Akurasi |
| Root Mean Square Error (RMSE)         | 4.483.520     |
| Mean Absolute Error (MAE)             | 3.274.253     |
| Mean Absolute Percentage Error (MAPE) | 85,11%        |

## Persyaratan Sistem
Proyek ini dikembangkan menggunakan bahasa pemrograman **R** dengan dependensi pustaka sebagai berikut:
- `forecast`
- `prophet`
- `tseries`
- `tidyverse`
- `ggplot2`

## Struktur Repositori
- `Kode/`: Dokumentasi kode sumber analisis dalam format R (.R atau .Rmd).
- `Data/`: Dataset yang digunakan dalam penelitian.
- `Paper/`: Paper penelitian lengkap dalam format PDF.
