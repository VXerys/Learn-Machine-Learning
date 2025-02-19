
# 📚 Dokumentasi Lengkap: Manipulasi dan Perbandingan Array dengan NumPy dalam Machine Learning

## 📑 Daftar Isi
1. [Pendahuluan](#-pendahuluan)
2. [Manipulasi Array dengan Operasi Aritmatika](#-manipulasi-array-dengan-operasi-aritmatika)
3. [Broadcasting dalam NumPy](#-broadcasting-dalam-numpy)
4. [Praktik: Implementasi Kode](#-praktik-implementasi-kode)
5. [Referensi](#-referensi)
6. [Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🌟 Pendahuluan
NumPy adalah library Python yang sangat penting untuk komputasi numerik, terutama dalam Machine Learning. Dalam video ini, kita akan mempelajari cara memanipulasi dan membandingkan array menggunakan NumPy. Operasi ini merupakan inti dari Machine Learning, di mana kita melakukan perhitungan dan menemukan pola dalam array angka.

---

## ➕ Manipulasi Array dengan Operasi Aritmatika
NumPy menyediakan berbagai operasi aritmatika yang dapat dilakukan pada array. Berikut adalah beberapa contoh operasi dasar:

### 1. Penjumlahan Array
```python
import numpy as np

a1 = np.array([1, 2, 3])
ones = np.ones(3)

result = a1 + ones
print(result)  # Output: [2. 3. 4.]
```

### 2. Pengurangan Array
```python
result = a1 - ones
print(result)  # Output: [0. 1. 2.]
```

### 3. Perkalian Array
```python
result = a1 * ones
print(result)  # Output: [1. 2. 3.]
```

### 4. Pembagian Array
```python
result = a1 / ones
print(result)  # Output: [1. 2. 3.]
```

### 5. Floor Division
```python
a2 = np.array([1, 2, 3.3])
result = a2 // a1
print(result)  # Output: [1. 1. 1.]
```

### 6. Modulo
```python
result = a1 % 2
print(result)  # Output: [1 0 1]
```

### 7. Pangkat
```python
result = a2 ** 2
print(result)  # Output: [1.   4.  10.89]
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📡 Broadcasting dalam NumPy
Broadcasting adalah teknik NumPy untuk melakukan operasi aritmatika pada array dengan bentuk (shape) yang berbeda. Berikut adalah penjelasan dan contohnya:

### 1. Aturan Broadcasting
- Dua dimensi kompatibel jika keduanya sama atau salah satunya adalah 1.
- NumPy membandingkan bentuk array dari dimensi terakhir ke depan.

### 2. Contoh Broadcasting
```python
a1 = np.array([1, 2, 3])  # Shape: (3,)
a2 = np.array([[1, 2, 3], [4, 5, 6]])  # Shape: (2, 3)

result = a1 + a2
print(result)  # Output: [[2 4 6], [5 7 9]]
```

### 3. Kesalahan Broadcasting
Jika bentuk array tidak kompatibel, NumPy akan menghasilkan error:
```python
a3 = np.array([[1, 2], [3, 4]])  # Shape: (2, 2)
try:
    result = a1 + a3
except ValueError as e:
    print(e)  # Output: operands could not be broadcast together with shapes (3,) (2,2)
```

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
