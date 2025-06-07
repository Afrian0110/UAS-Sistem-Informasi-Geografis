# 🌊 Sistem Prediksi Daerah Rawan Banjir Berbasis SIG-AI

Proyek ini bertujuan untuk membangun sistem interaktif berbasis web yang mampu memprediksi daerah rawan banjir menggunakan data spasial dan historis melalui algoritma machine learning.

## 📌 Deskripsi

Sistem ini dibuat dengan memanfaatkan model **Random Forest Classifier** yang dilatih menggunakan data curah hujan, kemiringan lereng, ketinggian wilayah, dan penggunaan lahan. Data tersebut divisualisasikan dalam peta interaktif menggunakan **Folium** dan ditampilkan melalui dashboard **Streamlit**.

Dashboard ini dapat digunakan oleh instansi pemerintah, pengambil kebijakan, maupun masyarakat umum untuk:
- Melihat prediksi daerah rawan banjir.
- Melihat statistik data spasial-historis.
- Mengunggah data CSV sendiri untuk prediksi baru.

---

## 📂 Data yang Digunakan

Data dummy yang digunakan mensimulasikan kondisi geografis suatu wilayah di **Jawa Tengah**, Indonesia. Format CSV memiliki kolom berikut:

- `latitude`: Garis lintang lokasi (derajat desimal)
- `longitude`: Garis bujur lokasi (derajat desimal)
- `rainfall`: Curah hujan (mm)
- `slope`: Kemiringan lereng (°)
- `elevation`: Ketinggian dari permukaan laut (meter)
- `land_use`: Tipe penggunaan lahan (0 = Hutan, 1 = Permukiman, 2 = Lahan Terbuka)
- `flood_risk`: Label risiko banjir (1 = Rawan, 0 = Tidak Rawan)

Contoh file: [`flood_prediction_jateng.csv`](./flood_prediction_jateng.csv)

---

## 🖼️ Output

- **Peta Interaktif**: Titik-titik lokasi diberi warna merah (rawan) dan hijau (tidak rawan).
- **Statistik Data**: Rata-rata dan distribusi nilai curah hujan, lereng, dan elevasi.
- **Prediksi dari Model**: Label risiko banjir ditentukan oleh model Random Forest berdasarkan input pengguna.

---

## ▶️ Penggunaan

### 1. Jalankan aplikasi secara lokal:
```bash
streamlit run app.py

