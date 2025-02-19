
# 📚 Panduan Lengkap NumPy untuk Ilmu Data dan Pembelajaran Mesin

## 📑 Daftar Isi
1. [Pengenalan NumPy](#-pengenalan-numpy)  
2. [Mengapa Menggunakan NumPy?](#-mengapa-menggunakan-numpy)  
3. [Fitur Utama NumPy](#-fitur-utama-numpy)  
4. [Praktik Langsung dengan NumPy](#-praktik-langsung-dengan-numpy)  
5. [Referensi & Sumber Tambahan](#-referensi--sumber-tambahan)  
6. [Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🚀 Pengenalan NumPy

NumPy, atau *Numerical Python*, adalah salah satu library paling penting dalam ekosistem Python untuk ilmu data, pembelajaran mesin, dan komputasi numerik. NumPy menyediakan struktur data yang efisien dan optimal untuk bekerja dengan array dan matriks, yang merupakan fondasi dari hampir semua algoritma pembelajaran mesin.

### Apa Itu NumPy?
NumPy adalah library Python yang digunakan untuk melakukan operasi numerik pada array dan matriks. Array NumPy adalah struktur data yang memungkinkan kita menyimpan dan memanipulasi data dalam bentuk angka secara efisien. Dalam pembelajaran mesin, data sering kali diubah menjadi array angka, dan algoritma kemudian mencari pola dalam angka-angka tersebut.

### Peran NumPy dalam Pembelajaran Mesin
Dalam kerangka kerja pembelajaran mesin, NumPy berperan penting dalam tahap analisis data. Misalnya, ketika kita memiliki dataset dalam bentuk tabel (seperti DataFrame pandas), NumPy membantu mengubah data tersebut menjadi array angka yang dapat diproses oleh algoritma pembelajaran mesin.

---

## 🏎️ Mengapa Menggunakan NumPy?

### Kecepatan
NumPy dirancang untuk melakukan operasi numerik dengan cepat. Ini karena NumPy menggunakan optimisasi kode C di balik layar, yang membuatnya jauh lebih cepat daripada menggunakan Python murni untuk perhitungan numerik skala besar.

### Vektorisasi
Salah satu fitur utama NumPy adalah *vektorisasi*, yang memungkinkan kita melakukan operasi pada seluruh array tanpa perlu menulis loop secara eksplisit. Ini tidak hanya membuat kode lebih ringkas tetapi juga lebih efisien.

### Dukungan untuk Operasi Matriks
NumPy menyediakan fungsi bawaan untuk operasi matriks seperti perkalian, transpos, dan invers, yang sangat berguna dalam pembelajaran mesin dan aljabar linear.

---

## 🛠️ Fitur Utama NumPy

### 1. **Array NumPy**
Array NumPy adalah struktur data utama dalam NumPy. Ini adalah kumpulan elemen dengan tipe data yang sama, yang disimpan dalam memori secara berurutan.

### 2. **Manipulasi Array**
NumPy menyediakan berbagai fungsi untuk memanipulasi array, seperti mengubah bentuk array, menggabungkan array, dan membagi array.

### 3. **Operasi Matematika**
NumPy mendukung operasi matematika dasar seperti penjumlahan, pengurangan, perkalian, dan pembagian pada array.

### 4. **Broadcasting**
Broadcasting adalah fitur NumPy yang memungkinkan operasi antara array dengan bentuk yang berbeda.

### 5. **Sorting dan Indexing**
NumPy menyediakan fungsi untuk mengurutkan array dan mengakses elemen array menggunakan indeks.

---

## 💻 Praktik Langsung dengan NumPy

### Instalasi NumPy
Sebelum menggunakan NumPy, pastikan Anda telah menginstalnya. Anda dapat menginstalnya menggunakan pip:
```bash
pip install numpy
```

### Contoh Kode Dasar
Berikut adalah beberapa contoh kode untuk memulai dengan NumPy:

#### 1. Membuat Array
```python
import numpy as np

# Membuat array dari list
arr = np.array([1, 2, 3, 4, 5])
print(arr)
```

#### 2. Operasi Matematika pada Array
```python
# Penjumlahan dua array
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
hasil = arr1 + arr2
print(hasil)
```

#### 3. Manipulasi Array
```python
# Mengubah bentuk array
arr = np.array([1, 2, 3, 4, 5, 6])
arr_reshape = arr.reshape(2, 3)
print(arr_reshape)
```

#### 4. Broadcasting
```python
# Menambahkan skalar ke array
arr = np.array([1, 2, 3])
hasil = arr + 5
print(hasil)
```

#### 5. Sorting Array
```python
# Mengurutkan array
arr = np.array([3, 1, 2, 5, 4])
arr_sorted = np.sort(arr)
print(arr_sorted)
```

---

## 📖 Referensi & Sumber Tambahan

- [Dokumentasi Resmi NumPy](https://numpy.org/doc/)  
- [Tutorial NumPy di W3Schools](https://www.w3schools.com/python/numpy_intro.asp)  
- [StackOverflow: Pertanyaan Umum tentang NumPy](https://stackoverflow.com/questions/tagged/numpy)  

---

## 🔙 Kembali ke Daftar Isi
[Kembali ke Daftar Isi](#-daftar-isi)