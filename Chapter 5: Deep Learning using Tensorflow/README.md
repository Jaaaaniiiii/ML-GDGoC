# 🧠 Deep Learning using TensorFlow  

Selamat datang di repositori **Deep Learning using TensorFlow**! 🚀  
Repositori ini berisi materi lengkap mengenai **Deep Learning**, termasuk konsep dasar, arsitektur neural network, pemrosesan gambar, dan **implementasi menggunakan TensorFlow & Keras**.  

📌 **Disusun oleh:**  
**Muhammad Karov Ardava Barus** - Machine Learning Mentor @GDGoC Tel-U  
📍 **On Campus - Telkom University Bandung**  

---

## 📌 Topics Covered  
### **1️⃣ Core Concepts**  
✅ Apa itu **Deep Learning**?  
✅ Arsitektur **Neural Network** 🧠  
✅ **TensorFlow & Keras** sebagai framework utama  
✅ Tantangan dalam **Deep Learning**  

### **2️⃣ Computer Vision**  
✅ Definisi & konsep dasar **Computer Vision**  
✅ **Image Processing** (Image Resizing, Grayscale, Normalization, Data Augmentation)  
✅ **Image Classification** dengan CNN & Vision Transformers  

### **3️⃣ Hands-on Implementation**  
✅ **Model Training** dengan TensorFlow & Keras  
✅ **Implementasi CNN (Convolutional Neural Network)**  
✅ **Eksperimen dengan Vision Transformers**  

---

# 🧑‍💻 1️⃣ Core Concepts

## 🔍 **Apa itu Deep Learning?**  
**Deep Learning** adalah bagian dari **Machine Learning** yang menggunakan **Neural Networks** dengan banyak layer (**deep neural networks**) untuk belajar dari data dalam jumlah besar.  

📌 **Perbedaan utama dibanding Machine Learning:**  
| **Machine Learning** | **Deep Learning** |
|----------------------|------------------|
| Bergantung pada fitur buatan (**feature engineering**) | Mampu mengekstrak fitur secara otomatis |
| Model lebih sederhana (**linear regression, decision trees**) | Model lebih kompleks (**CNN, RNN, Transformers**) |
| Cocok untuk dataset kecil-menengah | Cocok untuk dataset besar dengan jutaan sampel |

📌 **Kenapa Deep Learning berkembang pesat sekarang?**  
✅ **Big Data** → Data yang sangat besar & kompleks 📊  
✅ **Hardware Canggih** → GPU & TPU untuk komputasi lebih cepat ⚡  
✅ **Framework yang powerful** → TensorFlow, PyTorch, Keras 🔥  

---

# 🔢 2️⃣ Neural Networks

## 🎯 **Bagaimana Neural Network bekerja?**  
Neural Network terinspirasi dari cara kerja **otak manusia** 🧠.  
🔹 **Neuron (Node)** → Menerima input, melakukan operasi matematika, lalu mengirim output.  
🔹 **Layer** → Kombinasi neuron dalam **input layer, hidden layer, dan output layer**.  
🔹 **Bobot (Weights)** → Menentukan seberapa besar pengaruh setiap input dalam model.  

📌 **Struktur Neural Network:**  
```yaml
Input → Hidden Layers (Activation Function) → Output
```

📌 **Contoh penggunaan dalam kehidupan nyata:**  
✅ **Spam Detection** 📩 → Menganalisis email apakah spam atau tidak.  
✅ **Speech Recognition** 🎙️ → Mengubah suara menjadi teks.  
✅ **Autonomous Vehicles** 🚗 → Mobil self-driving yang memahami lingkungan sekitar.  

---

# ⚙️ 3️⃣ TensorFlow & Keras

## 🔹 **TensorFlow: Framework Deep Learning**  
TensorFlow adalah library open-source dari Google yang digunakan untuk membangun model Machine Learning & Deep Learning.  

✅ **Optimasi untuk CPU, GPU, dan TPU**  
✅ **Mendukung model skala besar**  
✅ **Digunakan di Google, Airbnb, Twitter, dan banyak perusahaan besar**  

📌 **Instalasi TensorFlow:**  
```bash
pip install tensorflow
```

---

## 🔹 **Keras: API Deep Learning High-Level**  
Keras adalah **high-level API** dari TensorFlow yang membuat proses **membangun Neural Network lebih mudah** dan lebih intuitif.  

📌 **Contoh implementasi Neural Network dengan Keras:**  
```python
import tensorflow as tf
from tensorflow import keras
from tensorflow.keras import layers

# Membuat model Neural Network sederhana
model = keras.Sequential([
    layers.Dense(64, activation='relu'),
    layers.Dense(32, activation='relu'),
    layers.Dense(1, activation='sigmoid')  # Output untuk binary classification
])

# Compile model
model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])

# Menampilkan struktur model
model.summary()
```

---

# 🖼️ 4️⃣ Computer Vision

## 🔍 **Apa itu Computer Vision?**  
Computer Vision adalah cabang **AI** yang memungkinkan komputer memahami & mengolah gambar serta video 📸🎥.  
✅ **Face Recognition** (Contoh: Face ID di iPhone)  
✅ **Autonomous Vehicles** 🚗 (Deteksi rambu lalu lintas)  
✅ **Medical Imaging** 🏥 (Mendeteksi penyakit dari hasil scan medis)  

---

## 🖼️ **Image Processing**
📌 **Preprocessing yang biasa dilakukan sebelum training model Computer Vision:**  
- **Resizing** → Mengubah ukuran gambar untuk menyamakan dimensi input.  
- **Grayscale Conversion** → Mengubah gambar berwarna menjadi hitam-putih.  
- **Normalization** → Menyesuaikan skala nilai pixel agar model lebih stabil.  
- **Data Augmentation** → Memperbanyak dataset dengan rotasi, flipping, zooming.  

📌 **Contoh implementasi Image Processing dengan TensorFlow:**  
```python
import tensorflow as tf
from tensorflow.keras.preprocessing.image import ImageDataGenerator

# Data Augmentation
datagen = ImageDataGenerator(
    rotation_range=20,
    width_shift_range=0.2,
    height_shift_range=0.2,
    horizontal_flip=True
)
```

---

# 📸 5️⃣ Image Classification

📌 **Jenis-jenis model Image Classification:**  
✅ **CNN (Convolutional Neural Networks)** → Model klasik untuk analisis gambar.  
✅ **Vision Transformers (ViT)** → Model terbaru berbasis arsitektur Transformer.  

📌 **Implementasi CNN menggunakan TensorFlow & Keras:**  
```python
model = keras.Sequential([
    layers.Conv2D(32, (3,3), activation='relu', input_shape=(128, 128, 3)),
    layers.MaxPooling2D(2,2),
    layers.Conv2D(64, (3,3), activation='relu'),
    layers.MaxPooling2D(2,2),
    layers.Flatten(),
    layers.Dense(128, activation='relu'),
    layers.Dense(10, activation='softmax')  # Output untuk klasifikasi multi-kelas
])

model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['accuracy'])
model.summary()
```

---

# 🏆 6️⃣ Hands-on Practice  

🔥 **Coba sendiri dengan dataset ini!**  
📥 **[Dataset: COVID-19 Image Classification](http://ristek.link/covid19-img-data)**  
📌 **Kompetisi Kaggle:**  
🔗 **[GDGoC Tel-U ML Competition](http://ristek.link/GDGoC_Tel-U_MLCompetition_2)**  

✅ **Challenge:**  
1️⃣ Latih model CNN untuk **image classification**.  
2️⃣ Optimalkan arsitektur menggunakan **Hyperparameter Tuning**.  
3️⃣ Submit hasil prediksi ke **Kaggle Competition** & bandingkan skor dengan peserta lain! 🎯  

---

# 📞 Let's Connect!  

📩 **Punya pertanyaan? Hubungi aku di:**  
🌎 **LinkedIn:** [Ardava Barus](http://www.linkedin.com/in/ardava-barus)  
📸 **Instagram:** [@rdavaa_](https://www.instagram.com/rdavaa_/)  

💡 **"Train your models, transform your data, and make AI-powered solutions!"** 🚀✨  
```

README ini **super detail, informatif, dan engaging** untuk repositori **Deep Learning using TensorFlow** di GitHub kamu! 🚀🔥
