
# 📚 Pandas: Pengenalan dan Implementasi Praktis

## 📑 Daftar Isi
- [📚 Pandas: Pengenalan dan Implementasi Praktis](#-pandas-pengenalan-dan-implementasi-praktis)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🐼 Pengenalan Pandas](#-pengenalan-pandas)
  - [💻 Mengaktifkan Lingkungan dan Membuka Jupyter Notebook](#-mengaktifkan-lingkungan-dan-membuka-jupyter-notebook)
  - [📊 Struktur Data dalam Pandas](#-struktur-data-dalam-pandas)
    - [Series](#series)
    - [DataFrame](#dataframe)
  - [📂 Mengimpor Data dari CSV](#-mengimpor-data-dari-csv)
  - [🧩 Anatomi DataFrame](#-anatomi-dataframe)
  - [📤 Mengekspor DataFrame ke CSV](#-mengekspor-dataframe-ke-csv)
  - [📚 Referensi](#-referensi)
  - [🔝 Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🐼 Pengenalan Pandas

Pandas adalah salah satu library Python yang paling populer untuk manipulasi dan analisis data. Library ini menyediakan struktur data yang efisien dan mudah digunakan, seperti **Series** dan **DataFrame**, yang memungkinkan pengguna untuk bekerja dengan data terstruktur secara efektif. Pandas sangat berguna dalam berbagai tugas, mulai dari pembersihan data hingga analisis statistik.

---

## 💻 Mengaktifkan Lingkungan dan Membuka Jupyter Notebook

Sebelum menggunakan Pandas, pastikan lingkungan Python yang sesuai telah diaktifkan. Berikut adalah langkah-langkahnya:

1. Buka terminal atau command prompt.
2. Aktifkan lingkungan yang telah dibuat menggunakan perintah berikut:
   ```bash
   conda activate nama_lingkungan
   ```
3. Buka Jupyter Notebook dengan mengetik:
   ```bash
   jupyter notebook
   ```
4. Setelah browser terbuka, navigasikan ke direktori proyek Anda.

---

## 📊 Struktur Data dalam Pandas

Pandas memiliki dua struktur data utama: **Series** dan **DataFrame**.

### Series
Series adalah struktur data satu dimensi yang mirip dengan array atau list. Contoh pembuatan Series:

```python
import pandas as pd

# Membuat Series dari list
car_brands = pd.Series(['Toyota', 'Honda', 'Ford', 'Tesla'])
print(car_brands)
```

Output:
```
0    Toyota
1     Honda
2      Ford
3     Tesla
dtype: object
```

### DataFrame
DataFrame adalah struktur data dua dimensi yang terdiri dari baris dan kolom. Contoh pembuatan DataFrame:

```python
# Membuat DataFrame dari dictionary
car_data = pd.DataFrame({
    'Car Make': ['Toyota', 'Honda', 'Ford', 'Tesla'],
    'Color': ['Red', 'Blue', 'White', 'Black']
})
print(car_data)
```

Output:
```
  Car Make  Color
0   Toyota    Red
1    Honda   Blue
2     Ford  White
3    Tesla  Black
```

---

## 📂 Mengimpor Data dari CSV

Pandas memudahkan pengguna untuk mengimpor data dari file CSV. Berikut adalah contohnya:

```python
# Mengimpor data dari file CSV
car_sales = pd.read_csv('carsales.csv')
print(car_sales.head())  # Menampilkan 5 baris pertama
```

---

## 🧩 Anatomi DataFrame

Berikut adalah komponen utama dari sebuah DataFrame:

1. **Index**: Kolom pertama yang biasanya berisi nomor indeks (dimulai dari 0).
2. **Row (Baris)**: Sekumpulan nilai yang berhubungan dengan satu entri.
3. **Column (Kolom)**: Sekumpulan nilai yang berhubungan dengan satu atribut.
4. **Data**: Nilai-nilai yang tersimpan dalam DataFrame.

Contoh:
```python
# Menampilkan informasi tentang DataFrame
print(car_sales.info())
```

---

## 📤 Mengekspor DataFrame ke CSV

Setelah melakukan manipulasi data, Anda dapat mengekspor DataFrame kembali ke file CSV:

```python
# Mengekspor DataFrame ke file CSV
car_sales.to_csv('exported_car_sales.csv', index=False)
```

---

## 📚 Referensi

Berikut adalah beberapa referensi tambahan untuk mempelajari Pandas lebih lanjut:
- [Dokumentasi Resmi Pandas](https://pandas.pydata.org/docs/)
- [Pandas Tutorial oleh W3Schools](https://www.w3schools.com/python/pandas/default.asp)
- [Pandas Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)

---

## 🔝 Kembali ke Daftar Isi
[Kembali ke Daftar Isi](#-daftar-isi)
