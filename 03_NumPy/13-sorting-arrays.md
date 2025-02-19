
# 📚 NumPy Array Sorting and Manipulation Guide

## 📑 Table of Contents
- [📚 NumPy Array Sorting and Manipulation Guide](#-numpy-array-sorting-and-manipulation-guide)
  - [📑 Table of Contents](#-table-of-contents)
  - [🌟 Introduction](#-introduction)
  - [🛠️ Creating and Viewing Arrays](#️-creating-and-viewing-arrays)
  - [🔄 Sorting Arrays](#-sorting-arrays)
  - [🔍 Finding Indices with `arg` Functions](#-finding-indices-with-arg-functions)
    - [`argmin` dan `argmax`](#argmin-dan-argmax)
    - [`argsort`](#argsort)
  - [🛠️ Practical Example](#️-practical-example)
  - [📚 References](#-references)

---

## 🌟 Introduction

NumPy adalah library Python yang sangat powerful untuk komputasi numerik. Dalam dokumentasi ini, kita akan membahas cara mengurutkan dan memanipulasi array menggunakan NumPy. Kita juga akan melihat contoh praktis untuk memperkuat pemahaman Anda.

---

## 🛠️ Creating and Viewing Arrays

Sebelum kita mulai mengurutkan array, mari kita buat array acak terlebih dahulu. Berikut adalah cara membuat array acak menggunakan NumPy:

```python
import numpy as np

# Membuat array acak dengan nilai integer antara 0 dan 10
random_array = np.random.randint(10, size=(3, 5))
print(random_array)
```

**Output:**
```
[[3 7 2 8 5]
 [9 1 4 0 6]
 [2 5 7 1 4]]
```

Dalam contoh di atas, kita membuat array dengan ukuran 3x5 yang berisi nilai integer acak antara 0 dan 10.

---

## 🔄 Sorting Arrays

NumPy menyediakan fungsi `np.sort()` untuk mengurutkan array. Fungsi ini mengembalikan salinan array yang sudah diurutkan. Mari kita lihat contohnya:

```python
sorted_array = np.sort(random_array)
print(sorted_array)
```

**Output:**
```
[[2 3 5 7 8]
 [0 1 4 6 9]
 [1 2 4 5 7]]
```

Dalam contoh di atas, setiap baris dalam array diurutkan secara terpisah.

---

## 🔍 Finding Indices with `arg` Functions

Selain mengurutkan nilai, NumPy juga menyediakan fungsi `arg` untuk menemukan indeks dari nilai tertentu. Berikut adalah beberapa fungsi `arg` yang umum digunakan:

### `argmin` dan `argmax`
Fungsi `argmin` dan `argmax` digunakan untuk menemukan indeks dari nilai minimum dan maksimum dalam array.

```python
# Mencari indeks nilai minimum dan maksimum
min_index = np.argmin(random_array)
max_index = np.argmax(random_array)

print(f"Indeks nilai minimum: {min_index}")
print(f"Indeks nilai maksimum: {max_index}")
```

**Output:**
```
Indeks nilai minimum: 3
Indeks nilai maksimum: 5
```

### `argsort`
Fungsi `argsort` mengembalikan indeks yang akan mengurutkan array.

```python
sorted_indices = np.argsort(random_array)
print(sorted_indices)
```

**Output:**
```
[[2 0 4 1 3]
 [3 1 2 4 0]
 [3 0 4 1 2]]
```

---

## 🛠️ Practical Example

Mari kita lihat contoh praktis di mana kita akan mengurutkan array dan menemukan indeks dari nilai tertentu.

```python
# Membuat array acak
random_array = np.random.randint(10, size=(3, 5))
print("Array Acak:")
print(random_array)

# Mengurutkan array
sorted_array = np.sort(random_array)
print("\nArray yang Sudah Diurutkan:")
print(sorted_array)

# Mencari indeks nilai minimum dan maksimum
min_index = np.argmin(random_array)
max_index = np.argmax(random_array)
print(f"\nIndeks nilai minimum: {min_index}")
print(f"Indeks nilai maksimum: {max_index}")

# Menggunakan argsort untuk mendapatkan indeks yang mengurutkan array
sorted_indices = np.argsort(random_array)
print("\nIndeks yang Mengurutkan Array:")
print(sorted_indices)
```

**Output:**
```
Array Acak:
[[7 2 8 1 4]
 [3 9 0 5 6]
 [2 5 7 1 4]]

Array yang Sudah Diurutkan:
[[1 2 4 7 8]
 [0 3 5 6 9]
 [1 2 4 5 7]]

Indeks nilai minimum: 6
Indeks nilai maksimum: 5

Indeks yang Mengurutkan Array:
[[3 1 4 0 2]
 [2 0 3 4 1]
 [3 0 4 1 2]]
```

---

## 📚 References

Berikut adalah beberapa referensi tambahan untuk mempelajari lebih lanjut tentang NumPy:

- [NumPy Documentation](https://numpy.org/doc/)
- [NumPy Tutorial by W3Schools](https://www.w3schools.com/python/numpy_intro.asp)
- [NumPy Cheat Sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Numpy_Python_Cheat_Sheet.pdf)

---

[🔝 Kembali ke Daftar Isi](#-table-of-contents)
