
# 📚 Panduan Lengkap untuk Manipulasi Array dan Matriks dengan NumPy 🧮

Selamat datang di dokumentasi ini! Di sini, kita akan membahas secara mendalam tentang cara memanipulasi dan melihat array serta matriks menggunakan library NumPy dalam Python. Dokumen ini dirancang untuk menjadi referensi lengkap yang mudah diakses, dengan penjelasan mendalam, contoh kode praktis, dan tautan referensi yang berguna.

## 📑 Daftar Isi
- [📚 Panduan Lengkap untuk Manipulasi Array dan Matriks dengan NumPy 🧮](#-panduan-lengkap-untuk-manipulasi-array-dan-matriks-dengan-numpy-)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🌟 Pengenalan](#-pengenalan)
  - [🔍 Mencari Elemen Unik dalam Array](#-mencari-elemen-unik-dalam-array)
    - [Contoh Kode:](#contoh-kode)
    - [Penjelasan:](#penjelasan)
  - [👀 Melihat Array dan Matriks](#-melihat-array-dan-matriks)
    - [Contoh Kode:](#contoh-kode-1)
    - [Penjelasan:](#penjelasan-1)
  - [🔪 Indexing dan Slicing Array](#-indexing-dan-slicing-array)
    - [Contoh Kode:](#contoh-kode-2)
    - [Penjelasan:](#penjelasan-2)
  - [🤖 Manipulasi Array untuk Machine Learning](#-manipulasi-array-untuk-machine-learning)
    - [Contoh Kode:](#contoh-kode-3)
    - [Penjelasan:](#penjelasan-3)
  - [📖 Referensi](#-referensi)

---

## 🌟 Pengenalan

NumPy adalah library Python yang sangat populer untuk komputasi numerik. Library ini menyediakan struktur data yang efisien seperti array dan matriks, serta fungsi-fungsi untuk melakukan operasi matematika yang kompleks. Dalam dokumentasi ini, kita akan fokus pada cara memanipulasi dan melihat array serta matriks menggunakan NumPy, yang merupakan keterampilan penting dalam Machine Learning.

---

## 🔍 Mencari Elemen Unik dalam Array

Salah satu operasi dasar yang sering dilakukan dalam analisis data adalah mencari elemen unik dalam sebuah array. NumPy menyediakan fungsi `np.unique()` untuk melakukan hal ini.

### Contoh Kode:
```python
import numpy as np

# Membuat array acak dengan bilangan bulat antara 0 dan 9
random_array = np.random.randint(10, size=(5, 3))

# Mencari elemen unik dalam array
unique_elements = np.unique(random_array)

print("Array Acak:")
print(random_array)
print("\nElemen Unik:")
print(unique_elements)
```

### Penjelasan:
- `np.random.randint(10, size=(5, 3))`: Membuat array 5x3 dengan bilangan bulat acak antara 0 dan 9.
- `np.unique(random_array)`: Mengembalikan array yang berisi elemen unik dari `random_array`.

---

## 👀 Melihat Array dan Matriks

Memahami struktur array dan matriks adalah kunci untuk bekerja dengan data multidimensi. NumPy memungkinkan kita untuk melihat elemen-elemen tertentu dalam array menggunakan indexing dan slicing.

### Contoh Kode:
```python
# Membuat array multidimensi
a3 = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])

# Melihat elemen pertama dari array
print("Elemen pertama dari a3:")
print(a3[0])

# Melihat baris pertama dari matriks dalam array
print("\nBaris pertama dari matriks dalam a3:")
print(a3[0, 0])
```

### Penjelasan:
- `a3[0]`: Mengembalikan elemen pertama dari array `a3`, yang merupakan matriks 2x3.
- `a3[0, 0]`: Mengembalikan baris pertama dari matriks pertama dalam array `a3`.

---

## 🔪 Indexing dan Slicing Array

Indexing dan slicing adalah teknik yang sangat berguna untuk mengambil bagian tertentu dari array. NumPy mendukung slicing yang mirip dengan Python, tetapi dengan kemampuan untuk bekerja dengan array multidimensi.

### Contoh Kode:
```python
# Membuat array 4 dimensi
a4 = np.random.randint(10, size=(2, 3, 4, 5))

# Mengambil 4 angka pertama dari dimensi terdalam
sliced_array = a4[:, :, :, :4]

print("Array 4 Dimensi:")
print(a4)
print("\nArray Setelah Slicing:")
print(sliced_array)
```

### Penjelasan:
- `a4[:, :, :, :4]`: Mengambil 4 angka pertama dari dimensi terdalam dalam array 4 dimensi `a4`.

---

## 🤖 Manipulasi Array untuk Machine Learning

Manipulasi array adalah inti dari banyak algoritma Machine Learning. Dengan memahami cara memanipulasi array, kita dapat mempersiapkan data untuk model Machine Learning dengan lebih efektif.

### Contoh Kode:
```python
from sklearn.model_selection import train_test_split

# Membuat dataset sederhana
X = np.random.rand(100, 5)  # 100 sampel, 5 fitur
y = np.random.randint(2, size=100)  # Label biner

# Membagi dataset menjadi data latih dan data uji
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

print("Data Latih:")
print(X_train)
print("\nData Uji:")
print(X_test)
```

### Penjelasan:
- `train_test_split(X, y, test_size=0.2, random_state=42)`: Membagi dataset menjadi data latih dan data uji dengan rasio 80:20.

---

## 📖 Referensi

Berikut adalah beberapa referensi tambahan yang dapat membantu Anda memahami lebih dalam tentang NumPy dan Machine Learning:

1. [Dokumentasi Resmi NumPy](https://numpy.org/doc/)
2. [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
3. [Scikit-Learn Documentation](https://scikit-learn.org/stable/)
4. [StackOverflow - NumPy](https://stackoverflow.com/questions/tagged/numpy)

