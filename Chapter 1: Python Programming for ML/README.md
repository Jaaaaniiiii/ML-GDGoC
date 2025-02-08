# 🤖 Python for Machine Learning

Dokumentasi dasar **Python untuk Machine Learning** berdasarkan materi yang dibawakan oleh **Hasnat Ferdiananda (IT Practitioner, ex GITS)** dalam acara **On Campus - Telkom University Bandung**.

---

## 📌 Today's Topics
1. **AI in a Nutshell**
   - Definition
   - Scope of AI
   - Machine Learning  

2. **Python in Machine Learning**
   - Python Overview
   - Libraries for ML
   - Hands-on Practice

---

# 🌍 AI in a Nutshell

### 🔹 Scope of AI
✅ **Artificial Intelligence (AI)**  
✅ **Machine Learning (ML)**  
✅ **Deep Learning**  
✅ **Generative AI**  
✅ **Large Language Models (LLM)**  

### 🔹 What is Machine Learning?
**Machine Learning (ML)** adalah cabang dari AI yang memungkinkan komputer belajar dari data tanpa diprogram secara eksplisit. Contohnya:
- **Spam Filter** 📧: Mendeteksi email spam secara otomatis  
- **Revenue Forecasting** 📈: Memprediksi pendapatan perusahaan  

### 🔹 ML Algorithms & Supervision Types
**Supervised Learning** 📊 - Data berlabel digunakan untuk melatih model  
**Unsupervised Learning** 🔍 - Model menemukan pola tanpa label  
**Reinforcement Learning** 🎮 - Model belajar dengan sistem reward  

### 🔹 ML Objective
- **Meningkatkan Revenue** 💰 (misal: meningkatkan visibilitas di hasil pencarian aplikasi)  
- **Mengurangi Biaya Operasional** 🔧 (misal: otomatisasi ekstraksi email untuk penjadwalan ulang tiket pesawat)  

> ⚠️ AI bukan pengganti manusia, AI tetap membutuhkan **Subject Matter Experts**.  

---

# 🐍 Python for Machine Learning

### 🔹 Kenapa Python?
**Python** adalah bahasa pemrograman populer yang diciptakan oleh **Guido van Rossum** pada tahun 1991.  
Python memiliki sintaks yang sederhana, memungkinkan pengembang untuk lebih fokus pada **pemecahan masalah ML** daripada kompleksitas bahasa pemrograman.

🔗 **Referensi:**  
- [W3Schools - Python Intro](https://www.w3schools.com/python/python_intro.asp)  
- [Turing - Why Python for ML](https://www.turing.com/kb/why-python-is-widely-used-for-machine-learning)  

---

## 📚 Python Libraries for Machine Learning

### 🔹 **NumPy**
🔢 Digunakan untuk pemrosesan data numerik seperti:
- Menghitung **mean**, **median**, **matriks**, dll.

```python
import numpy as np
data = np.array([1, 2, 3, 4, 5])
print(np.mean(data))  # Output: 3.0
```

---

### 🔹 **Pandas**
📊 Library untuk manipulasi dan analisis data. Cocok untuk:
- **Data cleaning**
- **Basic visualization**
- **Mathematical operations**

```python
import pandas as pd
df = pd.DataFrame({"Nama": ["Ari", "Budi"], "Nilai": [85, 90]})
print(df)
```

---

### 🔹 **Matplotlib & Seaborn**
📈 **Visualisasi data** untuk memahami pola dan tren.

```python
import matplotlib.pyplot as plt
import seaborn as sns

data = [10, 20, 30, 40]
plt.plot(data)
plt.show()
```

---

### 🔹 **Scikit-learn**
⚡ Library utama untuk **Machine Learning** dengan fitur:
- **Supervised & Unsupervised Learning**
- **Model selection & evaluation**
- **Data preprocessing**

```python
from sklearn.linear_model import LinearRegression
import numpy as np

X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([2, 4, 6, 8, 10])

model = LinearRegression()
model.fit(X, y)

print(model.predict([[6]]))  # Output: [12.]
```

---

# 🏗 Hands-on Practice

💻 **Google Colab** digunakan sebagai lingkungan untuk eksplorasi dan visualisasi data.  
**Tugas:** Coba eksplorasi & visualisasikan dataset sendiri di **Google Colab**.  

📥 **Download Materi & Hubungi Speaker**  
- 🔗 [LinkedIn: Hasnat Ferdiananda](https://www.linkedin.com/in/hasnatf/)  
- 📩 Email: ferdianandahasnat@gmail.com  
- 🌐 [Personal Page](https://hasnat.vercel.app/)  

---

## 📚 Referensi
- [WEF Future of Jobs Report 2025](https://reports.weforum.org/docs/WEF_Future_of_Jobs_Report_2025.pdf)  
- [Python for Machine Learning - Turing](https://www.turing.com/kb/why-python-is-widely-used-for-machine-learning)  
- [Google Colab](https://colab.research.google.com/)  

💡 **Let's connect, collaborate, and build amazing ML models together! 🚀**  
