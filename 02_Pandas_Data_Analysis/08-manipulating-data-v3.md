
# 📚 Dokumentasi Pandas untuk Machine Learning

Dokumentasi ini menjelaskan penggunaan library Pandas dalam konteks Machine Learning, dengan fokus pada manipulasi data, pengacakan data, dan penerapan fungsi pada kolom. Pandas adalah library Python yang sangat populer untuk analisis data dan sering digunakan dalam proyek Machine Learning.

## 📑 Daftar Isi
1. [Pengenalan](#-pengenalan)
2. [Mengacak Data dengan `sample`](#-mengacak-data-dengan-sample)
3. [Mereset Indeks dengan `reset_index`](#-mereset-indeks-dengan-reset_index)
4. [Menerapkan Fungsi dengan `apply`](#-menerapkan-fungsi-dengan-apply)
5. [Referensi](#-referensi)
6. [Kembali ke Daftar Isi](#-kembali-ke-daftar-isi)

---

## 🌟 Pengenalan

Pandas adalah library Python yang digunakan untuk manipulasi dan analisis data. Dalam Machine Learning, langkah pertama yang sering dilakukan adalah mempersiapkan data, termasuk mengacak data, membagi data menjadi set pelatihan dan pengujian, serta menerapkan fungsi untuk transformasi data.

---

## 🔀 Mengacak Data dengan `sample`

### Apa Itu `sample`?
Fungsi `sample` digunakan untuk mengacak baris dalam DataFrame. Ini sangat berguna saat Anda ingin memastikan bahwa urutan data tidak memengaruhi model Machine Learning Anda.

### Mengapa Mengacak Data?
- **Menghindari Bias:** Urutan data dapat memengaruhi pola yang dipelajari oleh model.
- **Pembagian Data:** Mengacak data adalah langkah penting sebelum membagi data menjadi set pelatihan, validasi, dan pengujian.

### Contoh Penggunaan
```python
import pandas as pd

# Contoh DataFrame
data = {'Merek': ['Toyota', 'Honda', 'Nissan', 'Ford', 'BMW'],
        'Model': ['Corolla', 'Civic', 'Altima', 'Mustang', 'X5'],
        'Odometer (km)': [150000, 120000, 90000, 80000, 50000]}
car_sales = pd.DataFrame(data)

# Mengacak DataFrame
car_sales_shuffled = car_sales.sample(frac=1.0)  # Mengacak 100% data
print(car_sales_shuffled)
```

### Penjelasan
- `frac=1.0`: Mengambil 100% data, sehingga semua baris diacak.
- Hasilnya adalah DataFrame dengan urutan baris yang diacak.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🔄 Mereset Indeks dengan `reset_index`

### Apa Itu `reset_index`?
Setelah mengacak data, indeks DataFrame mungkin tidak berurutan. Fungsi `reset_index` digunakan untuk mereset indeks ke urutan default.

### Contoh Penggunaan
```python
# Mereset indeks
car_sales_shuffled_reset = car_sales_shuffled.reset_index(drop=True)
print(car_sales_shuffled_reset)
```

### Penjelasan
- `drop=True`: Menghapus kolom indeks lama yang ditambahkan setelah mereset indeks.
- Hasilnya adalah DataFrame dengan indeks yang diurutkan ulang.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🛠️ Menerapkan Fungsi dengan `apply`

### Apa Itu `apply`?
Fungsi `apply` digunakan untuk menerapkan fungsi tertentu ke setiap elemen dalam kolom DataFrame. Ini sangat berguna untuk transformasi data.

### Contoh Penggunaan: Mengonversi Kilometer ke Mil
```python
# Mengonversi odometer dari kilometer ke mil
car_sales['Odometer (miles)'] = car_sales['Odometer (km)'].apply(lambda x: x / 1.6)
print(car_sales)
```

### Penjelasan
- `lambda x: x / 1.6`: Fungsi lambda yang mengonversi nilai kilometer ke mil.
- Hasilnya adalah kolom baru dengan nilai odometer dalam mil.

### Contoh Lain: Menerapkan Fungsi Kustom
```python
# Fungsi kustom untuk menambahkan teks
def add_text(value):
    return f"{value} km"

car_sales['Odometer (text)'] = car_sales['Odometer (km)'].apply(add_text)
print(car_sales)
```

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 📖 Referensi

Berikut adalah beberapa sumber tambahan untuk mempelajari Pandas lebih lanjut:
- [Dokumentasi Resmi Pandas](https://pandas.pydata.org/pandas-docs/stable/)
- [Tutorial Pandas oleh W3Schools](https://www.w3schools.com/python/pandas/default.asp)
- [Pandas Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)

[🔝 Kembali ke Daftar Isi](#-daftar-isi)

---

## 🏁 Kesimpulan

Pandas adalah alat yang sangat kuat untuk manipulasi data dalam Machine Learning. Dengan memahami fungsi seperti `sample`, `reset_index`, dan `apply`, Anda dapat mempersiapkan data dengan lebih efektif untuk model Machine Learning Anda.

[🔝 Kembali ke Daftar Isi](#-daftar-isi)
