
# 📊 NumPy Aggregation Functions: Variance and Standard Deviation

## 📑 Table of Contents
- [📊 NumPy Aggregation Functions: Variance and Standard Deviation](#-numpy-aggregation-functions-variance-and-standard-deviation)
  - [📑 Table of Contents](#-table-of-contents)
  - [1. Introduction 🎯](#1-introduction-)
  - [2. Variance and Standard Deviation Explained 📚](#2-variance-and-standard-deviation-explained-)
    - [Varians](#varians)
    - [Standar Deviasi](#standar-deviasi)
  - [3. Practical Code Examples 💻](#3-practical-code-examples-)
    - [Creating Arrays](#creating-arrays)
    - [Calculating Variance and Standard Deviation](#calculating-variance-and-standard-deviation)
    - [Visualizing Data Spread](#visualizing-data-spread)
  - [4. Key Takeaways 🚀](#4-key-takeaways-)
  - [5. References 📖](#5-references-)

---

## 1. Introduction 🎯
Dalam video sebelumnya, kita telah membahas beberapa fungsi agregasi menggunakan NumPy, seperti menghitung jumlah semua elemen dalam array. Kita juga melihat betapa cepatnya kode NumPy dibandingkan dengan kode Python murni saat bekerja dengan tipe data NumPy. Oleh karena itu, selalu gunakan fungsi agregasi NumPy pada array NumPy.

Pada video ini, kita akan melanjutkan dengan pengenalan singkat tentang **standar deviasi** dan **varians**. Kedua metrik ini adalah ukuran sebaran data. Mari kita fokus pada praktik langsung dengan menjalankan kode dan melihat contoh nyata.

---

## 2. Variance and Standard Deviation Explained 📚

### Varians
Varians adalah ukuran rata-rata seberapa jauh setiap angka dalam dataset berbeda dari mean (rata-rata). Varians yang tinggi menunjukkan rentang angka yang lebih luas, sedangkan varians yang rendah menunjukkan rentang angka yang lebih sempit.

### Standar Deviasi
Standar deviasi adalah ukuran seberapa tersebar angka-angka dalam dataset dari mean. Standar deviasi yang tinggi menunjukkan bahwa angka-angka dalam dataset tersebar jauh dari mean, sedangkan standar deviasi yang rendah menunjukkan bahwa angka-angka tersebut lebih dekat dengan mean.

---

## 3. Practical Code Examples 💻

### Creating Arrays
Mari kita mulai dengan membuat dua array: satu dengan varians tinggi dan satu dengan varians rendah.

```python
import numpy as np

# Array dengan varians tinggi
high_var_array = np.array([1, 100, 200, 300, 4000, 5000])

# Array dengan varians rendah
low_var_array = np.array([2, 4, 6, 8, 10])
```

### Calculating Variance and Standard Deviation
Selanjutnya, kita akan menghitung varians dan standar deviasi dari kedua array tersebut.

```python
# Menghitung varians
high_var = np.var(high_var_array)
low_var = np.var(low_var_array)

print(f"Varians high_var_array: {high_var}")
print(f"Varians low_var_array: {low_var}")

# Menghitung standar deviasi
high_std = np.std(high_var_array)
low_std = np.std(low_var_array)

print(f"Standar deviasi high_var_array: {high_std}")
print(f"Standar deviasi low_var_array: {low_std}")
```

### Visualizing Data Spread
Untuk memahami sebaran data secara visual, kita dapat menggunakan histogram.

```python
import matplotlib.pyplot as plt

# Membuat histogram untuk high_var_array
plt.hist(high_var_array, bins=5, color='blue', alpha=0.7)
plt.title('Histogram High Variance Array')
plt.show()

# Membuat histogram untuk low_var_array
plt.hist(low_var_array, bins=5, color='green', alpha=0.7)
plt.title('Histogram Low Variance Array')
plt.show()
```

---

## 4. Key Takeaways 🚀
- **Varians** dan **standar deviasi** adalah metrik penting untuk mengukur sebaran data.
- Varians yang tinggi menunjukkan rentang angka yang lebih luas, sedangkan varians yang rendah menunjukkan rentang angka yang lebih sempit.
- Standar deviasi yang tinggi menunjukkan bahwa angka-angka dalam dataset tersebar jauh dari mean, sedangkan standar deviasi yang rendah menunjukkan bahwa angka-angka tersebut lebih dekat dengan mean.
- Visualisasi data menggunakan histogram dapat membantu memahami sebaran data secara lebih intuitif.

---

## 5. References 📖
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Understanding Variance and Standard Deviation](https://www.khanacademy.org/math/statistics-probability/summarizing-quantitative-data/variance-standard-deviation-population/a/calculating-standard-deviation-step-by-step)

---

[🔝 Kembali ke Daftar Isi](#table-of-contents)
