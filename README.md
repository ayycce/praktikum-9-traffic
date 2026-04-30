# 🚦 Praktikum 9: Smart City AI Traffic
> Rancang Bangun Sistem Monitoring dan Prediksi Kepadatan Kendaraan Berbasis Big Data Framework

---

## 📌 Identitas Praktikan
- **Nama:** Aisyah Safitri  
- **NIM:** 230104040117  
- **Program Studi:** Teknologi Informasi  
- **Universitas:** UIN Antasari Banjarmasin  
- **Mata Kuliah:** Big Data Technology  

---

## 📖 Deskripsi Proyek

Repositori ini berisi implementasi **Praktikum 9**, yaitu pembangunan pipeline Big Data secara *end-to-end* untuk mensimulasikan sistem **Adaptive Traffic Control System (ATCS)** dalam konteks *Smart City*.

Proyek ini mengintegrasikan:
- Pemrosesan data skala besar menggunakan **Apache Spark**
- Penyimpanan efisien menggunakan **Parquet**
- Prediksi kepadatan kendaraan menggunakan **Machine Learning**
- Visualisasi real-time melalui **dashboard interaktif**

---

## 🏗️ Arsitektur Pipeline

```
Data Generation 
   ➡️ Spark Transformation 
   ➡️ Parquet Columnar Storage 
   ➡️ Machine Learning Modeling 
   ➡️ Serving (Streamlit Dashboard)
```

Pipeline ini dirancang modular agar mudah dikembangkan menjadi sistem produksi.

---

## 🛠️ Technology Stack

- **PySpark**  
  Distributed Data Processing Engine untuk pemrosesan data dalam skala besar (*micro-batch processing*)

- **Python (Scikit-Learn)**  
  Implementasi algoritma *Linear Regression* untuk prediksi kepadatan kendaraan

- **Streamlit**  
  Framework untuk membangun dashboard interaktif secara real-time

- **Plotly**  
  Library visualisasi untuk grafik time-series yang dinamis

- **Parquet Format**  
  Format penyimpanan berbasis kolom yang efisien dan cepat untuk analisis data

---

## ⚙️ Cara Menjalankan (How to Run)

Pastikan Anda menggunakan lingkungan Linux (WSL) dan Python 3 sudah terinstal.

### 1. Persiapan Environment

```bash
python3 -m venv venv
source venv/bin/activate
pip install pyspark streamlit plotly scikit-learn pandas setuptools
```

---

### 2. Menjalankan Engine Data (PySpark)

Script ini akan:
- Menghasilkan data sensor simulasi
- Melakukan transformasi data menggunakan Spark
- Menyimpan hasil dalam format Parquet ke folder `output/`

```bash
python main_uts_230104040117.py
```

---

### 3. Menjalankan Dashboard Interaktif (Streamlit)

Dashboard akan menampilkan:
- Visualisasi kepadatan kendaraan
- Grafik time-series
- Hasil prediksi AI

```bash
streamlit run dashboard_230104040117.py
```

---

## 🧠 Insight Utama Praktikum

### 📦 Parquet Storage
Format Parquet menyimpan data secara kolumnar dengan kompresi (misalnya Snappy), sehingga:
- Lebih hemat storage
- Lebih cepat dibaca dibanding CSV
- Sangat optimal untuk query analitik

---

### 📁 Absolute Path Management
Penggunaan path absolut memastikan:
- Script tetap stabil saat dipindahkan
- Tidak bergantung pada working directory
- Cocok untuk deployment di server Linux

---

### 🤖 Integrasi Machine Learning
Pemisahan antara:
- **Engine (Spark)**
- **Serving Layer (Streamlit)**

Memberikan keuntungan:
- Penggunaan memori lebih efisien
- Pipeline lebih modular
- Mudah integrasi model prediksi (Linear Regression)

---

## 🎯 Kesimpulan

Praktikum ini menunjukkan bagaimana membangun sistem Big Data sederhana namun mendekati implementasi nyata dalam Smart City, dengan kombinasi:

- Data Engineering (Spark)
- Data Storage Optimization (Parquet)
- Machine Learning (Prediction)
- Data Visualization (Dashboard)

---

## 👩‍💻 Author

Aisyah Safitri  
Teknologi Informasi  
UIN Antasari Banjarmasin