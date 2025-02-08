# 🚀 Git 101 & GitHub 101

Dokumentasi dasar **Git** dan **GitHub** untuk mempermudah pengelolaan proyek dan kolaborasi tim.
**[Link Recording](https://drive.google.com/file/d/1oM-VMhJxRYTo5TliU0bfBgcANwZ-MlXZ/view?usp=sharing)**

---

## 📝 GIT 101: Pengenalan Dasar Git

### 🔹 Apa itu Git?
**Git** adalah sistem kontrol versi terdistribusi (**DVCS**) yang digunakan untuk melacak perubahan dalam kode atau file, memungkinkan kolaborasi antar pengembang, dan mengelola proyek secara efisien.

### 🔹 Kenapa Git Penting?
✅ Mempermudah kolaborasi dalam tim  
✅ Menyimpan riwayat perubahan kode  
✅ Menghindari konflik saat bekerja pada file yang sama  
✅ Mendukung pengembangan paralel (**branching**)  

---

### 🔹 Istilah Penting dalam Git
- **Repository (Repo)**: Tempat penyimpanan proyek dan riwayat perubahan  
- **Commit**: Menyimpan snapshot perubahan ke dalam repository  
- **Branch**: Cabang independen untuk mengerjakan fitur baru  
- **Merge**: Menggabungkan perubahan dari branch lain  
- **Pull & Push**: Mengambil dan mengunggah perubahan ke repository remote  

---

## ⚙️ Instalasi Git

### 🔹 Windows
Unduh Git dari [git-scm.com](https://git-scm.com) dan ikuti proses instalasi.

### 🔹 MacOS/Linux
Gunakan package manager:

```sh
# MacOS
brew install git

# Ubuntu/Debian
sudo apt-get install git
```

### 🔹 Konfigurasi Git
Setelah instalasi, atur nama pengguna dan email:

```sh
git config --global user.name "Nama Kamu"
git config --global user.email "email@example.com"
```

---

## 📌 Workflow Dasar Git

### 🔹 Membuat Repository Baru

**Local Repository**
```sh
git init
```

**Clone Repository dari GitHub**
```sh
git clone <url-repository>
```

### 🔹 Menambahkan File ke Staging Area
```sh
git add <nama-file>
```

### 🔹 Commit Perubahan
```sh
git commit -m "Pesan perubahan"
```

### 🔹 Push ke Remote Repository
```sh
git push origin <nama-branch>
```

---

## 🏗 Hands-On Practice: Membuat Repository Sederhana

1️⃣ Buat folder baru:  
```sh
mkdir belajar-git
cd belajar-git
git init
```

2️⃣ Tambahkan file baru, lalu commit:  
```sh
echo "Halo Git!" > README.md
git add README.md
git commit -m "Menambahkan file README.md"
```

---

# 🌍 GitHub 101: Pengenalan Dasar GitHub

## 🔹 Apa itu GitHub?
**GitHub** adalah platform berbasis cloud untuk mengelola repository Git. GitHub mempermudah pengelolaan proyek, kolaborasi tim, dan berbagi kode secara publik atau privat.

### 🔹 Keunggulan GitHub
✅ Hosting repository Git di cloud  
✅ Fitur kolaborasi seperti **Pull Requests**, **Issues**, dan **Discussions**  
✅ Integrasi dengan layanan lain seperti CI/CD dan monitoring  
✅ Mendukung open-source community  

---

## 🔹 Terminologi Penting di GitHub
- **Repository**: Tempat menyimpan proyek dan riwayat perubahan  
- **Fork**: Menyalin repository untuk dikembangkan sendiri  
- **Pull Request (PR)**: Permintaan untuk menggabungkan perubahan ke repository utama  

---

## ⚙️ Persiapan Awal GitHub

### 🔹 Membuat Akun GitHub
1. Daftar di [github.com](https://github.com)  
2. Pilih username yang mencerminkan identitasmu sebagai developer  
3. Verifikasi email untuk mengaktifkan akun  

### 🔹 Instalasi GitHub CLI (Opsional)
GitHub CLI mempermudah interaksi dengan GitHub melalui terminal:

```sh
# MacOS
brew install gh

# Ubuntu/Debian
sudo apt install gh

# Login ke GitHub CLI
gh auth login
```

---

## 📌 Workflow Dasar GitHub

### 🔹 Membuat Repository Baru
1. Buka [GitHub](https://github.com)  
2. Klik **New Repository**  
3. Isi nama repository, deskripsi, dan pilih public atau private  
4. Klik **Create Repository**  

**Clone repository ke lokal**
```sh
git clone <url-repository>
cd <nama-repository>
```

### 🔹 Push Perubahan ke GitHub
Setelah menambahkan file dan commit di lokal:
```sh
git push origin main
```

---

## 🤝 Kolaborasi dengan Pull Request

1️⃣ Buat branch baru untuk fitur atau perbaikan:
```sh
git checkout -b fitur-baru
```

2️⃣ Push branch ke GitHub dan buat PR:
```sh
git push origin fitur-baru
```

3️⃣ Di GitHub, klik **Pull Request** untuk meminta review.

---

## 🏗 Hands-On Practice: Membuat Repository dan Push File ke GitHub

1️⃣ Buat repository baru di GitHub dengan nama `latihan-github`.  
2️⃣ Clone repository ke lokal:
```sh
git clone <url-repository>
cd latihan-github
```
3️⃣ Tambahkan file baru, commit, dan push:
```sh
echo "Halo GitHub!" > README.md
git add README.md
git commit -m "Menambahkan file README.md"
git push origin main
```

---

## 📚 Referensi
- [Git Documentation](https://git-scm.com/doc)  
- [GitHub Documentation](https://docs.github.com/)  

💡 **Happy Coding! 🚀**
