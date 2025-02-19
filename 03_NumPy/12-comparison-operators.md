
# 📚 Manipulating and Comparing Arrays in NumPy

## 📑 Table of Contents
- [📚 Manipulating and Comparing Arrays in NumPy](#-manipulating-and-comparing-arrays-in-numpy)
  - [📑 Table of Contents](#-table-of-contents)
  - [🌟 Introduction](#-introduction)
  - [🔍 Comparison Operators in NumPy](#-comparison-operators-in-numpy)
  - [🛠️ Practical Examples](#️-practical-examples)
    - [Contoh 1: Membandingkan Dua Array](#contoh-1-membandingkan-dua-array)
    - [Contoh 2: Membandingkan Array dengan Skalar](#contoh-2-membandingkan-array-dengan-skalar)
    - [Contoh 3: Mengecek Kesamaan Dua Array](#contoh-3-mengecek-kesamaan-dua-array)
  - [🧮 Boolean Arrays](#-boolean-arrays)
  - [🚀 Advanced Comparison Operators](#-advanced-comparison-operators)
    - [Contoh Penggunaan `np.all()` dan `np.any()`](#contoh-penggunaan-npall-dan-npany)
  - [📖 References](#-references)
  - [🔙 Back to Table of Contents](#-back-to-table-of-contents)

---

## 🌟 Introduction

Dalam video ini, kita akan membahas cara memanipulasi dan membandingkan array menggunakan NumPy. NumPy adalah library Python yang sangat populer untuk komputasi numerik, dan salah satu fitur utamanya adalah kemampuannya untuk bekerja dengan array multidimensi. Dalam konteks ini, kita akan fokus pada penggunaan operator perbandingan untuk membandingkan elemen-elemen dalam array.

---

## 🔍 Comparison Operators in NumPy

Operator perbandingan dalam NumPy mirip dengan yang digunakan dalam Python standar. Operator ini memungkinkan kita untuk membandingkan elemen-elemen dalam array dan menghasilkan array boolean yang menunjukkan hasil perbandingan tersebut. Beberapa operator perbandingan yang umum digunakan antara lain:

- `>` (lebih besar dari)
- `<` (lebih kecil dari)
- `>=` (lebih besar dari atau sama dengan)
- `<=` (lebih kecil dari atau sama dengan)
- `==` (sama dengan)
- `!=` (tidak sama dengan)

---

## 🛠️ Practical Examples

Mari kita lihat beberapa contoh praktis penggunaan operator perbandingan dalam NumPy.

### Contoh 1: Membandingkan Dua Array

```python
import numpy as np

a1 = np.array([1, 2, 3, 4, 5])
a2 = np.array([1, 2, 3.3, 4, 5])

# Membandingkan elemen a1 dengan a2
result = a1 > a2
print(result)  # Output: [False False False False False]
```

### Contoh 2: Membandingkan Array dengan Skalar

```python
# Membandingkan elemen a1 dengan skalar 5
result = a1 > 5
print(result)  # Output: [False False False False False]
```

### Contoh 3: Mengecek Kesamaan Dua Array

```python
# Mengecek apakah elemen a1 sama dengan elemen a2
result = a1 == a2
print(result)  # Output: [ True  True False  True  True]
```

---

## 🧮 Boolean Arrays

Ketika kita menggunakan operator perbandingan pada array NumPy, hasilnya adalah array boolean. Array ini berisi nilai `True` atau `False` yang menunjukkan hasil perbandingan untuk setiap elemen.

```python
# Membuat array boolean
bool_array = a1 >= a2
print(bool_array)  # Output: [ True  True False  True  True]

# Mengecek tipe data dari array boolean
print(type(bool_array))  # Output: <class 'numpy.ndarray'>
print(bool_array.dtype)  # Output: bool
```

---

## 🚀 Advanced Comparison Operators

Selain operator perbandingan dasar, NumPy juga menyediakan fungsi-fungsi logika yang dapat digunakan untuk melakukan operasi yang lebih kompleks pada array boolean. Beberapa fungsi tersebut antara lain:

- `np.all()`: Mengembalikan `True` jika semua elemen dalam array adalah `True`.
- `np.any()`: Mengembalikan `True` jika setidaknya satu elemen dalam array adalah `True`.

### Contoh Penggunaan `np.all()` dan `np.any()`

```python
# Mengecek apakah semua elemen dalam array boolean adalah True
all_true = np.all(bool_array)
print(all_true)  # Output: False

# Mengecek apakah setidaknya satu elemen dalam array boolean adalah True
any_true = np.any(bool_array)
print(any_true)  # Output: True
```

---

## 📖 References

Berikut adalah beberapa referensi tambahan yang dapat membantu Anda memahami lebih dalam tentang manipulasi dan perbandingan array dalam NumPy:

- [NumPy Documentation: Comparison Operators](https://numpy.org/doc/stable/reference/routines.logic.html)
- [Python Data Science Handbook: NumPy Basics](https://jakevdp.github.io/PythonDataScienceHandbook/02.02-the-basics-of-numpy-arrays.html)
- [NumPy Tutorial: Array Manipulation](https://numpy.org/doc/stable/user/basics.creation.html)

---

## 🔙 Back to Table of Contents

[Kembali ke Daftar Isi](#-table-of-contents)
