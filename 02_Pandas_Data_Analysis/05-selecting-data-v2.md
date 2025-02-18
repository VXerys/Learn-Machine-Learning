
# 📚 Dokumentasi Pandas: Manipulasi dan Visualisasi Data

## 📑 Daftar Isi
- [📚 Dokumentasi Pandas: Manipulasi dan Visualisasi Data](#-dokumentasi-pandas-manipulasi-dan-visualisasi-data)
  - [📑 Daftar Isi](#-daftar-isi)
  - [🎯 Pendahuluan](#-pendahuluan)
  - [📊 Cross Tab](#-cross-tab)
    - [Contoh Kode:](#contoh-kode)
    - [Penjelasan:](#penjelasan)
  - [📂 Group By](#-group-by)
    - [Contoh Kode:](#contoh-kode-1)
    - [Penjelasan:](#penjelasan-1)
  - [📈 Visualisasi Data](#-visualisasi-data)
    - [📉 Plot Sederhana](#-plot-sederhana)
      - [Contoh Kode:](#contoh-kode-2)
      - [Penjelasan:](#penjelasan-2)
    - [📊 Histogram](#-histogram)
      - [Contoh Kode:](#contoh-kode-3)
      - [Penjelasan:](#penjelasan-3)
  - [🛠️ Mengatasi Masalah Data Non-Numerik](#️-mengatasi-masalah-data-non-numerik)
    - [Contoh Kode:](#contoh-kode-4)
    - [Penjelasan:](#penjelasan-4)
  - [📚 Referensi](#-referensi)
  - [🔙 Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🎯 Pendahuluan
Pandas adalah library Python yang sangat powerful untuk manipulasi dan analisis data. Dalam dokumentasi ini, kita akan membahas beberapa teknik dasar dalam Pandas seperti `Cross Tab`, `Group By`, dan visualisasi data. Selain itu, kita juga akan mempelajari cara mengatasi masalah data non-numerik dan melakukan konversi tipe data.

---

## 📊 Cross Tab
`Cross Tab` adalah metode yang digunakan untuk membandingkan dua kolom dalam sebuah DataFrame. Ini sangat berguna untuk melihat hubungan antara dua variabel kategorikal.

### Contoh Kode:
```python
import pandas as pd

# Contoh DataFrame
data = {
    'Make': ['Toyota', 'Honda', 'BMW', 'Nissan', 'Toyota', 'Honda'],
    'Doors': [3, 4, 5, 4, 3, 4]
}
car_sales = pd.DataFrame(data)

# Cross Tab
cross_tab = pd.crosstab(car_sales['Make'], car_sales['Doors'])
print(cross_tab)
```

### Penjelasan:
- `pd.crosstab()` mengambil dua kolom sebagai argumen dan menghasilkan tabel yang menunjukkan frekuensi kombinasi nilai dari kedua kolom tersebut.
- Dalam contoh di atas, kita melihat berapa banyak mobil dari setiap merek yang memiliki jumlah pintu tertentu.

---

## 📂 Group By
`Group By` adalah metode yang digunakan untuk mengelompokkan data berdasarkan satu atau lebih kolom dan kemudian menerapkan fungsi agregasi pada kelompok tersebut.

### Contoh Kode:
```python
# Group By
grouped = car_sales.groupby('Make').mean()
print(grouped)
```

### Penjelasan:
- `groupby('Make')` mengelompokkan data berdasarkan kolom `Make`.
- `.mean()` menghitung nilai rata-rata untuk setiap kelompok.
- Hasilnya adalah DataFrame yang menunjukkan nilai rata-rata untuk setiap merek mobil.

---

## 📈 Visualisasi Data
Visualisasi data adalah cara yang efektif untuk memahami data dengan cepat. Pandas menyediakan beberapa metode untuk membuat visualisasi sederhana.

### 📉 Plot Sederhana
Plot sederhana dapat dibuat menggunakan metode `.plot()`.

#### Contoh Kode:
```python
# Plot sederhana
car_sales['Odometer'].plot()
```

#### Penjelasan:
- `.plot()` menghasilkan plot garis dari nilai dalam kolom `Odometer`.
- Ini membantu kita melihat tren atau pola dalam data.

### 📊 Histogram
Histogram digunakan untuk melihat distribusi data.

#### Contoh Kode:
```python
# Histogram
car_sales['Odometer'].plot(kind='hist')
```

#### Penjelasan:
- `kind='hist'` menghasilkan histogram yang menunjukkan distribusi nilai dalam kolom `Odometer`.
- Ini membantu kita mengidentifikasi outliers atau nilai yang tidak biasa.

---

## 🛠️ Mengatasi Masalah Data Non-Numerik
Terkadang, kita menemui kolom yang seharusnya numerik tetapi disimpan sebagai objek. Untuk mengatasi ini, kita perlu mengonversi tipe data tersebut.

### Contoh Kode:
```python
# Konversi kolom 'Price' ke integer
car_sales['Price'] = car_sales['Price'].str.replace('$', '').str.replace(',', '').astype(int)
```

### Penjelasan:
- `str.replace('$', '')` menghapus simbol `$` dari kolom `Price`.
- `str.replace(',', '')` menghapus koma dari kolom `Price`.
- `astype(int)` mengonversi kolom `Price` ke tipe data integer.

---

## 📚 Referensi
- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Stack Overflow: Convert Pandas Column to Integer](https://stackoverflow.com/questions/15891038/change-column-type-in-pandas)

---

## 🔙 Kembali ke Daftar Isi
[Kembali ke Daftar Isi](#-daftar-isi)