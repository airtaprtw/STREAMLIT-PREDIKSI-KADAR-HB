# Prediksi Kadar Hemoglobin - Deployment App

Repo ini adalah versi ringan khusus untuk deployment publik (Streamlit Community Cloud),
diturunkan dari repo riset utama. Tidak berisi data pasien asli maupun notebook analisis --
hanya kode aplikasi (`app/`) dan pipeline retraining (`notebooks/train.py`, `notebooks/utils.py`).

Master data dan model akan terbentuk otomatis saat pengguna mengunggah data lewat
menu "Retraining System" di aplikasi.
