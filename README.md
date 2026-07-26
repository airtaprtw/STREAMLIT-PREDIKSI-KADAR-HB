# Sistem Prediksi Kadar Hemoglobin Pasien Hemodialisis

> **Instrumen Early Warning Berbasis Machine Learning dan Streamlit Dashboard**  
> Repositori ini berisi kode sumber (*source code*), *automated pipeline preprocessing*, pemodelan *machine learning*, serta *dashboard* interaktif untuk memprediksi kadar Hemoglobin (Hb) pasien hemodialisis satu bulan ke depan.

---

## Ringkasan Penelitian & Sistem

Penurunan kadar hemoglobin merupakan masalah umum pada pasien *End-Stage Renal Disease* (ESRD) yang menjalani terapi hemodialisis. Sistem ini dibangun untuk memberikan dukungan keputusan klinis bagi tenaga kesehatan melalui:
1. **Prediksi Kadar Hb:** Memprediksi nilai Hb bulan berikutnya menggunakan algoritma **LightGBM** (mencapai *MAE* 0.657 g/dL, *RMSE* 0.832 g/dL, dan $R^2$ 0.434).
2. **Explainable AI (XAI):** Transparansi keputusan model berbasis **SHAP (SHapley Additive exPlanations)** dan *Permutation Feature Importance* untuk memahami kontribusi fitur medis pasien (seperti `hb_lag`, `MCV`, dan `epo_resist`).
3. **Automated Retraining System:** Fitur pembaruan model secara otomatis saat ada data baru tanpa menimpa (*overwrite*) model lama (*model versioning*).

---

## Arsitektur & Teknologi (*Tech Stack*)

* **Bahasa Pemrograman:** Python 3.10+
* **Framework Web:** Streamlit
* **Machine Learning:** LightGBM, Scikit-Learn
* **Interpretabilitas Model:** SHAP
* **Pengolahan & Visualisasi Data:** Pandas, NumPy, Plotly, Seaborn, Matplotlib
* **Format Model & Persistence:** Joblib, JSON

---

## 📂 Struktur Repositori

```text
.
├── app/                        
│   └── main.py                 # Berkas utama aplikasi Streamlit
├── data/                       
│   ├── processed/              
│   └── raw/                    
├── models/                     # Penyimpanan versi model (.pkl) & riwayat retraining
│   ├── active_model.txt        
│   ├── lgbm_best_model.pkl     
│   ├── lgbm_model_*.pkl        
│   └── model_history.json      
├── notebooks/                  
│   ├── 01_EDA.ipynb            
│   ├── 02_GridSearchModelling.ipynb # Eksperimen pemodelan GridSearch
│   ├── 02_Optuna.ipynb         # Tuning hiperparameter Optuna
│   ├── train.py                
│   └── utils.py                # Automated pipeline preprocessing & helper functions
├── .gitignore                  
└── requirements.txt            


## 🌐 Tautan Akses

*  **Aplikasi Web Live:** [app-prediksi-kadar-hb.streamlit.app](https://app-prediksi-kadar-hb.streamlit.app)
*  **Dokumentasi Kode:** [GitHub Repository](https://github.com/airtaprtw/STREAMLIT-PREDIKSI-KADAR-HB)

---

## ✉️ Kontak & Pengembang

*  **Pengembang:** Airta Pertiwi
*  **Program Studi:** Teknik Informatika (S1)
*  **Universitas:** Universitas Lampung
*  **LinkedIn:** [Airta Pertiwi](https://www.linkedin.com/in/airtaprtw)
.
