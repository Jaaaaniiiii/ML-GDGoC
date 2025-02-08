# 🚀 Feature Engineering & Data Preprocessing

Dokumentasi ini berisi materi lengkap tentang **Feature Engineering & Data Preprocessing** yang dibawakan dalam acara **On Campus - Telkom University Bandung**.  
Proses ini sangat penting dalam **Machine Learning**, karena kualitas data yang buruk akan berdampak langsung pada hasil prediksi yang dihasilkan oleh model! 📊

---

## 📌 Today's Topics
### 🔹 **Data Preprocessing**
✅ **Definisi Data Preprocessing**  
✅ **Handling Missing & Duplicated Data**  
✅ **Outliers Engineering**  
✅ **Feature Scaling**  

### 🔹 **Feature Engineering**
✅ **Definisi Feature Engineering**  
✅ **Categorical Encoding**  
✅ **Rare Label Handling**  
✅ **Variable Transformation**  
✅ **Date Time Feature Engineering**  

---

# 📊 1. Data Preprocessing

### 🔍 **Apa itu Data Preprocessing?**
**Data Preprocessing** adalah proses membersihkan dan menyiapkan data agar dapat digunakan secara efektif dalam model **Machine Learning**.  
Tahapan ini **krusial**, karena model tidak akan bekerja optimal jika data mentah memiliki noise, missing values, atau outliers yang belum ditangani.  

> **"Garbage in, garbage out"** – Data berkualitas buruk akan menghasilkan model yang buruk! ❌

---

## 🛠 1.1 Handling Missing & Duplicated Data

🔹 **Missing Data** adalah kondisi ketika suatu nilai dalam dataset tidak tersedia atau hilang. Ini bisa terjadi karena kesalahan input data, keterbatasan sensor, atau faktor lain.  

📌 **Metode menangani Missing Data:**
- **Imputasi Mean, Median, Mode**  
  - Untuk data numerik, gunakan nilai **mean (rata-rata)** atau **median (nilai tengah)**.
  - Untuk data kategorikal, gunakan **mode (nilai yang paling sering muncul)**.  

- **Imputasi dengan Arbitrary Value**  
  - Gantilah nilai kosong dengan angka spesifik seperti **0, -999, atau 999**.  

- **Menghapus Baris dengan Missing Values**  
  - Jika jumlah data yang hilang cukup banyak, lebih baik menghapus baris tersebut agar tidak mengganggu analisis.  

🔹 **Duplicated Data**  
Data yang sama muncul lebih dari satu kali dapat menyebabkan **analisis yang tidak akurat**.  

📌 **Solusi:**  
- Menggunakan fungsi `drop_duplicates()` pada **Pandas** untuk menghapus data yang duplikat.  

```python
import pandas as pd

# Contoh dataset dengan duplikasi
data = {'Nama': ['Ari', 'Budi', 'Ari', 'Dewi'],
        'Nilai': [85, 90, 85, 75]}

df = pd.DataFrame(data)
df = df.drop_duplicates()  # Menghapus duplikasi
print(df)
```

---

## 🚀 1.2 Outliers Engineering

🔹 **Apa itu Outlier?**  
Outlier adalah **nilai yang sangat berbeda** dari data lain dalam dataset. Ini bisa terjadi karena kesalahan input data, atau memang ada variasi alami dalam data.  

📌 **Cara mengidentifikasi Outlier:**  
- **Boxplot** 📦  
- **Scatter Plot** 📊  
- **Histogram** 📈  

📌 **Metode menangani Outlier:**  
✅ **Remove (hapus)** jika jelas merupakan kesalahan input data.  
✅ **Transform** menggunakan **log transformation, winsorization, atau z-score normalization**.  
✅ **Keep** jika data tersebut memang valid dan penting dalam analisis.  

```python
import numpy as np
import matplotlib.pyplot as plt

data = [10, 12, 15, 14, 100]  # Outlier pada nilai 100
plt.boxplot(data)
plt.show()
```

---

## 📏 1.3 Feature Scaling

🔹 **Kenapa Feature Scaling penting?**  
Beberapa algoritma **Machine Learning** seperti **K-NN, SVM, dan Gradient Descent** sangat sensitif terhadap skala data.  

📌 **Metode Feature Scaling:**  
- **Standardization (Z-score scaling)**: Mean = 0, Standard Deviation = 1.  
- **Normalization (Min-Max Scaling)**: Skala data antara **0 dan 1**.  
- **Robust Scaling**: Menggunakan median dan **IQR** untuk menangani outlier.  

```python
from sklearn.preprocessing import StandardScaler

data = [[50], [20], [100], [5]]
scaler = StandardScaler()
scaled_data = scaler.fit_transform(data)
print(scaled_data)
```

---

# 🛠 2. Feature Engineering

### 🔍 **Apa itu Feature Engineering?**
Feature Engineering adalah proses menciptakan atau mengubah fitur dalam dataset agar lebih sesuai dengan model **Machine Learning**.  

---

## 🔢 2.1 Categorical Encoding

🔹 **Kenapa perlu encoding?**  
Model Machine Learning tidak bisa memahami data dalam bentuk **teks** atau **kategori**, sehingga harus dikonversi ke bentuk numerik.  

📌 **Metode Categorical Encoding:**  
✅ **One-Hot Encoding** → Untuk kategori yang jumlahnya kecil.  
✅ **Label Encoding** → Untuk kategori yang memiliki urutan/hierarki.  
✅ **Frequency Encoding** → Menggunakan jumlah kemunculan kategori.  

```python
import pandas as pd
from sklearn.preprocessing import OneHotEncoder

df = pd.DataFrame({'Warna': ['Merah', 'Biru', 'Hijau', 'Merah']})
encoder = OneHotEncoder(sparse=False)
encoded = encoder.fit_transform(df[['Warna']])
print(encoded)
```

---

## ⚠️ 2.2 Rare Label Handling

🔹 **Apa itu Rare Label?**  
Kategori yang muncul **sangat sedikit** dalam dataset dapat menyebabkan **high cardinality**, yang menghambat performa model.  

📌 **Solusi:**  
Gabungkan semua kategori yang memiliki frekuensi rendah menjadi satu **label umum**, misalnya **"Other"**.  

```python
df['Kategori'] = df['Kategori'].apply(lambda x: x if x in common_labels else "Other")
```

---

## 📉 2.3 Variable Transformation

🔹 **Metode Transformasi:**  
✅ **Log Transformation** → Mengurangi skewness dalam distribusi data.  
✅ **Square-root Transformation** → Mengatasi variabel dengan distribusi Poisson.  

```python
import numpy as np

data = np.array([1, 2, 3, 4, 100])
transformed = np.log(data)
print(transformed)
```

---

## 📅 2.4 Date Time Feature Engineering

🔹 **Ekstraksi Fitur dari Data Waktu**  
- **Day, Month, Year**  
- **Day of the week**  
- **Elapsed time since event**  

```python
df['Tanggal'] = pd.to_datetime(df['Tanggal'])
df['Bulan'] = df['Tanggal'].dt.month
df['Hari'] = df['Tanggal'].dt.day
```

---

# 💻 Hands-on Practice

🔥 **Coba sendiri!**  
- 📥 **[Demo Dataset](http://ristek.link/demo-datasetGDG)**  
- 🔗 **[Source Code](http://ristek.link/demo-src-ML-FEDP)**  

📌 **Tugas:**  
Lakukan **Feature Engineering & Data Preprocessing** pada minimal **5 dataset** dengan teknik yang sudah dibahas! 🚀  
➡ **[Download Dataset](http://ristek.link/dataset-penugasan-gdgoc)**  

---

# 📞 Let's Connect!

📩 **Tertarik berdiskusi lebih lanjut? Hubungi aku di:**  
- 🌎 **LinkedIn:** [Ardava Barus](http://www.linkedin.com/in/ardava-barus)  
- 📸 **Instagram:** [@rdavaa_](https://www.instagram.com/rdavaa_/)  

---

💡 **"Great models start with great data!"** ✨
