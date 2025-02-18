
# 📚 Dokumentasi Manipulasi Data dengan Pandas 🐼

## 📑 Daftar Isi
- [📚 Dokumentasi Manipulasi Data dengan Pandas 🐼](#-dokumentasi-manipulasi-data-dengan-pandas-)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🌟 Pendahuluan](#-pendahuluan)
  - [🐼 Manipulasi Data dengan Pandas](#-manipulasi-data-dengan-pandas)
    - [📝 Metode String](#-metode-string)
    - [🕳️ Menangani Data yang Hilang](#️-menangani-data-yang-hilang)
    - [🔄 Parameter `inplace`](#-parameter-inplace)
  - [🛠️ Contoh Praktis](#️-contoh-praktis)
  - [📖 Referensi](#-referensi)
  - [🔙 Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🌟 Pendahuluan

Selamat datang di dokumentasi ini! Di sini, kita akan membahas cara memanipulasi data menggunakan library **Pandas** dalam Python. Pandas adalah alat yang sangat kuat untuk analisis data, terutama dalam konteks *Machine Learning*. Meskipun awalnya terasa rumit, dengan latihan, Anda akan semakin terbiasa. 🚀

---

## 🐼 Manipulasi Data dengan Pandas

### 📝 Metode String

Pandas memungkinkan Anda untuk melakukan operasi string pada kolom data. Misalnya, Anda dapat mengubah semua huruf dalam kolom menjadi huruf kecil menggunakan metode `.lower()`.

```python
import pandas as pd

# Contoh DataFrame
data = {'Make': ['Toyota', 'Honda', 'Ford']}
car_sales = pd.DataFrame(data)

# Mengubah semua huruf menjadi kecil
car_sales['Make'] = car_sales['Make'].str.lower()
print(car_sales)
```

**Output:**
```
     Make
0  toyota
1   honda
2    ford
```

### 🕳️ Menangani Data yang Hilang

Data yang hilang (*missing data*) adalah hal yang umum dalam dataset nyata. Pandas menyediakan fungsi `fillna()` untuk mengisi nilai yang hilang. Misalnya, Anda dapat mengisi nilai yang hilang dengan nilai rata-rata kolom tersebut.

```python
# Contoh DataFrame dengan data yang hilang
data = {'Odometer': [10000, None, 20000, None, 30000]}
car_sales_missing = pd.DataFrame(data)

# Mengisi nilai yang hilang dengan rata-rata
car_sales_missing['Odometer'].fillna(car_sales_missing['Odometer'].mean(), inplace=True)
print(car_sales_missing)
```

**Output:**
```
   Odometer
0   10000.0
1   20000.0
2   20000.0
3   20000.0
4   30000.0
```

### 🔄 Parameter `inplace`

Parameter `inplace` memungkinkan Anda untuk memodifikasi DataFrame secara langsung tanpa perlu melakukan reassignment. Secara default, nilai `inplace` adalah `False`.

```python
# Contoh penggunaan inplace=True
car_sales_missing.dropna(inplace=True)
print(car_sales_missing)
```

**Output:**
```
   Odometer
0   10000.0
2   20000.0
4   30000.0
```

---

## 🛠️ Contoh Praktis

Berikut adalah contoh lengkap yang menggabungkan semua konsep di atas:

```python
import pandas as pd

# Membuat DataFrame
data = {'Make': ['Toyota', 'Honda', 'Ford', None],
        'Odometer': [10000, None, 20000, None]}
car_sales = pd.DataFrame(data)

# Mengubah huruf menjadi kecil
car_sales['Make'] = car_sales['Make'].str.lower()

# Mengisi nilai yang hilang
car_sales['Odometer'].fillna(car_sales['Odometer'].mean(), inplace=True)

# Menghapus baris dengan nilai yang hilang
car_sales.dropna(inplace=True)

print(car_sales)
```

**Output:**
```
     Make   Odometer
0  toyota  10000.0
2    ford  20000.0
```

---

## 📖 Referensi

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Working with Missing Data in Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/missing_data.html)
- [Python String Methods](https://docs.python.org/3/library/stdtypes.html#string-methods)

---

## 🔙 Kembali ke Daftar Isi

[Kembali ke Daftar Isi](#-daftar-isi)
