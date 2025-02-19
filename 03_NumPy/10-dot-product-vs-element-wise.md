# 📚 Panduan Lengkap: Dot Product dan Transpose dalam Machine Learning 🧮

## 📑 Daftar Isi
- [📚 Panduan Lengkap: Dot Product dan Transpose dalam Machine Learning 🧮](#-panduan-lengkap-dot-product-dan-transpose-dalam-machine-learning-)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🌟 Pengenalan](#-pengenalan)
  - [🔍 Apa Itu Dot Product?](#-apa-itu-dot-product)
    - [Rumus Dot Product](#rumus-dot-product)
  - [🛠 Implementasi Dot Product dengan NumPy](#-implementasi-dot-product-dengan-numpy)
    - [Penjelasan Kode:](#penjelasan-kode)
  - [🔄 Transpose Matriks](#-transpose-matriks)
    - [Contoh Transpose](#contoh-transpose)
  - [🧪 Praktik: Dot Product dengan Transpose](#-praktik-dot-product-dengan-transpose)
    - [Hasil:](#hasil)
  - [📖 Referensi](#-referensi)

---

## 🌟 Pengenalan

Dalam dunia Machine Learning, operasi matriks seperti **dot product** dan **transpose** sangat penting. Operasi ini membantu kita dalam menemukan pola dan hubungan antara data. Dalam dokumentasi ini, kita akan membahas secara mendalam tentang dot product dan transpose, serta bagaimana mengimplementasikannya menggunakan Python dan NumPy.

---

## 🔍 Apa Itu Dot Product?

Dot product (atau produk titik) adalah operasi matematika yang dilakukan antara dua vektor atau matriks. Operasi ini menghasilkan skalar atau matriks baru, tergantung pada dimensi input. Dot product sering digunakan dalam Machine Learning untuk menghitung kesamaan antara dua set data.

### Rumus Dot Product
Untuk dua vektor **A** dan **B**, dot product dihitung sebagai:
\[ A \cdot B = \sum_{i=1}^{n} A_i \times B_i \]

Untuk matriks, dot product dilakukan dengan mengalikan baris matriks pertama dengan kolom matriks kedua.

---

## 🛠 Implementasi Dot Product dengan NumPy

NumPy menyediakan fungsi `np.dot()` untuk melakukan dot product. Berikut adalah contoh implementasinya:

```python
import numpy as np

# Membuat dua matriks acak
mat1 = np.random.randint(10, size=(5, 3))
mat2 = np.random.randint(10, size=(5, 3))

# Melakukan dot product
dot_product = np.dot(mat1, mat2.T)  # Transpose mat2 untuk mencocokkan dimensi
print("Dot Product:\n", dot_product)
```

### Penjelasan Kode:
1. **Membuat Matriks**: `np.random.randint()` digunakan untuk membuat matriks dengan nilai acak.
2. **Dot Product**: `np.dot()` menghitung dot product antara dua matriks. Karena dimensi mat1 dan mat2 tidak cocok, kita melakukan transpose pada mat2 (`mat2.T`).

---

## 🔄 Transpose Matriks

Transpose adalah operasi yang membalik sumbu matriks. Misalnya, jika matriks A memiliki dimensi (m, n), maka transpose-nya (A.T) akan memiliki dimensi (n, m).

### Contoh Transpose
```python
mat1 = np.random.randint(10, size=(5, 3))
mat1_transpose = mat1.T
print("Matriks Asli:\n", mat1)
print("Matriks Transpose:\n", mat1_transpose)
```

---

## 🧪 Praktik: Dot Product dengan Transpose

Berikut adalah contoh lengkap penggunaan dot product dan transpose:

```python
import numpy as np

# Membuat dua matriks acak
mat1 = np.random.randint(10, size=(5, 3))
mat2 = np.random.randint(10, size=(5, 3))

# Melakukan transpose pada mat2
mat2_transpose = mat2.T

# Melakukan dot product
dot_product = np.dot(mat1, mat2_transpose)
print("Dot Product dengan Transpose:\n", dot_product)
```

### Hasil:
Operasi ini menghasilkan matriks baru dengan dimensi (5, 5), sesuai dengan aturan dot product.

---

## 📖 Referensi

1. [NumPy Documentation: Dot Product](https://numpy.org/doc/stable/reference/generated/numpy.dot.html)
2. [Matrix Multiplication Explained](https://www.mathsisfun.com/algebra/matrix-multiplying.html)
3. [Interactive Matrix Multiplication Demo](https://matrixmultiplication.xyz/)

---

[🔝 Kembali ke Daftar Isi](#-daftar-isi)
