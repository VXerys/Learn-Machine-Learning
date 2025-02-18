
# 📚 Pandas: Melihat dan Memilih Data

Selamat datang kembali! Dalam dokumentasi ini, kita akan membahas berbagai cara untuk melihat dan memilih data yang telah diimpor ke dalam DataFrame menggunakan Pandas. Kita akan menjelajahi fungsi-fungsi penting seperti `head`, `tail`, `loc`, dan `iloc`, serta memberikan contoh kode praktis yang dapat dijalankan di Jupyter Notebook.

## 📑 Daftar Isi
- [📚 Pandas: Melihat dan Memilih Data](#-pandas-melihat-dan-memilih-data)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🧐 Melihat Data dengan `head` dan `tail`](#-melihat-data-dengan-head-dan-tail)
    - [`head()`](#head)
    - [`tail()`](#tail)
  - [🎯 Memilih Data dengan `loc` dan `iloc`](#-memilih-data-dengan-loc-dan-iloc)
    - [`loc`](#loc)
    - [`iloc`](#iloc)
    - [Slicing dengan `loc` dan `iloc`](#slicing-dengan-loc-dan-iloc)
  - [📊 Memilih Kolom](#-memilih-kolom)
  - [🔍 Boolean Indexing](#-boolean-indexing)
  - [📖 Referensi](#-referensi)

---

## 🧐 Melihat Data dengan `head` dan `tail`

### `head()`
Fungsi `head()` digunakan untuk melihat beberapa baris pertama dari DataFrame. Secara default, fungsi ini akan menampilkan 5 baris pertama.

```python
import pandas as pd

# Contoh DataFrame
data = {'Make': ['Toyota', 'Honda', 'BMW', 'Audi', 'Ford'],
        'Color': ['Red', 'Blue', 'Black', 'White', 'Green'],
        'Odometer': [15000, 20000, 22000, 18000, 25000]}
df = pd.DataFrame(data)

# Menampilkan 5 baris pertama
df.head()
```

Anda juga dapat menentukan jumlah baris yang ingin ditampilkan dengan memberikan argumen ke dalam fungsi `head()`.

```python
# Menampilkan 3 baris pertama
df.head(3)
```

### `tail()`
Fungsi `tail()` mirip dengan `head()`, tetapi menampilkan beberapa baris terakhir dari DataFrame.

```python
# Menampilkan 5 baris terakhir
df.tail()
```

Seperti `head()`, Anda juga dapat menentukan jumlah baris yang ingin ditampilkan.

```python
# Menampilkan 2 baris terakhir
df.tail(2)
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🎯 Memilih Data dengan `loc` dan `iloc`

### `loc`
Fungsi `loc` digunakan untuk memilih data berdasarkan label indeks.

```python
# Membuat Series dengan indeks kustom
animals = pd.Series(['Dog', 'Cat', 'Panda', 'Snake', 'Bird'], index=[0, 3, 2, 3, 9])

# Memilih data dengan indeks 3
animals.loc[3]
```

### `iloc`
Fungsi `iloc` digunakan untuk memilih data berdasarkan posisi (indeks numerik).

```python
# Memilih data pada posisi 3
animals.iloc[3]
```

### Slicing dengan `loc` dan `iloc`
Anda juga dapat menggunakan slicing untuk memilih rentang data.

```python
# Slicing dengan iloc
animals.iloc[:3]

# Slicing dengan loc
df.loc[:3]
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📊 Memilih Kolom

Anda dapat memilih kolom tertentu dari DataFrame dengan menggunakan nama kolom.

```python
# Memilih kolom 'Make'
df['Make']

# Alternatif menggunakan dot notation
df.Make
```

Namun, dot notation tidak dapat digunakan jika nama kolom mengandung spasi.

```python
# Memilih kolom 'Odometer'
df['Odometer']
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🔍 Boolean Indexing

Boolean indexing memungkinkan Anda memilih data berdasarkan kondisi tertentu.

```python
# Memilih mobil dengan merek 'Toyota'
df[df['Make'] == 'Toyota']

# Memilih mobil dengan odometer lebih dari 20000
df[df['Odometer'] > 20000]
```

Anda juga dapat menggabungkan beberapa kondisi menggunakan operator logika.

```python
# Memilih mobil dengan merek 'Toyota' dan odometer lebih dari 15000
df[(df['Make'] == 'Toyota') & (df['Odometer'] > 15000)]
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📖 Referensi

Berikut adalah beberapa referensi tambahan untuk mempelajari lebih lanjut tentang Pandas:

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)
- [Real Python: Pandas Tutorials](https://realpython.com/tutorials/pandas/)

[🔝 Kembali ke Daftar Isi](#-daftar-isi)
