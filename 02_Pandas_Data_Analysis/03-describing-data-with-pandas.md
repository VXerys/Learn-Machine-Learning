
# 📊 Pandas: Deskripsi Data dan Analisis Statistik

## 📑 Daftar Isi
- [📊 Pandas: Deskripsi Data dan Analisis Statistik](#-pandas-deskripsi-data-dan-analisis-statistik)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🎯 Pendahuluan](#-pendahuluan)
  - [🔍 Mengenal Fungsi dan Atribut](#-mengenal-fungsi-dan-atribut)
  - [🧮 Menjelajahi Tipe Data](#-menjelajahi-tipe-data)
  - [📊 Analisis Statistik dengan `describe`](#-analisis-statistik-dengan-describe)
  - [ℹ️ Informasi Detail dengan `info`](#ℹ️-informasi-detail-dengan-info)
  - [📈 Operasi Statistik Lanjutan](#-operasi-statistik-lanjutan)
    - [Menghitung Rata-Rata](#menghitung-rata-rata)
    - [Menghitung Total](#menghitung-total)
    - [Menghitung Median](#menghitung-median)
  - [📏 Menghitung Panjang Data Frame](#-menghitung-panjang-data-frame)
  - [📚 Referensi](#-referensi)

---

## 🎯 Pendahuluan
Dalam video sebelumnya, kita telah mempelajari berbagai tipe data dalam Pandas Series dan DataFrame, serta cara mengimpor dan mengekspor data. Pada bagian ini, kita akan fokus pada cara mendeskripsikan dan menganalisis data menggunakan Pandas. Kita akan menjelajahi berbagai fungsi dan atribut yang dapat digunakan untuk memahami struktur dan karakteristik data.

---

## 🔍 Mengenal Fungsi dan Atribut
Dalam Pandas, terdapat dua konsep utama yang perlu dipahami: **fungsi** dan **atribut**.

- **Fungsi**: Melakukan operasi tertentu pada data. Contoh: `to_csv()`, `describe()`.
- **Atribut**: Menyimpan informasi meta tentang data. Contoh: `dtypes`, `columns`.

Contoh penggunaan:
```python
# Fungsi
car_sales.to_csv('car_sales.csv')

# Atribut
car_sales.dtypes
```

---

## 🧮 Menjelajahi Tipe Data
Untuk melihat tipe data dari setiap kolom dalam DataFrame, kita dapat menggunakan atribut `dtypes`.

```python
print(car_sales.dtypes)
```
Output:
```
make       object
color      object
odometer    int64
doors       int64
price      object
dtype: object
```
Penjelasan:
- `object`: Kolom berisi teks atau campuran tipe data.
- `int64`: Kolom berisi bilangan bulat.

---

## 📊 Analisis Statistik dengan `describe`
Fungsi `describe()` memberikan ringkasan statistik untuk kolom numerik dalam DataFrame.

```python
print(car_sales.describe())
```
Output:
```
       odometer      doors
count  10.000000  10.000000
mean   78601.000000   4.000000
std     47140.471405   0.471405
min    10000.000000   3.000000
25%    50000.000000   4.000000
50%    75000.000000   4.000000
75%    100000.000000   4.000000
max    150000.000000   5.000000
```
Penjelasan:
- `count`: Jumlah data yang valid.
- `mean`: Rata-rata nilai.
- `std`: Standar deviasi.
- `min`, `max`: Nilai minimum dan maksimum.
- Persentil (25%, 50%, 75%): Distribusi data.

---

## ℹ️ Informasi Detail dengan `info`
Fungsi `info()` memberikan gambaran umum tentang DataFrame, termasuk tipe data dan jumlah nilai non-null.

```python
print(car_sales.info())
```
Output:
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10 entries, 0 to 9
Data columns (total 5 columns):
 #   Column    Non-Null Count  Dtype 
---  ------    --------------  ----- 
 0   make      10 non-null     object
 1   color     10 non-null     object
 2   odometer  10 non-null     int64 
 3   doors     10 non-null     int64 
 4   price     10 non-null     object
dtypes: int64(2), object(3)
memory usage: 528.0+ bytes
```

---

## 📈 Operasi Statistik Lanjutan
Pandas menyediakan berbagai fungsi statistik seperti `mean`, `median`, dan `sum`.

### Menghitung Rata-Rata
```python
print(car_sales['odometer'].mean())
```

### Menghitung Total
```python
print(car_sales['doors'].sum())
```

### Menghitung Median
```python
print(car_sales['odometer'].median())
```

---

## 📏 Menghitung Panjang Data Frame
Untuk mengetahui jumlah baris dalam DataFrame, kita dapat menggunakan fungsi `len()`.

```python
print(len(car_sales))
```
Output:
```
10
```

---

## 📚 Referensi
Berikut beberapa sumber tambahan untuk mempelajari Pandas lebih lanjut:
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Scikit-Learn Documentation](https://scikit-learn.org/stable/)


[Kembali ke Daftar Isi](#-daftar-isi)
