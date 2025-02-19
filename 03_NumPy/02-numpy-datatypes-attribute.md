
# 📚 Dokumentasi: Pengenalan NumPy untuk Machine Learning

## 📑 Daftar Isi
- [📚 Dokumentasi: Pengenalan NumPy untuk Machine Learning](#-dokumentasi-pengenalan-numpy-untuk-machine-learning)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🌟 Pendahuluan](#-pendahuluan)
  - [🛠 Menyiapkan Lingkungan](#-menyiapkan-lingkungan)
  - [📓 Membuat Jupyter Notebook](#-membuat-jupyter-notebook)
  - [📥 Mengimpor NumPy](#-mengimpor-numpy)
  - [🧮 Tipe Data dan Atribut NumPy](#-tipe-data-dan-atribut-numpy)
  - [📐 Anatomi Array NumPy](#-anatomi-array-numpy)
  - [🔍 Atribut Array NumPy](#-atribut-array-numpy)
  - [🗂 Membuat DataFrame dari Array NumPy](#-membuat-dataframe-dari-array-numpy)
  - [📖 Referensi](#-referensi)

---

## 🌟 Pendahuluan
NumPy adalah salah satu library paling penting dalam ekosistem Python untuk komputasi numerik, terutama dalam bidang Machine Learning. Library ini menyediakan struktur data yang efisien untuk bekerja dengan array multidimensi dan berbagai fungsi untuk memanipulasi data tersebut. Dalam dokumentasi ini, kita akan mempelajari dasar-dasar NumPy, mulai dari menyiapkan lingkungan hingga memahami tipe data dan atributnya.

---

## 🛠 Menyiapkan Lingkungan
Sebelum memulai, pastikan Anda telah menginstal Anaconda atau Miniconda untuk mengelola lingkungan Python. Berikut langkah-langkahnya:

1. Buka terminal atau command prompt.
2. Navigasikan ke direktori proyek Anda:
   ```bash
   cd /path/to/your/project
   ```
3. Aktifkan lingkungan yang telah Anda buat:
   ```bash
   conda activate nama_lingkungan
   ```

---

## 📓 Membuat Jupyter Notebook
Jupyter Notebook adalah alat yang sangat berguna untuk eksplorasi data dan pengembangan kode Python. Berikut cara membuatnya:

1. Setelah mengaktifkan lingkungan, jalankan Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Di dashboard Jupyter, buat notebook baru dengan memilih `New > Python 3`.
3. Ubah nama notebook menjadi `Introduction_to_NumPy`.

---

## 📥 Mengimpor NumPy
Langkah pertama dalam menggunakan NumPy adalah mengimpornya ke dalam notebook Anda. Gunakan kode berikut:

```python
import numpy as np
```
Di sini, `np` adalah alias yang umum digunakan untuk NumPy, sehingga kita tidak perlu mengetik `numpy` setiap kali.

---

## 🧮 Tipe Data dan Atribut NumPy
NumPy memiliki satu tipe data utama, yaitu `ndarray` (n-dimensional array). Array ini dapat berupa vektor (1D), matriks (2D), atau array multidimensi (nD). Berikut contoh pembuatan array:

```python
a1 = np.array([1, 2, 3])
a2 = np.array([[1, 2, 3], [4, 5, 6]])
a3 = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])
```

---

## 📐 Anatomi Array NumPy
Setiap array NumPy memiliki bentuk (shape) yang menggambarkan dimensinya. Misalnya:
- `a1` memiliki bentuk `(3,)` (vektor 1D).
- `a2` memiliki bentuk `(2, 3)` (matriks 2D).
- `a3` memiliki bentuk `(2, 2, 3)` (array 3D).

---

## 🔍 Atribut Array NumPy
NumPy menyediakan beberapa atribut untuk memeriksa properti array:

1. **Shape**: Menampilkan dimensi array.
   ```python
   print(a1.shape)  # Output: (3,)
   ```
2. **ndim**: Menampilkan jumlah dimensi.
   ```python
   print(a2.ndim)  # Output: 2
   ```
3. **dtype**: Menampilkan tipe data elemen array.
   ```python
   print(a2.dtype)  # Output: int64
   ```
4. **size**: Menampilkan jumlah total elemen.
   ```python
   print(a3.size)  # Output: 12
   ```

---

## 🗂 Membuat DataFrame dari Array NumPy
NumPy adalah dasar dari banyak library Python, termasuk Pandas. Anda dapat mengonversi array NumPy menjadi DataFrame Pandas:

```python
import pandas as pd
df = pd.DataFrame(a2)
print(df)
```

---

## 📖 Referensi
- [Dokumentasi Resmi NumPy](https://numpy.org/doc/)
- [Panduan Pandas untuk Pemula](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)
- [Tutorial Jupyter Notebook](https://jupyter.org/try)

---

🔙 [Kembali ke Daftar Isi](#-daftar-isi)