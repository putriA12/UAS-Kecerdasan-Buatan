#  💸 Proyek UAS Kecerdasan Buatan

## Analisis Sentimen Ulasan Aplikasi Wondr by BNI Menggunakan Algoritma Long Short-Term Memory (LSTM) dan Support Vector Machine (SVM)

---

## 📖 Deskripsi Proyek

Proyek ini merupakan tugas akhir mata kuliah **Kecerdasan Buatan** yang bertujuan untuk membangun sistem analisis sentimen terhadap ulasan pengguna aplikasi **Wondr by BNI** di Google Play Store.

Penelitian ini membandingkan dua algoritma klasifikasi, yaitu **Long Short-Term Memory (LSTM)** sebagai metode Deep Learning dan **Support Vector Machine (SVM)** sebagai metode Machine Learning. Perbandingan dilakukan berdasarkan nilai **Accuracy, Precision, Recall, dan F1-Score** untuk menentukan algoritma dengan performa terbaik.

---

# 🎯 Tujuan Proyek

* Mengumpulkan data ulasan aplikasi Wondr by BNI dari Google Play Store.
* Melakukan preprocessing data teks.
* Membangun model klasifikasi sentimen menggunakan algoritma LSTM.
* Membangun model klasifikasi sentimen menggunakan algoritma SVM.
* Membandingkan performa kedua algoritma.
* Menentukan algoritma terbaik berdasarkan hasil evaluasi.

---

# 📂 Dataset

Dataset diperoleh melalui proses scraping ulasan aplikasi **Wondr by BNI** menggunakan library **Google Play Scraper**.

Dataset memiliki atribut sebagai berikut.

| No | Atribut  | Keterangan      |
| -- | -------- | --------------- |
| 1  | userName | Nama pengguna   |
| 2  | score    | Rating pengguna |
| 3  | at       | Tanggal ulasan  |
| 4  | content  | Isi ulasan      |
| 5  | sentimen | Label sentimen  |

---

# 🔄 Tahapan Pengerjaan

## 1️⃣ Data Collection

Melakukan scraping data ulasan aplikasi Wondr by BNI dari Google Play Store menggunakan Google Play Scraper.

---

## 2️⃣ Data Preprocessing

Tahapan preprocessing meliputi:

* Menghapus data kosong
* Case Folding
* Cleaning Text
* Tokenizing
* Stopword Removal
* Stemming menggunakan Sastrawi
* Pelabelan Sentimen
* Train Test Split

---

## 3️⃣ Exploratory Data Analysis (EDA)

Analisis data dilakukan menggunakan beberapa visualisasi, yaitu:

* Distribusi Sentimen
* Distribusi Rating
* WordCloud
* Frekuensi Kata
* Visualisasi Dataset

---

## 4️⃣ Data Preparation

### Untuk Model LSTM

* Label Encoding
* Tokenizer
* Sequence Padding
* One Hot Encoding

### Untuk Model SVM

* TF-IDF Vectorization
* Label Encoding

---

# 🤖 Algoritma yang Digunakan

## 1. Long Short-Term Memory (LSTM)

Model LSTM dibangun menggunakan TensorFlow/Keras dengan arsitektur:

* Embedding Layer
* Bidirectional LSTM
* Dropout
* Dense Layer
* Softmax Output

---

## 2. Support Vector Machine (SVM)

Model SVM dibangun menggunakan Scikit-Learn dengan:

* TF-IDF Feature Extraction
* Linear Kernel

---

# 📊 Evaluasi Model

Model dievaluasi menggunakan metrik:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Selanjutnya dilakukan perbandingan performa antara algoritma **LSTM** dan **SVM** untuk menentukan model terbaik.

---

# 🛠 Library yang Digunakan

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* TensorFlow
* Scikit-Learn
* NLTK
* Sastrawi
* WordCloud
* Google Play Scraper
* Pickle

---

# 📁 Struktur Project

```text
UAS-KecerdasanBuatan
│
├── README.md
├── laporan_uas.md
├── AnalisisSentimenWondrBNI.ipynb
├── requirements.txt
│
├── dataset/
│     └── wondrbyBNI.csv
│
├── model/
│     ├── model_lstm.keras
│     ├── model_svm.pkl
│     ├── tokenizer.pkl
│     ├── tfidf.pkl
│     └── label_encoder.pkl
│
└── streamlit/
      ├── app.py
      └── assets/
```

---

# ▶️ Cara Menjalankan Project

## 1. Clone Repository

```bash
git clone https://github.com/username/UAS-KecerdasanBuatan.git
```

## 2. Install Dependency

```bash
pip install -r requirements.txt
```

## 3. Jalankan Notebook

Buka file:

```
AnalisisSentimenWondrBNI.ipynb
```

Kemudian jalankan seluruh cell secara berurutan.

---

# 📈 Hasil

Model **LSTM** dan **SVM** berhasil dibangun dan dievaluasi menggunakan metrik Accuracy, Precision, Recall, dan F1-Score. Berdasarkan hasil evaluasi, dilakukan perbandingan performa kedua algoritma untuk menentukan model yang memberikan hasil klasifikasi sentimen terbaik.

---

# 👥 Anggota Kelompok

* Putri Fitriani Azzahra 2406026
* Siti Maulida Rahayu 2406005

---

# 📚 Referensi

1. TensorFlow Documentation
2. Scikit-Learn Documentation
3. Google Play Scraper Documentation
4. NLTK Documentation
5. Sastrawi Documentation

---

⭐ **Terima kasih telah mengunjungi repository ini.**
