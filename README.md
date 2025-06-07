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

---

## 🖥️ Tampilan Dashboard

### 📌 Tampilan Awal
Menampilkan dashboard dengan pilihan data, statistik, dan peta interaktif.

![Tampilan Awal](https://github.com/user-attachments/assets/5b64c136-783f-4706-834c-05ee92aef2f0)

---

### 🌧️ Tampilan Menampilkan Daerah Rawan dan Tidak Rawan Banjir
Model memprediksi berdasarkan data historis dan spasial, kemudian memvisualisasikan hasilnya ke dalam peta interaktif berwarna:

- 🔴 **Merah** → Daerah Rawan Banjir  
- 🟢 **Hijau** → Daerah Tidak Rawan

![Prediksi Rawan Banjir 1](https://github.com/user-attachments/assets/d12132f1-71f4-44ae-8d8f-14c3d31cf326)

![Prediksi Rawan Banjir 2](https://github.com/user-attachments/assets/5140e4de-9148-46eb-b233-46f2065b6193)

![Prediksi Rawan Banjir 3](https://github.com/user-attachments/assets/261c8e3d-d79f-4b96-b282-002d050192a3)




