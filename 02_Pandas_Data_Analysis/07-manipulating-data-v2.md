
# 📚 Pandas Data Manipulation: Panduan Lengkap untuk Manipulasi Data dengan Pandas

## 📑 Daftar Isi
- [📚 Pandas Data Manipulation: Panduan Lengkap untuk Manipulasi Data dengan Pandas](#-pandas-data-manipulation-panduan-lengkap-untuk-manipulasi-data-dengan-pandas)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🎯 Pendahuluan](#-pendahuluan)
  - [📊 Membuat Kolom Baru dari Series](#-membuat-kolom-baru-dari-series)
  - [📋 Membuat Kolom Baru dari List](#-membuat-kolom-baru-dari-list)
  - [🔄 Membuat Kolom Baru dari Kolom Lain](#-membuat-kolom-baru-dari-kolom-lain)
  - [🔢 Membuat Kolom Baru dari Nilai Tunggal](#-membuat-kolom-baru-dari-nilai-tunggal)
  - [🗑️ Menghapus Kolom](#️-menghapus-kolom)
  - [📖 Referensi](#-referensi)
  - [🔙 Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🎯 Pendahuluan
Pandas adalah salah satu library Python yang paling populer untuk manipulasi dan analisis data. Dalam dokumentasi ini, kita akan membahas berbagai cara untuk memanipulasi data menggunakan Pandas, khususnya dalam hal membuat dan menghapus kolom. Kita akan menggunakan contoh dataset penjualan mobil untuk menjelaskan konsep-konsep ini.

---

## 📊 Membuat Kolom Baru dari Series
Untuk membuat kolom baru dari sebuah Series, kita dapat menggunakan metode berikut:

```python
import pandas as pd

# Contoh DataFrame
data = {'Merk': ['Toyota', 'Honda', 'Ford'], 'Harga': [400000, 350000, 300000]}
car_sales = pd.DataFrame(data)

# Membuat Series baru
seats_column = pd.Series([5, 5, 5])

# Menambahkan Series sebagai kolom baru
car_sales['Seats'] = seats_column

print(car_sales)
```

**Penjelasan:**
- Kita membuat Series `seats_column` yang berisi jumlah kursi untuk setiap mobil.
- Kemudian, kita menambahkan Series tersebut sebagai kolom baru `Seats` ke dalam DataFrame `car_sales`.

**Catatan:** Jika panjang Series tidak sama dengan jumlah baris di DataFrame, nilai yang tidak terisi akan diisi dengan `NaN`.

---

## 📋 Membuat Kolom Baru dari List
Kita juga dapat membuat kolom baru dari sebuah list. Namun, panjang list harus sama dengan jumlah baris di DataFrame.

```python
# Membuat list baru
fuel_economy = [7.5, 9.2, 8.7]

# Menambahkan list sebagai kolom baru
car_sales['Fuel per 100 km'] = fuel_economy

print(car_sales)
```

**Penjelasan:**
- List `fuel_economy` berisi data konsumsi bahan bakar per 100 km untuk setiap mobil.
- List tersebut ditambahkan sebagai kolom baru `Fuel per 100 km` ke dalam DataFrame.

---

## 🔄 Membuat Kolom Baru dari Kolom Lain
Kita dapat membuat kolom baru dengan melakukan operasi pada kolom yang sudah ada. Misalnya, menghitung total bahan bakar yang digunakan berdasarkan odometer dan konsumsi bahan bakar.

```python
# Menghitung total bahan bakar yang digunakan
car_sales['Total Fuel Used (L)'] = (car_sales['Odometer'] / 100) * car_sales['Fuel per 100 km']

print(car_sales)
```

**Penjelasan:**
- Kolom `Total Fuel Used (L)` dihitung dengan membagi nilai odometer dengan 100 dan mengalikannya dengan konsumsi bahan bakar per 100 km.

---

## 🔢 Membuat Kolom Baru dari Nilai Tunggal
Kita juga dapat membuat kolom baru dengan nilai tunggal yang sama untuk semua baris.

```python
# Menambahkan kolom dengan nilai tunggal
car_sales['Number of Wheels'] = 4

print(car_sales)
```

**Penjelasan:**
- Kolom `Number of Wheels` diisi dengan nilai 4 untuk semua mobil.

---

## 🗑️ Menghapus Kolom
Untuk menghapus kolom yang tidak diperlukan, kita dapat menggunakan metode `drop`.

```python
# Menghapus kolom 'Total Fuel Used (L)'
car_sales = car_sales.drop('Total Fuel Used (L)', axis=1)

print(car_sales)
```

**Penjelasan:**
- Metode `drop` digunakan untuk menghapus kolom `Total Fuel Used (L)`. Parameter `axis=1` menunjukkan bahwa kita ingin menghapus kolom, bukan baris.

---

## 📖 Referensi
- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)

---

## 🔙 Kembali ke Daftar Isi
[Kembali ke Daftar Isi](#-daftar-isi)
