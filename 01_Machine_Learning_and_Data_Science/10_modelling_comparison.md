
# 📚 Dokumentasi Evaluasi Model Machine Learning

## 📑 Daftar Isi Interaktif
- [📚 Dokumentasi Evaluasi Model Machine Learning](#-dokumentasi-evaluasi-model-machine-learning)
  - [📑 Daftar Isi Interaktif](#-daftar-isi-interaktif)
  - [🔍 Evaluasi Model pada Data Uji](#-evaluasi-model-pada-data-uji)
    - [Mengapa Data Uji Penting?](#mengapa-data-uji-penting)
    - [Contoh Implementasi di Python:](#contoh-implementasi-di-python)
  - [⚖️ Overfitting vs. Underfitting](#️-overfitting-vs-underfitting)
    - [Overfitting (Terlalu Sesuai)](#overfitting-terlalu-sesuai)
    - [Underfitting (Kurang Sesuai)](#underfitting-kurang-sesuai)
  - [🚫 Kebocoran Data \& Ketidaksesuaian Data](#-kebocoran-data--ketidaksesuaian-data)
    - [Kebocoran Data (Data Leakage)](#kebocoran-data-data-leakage)
    - [Ketidaksesuaian Data (Data Mismatch)](#ketidaksesuaian-data-data-mismatch)
  - [📊 Perbandingan Model](#-perbandingan-model)
    - [Kriteria Perbandingan](#kriteria-perbandingan)
    - [Contoh Kasus:](#contoh-kasus)
  - [💡 Praktik Terbaik](#-praktik-terbaik)
    - [Tips untuk Pemula:](#tips-untuk-pemula)
  - [🔗 Referensi \& Sumber Tambahan](#-referensi--sumber-tambahan)

---

## 🔍 Evaluasi Model pada Data Uji
Setelah melakukan pelatihan dan penyetelan hiperparameter, langkah kritis adalah mengevaluasi model menggunakan **data uji** (test set). Data uji berperan sebagai simulasi dunia nyata untuk menguji kemampuan generalisasi model. 

### Mengapa Data Uji Penting?
- **Indikator Generalisasi**: Data uji harus *belum pernah dilihat* oleh model selama pelatihan. Ini memastikan evaluasi objektif.  
- **Akurasi yang Realistis**: Contoh: Akurasi 98% pada data latih vs. 96% pada data uji menunjukkan model masih stabil.  
- **Tanda Bahaya**: Perbedaan signifikan (misal: 99% vs. 70%) mengindikasikan masalah seperti overfitting atau kebocoran data.

### Contoh Implementasi di Python:
```python
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

# Bagi data menjadi latih dan uji
X_train, X_test, y_train, y_test = train_test_split(fitur, target, test_size=0.2, random_state=42)

# Latih model
model.fit(X_train, y_train)

# Evaluasi pada data uji
prediksi = model.predict(X_test)
print(f"Akurasi Data Uji: {accuracy_score(y_test, prediksi)*100:.2f}%")
```

[⬆ Kembali ke Daftar Isi](#-daftar-isi-interaktif)

---

## ⚖️ Overfitting vs. Underfitting
### Overfitting (Terlalu Sesuai)
- **Ciri**: Model "menghafal" data latih, performa buruk pada data baru.  
- **Penyebab**:  
  - Model terlalu kompleks (contoh: neural network dengan terlalu banyak lapisan).  
  - Data latih tidak cukup beragam.  
- **Solusi**:  
  - Gunakan teknik regularisasi (L1/L2).  
  - Tambahkan lebih banyak data atau augmentasi data.  
  - Kurangi kompleksitas model.

### Underfitting (Kurang Sesuai)
- **Ciri**: Model gagal menangkap pola dasar dalam data.  
- **Penyebab**:  
  - Model terlalu sederhana (contoh: regresi linear untuk masalah non-linear).  
  - Fitur yang relevan tidak tercakup.  
- **Solusi**:  
  - Tingkatkan kompleksitas model (contoh: gunakan decision tree -> random forest).  
  - Lakukan feature engineering untuk mengekstrak pola lebih baik.

![Overfitting vs Underfitting](https://miro.medium.com/v2/resize:fit:1400/1*_7OPgojau8hkiPUiHoGK_w.png)  
*Ilustrasi: Model ideal berada di "Zona Goldilocks" (tidak terlalu sederhana atau kompleks).*

[⬆ Kembali ke Daftar Isi](#-daftar-isi-interaktif)

---

## 🚫 Kebocoran Data & Ketidaksesuaian Data
### Kebocoran Data (Data Leakage)
- **Apa Itu?**: Informasi dari data uji "bocor" ke data latih.  
- **Contoh**:  
  - Melakukan preprocessing (seperti normalisasi) *sebelum* membagi data.  
  - Menggunakan fitur yang hanya tersedia setelah prediksi (misal: hasil lab yang belum diketahui).  
- **Dampak**: Akurasi artifisial tinggi tetapi gagal di produksi.  
- **Pencegahan**:  
  - Selakukan pembagian data sebelum preprocessing.  
  - Gunakan pipeline (contoh: `sklearn.pipeline`).

### Ketidaksesuaian Data (Data Mismatch)
- **Apa Itu?**: Data latih dan uji berasal dari distribusi berbeda.  
- **Contoh**:  
  - Data latih berisi gambar siang hari, data uji gambar malam hari.  
  - Perbedaan format atau skala fitur.  
- **Solusi**:  
  - Lakukan analisis EDA (Exploratory Data Analysis) untuk memastikan konsistensi.  
  - Gunakan teknik domain adaptation jika diperlukan.

[⬆ Kembali ke Daftar Isi](#-daftar-isi-interaktif)

---

## 📊 Perbandingan Model
### Kriteria Perbandingan
1. **Akurasi**: Metrik utama (presisi, recall, F1-score).  
2. **Kecepatan Prediksi**: Penting untuk aplikasi real-time.  
3. **Sumber Daya Komputasi**: RAM, GPU, dll.  
4. **Interpretabilitas**: Model linear vs. black-box (seperti neural network).

### Contoh Kasus:
| Model | Akurasi | Waktu Prediksi (ms) | Konsumsi RAM |
|-------|---------|----------------------|-------------|
| A     | 92%     | 50                   | 2GB         |
| B     | 94%     | 200                  | 8GB         |

**Pertimbangan**: Jika aplikasi memprioritaskan kecepatan, Model A lebih baik meski akurasi sedikit lebih rendah.

[⬆ Kembali ke Daftar Isi](#-daftar-isi-interaktif)

---

## 💡 Praktik Terbaik
1. **Jaga Data Uji Tetap Terisolasi**: Jangan gunakan untuk tuning atau validasi.  
2. **Validasi Silang**: Gunakan teknik k-fold cross-validation untuk evaluasi lebih robust.  
3. **Logging & Tracking**: Catat semua eksperimen (tools: MLflow, TensorBoard).  
4. **Evaluasi Berkelanjutan**: Monitor performa model secara berkala setelah deployment.

### Tips untuk Pemula:
- Mulailah dengan model sederhana (seperti regresi/logistic regression) sebagai baseline.  
- Lakukan eksperimen bertahap: tambahkan kompleksitas hanya jika diperlukan.  
- Dokumentasikan setiap perubahan hiperparameter dan hasilnya.

[⬆ Kembali ke Daftar Isi](#-daftar-isi-interaktif)

---

## 🔗 Referensi & Sumber Tambahan
1. [Scikit-learn Documentation: Model Evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html)  
2. [Artikel Medium: Mengatasi Overfitting](https://towardsdatascience.com/overfitting-vs-underfitting-a-complete-example-d05dd7e19765)  
3. [Buku "Hands-On Machine Learning with Scikit-Learn & TensorFlow"](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)  
4. [Video Tutorial: Cross-Validation oleh StatQuest](https://youtu.be/fSytzGwwBVw)  
5. [Kursus Gratis: Machine Learning di Kaggle](https://www.kaggle.com/learn/machine-learning)  

[⬆ Kembali ke Daftar Isi](#-daftar-isi-interaktif)
