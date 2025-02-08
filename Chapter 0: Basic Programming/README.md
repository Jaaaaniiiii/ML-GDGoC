# Basic Programming - Study Group #1

Dokumentasi materi **Basic Programming** dari **Google Developer Groups on Campus**.

## 📌 Agenda
1. Tipe Data & Variabel
2. Operasi Aritmatika & Logika
3. Struktur Kontrol: Percabangan & Perulangan
4. Sub-Program: Function
5. Array
6. Algoritma - Studi Kasus

---

## 📝 Materi
### 🔹 Variabel & Tipe Data
Variabel adalah tempat untuk menyimpan data. Beberapa tipe data umum:
- **Integer**: Bilangan bulat (contoh: `1`, `42`)
- **Float**: Bilangan desimal (contoh: `3.14`, `0.99`)
- **String**: Teks (contoh: `"Halo Dunia"`, `"100"`)
- **Boolean**: Nilai kebenaran (`True` atau `False`)

---

### 🔹 Operasi Aritmatika
Operasi dasar yang sering digunakan:
- **Penjumlahan**: `1 + 4`
- **Pengurangan**: `4 - 2`
- **Perkalian**: `30 * 2`
- **Pembagian**: `30 / 2`
- **Modulus** (sisa bagi): `8 % 3`

---

### 🔹 Operasi Logika
Digunakan untuk menentukan nilai kebenaran (`True` atau `False`):
- **AND (`&&`)**: Semua nilai harus `True` agar hasilnya `True`
- **OR (`||`)**: Minimal ada satu nilai `True` agar hasilnya `True`
- **NOT (`!`)**: Mengubah `True` ke `False` dan sebaliknya

---

### 🔹 Percabangan (Conditional Statement)
Digunakan untuk menentukan alur program berdasarkan kondisi tertentu:

```python
nilai = 85
if nilai >= 80:
    print("Nilai Baik!")
elif nilai >= 60:
    print("Lulus")
else:
    print("Tidak Lulus")
```

---

### 🔹 Perulangan (Looping)
Digunakan untuk mengulang eksekusi kode secara otomatis:

```python
for i in range(1, 101):
    print(i)  # Mencetak angka 1 sampai 100
```

---

### 🔹 Function (Sub-Program)
Membantu mengorganisir kode agar lebih modular:

```python
def sapa(nama):
    print(f"Halo, {nama}!")

sapa("Emir")
```

---

### 🔹 Array (List)
Struktur data yang dapat menyimpan banyak nilai:

```python
nilai_uas = [75, 80, 60, 90, 55]

# a) Banyak yang lulus (min: 60)
lulus = len([n for n in nilai_uas if n >= 60])

# b) Banyak nilai baik (min: 80)
nilai_baik = len([n for n in nilai_uas if n >= 80])

# c) Rata-rata nilai
rata_rata = sum(nilai_uas) / len(nilai_uas)

print(f"Lulus: {lulus}, Nilai Baik: {nilai_baik}, Rata-rata: {rata_rata}")
```

---

## 🚀 Reminder
⚠️ Materi padat, jangan lupa belajar mandiri!  
💡 Jangan ragu bertanya jika bingung!  
🎯 Enjoy dan coba langsung coding-nya!  
