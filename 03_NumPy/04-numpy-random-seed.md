
# 📚 Dokumentasi Lengkap: NumPy dan Pembangkitan Angka Acak dalam Machine Learning

## 📑 Daftar Isi
1. [Pendahuluan](#-pendahuluan)
2. [Membuat Array dengan NumPy](#-membuat-array-dengan-numpy)
3. [Pembangkitan Angka Acak](#-pembangkitan-angka-acak)
4. [Menggunakan `numpy.random.seed`](#-menggunakan-numpyrandomseed)
5. [Praktik: Implementasi Kode](#-praktik-implementasi-kode)
6. [Referensi](#-referensi)
7. [Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🌟 Pendahuluan
NumPy adalah salah satu library paling penting dalam Python untuk komputasi numerik, terutama dalam bidang Machine Learning. Dalam video ini, kita akan mempelajari cara membuat array, membangkitkan angka acak, dan memahami konsep `numpy.random.seed` untuk memastikan hasil yang dapat direproduksi.

---

## 🛠️ Membuat Array dengan NumPy
NumPy menyediakan berbagai cara untuk membuat array. Berikut adalah beberapa contohnya:

### 1. Array Sederhana
```python
import numpy as np
array_sederhana = np.array([1, 2, 3, 4, 5])
print(array_sederhana)
```

### 2. Array Berisi Angka Satu
```python
array_ones = np.ones((3, 3))  # Membuat array 3x3 berisi angka 1
print(array_ones)
```

### 3. Array Berisi Angka Nol
```python
array_zeros = np.zeros((2, 4))  # Membuat array 2x4 berisi angka 0
print(array_zeros)
```

### 4. Array dengan Rentang Tertentu
```python
array_range = np.arange(0, 10, 2)  # Membuat array dari 0 hingga 10 dengan langkah 2
print(array_range)
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🎲 Pembangkitan Angka Acak
NumPy menyediakan fungsi untuk membangkitkan angka acak. Berikut adalah beberapa contohnya:

### 1. Angka Acak antara 0 dan 1
```python
random_floats = np.random.random((5, 3))  # Membuat array 5x3 berisi angka acak antara 0 dan 1
print(random_floats)
```

### 2. Angka Acak Integer dalam Rentang Tertentu
```python
random_ints = np.random.randint(0, 10, (5, 3))  # Membuat array 5x3 berisi angka acak antara 0 dan 10
print(random_ints)
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🔐 Menggunakan `numpy.random.seed`
Angka acak yang dihasilkan oleh NumPy sebenarnya adalah *pseudo-random*, artinya angka tersebut terlihat acak tetapi sebenarnya dihasilkan dari algoritma deterministik. Untuk memastikan hasil yang dapat direproduksi, kita dapat menggunakan `numpy.random.seed`.

### Contoh Penggunaan
```python
np.random.seed(0)  # Menetapkan seed ke 0
random_array = np.random.randint(0, 10, (5, 3))
print(random_array)
```

Dengan menetapkan seed yang sama, kita akan selalu mendapatkan angka acak yang sama setiap kali kode dijalankan.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 💻 Praktik: Implementasi Kode
Berikut adalah contoh lengkap penggunaan NumPy dalam konteks Machine Learning:

### 1. Manipulasi Data dengan Pandas
```python
import pandas as pd

# Membuat DataFrame dari array NumPy
data = np.random.randint(0, 100, (10, 3))
df = pd.DataFrame(data, columns=['Feature1', 'Feature2', 'Feature3'])
print(df)
```

### 2. Implementasi Algoritma Machine Learning dengan Scikit-Learn
```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Membagi data menjadi training dan testing set
X = df[['Feature1', 'Feature2']]
y = df['Feature3']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Melatih model regresi linear
model = LinearRegression()
model.fit(X_train, y_train)

# Memprediksi hasil
predictions = model.predict(X_test)
print(predictions)
```

### 3. Visualisasi Data dengan Matplotlib
```python
import matplotlib.pyplot as plt

# Membuat scatter plot
plt.scatter(X_test['Feature1'], y_test, color='blue', label='Actual')
plt.scatter(X_test['Feature1'], predictions, color='red', label='Predicted')
plt.legend()
plt.show()
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📖 Referensi
- [Dokumentasi Resmi NumPy](https://numpy.org/doc/)
- [Panduan Scikit-Learn](https://scikit-learn.org/stable/documentation.html)
- [Tutorial Matplotlib](https://matplotlib.org/stable/tutorials/index.html)

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🔄 Kembali ke Daftar Isi
[Klik di sini untuk kembali ke Daftar Isi](#-daftar-isi)
