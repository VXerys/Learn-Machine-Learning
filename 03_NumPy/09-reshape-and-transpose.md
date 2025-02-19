
# 📚 NumPy Array Manipulation: Reshaping and Transposing

## 📑 Table of Contents
- [📚 NumPy Array Manipulation: Reshaping and Transposing](#-numpy-array-manipulation-reshaping-and-transposing)
  - [📑 Table of Contents](#-table-of-contents)
  - [🌟 Introduction](#-introduction)
  - [❓ Why Reshape Arrays?](#-why-reshape-arrays)
  - [🔧 Reshaping Arrays in NumPy](#-reshaping-arrays-in-numpy)
    - [Contoh Kode:](#contoh-kode)
  - [📏 Broadcasting Rules](#-broadcasting-rules)
    - [Contoh:](#contoh)
  - [🛠️ Practical Example: Reshaping for Broadcasting](#️-practical-example-reshaping-for-broadcasting)
    - [Contoh Kode:](#contoh-kode-1)
  - [🔄 Transposing Arrays](#-transposing-arrays)
    - [Contoh Kode:](#contoh-kode-2)
  - [🔄 vs 🔧 Difference Between Reshape and Transpose](#-vs--difference-between-reshape-and-transpose)
    - [Contoh Perbandingan:](#contoh-perbandingan)
  - [🎯 Conclusion](#-conclusion)
  - [📚 References](#-references)

---

## 🌟 Introduction
Dalam dunia *Machine Learning*, data seringkali perlu diatur dalam bentuk tertentu agar dapat diproses dengan benar oleh algoritma. Salah satu cara untuk mengatur data adalah dengan mengubah bentuk (*reshape*) atau mentranspos (*transpose*) array menggunakan library NumPy. Dokumen ini akan menjelaskan secara mendetail cara melakukan kedua operasi tersebut beserta contoh praktisnya.

---

## ❓ Why Reshape Arrays?
Dalam *Machine Learning*, data yang dimasukkan ke dalam algoritma harus memiliki bentuk yang sesuai. Misalnya, jika Anda memiliki data dalam bentuk array 2D, tetapi algoritma memerlukan data dalam bentuk 3D, Anda perlu mengubah bentuk array tersebut. Reshaping memungkinkan Anda untuk mengatur ulang data tanpa mengubah isinya.

---

## 🔧 Reshaping Arrays in NumPy
NumPy menyediakan metode `reshape` untuk mengubah bentuk array. Metode ini mengembalikan array baru dengan bentuk yang diinginkan, tetapi data asli tetap sama.

### Contoh Kode:
```python
import numpy as np

# Membuat array 2D
a = np.array([[1, 2, 3], [4, 5, 6]])
print("Array Awal:\n", a)
print("Bentuk Awal:", a.shape)

# Mengubah bentuk array menjadi 3D
a_reshaped = a.reshape(2, 3, 1)
print("Array Setelah Reshape:\n", a_reshaped)
print("Bentuk Baru:", a_reshaped.shape)
```

---

## 📏 Broadcasting Rules
*Broadcasting* adalah aturan dalam NumPy yang memungkinkan operasi aritmatika antara array dengan bentuk yang berbeda. Aturan utamanya adalah:
1. Dimensi array harus sama, atau
2. Salah satu dimensi harus bernilai 1.

### Contoh:
```python
b = np.array([1, 2, 3])
print("Array B:\n", b)
print("Bentuk B:", b.shape)

# Reshape array b agar sesuai dengan aturan broadcasting
b_reshaped = b.reshape(1, 3)
print("Array B Setelah Reshape:\n", b_reshaped)
print("Bentuk Baru B:", b_reshaped.shape)

# Operasi perkalian dengan broadcasting
result = a * b_reshaped
print("Hasil Perkalian:\n", result)
```

---

## 🛠️ Practical Example: Reshaping for Broadcasting
Misalkan Anda memiliki dua array dengan bentuk yang tidak kompatibel. Dengan menggunakan `reshape`, Anda dapat membuatnya kompatibel untuk operasi aritmatika.

### Contoh Kode:
```python
# Array dengan bentuk (2, 3)
a2 = np.array([[1, 2, 3], [4, 5, 6]])

# Array dengan bentuk (2, 3, 3)
a3 = np.array([[[1, 2, 3], [4, 5, 6], [7, 8, 9]], 
               [[10, 11, 12], [13, 14, 15], [16, 17, 18]]])

# Reshape a2 menjadi (2, 3, 1) agar kompatibel dengan a3
a2_reshaped = a2.reshape(2, 3, 1)

# Operasi perkalian dengan broadcasting
result = a2_reshaped * a3
print("Hasil Perkalian:\n", result)
```

---

## 🔄 Transposing Arrays
Transpose adalah operasi yang menukar baris dan kolom dari sebuah array. Dalam NumPy, Anda dapat menggunakan atribut `.T` atau metode `transpose()` untuk melakukan ini.

### Contoh Kode:
```python
# Array awal
a = np.array([[1, 2, 3], [4, 5, 6]])
print("Array Awal:\n", a)
print("Bentuk Awal:", a.shape)

# Transpose array
a_transposed = a.T
print("Array Setelah Transpose:\n", a_transposed)
print("Bentuk Baru:", a_transposed.shape)
```

---

## 🔄 vs 🔧 Difference Between Reshape and Transpose
- **Reshape**: Mengubah bentuk array tanpa mengubah urutan data.
- **Transpose**: Menukar baris dan kolom array.

### Contoh Perbandingan:
```python
# Reshape
a_reshaped = a.reshape(3, 2)
print("Reshape:\n", a_reshaped)

# Transpose
a_transposed = a.T
print("Transpose:\n", a_transposed)
```

---

## 🎯 Conclusion
Mengubah bentuk dan mentranspos array adalah keterampilan penting dalam *Machine Learning*. Dengan memahami cara menggunakan `reshape` dan `transpose`, Anda dapat memastikan data Anda sesuai dengan persyaratan algoritma yang digunakan. Praktikkan contoh-contoh di atas untuk memperdalam pemahaman Anda.

[🔝 Kembali ke Daftar Isi](#table-of-contents)

---

## 📚 References
- [NumPy Documentation](https://numpy.org/doc/)
- [Broadcasting in NumPy](https://numpy.org/doc/stable/user/basics.broadcasting.html)
- [Reshape vs Transpose](https://stackoverflow.com/questions/32034237/reshape-vs-transpose-in-numpy)

[🔝 Kembali ke Daftar Isi](#table-of-contents)
