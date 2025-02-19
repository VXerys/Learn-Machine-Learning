
# 🐼 NumPy in Action: Turning Images into Numbers for Machine Learning 🚗🐶

## 📚 Table of Contents
- [🐼 NumPy in Action: Turning Images into Numbers for Machine Learning 🚗🐶](#-numpy-in-action-turning-images-into-numbers-for-machine-learning-)
  - [📚 Table of Contents](#-table-of-contents)
  - [🌟 Introduction](#-introduction)
  - [🤔 Why NumPy in Machine Learning?](#-why-numpy-in-machine-learning)
  - [🛠️ Practical Example: Turning Images into NumPy Arrays](#️-practical-example-turning-images-into-numpy-arrays)
    - [Step 1: Importing Libraries](#step-1-importing-libraries)
    - [Step 2: Loading an Image as a NumPy Array](#step-2-loading-an-image-as-a-numpy-array)
    - [Step 3: Exploring the NumPy Array](#step-3-exploring-the-numpy-array)
    - [Step 4: Applying NumPy Functions](#step-4-applying-numpy-functions)
  - [💻 Code Implementation in Jupyter Notebook](#-code-implementation-in-jupyter-notebook)
  - [🎯 Conclusion](#-conclusion)
  - [📖 References](#-references)

---

## 🌟 Introduction

NumPy adalah salah satu library paling penting dalam Python, terutama dalam bidang *Machine Learning*. Library ini memungkinkan kita untuk melakukan operasi matematika yang kompleks dengan mudah dan efisien. Dalam video ini, kita akan melihat bagaimana NumPy dapat digunakan untuk mengubah gambar menjadi array numerik, yang merupakan langkah penting dalam proses *Machine Learning*.

---

## 🤔 Why NumPy in Machine Learning?

Dalam *Machine Learning*, data yang kita miliki harus diubah menjadi bentuk numerik agar dapat diproses oleh algoritma. NumPy sangat cocok untuk tugas ini karena kemampuannya dalam menangani array multidimensi dan operasi matematika yang cepat. Dengan NumPy, kita dapat mengubah gambar, teks, atau data lainnya menjadi array numerik yang siap digunakan untuk analisis dan pemodelan.

---

## 🛠️ Practical Example: Turning Images into NumPy Arrays

### Step 1: Importing Libraries

Pertama, kita perlu mengimpor library yang diperlukan, yaitu NumPy dan Matplotlib. Matplotlib digunakan untuk membaca gambar dan mengubahnya menjadi array NumPy.

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.image import imread
```

### Step 2: Loading an Image as a NumPy Array

Kita akan menggunakan fungsi `imread` dari Matplotlib untuk membaca gambar dan mengubahnya menjadi array NumPy. Misalnya, kita memiliki gambar panda yang disimpan dalam folder `images`.

```python
panda_image = imread('images/panda.png')
```

### Step 3: Exploring the NumPy Array

Setelah gambar diubah menjadi array NumPy, kita dapat menjelajahi atributnya seperti bentuk (`shape`), ukuran (`size`), dan dimensi (`ndim`).

```python
print("Shape of the array:", panda_image.shape)
print("Size of the array:", panda_image.size)
print("Number of dimensions:", panda_image.ndim)
```

### Step 4: Applying NumPy Functions

Kita dapat menggunakan berbagai fungsi NumPy untuk memanipulasi array ini. Misalnya, kita dapat mengubah nilai piksel atau melakukan operasi matematika pada array.

```python
# Mengubah nilai piksel pada array
panda_image[100:150, 100:150] = [255, 0, 0]  # Mengubah area tertentu menjadi merah

# Menampilkan gambar yang telah dimodifikasi
plt.imshow(panda_image)
plt.show()
```

---

## 💻 Code Implementation in Jupyter Notebook

Berikut adalah contoh lengkap kode yang dapat dijalankan di Jupyter Notebook:

```python
# Import libraries
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.image import imread

# Load an image as a NumPy array
panda_image = imread('images/panda.png')

# Explore the array
print("Shape of the array:", panda_image.shape)
print("Size of the array:", panda_image.size)
print("Number of dimensions:", panda_image.ndim)

# Modify the array
panda_image[100:150, 100:150] = [255, 0, 0]  # Change a specific area to red

# Display the modified image
plt.imshow(panda_image)
plt.show()
```

---

## 🎯 Conclusion

NumPy adalah alat yang sangat kuat untuk mengubah data menjadi bentuk numerik, yang merupakan langkah penting dalam *Machine Learning*. Dengan memahami cara kerja NumPy, kita dapat memanipulasi dan menganalisis data dengan lebih efektif. Jangan khawatir jika tidak semua konsep langsung dipahami, karena praktik dan eksperimen adalah kunci untuk menguasai NumPy.

[🔝 Kembali ke Daftar Isi](#-table-of-contents)

---

## 📖 References

- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Machine Learning Mastery: NumPy for Machine Learning](https://machinelearningmastery.com/numpy-for-machine-learning/)

[🔝 Kembali ke Daftar Isi](#-table-of-contents)
