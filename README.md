# Python-Classification-Online-Learning-Adaptivity-level

## Domain Proyek

Proyek ini bertujuan untuk menganalisis tingkat adaptasi siswa terhadap pembelajaran daring (online learning) berdasarkan berbagai faktor demografis dan teknologi. Dengan semakin pentingnya pendidikan daring terutama pasca-pandemi, pemahaman terhadap faktor-faktor yang memengaruhi adaptasi siswa sangatlah penting agar institusi pendidikan dapat merancang strategi yang inklusif dan efektif.

## Mengapa Masalah Ini Harus Diselesaikan

- Tidak semua siswa memiliki akses dan kesiapan yang sama dalam mengikuti pembelajaran daring.
- Perbedaan dalam ketersediaan perangkat, koneksi internet, hingga kondisi finansial dapat menjadi penghambat adaptasi.
- Dengan memahami pola-pola ini, institusi pendidikan dapat memberikan dukungan lebih tepat sasaran untuk meningkatkan kualitas pendidikan daring secara merata.

**Referensi:**
- Online Learning Readiness and Learning Achievement among University Students during COVID-19 Pandemic
- Predicting E-Learning Readiness using Machine Learning Algorithms

---

## Business Understanding

### Problem Statements

1. Bagaimana cara memprediksi tingkat adaptasi siswa terhadap pembelajaran daring berdasarkan fitur-fitur seperti usia, tingkat pendidikan, jenis koneksi internet, dan perangkat yang digunakan?
2. Apakah kondisi finansial atau jenis institusi berpengaruh signifikan terhadap adaptasi siswa?
3. Bagaimana mengatasi ketidakseimbangan kelas dalam data adaptasi (misalnya, lebih banyak siswa dengan adaptasi rendah dibanding tinggi)?

### Goals

- Mengembangkan model Machine Learning yang mampu memprediksi adaptasi siswa terhadap pembelajaran daring secara akurat.
- Menganalisis pengaruh fitur-fitur seperti usia, perangkat, internet, dan kondisi keuangan terhadap tingkat adaptasi.
- Mengatasi ketidakseimbangan data agar model tidak bias terhadap salah satu kelas adaptasi.

### Solution Statements

- Menggunakan algoritma klasifikasi seperti Decision Tree, Random Forest, Logistic Regression, dan K-Nearest Neighbor (KNN) untuk membangun model prediksi.
- Menerapkan teknik penyeimbangan data seperti SMOTE (Synthetic Minority Over-sampling Technique) atau under/oversampling sederhana.
- Mengevaluasi model menggunakan metrik seperti akurasi, precision, recall, dan F1-score.

---

## Data Understanding

Dataset ini berisi data survei siswa dari berbagai latar belakang pendidikan mengenai kesiapan mereka dalam mengikuti pembelajaran daring. Data dikumpulkan dalam format tabular dan terdiri dari 14 kolom dan beberapa baris responden.

- **Jumlah Baris Data:** 1205 baris (contoh kecil dari dataset yang sebenarnya)
- **Kondisi Data:** Data terdiri dari kombinasi informasi demografis dan teknis yang berkaitan dengan kesiapan pembelajaran daring.
- **Cocok Untuk:** Supervised Learning dengan algoritma klasifikasi, karena label `Adaptivity Level` merupakan target variabel dengan kelas 0 dan 1.

---

## Fitur-Fitur Dataset

| Nama Kolom           | Deskripsi                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| Gender               | Jenis kelamin responden (Boy/Girl)                                              |
| Age                  | Rentang usia siswa                                                              |
| Education Level      | Tingkat pendidikan (School, College, University)                               |
| Institution Type     | Jenis institusi pendidikan (Government/Non Government)                         |
| IT Student           | Apakah siswa merupakan siswa jurusan IT                                        |
| Location             | Apakah berada di wilayah yang mengalami pemadaman listrik (Yes/No)             |
| Load-shedding        | Indikasi adanya pemadaman listrik                                               |
| Financial Condition  | Kondisi ekonomi siswa (Low, Mid, High)                                          |
| Internet Type        | Jenis koneksi internet (Wifi, Mobile Data)                                     |
| Network Type         | Tipe jaringan internet (3G, 4G)                                                 |
| Class Duration       | Durasi kelas daring (0, 1–3, 3–6 jam per hari)                                  |
| Self LMS             | Apakah siswa menggunakan Learning Management System sendiri                    |
| Device               | Perangkat yang digunakan untuk belajar daring (Mobile, Tab, dll.)              |
| **Adaptivity Level** | **Label target**: Tingkat adaptasi terhadap pembelajaran daring (0, 1, ...)     |

---

## Visualisasi Data
Memvisualisasikan data agar mengetahui gambaran umum terhadap dataset

## Validasi Data

### 1. Cek Tipe Data
Langkah pertama adalah memverifikasi tipe data dari setiap kolom dalam dataset. Ini bertujuan untuk memastikan bahwa data memiliki format yang sesuai sebelum dilakukan pemrosesan lebih lanjut. Misalnya, kolom kategorikal seperti "Gender", "Internet Type", dan "Device" harus dikenali sebagai tipe objek (string), sementara label target "Adaptivity Level" harus bertipe numerik atau dikonversi sebelum proses modeling.

### 2. Cek Missing Value
Setelah pengecekan dilakukan, dipastikan bahwa dataset tidak mengandung missing value. Hal ini sangat penting karena nilai kosong dapat memengaruhi proses pelatihan model dan menyebabkan bias atau error dalam hasil analisis. Oleh karena itu, tidak diperlukan langkah imputasi atau penghapusan data.

---

## Menentukan Objek Data

### 1. Variabel X (Features)
Semua kolom selain `Adaptivity Level` diperlakukan sebagai variabel fitur (`X`). Fitur-fitur ini mencerminkan karakteristik demografis dan teknologi dari responden, seperti usia, jenis kelamin, tipe perangkat, hingga jenis koneksi internet.

### 2. Variabel y (Target)
Kolom `Adaptivity Level` adalah target dari model, yaitu label yang menunjukkan tingkat adaptasi siswa terhadap pembelajaran daring. Ini adalah variabel kategorikal yang menunjukkan dua kemungkinan kelas (misalnya, 0 dan 1).

---

## Konstruksi Data

### One-Hot Encoding
Untuk dapat digunakan dalam algoritma Machine Learning, semua variabel kategorikal perlu dikonversi ke format numerik. Proses ini dilakukan menggunakan OneHotEncoder. One-hot encoding akan mengubah setiap kategori menjadi kolom biner terpisah, memungkinkan model mengenali dan membedakan antar kategori tanpa asumsi urutan atau nilai numerik intrinsik.

---

## Skenario Model

### Split Dataset
Dataset dibagi menjadi dua bagian: 90% untuk data pelatihan dan 10% untuk data pengujian. Rasio ini dipilih agar model memiliki cukup data untuk belajar, sekaligus menyisakan sebagian data untuk menguji performa model secara independen.

---

## Pemilihan Model

### Support Vector Machine (SVM)
Model klasifikasi yang digunakan dalam proyek ini adalah Support Vector Machine (SVM), yang dikenal efektif untuk klasifikasi dengan dimensi tinggi. SVM bekerja dengan mencari hyperplane optimal yang memisahkan kelas-kelas dengan margin maksimum.

---

## Evaluasi

### 1. Confusion Matrix
Confusion matrix digunakan untuk mengevaluasi kinerja klasifikasi model dengan menunjukkan jumlah prediksi yang benar dan salah untuk setiap kelas. Matriks ini membantu memahami di mana model mengalami kesalahan dalam klasifikasi.

### 2. Classification Report
Laporan klasifikasi memberikan metrik seperti precision, recall, f1-score, dan support untuk masing-masing kelas. Metrik ini memberikan gambaran menyeluruh tentang performa model, terutama dalam konteks data yang tidak seimbang.

---

## Review Model

### 1. Hyperparameter Tuning
Untuk meningkatkan performa model, dilakukan pencarian hyperparameter terbaik menggunakan `GridSearchCV`. Parameter yang diuji meliputi:
- `C`: parameter regulasi
- `gamma`: parameter kernel
- `kernel`: jenis kernel yang digunakan (rbf dan poly)

Proses ini dilakukan untuk menemukan kombinasi parameter yang memberikan akurasi terbaik pada data validasi.

### 2. Mutual Information Regression
Sebagai bagian dari analisis fitur, dilakukan evaluasi menggunakan teknik mutual information regression. Teknik ini bertujuan untuk mengukur tingkat keterkaitan antara setiap fitur dengan target. Fitur-fitur dengan nilai mutual information yang tinggi dianggap lebih relevan dan berkontribusi signifikan terhadap prediksi.

---
