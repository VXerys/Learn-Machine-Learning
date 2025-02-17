
# 📚 Dokumentasi Pembelajaran Mesin: Memahami Pembagian Data Training, Validasi, dan Testing

## 📑 Daftar Isi
- [📚 Dokumentasi Pembelajaran Mesin: Memahami Pembagian Data Training, Validasi, dan Testing](#-dokumentasi-pembelajaran-mesin-memahami-pembagian-data-training-validasi-dan-testing)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🚀 Pengantar](#-pengantar)
  - [📊 Konsep Tiga Set Data](#-konsep-tiga-set-data)
    - [🎯 Training Set](#-training-set)
    - [🔍 Validation Set](#-validation-set)
    - [📝 Test Set](#-test-set)
  - [⚙️ Proses Pembagian Data](#️-proses-pembagian-data)
    - [Algoritma Pembagian](#algoritma-pembagian)
    - [Rasio yang Direkomendasikan](#rasio-yang-direkomendasikan)
  - [💡 Contoh Praktis: Prediksi Penyakit Jantung](#-contoh-praktis-prediksi-penyakit-jantung)
    - [Langkah 1: Pembagian Data](#langkah-1-pembagian-data)
    - [Langkah 2: Pelatihan Model](#langkah-2-pelatihan-model)
    - [Langkah 3: Evaluasi di Validation Set](#langkah-3-evaluasi-di-validation-set)
    - [Langkah 4: Uji di Test Set](#langkah-4-uji-di-test-set)
    - [Hasil:](#hasil)
  - [⚠️ Tips dan Praktik Terbaik](#️-tips-dan-praktik-terbaik)
  - [🔗 Referensi](#-referensi)
  - [❓ FAQ](#-faq)

---

## 🚀 Pengantar
Pembagian data menjadi **training**, **validation**, dan **test set** adalah fondasi kritis dalam membangun model _machine learning_ yang andal. Konsep ini memastikan model tidak hanya menghafal data (_overfitting_), tetapi juga mampu beradaptasi dengan data baru. Bayangkan ini seperti persiapan ujian:  
- **Materi kuliah** (training set) untuk memahami konsep.  
- **Ujian latihan** (validation set) untuk mengevaluasi pemahaman.  
- **Ujian akhir** (test set) untuk menguji kemampuan sebenarnya.  

📌 **Mengapa ini penting?**  
Model yang diuji hanya pada data latihan ibarat siswa yang menghafal jawaban tanpa memahami konsep. Hasilnya mungkin bagus di data latihan, tetapi gagal di dunia nyata.

[🔙 Kembali ke Daftar Isi](#daftar-isi)

---

## 📊 Konsep Tiga Set Data
### 🎯 Training Set
- **Fungsi**: Melatih model untuk mengenali pola.  
- **Contoh**: 70% data pasien penyakit jantung digunakan untuk melatih model.  
- **Detail**: Selama pelatihan, model menyesuaikan parameter (e.g., bobot dalam jaringan saraf) berdasarkan kesalahan prediksi.  

### 🔍 Validation Set
- **Fungsi**: Menyempurnakan model (e.g., memilih hyperparameter seperti _learning rate_).  
- **Contoh**: 15% data digunakan untuk menguji berbagai konfigurasi model.  
- **Peringatan**: Jangan gunakan validation set berkali-kali, karena dapat menyebabkan _overfitting_ tidak langsung.  

### 📝 Test Set
- **Fungsi**: Evaluasi akhir performa model sebelum deploy.  
- **Contoh**: 15% data yang **tidak pernah** dilihat selama pelatihan atau tuning.  
- **Analog**: Ujian akhir yang soalnya benar-benar baru.  

[🔙 Kembali ke Daftar Isi](#daftar-isi)

---

## ⚙️ Proses Pembagian Data
### Algoritma Pembagian
1. **Random Shuffle**: Acak data sebelum dibagi (untuk data independen waktu).  
   ```python
   from sklearn.model_selection import train_test_split
   X_train, X_temp, y_train, y_temp = train_test_split(X, y, test_size=0.3, random_state=42)
   X_val, X_test, y_val, y_test = train_test_split(X_temp, y_temp, test_size=0.5)
   ```
2. **Stratified Sampling**: Mempertahankan distribusi kelas (penting untuk data tidak seimbang).  
3. **Time-Based Split**: Untuk data time series (e.g., data 2020-2022 untuk training, 2023 untuk testing).  

### Rasio yang Direkomendasikan
| Tipe Data          | Training | Validation | Testing |  
|---------------------|----------|------------|---------|  
| Data Kecil (<10k)   | 70%      | 15%        | 15%     |  
| Data Besar          | 80-90%   | 5-10%      | 5-10%   |  

[🔙 Kembali ke Daftar Isi](#daftar-isi)

---

## 💡 Contoh Praktis: Prediksi Penyakit Jantung
### Langkah 1: Pembagian Data
- **100 pasien** → 70 training, 15 validation, 15 testing.  
- **Pisahkan fitur (X)** dan **target (y)** sebelum pembagian.  

### Langkah 2: Pelatihan Model
```python
model = RandomForestClassifier()
model.fit(X_train, y_train)
```

### Langkah 3: Evaluasi di Validation Set
```python
val_accuracy = model.score(X_val, y_val)
print(f"Akurasi Validasi: {val_accuracy:.2f}")
```

### Langkah 4: Uji di Test Set
```python
test_accuracy = model.score(X_test, y_test)
print(f"Akurasi Testing: {test_accuracy:.2f}")
```

### Hasil:
- Jika akurasi validation dan testing mirip (e.g., 85% vs 83%), model dianggap _generalize_.  
- Jika validation jauh lebih tinggi (e.g., 90% vs 75%), terjadi _overfitting_.

[🔙 Kembali ke Daftar Isi](#daftar-isi)

---

## ⚠️ Tips dan Praktik Terbaik
1. **Hindari Data Leakage**:  
   - Jangan gunakan informasi dari test set untuk preprocessing (e.g., normalisasi).  
2. **Cross-Validation**:  
   - Untuk data kecil, gunakan teknik seperti 5-fold CV di training set.  
3. **Reproduktibilitas**:  
   - Tetapkan `random_state` saat membagi data.  
4. **Update Berkala**:  
   - Jika data terus bertambah, evaluasi ulang rasio pembagian.  

[🔙 Kembali ke Daftar Isi](#daftar-isi)

---

## 🔗 Referensi
1. [📄 Dokumentasi Scikit-Learn: Pembagian Data](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html)  
2. [🎓 Artikel "Understanding Train, Validation, and Test Sets" oleh Towards Data Science](https://towardsdatascience.com/train-validation-and-test-sets-72cb40cba9e7)  
3. [📚 Buku "Hands-On Machine Learning with Scikit-Learn and TensorFlow" (Bab 2)](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)  

[🔙 Kembali ke Daftar Isi](#daftar-isi)

---

## ❓ FAQ
**Q: Apa beda validation set dan test set?**  
A: Validation set digunakan selama pengembangan model (e.g., tuning hyperparameter), sedangkan test set hanya untuk evaluasi akhir.  

**Q: Bagaimana jika data sangat tidak seimbang?**  
A: Gunakan stratified sampling atau teknik oversampling/undersampling.  

**Q: Bisakah hanya menggunakan training dan test set?**  
A: Bisa, tetapi kurang optimal untuk tuning model. Validation set membantu menghindari overfitting ke test set.  

[🔙 Kembali ke Daftar Isi](#daftar-isi)