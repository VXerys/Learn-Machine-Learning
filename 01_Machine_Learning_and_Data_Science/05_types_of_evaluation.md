# 📚 Dokumentasi Evaluasi Metrik dalam Machine Learning

## 📑 Daftar Isi
- [📚 Dokumentasi Evaluasi Metrik dalam Machine Learning](#-dokumentasi-evaluasi-metrik-dalam-machine-learning)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🌟 Pendahuluan](#-pendahuluan)
  - [📊 Apa Itu Metrik Evaluasi?](#-apa-itu-metrik-evaluasi)
  - [📈 Jenis-Jenis Metrik Evaluasi](#-jenis-jenis-metrik-evaluasi)
    - [🎯 Klasifikasi](#-klasifikasi)
    - [📉 Regresi](#-regresi)
    - [🛍️ Rekomendasi](#️-rekomendasi)
  - [🏁 Contoh Praktis Metrik Evaluasi](#-contoh-praktis-metrik-evaluasi)
  - [📖 Referensi \& Sumber Tambahan](#-referensi--sumber-tambahan)
  - [🔄 Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🌟 Pendahuluan

![image](https://github.com/user-attachments/assets/1facdfe3-d74d-40ee-ad6f-b4b512c86104)

Setelah melalui langkah pertama (definisi masalah) dan langkah kedua (pengumpulan data), kita tiba pada langkah ketiga: **evaluasi**. Evaluasi adalah proses penting dalam machine learning yang bertujuan untuk mengukur seberapa baik model kita dalam memprediksi masa depan berdasarkan data yang ada. Dalam dokumentasi ini, kita akan membahas secara mendalam tentang metrik evaluasi, jenis-jenisnya, serta contoh praktis penggunaannya.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📊 Apa Itu Metrik Evaluasi?

![image](https://github.com/user-attachments/assets/91bf057a-a66a-4a44-a50a-eb87857c086e)

Metrik evaluasi adalah alat yang digunakan untuk mengukur performa suatu model machine learning. Tujuannya adalah untuk menjawab pertanyaan: **Apa yang mendefinisikan kesuksesan bagi kita?** Misalnya, jika kita ingin memprediksi apakah seorang pasien menderita penyakit jantung berdasarkan rekam medisnya, kita mungkin menetapkan bahwa model harus memiliki akurasi di atas 99% untuk dianggap berhasil.

Metrik evaluasi membantu tim proyek memiliki tujuan yang sama dan memastikan bahwa model yang dibangun memenuhi standar yang diperlukan. Namun, penting untuk diingat bahwa metrik evaluasi bisa berubah seiring dengan perkembangan proyek, terutama ketika kita semakin memahami data yang kita miliki.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📈 Jenis-Jenis Metrik Evaluasi

![image](https://github.com/user-attachments/assets/8e0bf4fa-e592-4563-8ad5-4cc246af9499)

Metrik evaluasi bervariasi tergantung pada jenis masalah yang dihadapi. Berikut adalah beberapa jenis metrik evaluasi yang umum digunakan:

### 🎯 Klasifikasi
Dalam masalah klasifikasi, kita ingin memprediksi apakah suatu data termasuk dalam kategori tertentu. Beberapa metrik yang umum digunakan adalah:
- **Akurasi**: Persentase prediksi yang benar dari total prediksi.
- **Presisi**: Proporsi prediksi positif yang benar dari total prediksi positif.
- **Recall**: Proporsi prediksi positif yang benar dari total data yang sebenarnya positif.

Contoh: Jika kita ingin memprediksi apakah seseorang menderita penyakit jantung, akurasi adalah metrik yang penting karena kita ingin meminimalkan kesalahan prediksi.

### 📉 Regresi
Dalam masalah regresi, kita ingin memprediksi nilai numerik. Beberapa metrik yang umum digunakan adalah:
- **Mean Absolute Error (MAE)**: Rata-rata selisih absolut antara nilai prediksi dan nilai sebenarnya.
- **Mean Squared Error (MSE)**: Rata-rata kuadrat selisih antara nilai prediksi dan nilai sebenarnya.

Contoh: Jika kita ingin memprediksi harga jual mobil, MAE atau MSE bisa digunakan untuk mengukur seberapa dekat prediksi kita dengan harga sebenarnya.

### 🛍️ Rekomendasi
Dalam masalah rekomendasi, kita ingin memberikan rekomendasi yang relevan kepada pengguna. Salah satu metrik yang umum digunakan adalah:
- **Precision at K**: Proporsi rekomendasi yang relevan dalam K rekomendasi teratas.

Contoh: Jika kita memiliki ribuan produk untuk direkomendasikan, kita mungkin hanya peduli dengan 10 rekomendasi teratas dan seberapa baik mereka sesuai dengan minat pelanggan.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🏁 Contoh Praktis Metrik Evaluasi

![image](https://github.com/user-attachments/assets/ebd06f79-2dca-4cfd-a037-20837af1a1ff)

Sebagai contoh praktis, mari kita lihat sebuah proyek di mana kita ingin menggunakan teks dari klaim asuransi mobil untuk memprediksi siapa yang menyebabkan kecelakaan: orang yang mengajukan klaim atau orang lain yang terlibat. Perusahaan asuransi menetapkan bahwa model harus memiliki akurasi minimal 95% untuk dianggap berhasil. Ini berarti model hanya boleh salah dalam 1 dari 20 klaim.

Dalam kasus ini, akurasi adalah metrik evaluasi yang tepat karena kita ingin memastikan bahwa prediksi model sangat akurat. Proyek ini menunjukkan pentingnya memilih metrik evaluasi yang sesuai dengan tujuan proyek.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📖 Referensi & Sumber Tambahan
Berikut adalah beberapa referensi dan sumber tambahan yang dapat membantu Anda memahami lebih dalam tentang metrik evaluasi dalam machine learning:
- [Scikit-learn Documentation on Model Evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html)
- [Towards Data Science: Understanding Evaluation Metrics](https://towardsdatascience.com/understanding-evaluation-metrics-980b6d86f1a0)
- [Machine Learning Mastery: How to Choose Metrics for Classification](https://machinelearningmastery.com/metrics-evaluate-machine-learning-algorithms-python/)

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🔄 Kembali ke Daftar Isi
[Kembali ke Daftar Isi](#-daftar-isi)
