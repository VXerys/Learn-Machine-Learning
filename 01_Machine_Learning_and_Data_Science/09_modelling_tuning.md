# 📚 Dokumentasi: Tuning Model Machine Learning

## 📑 Daftar Isi
- [📚 Dokumentasi: Tuning Model Machine Learning](#-dokumentasi-tuning-model-machine-learning)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🎯 Pendahuluan](#-pendahuluan)
  - [🔧 Apa Itu Tuning Model?](#-apa-itu-tuning-model)
  - [🎛️ Parameter yang Dapat Disesuaikan](#️-parameter-yang-dapat-disesuaikan)
    - [🌳 Random Forest](#-random-forest)
    - [🧠 Neural Network](#-neural-network)
    - [🌡️ Analogi Oven](#️-analogi-oven)
  - [🔄 Proses Tuning Model](#-proses-tuning-model)
  - [🔍 Perbandingan Model](#-perbandingan-model)
  - [📖 Referensi \& Sumber Tambahan](#-referensi--sumber-tambahan)

---

## 🎯 Pendahuluan

![image](https://github.com/user-attachments/assets/a5682032-d9a0-4193-b347-597d88e1f8cb)

Setelah Anda puas dengan performa awal model Anda pada dataset pelatihan, langkah selanjutnya adalah mencoba meningkatkan performa tersebut. Proses ini dikenal sebagai **tuning model**. Seperti halnya menyetel mobil untuk gaya mengemudi yang berbeda, model machine learning juga dapat disetel untuk berbagai jenis data, khususnya data yang Anda miliki.

Dalam dokumentasi ini, kita akan membahas secara mendalam tentang apa itu tuning model, parameter apa yang dapat disesuaikan, proses tuning, dan bagaimana membandingkan model yang berbeda. Mari kita mulai!

---

## 🔧 Apa Itu Tuning Model?

![image](https://github.com/user-attachments/assets/b373a8e4-98f3-4b24-bbe9-17468507ee3b)

Tuning model adalah proses menyesuaikan **hyperparameter** dari model machine learning untuk meningkatkan performanya. Hyperparameter adalah parameter yang tidak dipelajari oleh model selama pelatihan, tetapi ditentukan sebelum proses pelatihan dimulai. Contoh hyperparameter termasuk jumlah pohon dalam Random Forest atau jumlah lapisan dalam Neural Network.

Proses tuning biasanya dilakukan pada **dataset validasi**. Namun, jika Anda tidak memiliki dataset validasi karena cara Anda membagi data pelatihan, validasi, dan uji, tuning juga dapat dilakukan pada dataset pelatihan.

---

## 🎛️ Parameter yang Dapat Disesuaikan

![image](https://github.com/user-attachments/assets/fbf9cb97-370e-4b72-ba21-2732a276433b)

Setiap model machine learning memiliki hyperparameter yang berbeda yang dapat disesuaikan. Berikut adalah beberapa contoh:

### 🌳 Random Forest
- **Jumlah Pohon**: Anda dapat menyesuaikan jumlah pohon dalam Random Forest. Misalnya, Anda bisa mencoba dengan 3 pohon atau 5 pohon untuk melihat mana yang memberikan hasil terbaik.

### 🧠 Neural Network
- **Jumlah Lapisan**: Anda dapat menyesuaikan jumlah lapisan dalam Neural Network. Semakin banyak lapisan, semakin kompleks modelnya.

### 🌡️ Analogi Oven
Bayangkan hyperparameter seperti tombol pada oven. Jika Anda memasak ayam pada suhu 180°C selama satu jam dan hasilnya kurang matang, Anda bisa mencoba meningkatkan suhu menjadi 200°C untuk mendapatkan hasil yang lebih baik. Demikian pula, Anda dapat menyesuaikan hyperparameter model untuk meningkatkan performanya.

![image](https://github.com/user-attachments/assets/52b0e3b3-5108-4331-8d1d-89c6c3918704)

---

## 🔄 Proses Tuning Model

Proses tuning model melibatkan beberapa langkah:

1. **Pelatihan Awal**: Latih model dengan set hyperparameter awal (biasanya default).
2. **Evaluasi**: Evaluasi performa model pada dataset validasi atau pelatihan.
3. **Penyesuaian**: Sesuaikan hyperparameter berdasarkan hasil evaluasi.
4. **Pelatihan Ulang**: Latih ulang model dengan hyperparameter yang telah disesuaikan.
5. **Evaluasi Ulang**: Evaluasi kembali performa model.

Proses ini diulang hingga Anda mendapatkan performa yang memuaskan.

---

## 🔍 Perbandingan Model

Setelah Anda melatih beberapa model berbeda pada dataset yang sama, langkah selanjutnya adalah membandingkan performa mereka. Perbandingan ini dilakukan pada **dataset uji**. Berikut adalah beberapa metrik yang dapat digunakan untuk membandingkan model:

- **Akurasi**: Seberapa sering model membuat prediksi yang benar.
- **Presisi & Recall**: Berguna untuk masalah klasifikasi, terutama ketika kelas tidak seimbang.
- **F1-Score**: Rata-rata harmonik dari presisi dan recall.
- **RMSE (Root Mean Squared Error)**: Berguna untuk masalah regresi, mengukur seberapa jauh prediksi model dari nilai sebenarnya.

Dengan membandingkan model menggunakan metrik ini, Anda dapat memilih model yang paling sesuai untuk kebutuhan Anda.

---

## 📖 Referensi & Sumber Tambahan

Berikut adalah beberapa sumber tambahan yang dapat membantu Anda memahami lebih dalam tentang tuning model:

- [Scikit-learn Documentation on Hyperparameter Tuning](https://scikit-learn.org/stable/modules/grid_search.html)
- [Towards Data Science: A Comprehensive Guide to Hyperparameter Tuning](https://towardsdatascience.com/a-comprehensive-guide-to-hyperparameter-tuning-7b4d1c9b7f7a)
- [Machine Learning Mastery: How to Tune Algorithm Parameters](https://machinelearningmastery.com/how-to-tune-algorithm-parameters-with-scikit-learn/)

---

[🔝 Kembali ke Daftar Isi](#-daftar-isi)
