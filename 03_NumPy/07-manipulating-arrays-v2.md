
# 📚 NumPy Aggregation Functions: A Comprehensive Guide

## 📑 Table of Contents
- [📚 NumPy Aggregation Functions: A Comprehensive Guide](#-numpy-aggregation-functions-a-comprehensive-guide)
  - [📑 Table of Contents](#-table-of-contents)
  - [1. Introduction to Aggregation 🧮](#1-introduction-to-aggregation-)
  - [2. Python Sum vs. NumPy Sum ⚖️](#2-python-sum-vs-numpy-sum-️)
  - [3. Practical Example: Timing Python Sum vs. NumPy Sum ⏱️](#3-practical-example-timing-python-sum-vs-numpy-sum-️)
  - [4. Other NumPy Aggregation Functions 📊](#4-other-numpy-aggregation-functions-)
  - [5. Understanding Variance and Standard Deviation 📏](#5-understanding-variance-and-standard-deviation-)
  - [6. References \& Additional Resources 📖](#6-references--additional-resources-)

---

## 1. Introduction to Aggregation 🧮

Aggregasi adalah proses melakukan operasi yang sama pada sejumlah elemen data. Dalam konteks NumPy, aggregasi melibatkan operasi matematika seperti penjumlahan, rata-rata, maksimum, minimum, dan lainnya pada array NumPy. Aggregasi sangat penting dalam analisis data dan machine learning karena memungkinkan kita untuk meringkas dan memahami data dengan lebih baik.

Contoh sederhana dari aggregasi adalah menghitung total dari semua elemen dalam sebuah array. Misalnya, jika kita memiliki array `[1, 2, 3]`, maka hasil aggregasi dengan fungsi `sum` adalah `6`.

---

## 2. Python Sum vs. NumPy Sum ⚖️

Ada dua cara untuk melakukan penjumlahan pada data: menggunakan fungsi `sum` bawaan Python dan menggunakan fungsi `np.sum` dari NumPy. Meskipun keduanya menghasilkan hasil yang sama, ada perbedaan penting dalam performa dan penggunaan.

- **Python Sum**: Fungsi ini digunakan pada tipe data Python seperti list. Contoh:
  ```python
  list_data = [1, 2, 3]
  total = sum(list_data)  # Hasil: 6
  ```

- **NumPy Sum**: Fungsi ini digunakan pada array NumPy. Contoh:
  ```python
  import numpy as np
  array_data = np.array([1, 2, 3])
  total = np.sum(array_data)  # Hasil: 6
  ```

**Tip Praktis**: Gunakan fungsi `sum` bawaan Python untuk tipe data Python, dan gunakan `np.sum` untuk array NumPy. Ini akan memastikan performa yang optimal.

---

## 3. Practical Example: Timing Python Sum vs. NumPy Sum ⏱️

Untuk menunjukkan perbedaan performa antara `sum` Python dan `np.sum`, mari kita buat array besar dengan 100.000 elemen dan mengukur waktu yang dibutuhkan untuk menjumlahkannya.

```python
import numpy as np
import time

# Membuat array besar dengan 100.000 elemen
massive_array = np.random.rand(100000)

# Mengukur waktu untuk Python sum
start_time = time.time()
total_python = sum(massive_array)
end_time = time.time()
print(f"Python Sum Time: {end_time - start_time} seconds")

# Mengukur waktu untuk NumPy sum
start_time = time.time()
total_numpy = np.sum(massive_array)
end_time = time.time()
print(f"NumPy Sum Time: {end_time - start_time} seconds")
```

**Hasil**: `np.sum` akan jauh lebih cepat daripada `sum` Python, terutama untuk array yang besar. Ini karena NumPy dioptimalkan untuk perhitungan numerik.

---

## 4. Other NumPy Aggregation Functions 📊

Selain `sum`, NumPy menyediakan berbagai fungsi aggregasi lainnya yang berguna dalam analisis data:

- **Mean (Rata-rata)**: Menghitung nilai rata-rata dari array.
  ```python
  mean_value = np.mean(array_data)
  ```

- **Maximum (Nilai Maksimum)**: Menemukan nilai maksimum dalam array.
  ```python
  max_value = np.max(array_data)
  ```

- **Minimum (Nilai Minimum)**: Menemukan nilai minimum dalam array.
  ```python
  min_value = np.min(array_data)
  ```

- **Standard Deviation (Simpangan Baku)**: Mengukur seberapa tersebar nilai dalam array.
  ```python
  std_dev = np.std(array_data)
  ```

- **Variance (Variansi)**: Mengukur variabilitas nilai dalam array.
  ```python
  variance = np.var(array_data)
  ```

---

## 5. Understanding Variance and Standard Deviation 📏

**Variansi** adalah ukuran seberapa jauh setiap angka dalam dataset berbeda dari rata-rata. Variansi yang tinggi menunjukkan bahwa angka-angka dalam dataset tersebar luas, sedangkan variansi yang rendah menunjukkan bahwa angka-angka tersebut cenderung mendekati rata-rata.

**Simpangan Baku** adalah akar kuadrat dari variansi. Ini memberikan gambaran tentang seberapa jauh nilai-nilai dalam dataset tersebar dari rata-rata. Simpangan baku yang tinggi menunjukkan variabilitas yang besar, sedangkan simpangan baku yang rendah menunjukkan konsistensi.

Contoh perhitungan:
```python
import numpy as np

data = np.array([1, 2, 3, 4, 5, 6])
variance = np.var(data)
std_dev = np.std(data)

print(f"Variance: {variance}")
print(f"Standard Deviation: {std_dev}")
```

---

## 6. References & Additional Resources 📖

Untuk mempelajari lebih lanjut tentang NumPy dan konsep-konsep yang dibahas dalam dokumentasi ini, berikut beberapa sumber daya yang berguna:

- [NumPy Documentation](https://numpy.org/doc/)
- [Python Data Science Handbook by Jake VanderPlas](https://jakevdp.github.io/PythonDataScienceHandbook/)
- [Khan Academy: Variance and Standard Deviation](https://www.khanacademy.org/math/statistics-probability/summarizing-quantitative-data/variance-standard-deviation-population/a/variance-and-standard-deviation)

---

[🔝 Kembali ke Daftar Isi](#-table-of-contents)
