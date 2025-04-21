# Python-Classification-Online-Learnng-Adaptibility-level

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

- **Jumlah Baris Data:** 5 baris (contoh kecil dari dataset yang sebenarnya)
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
