
# 📚 Dokumentasi Fitur dalam Pembelajaran Mesin

## 📑 Daftar Isi
- [📚 Dokumentasi Fitur dalam Pembelajaran Mesin](#-dokumentasi-fitur-dalam-pembelajaran-mesin)
  - [📑 Daftar Isi](#-daftar-isi)
  - [📌 Pengenalan Fitur](#-pengenalan-fitur)
  - [🔢 Jenis-Jenis Fitur](#-jenis-jenis-fitur)
    - [Numerik](#numerik)
    - [Kategorikal](#kategorikal)
    - [Fitur Turunan](#fitur-turunan)
  - [🛠️ Rekayasa Fitur](#️-rekayasa-fitur)
    - [Teknik Umum:](#teknik-umum)
  - [🎨 Fitur dalam Data Tidak Terstruktur](#-fitur-dalam-data-tidak-terstruktur)
    - [Contoh:](#contoh)
  - [📊 Cakupan Fitur](#-cakupan-fitur)
    - [Masalah Umum:](#masalah-umum)
  - [💡 Contoh Praktis](#-contoh-praktis)
  - [📖 Referensi \& Sumber Tambahan](#-referensi--sumber-tambahan)
  - [🔗 Tautan Cepat](#-tautan-cepat)

---

## 📌 Pengenalan Fitur
**Fitur** (atau *feature variables*) adalah elemen data yang digunakan untuk memprediksi target dalam model pembelajaran mesin. Misalnya, dalam prediksi penyakit jantung, fitur bisa berupa berat badan, jenis kelamin, atau detak jantung istirahat. Fitur ini menjadi dasar bagi algoritma untuk mempelajari pola dan membuat prediksi.  

🔍 **Mengapa Fitur Penting?**  
- Fitur menentukan kualitas prediksi model.  
- Pemilihan fitur yang relevan dapat meningkatkan akurasi.  
- Fitur yang tidak relevan atau redundan dapat memperlambat pelatihan model.  

Contoh lain: Dalam prediksi harga rumah, fitur mungkin mencakup luas bangunan, jumlah kamar, atau lokasi.  

[⬆ Kembali ke Daftar Isi](#-daftar-isi)

---

## 🔢 Jenis-Jenis Fitur

### Numerik
Fitur numerik berupa angka yang dapat diukur atau dihitung.  
- **Contoh**:  
  - Berat badan (kg).  
  - Detak jantung (bpm).  
  - Harga rumah (dalam juta rupiah).  

📈 **Karakteristik**:  
- Dapat dioperasikan secara matematis (rata-rata, standar deviasi).  
- Sering dinormalisasi untuk menghindari bias skala.  

### Kategorikal
Fitur kategorikal mewakili kelompok atau kelas tertentu.  
- **Contoh**:  
  - Jenis kelamin (Laki-laki/Perempuan).  
  - Status merokok (Ya/Tidak).  
  - Jenis properti (Rumah/Apartemen).  

📉 **Karakteristik**:  
- Diubah menjadi angka (misal: *one-hot encoding*) sebelum diproses.  
- Tidak memiliki urutan intrinsik (kecuali *ordinal*).  

### Fitur Turunan
Fitur turunan (*derived features*) dibuat dari fitur yang sudah ada.  
- **Contoh**:  
  - **BMI** (Berat Badan / Tinggi Badan²).  
  - **Usia Bangunan** (Tahun Sekarang - Tahun Dibangun).  

⚙️ **Proses Pembuatan**:  
- Menggabungkan, memotong, atau mengubah data mentah.  
- Memerlukan kreativitas dan pemahaman domain.  

[⬆ Kembali ke Daftar Isi](#-daftar-isi)

---

## 🛠️ Rekayasa Fitur
Rekayasa fitur (*feature engineering*) adalah proses mengoptimalkan fitur untuk meningkatkan performa model.  

### Teknik Umum:
1. **Normalisasi**:  
   ```python
   from sklearn.preprocessing import MinMaxScaler
   scaler = MinMaxScaler()
   data_normalized = scaler.fit_transform(data)
   ```
2. **Pengkodean Kategorikal**:  
   - *One-Hot Encoding* untuk fitur tanpa urutan.  
   - *Label Encoding* untuk fitur ordinal.  

3. **Pembuatan Fitur Interaksi**:  
   - Contoh: `Luas Tanah × Harga per Meter²`.  

🎯 **Tujuan**:  
- Mengurangi dimensi data.  
- Menyoroti pola yang tersembunyi.  

[⬆ Kembali ke Daftar Isi](#-daftar-isi)

---

## 🎨 Fitur dalam Data Tidak Terstruktur
Data tidak terstruktur (seperti gambar, teks, atau audio) juga memiliki fitur, meski lebih abstrak.  

### Contoh:
- **Gambar**:  
  - Bentuk tepi (*edges*), tekstur, atau warna.  
  - Fitur diekstraksi menggunakan CNN (*Convolutional Neural Network*).  

- **Teks**:  
  - Frekuensi kata (*TF-IDF*), vektor kata (*Word2Vec*).  

- **Audio**:  
  - Frekuensi suara (*MFCC*), amplitudo.  

🤖 **Peran Algoritma**:  
Algoritma pembelajaran mendalam (*deep learning*) secara otomatis mengekstraksi fitur dari data mentah.  

[⬆ Kembali ke Daftar Isi](#-daftar-isi)

---

## 📊 Cakupan Fitur
Cakupan fitur (*feature coverage*) mengacu pada seberapa lengkap nilai fitur tersedia dalam dataset.  

### Masalah Umum:
- **Data Hilang**: Hanya 10% sampel yang memiliki nilai untuk fitur tertentu.  
- **Solusi**:  
  - Hapus fitur dengan cakupan rendah.  
  - Isi nilai yang hilang (*imputation*) dengan rata-rata atau modus.  

📉 **Dampak Cakupan Rendah**:  
- Model kesulitan mempelajari pola.  
- Akurasi prediksi menurun.  

[⬆ Kembali ke Daftar Isi](#-daftar-isi)

---

## 💡 Contoh Praktis
**Studi Kasus: Prediksi Harga Rumah**  
- **Fitur Numerik**: Luas bangunan, jumlah kamar.  
- **Fitur Kategorikal**: Lokasi (Jakarta Selatan, Bandung).  
- **Fitur Turunan**: Harga per meter² (Harga Total / Luas Tanah).  

🔧 **Rekayasa Fitur**:  
- Normalisasi fitur numerik.  
- *One-hot encoding* untuk lokasi.  

📈 **Hasil**: Model dapat memprediksi harga dengan akurasi 95%.  

[⬆ Kembali ke Daftar Isi](#-daftar-isi)

---

## 📖 Referensi & Sumber Tambahan
1. [📘 Panduan Feature Engineering - Towards Data Science](https://towardsdatascience.com/feature-engineering-for-machine-learning-3a5e293a5114)  
2. [🔍 Kaggle: Contoh Dataset dengan Fitur Beragam](https://www.kaggle.com/datasets)  
3. [🎥 Video Tutorial: Feature Engineering dengan Python](https://youtube.com/feature-engineering-python)  

---

## 🔗 Tautan Cepat
- [📌 Pengenalan Fitur](#-pengenalan-fitur)  
- [🔢 Jenis-Jenis Fitur](#-jenis-jenis-fitur)  
- [🛠️ Rekayasa Fitur](#️-rekayasa-fitur) 