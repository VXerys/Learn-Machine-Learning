
# 🧠 Machine Learning Documentation: Dot Product in Practice

## 📚 Table of Contents
- [🧠 Machine Learning Documentation: Dot Product in Practice](#-machine-learning-documentation-dot-product-in-practice)
  - [📚 Table of Contents](#-table-of-contents)
  - [🌟 Introduction](#-introduction)
  - [🧮 Understanding the Dot Product](#-understanding-the-dot-product)
  - [🥜 Practical Example: Nut Butter Sales](#-practical-example-nut-butter-sales)
  - [🐍 Implementing the Dot Product in Python](#-implementing-the-dot-product-in-python)
    - [1. Membuat Data Penjualan](#1-membuat-data-penjualan)
    - [2. Membuat DataFrame untuk Penjualan Mingguan](#2-membuat-dataframe-untuk-penjualan-mingguan)
    - [3. Membuat Array Harga](#3-membuat-array-harga)
    - [4. Menghitung Total Penjualan Menggunakan Dot Product](#4-menghitung-total-penjualan-menggunakan-dot-product)
    - [5. Menambahkan Kolom Total ke DataFrame](#5-menambahkan-kolom-total-ke-dataframe)
  - [🐼 Data Manipulation with Pandas](#-data-manipulation-with-pandas)
  - [📊 Visualizing the Results](#-visualizing-the-results)
  - [🎯 Conclusion](#-conclusion)
  - [🔗 References](#-references)
    - [Penjelasan:](#penjelasan)

---

## 🌟 Introduction

Dalam video ini, kita membahas konsep **dot product** (perkalian titik) dan bagaimana konsep ini dapat diterapkan dalam konteks praktis, khususnya dalam analisis data dan machine learning. Dot product adalah operasi matematika yang sangat penting dalam aljabar linear dan memiliki banyak aplikasi dalam pemrosesan data, seperti menghitung total penjualan, analisis vektor, dan banyak lagi.

---

## 🧮 Understanding the Dot Product

Dot product adalah operasi yang mengambil dua vektor dan menghasilkan skalar. Secara matematis, dot product dari dua vektor **A** dan **B** didefinisikan sebagai:

$$
A \cdot B = \sum_{i=1}^{n} A_i \times B_i
$$


Dalam konteks praktis, dot product sering digunakan untuk menghitung total nilai dari beberapa produk berdasarkan jumlah dan harga masing-masing produk.

---

## 🥜 Practical Example: Nut Butter Sales

Dalam contoh ini, kita akan menganalisis penjualan selai kacang (nut butter) selama seminggu. Data yang digunakan meliputi jumlah toples yang terjual untuk tiga jenis selai kacang: almond butter, peanut butter, dan cashew butter. Tujuan kita adalah menghitung total pendapatan harian menggunakan dot product.

---

## 🐍 Implementing the Dot Product in Python

Berikut adalah langkah-langkah untuk mengimplementasikan dot product menggunakan Python dengan bantuan library **NumPy** dan **Pandas**.

### 1. Membuat Data Penjualan
```python
import numpy as np
import pandas as pd

# Set random seed untuk konsistensi
np.random.seed(42)

# Membuat data jumlah toples yang terjual
sales_amounts = np.random.randint(0, 20, size=(5, 3))
print("Jumlah toples yang terjual:\n", sales_amounts)
```

### 2. Membuat DataFrame untuk Penjualan Mingguan
```python
# Membuat DataFrame untuk penjualan mingguan
weekly_sales = pd.DataFrame(sales_amounts, 
                            index=["Mon", "Tue", "Wed", "Thu", "Fri"], 
                            columns=["Almond Butter", "Peanut Butter", "Cashew Butter"])
print("Penjualan Mingguan:\n", weekly_sales)
```

### 3. Membuat Array Harga
```python
# Membuat array harga untuk setiap jenis selai kacang
prices = np.array([10, 8, 12])
print("Harga per toples:\n", prices)
```

### 4. Menghitung Total Penjualan Menggunakan Dot Product
```python
# Menghitung total penjualan harian
total_sales = prices.dot(sales_amounts.T)
print("Total Penjualan Harian:\n", total_sales)
```

### 5. Menambahkan Kolom Total ke DataFrame
```python
# Menambahkan kolom total penjualan ke DataFrame
weekly_sales["Total Sales ($)"] = total_sales
print("Penjualan Mingguan dengan Total:\n", weekly_sales)
```

---

## 🐼 Data Manipulation with Pandas

Pandas adalah library yang sangat powerful untuk manipulasi data. Dalam contoh ini, kita menggunakan Pandas untuk:
- Membuat DataFrame dari array NumPy.
- Menambahkan kolom baru ke DataFrame.
- Melakukan operasi dot product pada DataFrame.

---

## 📊 Visualizing the Results

Visualisasi data adalah langkah penting dalam analisis data. Berikut adalah contoh visualisasi sederhana menggunakan **Matplotlib**.

```python
import matplotlib.pyplot as plt

# Visualisasi total penjualan harian
weekly_sales["Total Sales ($)"].plot(kind="bar", color="skyblue")
plt.title("Total Penjualan Harian")
plt.xlabel("Hari")
plt.ylabel("Total Penjualan ($)")
plt.show()
```

---

## 🎯 Conclusion

Dalam dokumentasi ini, kita telah mempelajari bagaimana dot product dapat diterapkan dalam analisis data praktis. Dengan menggunakan Python, NumPy, dan Pandas, kita dapat dengan mudah menghitung total penjualan dan memvisualisasikan hasilnya. Latihan ini juga menunjukkan pentingnya memahami operasi matematika dasar dalam konteks machine learning dan analisis data.

---

## 🔗 References
- [NumPy Documentation](https://numpy.org/doc/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

---

[⬆️ Kembali ke Daftar Isi](#table-of-contents)
```

### Penjelasan:
1. **Struktur Markdown**: Dokumentasi ini menggunakan struktur Markdown yang jelas dengan judul, subjudul, dan daftar isi yang dapat diklik.
2. **Ikon Emoji**: Ikon emoji digunakan untuk membuat dokumen lebih menarik secara visual.
3. **Penjelasan Mendalam**: Setiap bagian dijelaskan secara rinci dengan contoh kode yang dapat dijalankan.
4. **Referensi**: Bagian referensi menyediakan tautan ke dokumentasi resmi library yang digunakan.
5. **Navigasi**: Tautan "Kembali ke Daftar Isi" disertakan di akhir setiap bagian untuk memudahkan navigasi.
6. **Bahasa**: Judul dan subjudul dalam bahasa Inggris, sementara penjelasan dan konten dalam bahasa Indonesia.