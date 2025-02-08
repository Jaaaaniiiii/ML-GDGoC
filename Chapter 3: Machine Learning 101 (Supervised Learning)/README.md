# 🎯 Supervised Learning

Dokumentasi ini membahas konsep **Supervised Learning** dalam **Machine Learning**, mencakup **Regression**, **Classification**, dan **Evaluation Metrics**.  
Materi ini disampaikan dalam acara **On Campus - Telkom University Bandung** oleh **Hasnat Ferdiananda (IT Practitioner, ex GITS).**  

---

## 📌 Today's Topics
### 🔹 **Supervised Learning**
✅ **Overview & Machine Learning Process**  
✅ **Regression**  
✅ **Classification**  

### 🔹 **Evaluation Metrics**
✅ **Overview**  
✅ **Regression Metrics**  
✅ **Classification Metrics**  

---

# 🤖 1. Supervised Learning Overview

### 🔍 **Apa itu Supervised Learning?**
**Supervised Learning** adalah metode **Machine Learning** di mana model dilatih menggunakan dataset yang memiliki **label** atau **target yang diketahui**.  
Model mempelajari hubungan antara fitur (X) dan target (Y), lalu digunakan untuk **memprediksi output dari data baru**.  

📌 **Contoh Aplikasi:**  
- **Spam Detection** 📧 → Mendeteksi apakah email adalah spam atau bukan.  
- **Face Recognition** 📷 → Mendeteksi wajah dalam gambar.  
- **Predictive Maintenance** 🏭 → Memprediksi kapan mesin akan mengalami kerusakan.  

📌 **Supervised Learning dibagi menjadi 2 jenis utama:**  
1. **Regression** → Memprediksi nilai **kontinu** (misal: harga rumah, suhu udara).  
2. **Classification** → Memprediksi kategori **diskrit** (misal: email spam/tidak spam).  

---

# 📊 2. Regression

🔹 **Apa itu Regression?**  
Regression adalah teknik **Supervised Learning** yang digunakan untuk memprediksi **nilai numerik kontinu**.  

📌 **Contoh Aplikasi Regression:**  
✅ **Prediksi Harga Rumah** 🏠 → Berdasarkan luas rumah, lokasi, dan jumlah kamar.  
✅ **Prediksi Penjualan Produk** 🛒 → Berdasarkan tren penjualan sebelumnya.  
✅ **Analisis Risiko Kredit** 💳 → Menentukan kemungkinan seseorang gagal bayar.  

---

## 📈 2.1 Simple Linear Regression

🔹 **Definisi:**  
Linear Regression adalah model yang mencari hubungan **linear** antara satu variabel independen **(X)** dan variabel dependen **(Y)**.  
Persamaan regresinya adalah:  

\[
Y = mX + b
\]

📌 **Langkah-langkah:**
1. **Menentukan fitur dan target**  
2. **Melatih model dengan dataset**  
3. **Membuat prediksi untuk data baru**  
4. **Mengukur error dengan **Mean Squared Error (MSE)**  

📌 **Contoh Implementasi di Python:**
```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Dataset
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([2, 4, 6, 8, 10])

# Membuat model Linear Regression
model = LinearRegression()
model.fit(X, y)

# Prediksi nilai baru
predicted = model.predict([[6]])
print(f"Prediksi untuk X=6: {predicted[0]}")  # Output: 12.0

# Visualisasi
plt.scatter(X, y, color="blue")
plt.plot(X, model.predict(X), color="red")
plt.show()
```

---

# 🏷️ 3. Classification

🔹 **Apa itu Classification?**  
Classification adalah teknik **Supervised Learning** untuk mengelompokkan data ke dalam **kategori diskrit**.  

📌 **Contoh Aplikasi Classification:**  
✅ **Spam Detection** 📩 → Apakah email adalah spam atau bukan?  
✅ **Fraud Detection** 💳 → Apakah transaksi ini penipuan atau tidak?  
✅ **Sentiment Analysis** 💬 → Apakah review produk positif atau negatif?  

---

## 🏆 3.1 Perbandingan Algoritma Classification

📌 **Jenis-Jenis Algoritma Classification:**
| **Algoritma**            | **Kelebihan**                                      | **Kekurangan**                               |
|--------------------------|--------------------------------------------------|---------------------------------------------|
| **Logistic Regression**  | Sederhana & cepat 🚀 | Tidak cocok untuk dataset non-linear ❌ |
| **K-Nearest Neighbors**  | Mudah dipahami 🧑‍🏫 | Lambat untuk dataset besar 🐢 |
| **Random Forest**        | Akurat & tahan outlier 🎯 | Model besar & lambat ❌ |
| **Gradient Boosting**    | Performa tinggi 💡 | Rentan overfitting 📉 |

📌 **Visualisasi Decision Boundary:**
```python
from sklearn.datasets import make_classification
import matplotlib.pyplot as plt
from sklearn.svm import SVC

# Membuat dataset dummy
X, y = make_classification(n_samples=100, n_features=2, n_classes=2, random_state=42)

# Membuat model SVM
model = SVC(kernel='linear')
model.fit(X, y)

# Visualisasi
plt.scatter(X[:, 0], X[:, 1], c=y, cmap='coolwarm')
plt.title("Decision Boundary Example")
plt.show()
```

---

# 📏 4. Evaluation Metrics

🔹 **Kenapa Evaluation Metrics penting?**  
Saat membangun model **Supervised Learning**, kita perlu mengukur performanya untuk memastikan hasilnya **akurat** dan **reliable**.  

📌 **Tipe Evaluation Metrics berdasarkan jenis model:**  
✅ **Regression Metrics** → Mengukur seberapa jauh prediksi dari nilai sebenarnya.  
✅ **Classification Metrics** → Mengukur seberapa baik model mengklasifikasikan data.  

---

## 📉 4.1 Regression Metrics

📌 **Metode Evaluasi Regression:**
1. **Mean Squared Error (MSE)** → Rata-rata kuadrat error.  
2. **Root Mean Squared Error (RMSE)** → Akar kuadrat dari MSE.  
3. **Mean Absolute Error (MAE)** → Rata-rata nilai absolut error.  

📌 **Contoh Implementasi:**
```python
from sklearn.metrics import mean_squared_error

y_true = [3, -0.5, 2, 7]
y_pred = [2.5, 0.0, 2, 8]

mse = mean_squared_error(y_true, y_pred)
print(f"MSE: {mse}")
```

---

## 🏷️ 4.2 Classification Metrics

📌 **Metode Evaluasi Classification:**
1. **Accuracy** → Persentase prediksi yang benar.  
2. **Precision** → Ketepatan model dalam memprediksi kelas positif.  
3. **Recall** → Kemampuan model menangkap kelas positif.  
4. **F1-Score** → Kombinasi antara Precision dan Recall.  

📌 **Confusion Matrix:**
```python
from sklearn.metrics import confusion_matrix

y_true = [0, 1, 1, 0, 1, 0]
y_pred = [0, 1, 0, 0, 1, 1]

cm = confusion_matrix(y_true, y_pred)
print(cm)
```

---

# 🎯 Hands-on Practice

🔥 **Coba sendiri!**  
- 📥 **[Dataset: Telco Customer Churn](https://www.kaggle.com/datasets/yeanzc/telco-customer-churn-ibm-dataset/data)**  
- 🛠 **[Google Colab Notebook](https://www.kaggle.com/t/eae59a87b88945f1a17384afd23e1eac)**  

📌 **Tugas:**  
Bangun model **Supervised Learning** untuk memprediksi **customer churn**! 🚀  

---

# 📞 Let's Connect!

📩 **Ingin berdiskusi lebih lanjut? Hubungi aku di:**  
- 🌎 **LinkedIn:** [Hasnat Ferdiananda](https://www.linkedin.com/in/hasnatf/)  
- 📸 **Instagram:** [@hasnat5_](https://www.instagram.com/hasnat5_/)  

---

💡 **"The best models are built on quality data & great evaluation!"** 🚀✨
