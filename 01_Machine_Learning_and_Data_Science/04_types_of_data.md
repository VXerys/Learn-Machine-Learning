# 📚 Dokumentasi: Jenis Data dalam Pembelajaran Mesin

## 📑 Daftar Isi
- [📚 Dokumentasi: Jenis Data dalam Pembelajaran Mesin](#-dokumentasi-jenis-data-dalam-pembelajaran-mesin)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🌟 Pendahuluan](#-pendahuluan)
  - [📊 Jenis Data](#-jenis-data)
    - [🗂️ Data Terstruktur](#️-data-terstruktur)
    - [🎨 Data Tidak Terstruktur](#-data-tidak-terstruktur)
  - [⏳ Data Statis vs Data Streaming](#-data-statis-vs-data-streaming)
    - [📂 Data Statis](#-data-statis)
    - [🌊 Data Streaming](#-data-streaming)
  - [🛠️ Workflow Data Science](#️-workflow-data-science)
  - [📖 Referensi](#-referensi)

---

## 🌟 Pendahuluan

Dalam dunia pembelajaran mesin (machine learning), memahami jenis data yang kita miliki adalah langkah penting sebelum memulai analisis atau membangun model. Data yang kita gunakan dapat bervariasi dalam bentuk dan ukuran, dan setiap jenis data memerlukan pendekatan yang berbeda. Dokumen ini akan membahas secara mendalam tentang jenis-jenis data, perbedaan antara data statis dan streaming, serta alur kerja umum dalam data science.

[🔙 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📊 Jenis Data

### 🗂️ Data Terstruktur

Data terstruktur adalah jenis data yang biasanya disimpan dalam format tabel, seperti file Excel atau CSV (Comma Separated Values). Data ini memiliki format yang konsisten, di mana setiap baris mewakili satu sampel (misalnya, catatan medis pasien), dan setiap kolom mewakili atribut tertentu (misalnya, berat badan, jenis kelamin, atau tekanan darah).

**Contoh:**
- **Catatan Medis Pasien:** Setiap baris mewakili satu pasien, dan kolom-kolomnya berisi informasi seperti ID pasien, berat badan, jenis kelamin, dan apakah pasien tersebut memiliki penyakit jantung.
- **Transaksi Pembelian Pelanggan:** Setiap baris mewakili satu transaksi, dan kolom-kolomnya berisi informasi seperti ID pelanggan, tanggal transaksi, dan jumlah pembelian.

Data terstruktur sangat cocok untuk analisis statistik dan pembelajaran mesin karena formatnya yang konsisten dan mudah diproses.

[🔙 Kembali ke Daftar Isi](#-daftar-isi)

### 🎨 Data Tidak Terstruktur

Data tidak terstruktur adalah jenis data yang tidak memiliki format yang konsisten. Contohnya termasuk gambar, teks, video, dan file audio. Meskipun data ini dapat diubah menjadi angka dan diberi struktur, format aslinya sangat bervariasi.

**Contoh:**
- **Gambar:** Satu gambar anjing mungkin terlihat sangat berbeda dengan gambar anjing lainnya.
- **Teks:** Email yang Anda tulis kepada teman mungkin memiliki struktur yang berbeda dengan email yang Anda tulis kepada rekan kerja.

Data tidak terstruktur memerlukan teknik khusus untuk diproses, seperti pengolahan gambar (image processing) atau pengolahan bahasa alami (natural language processing).

[🔙 Kembali ke Daftar Isi](#-daftar-isi)

---

## ⏳ Data Statis vs Data Streaming

### 📂 Data Statis

Data statis adalah data yang tidak berubah seiring waktu. Contohnya adalah file CSV yang berisi catatan medis pasien. Data ini biasanya disimpan dalam satu file dan dapat dibaca menggunakan alat seperti pandas, sebuah library Python untuk analisis data.

**Contoh:**
- **File CSV:** File ini berisi data yang dipisahkan oleh koma, seperti ID, berat badan, dan jenis kelamin. Data ini dapat diubah menjadi tabel yang lebih terstruktur untuk analisis lebih lanjut.

Data statis sangat berguna dalam pembelajaran mesin karena kita dapat mengumpulkan banyak contoh untuk melatih model. Semakin banyak data yang kita miliki, semakin baik model kita dalam menemukan pola dan membuat prediksi.

[🔙 Kembali ke Daftar Isi](#-daftar-isi)

### 🌊 Data Streaming

Data streaming adalah data yang terus berubah seiring waktu. Contohnya adalah berita terkini yang memengaruhi harga saham. Data ini terus diperbarui, dan kita perlu memprosesnya secara real-time untuk mendapatkan wawasan yang relevan.

**Contoh:**
- **Berita Saham:** Berita terkini dapat memengaruhi harga saham secara instan. Untuk memprediksi perubahan harga saham, kita perlu memproses data streaming ini secara terus-menerus.

Meskipun data streaming lebih kompleks untuk diproses, data ini sangat penting dalam aplikasi real-time seperti prediksi pasar saham atau analisis media sosial.

[🔙 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🛠️ Workflow Data Science

Alur kerja umum dalam data science dimulai dengan membuka file CSV di Jupyter Notebook, sebuah alat untuk membangun proyek pembelajaran mesin. Langkah selanjutnya adalah menjelajahi data dan melakukan analisis data menggunakan pandas. Kita juga dapat membuat visualisasi data menggunakan matplotlib, sebuah library Python untuk membuat grafik.

Setelah itu, kita dapat membangun model pembelajaran mesin menggunakan scikit-learn, sebuah library Python untuk pembelajaran mesin. Model ini dapat digunakan untuk memprediksi hasil berdasarkan pola yang ditemukan dalam data.

**Contoh:**
- **Prediksi Penyakit Jantung:** Dengan menggunakan data pasien, kita dapat membangun model untuk memprediksi apakah seorang pasien memiliki penyakit jantung atau tidak.

Meskipun alat-alat ini mungkin terdengar asing, kita akan mempelajarinya lebih lanjut dalam proyek-proyek mendatang.

[🔙 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📖 Referensi

Berikut adalah beberapa referensi tambahan untuk mempelajari lebih lanjut tentang jenis data dan alur kerja data science:

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Jupyter Notebook Documentation](https://jupyter.org/documentation)

[🔙 Kembali ke Daftar Isi](#-daftar-isi)