# 1. Judul Proyek

# Analisis Sentimen Ulasan Aplikasi Wondr by BNI Menggunakan Algoritma Long Short-Term Memory (LSTM) dan Support Vector Machine (SVM)

## Nama Kelompok

| No | Nama | NIM |
|----|------|-----|
| 1 | Putri Fitriani Azzahra | 2406026 |
| 2 | Siti Maulida Rahayu | 2406005 |

---

## Domain Proyek (Latar Belakang)

Perkembangan teknologi digital telah membawa perubahan yang signifikan pada berbagai sektor, salah satunya adalah sektor perbankan. Saat ini, berbagai layanan perbankan dapat diakses secara praktis melalui aplikasi **mobile banking**, sehingga masyarakat tidak lagi bergantung pada pelayanan di kantor cabang. Salah satu aplikasi mobile banking yang banyak digunakan di Indonesia adalah **Wondr by BNI**, yaitu aplikasi resmi milik PT Bank Negara Indonesia (Persero) Tbk. yang menyediakan berbagai layanan transaksi keuangan, seperti transfer dana, pembayaran tagihan, pembelian produk digital, hingga pengelolaan rekening secara daring.

Sebagai aplikasi yang digunakan oleh jutaan pengguna, Wondr by BNI menerima ribuan ulasan dari pengguna melalui Google Play Store. Ulasan tersebut berisi berbagai pendapat mengenai pengalaman pengguna dalam menggunakan aplikasi, baik berupa apresiasi terhadap fitur yang tersedia maupun kritik dan keluhan terkait performa aplikasi. Informasi tersebut merupakan sumber masukan yang sangat penting bagi pengembang dalam melakukan evaluasi dan pengembangan aplikasi agar sesuai dengan kebutuhan pengguna.

Namun, banyaknya jumlah ulasan yang terus bertambah setiap hari menyebabkan proses analisis secara manual menjadi kurang efektif. Selain membutuhkan waktu yang lama, setiap pengguna memiliki gaya bahasa, pilihan kata, serta cara penyampaian pendapat yang berbeda-beda sehingga proses identifikasi sentimen menjadi semakin sulit apabila dilakukan secara manual. Oleh karena itu, diperlukan suatu sistem yang mampu melakukan analisis sentimen secara otomatis untuk membantu mengelompokkan opini pengguna ke dalam kategori sentimen positif, netral, maupun negatif.

Analisis sentimen merupakan salah satu penerapan **Natural Language Processing (NLP)** yang bertujuan untuk mengidentifikasi opini atau emosi yang terkandung dalam suatu teks. Dengan memanfaatkan teknik NLP, sistem dapat membantu pengembang memahami persepsi pengguna terhadap aplikasi secara lebih cepat, objektif, dan efisien. Hasil analisis sentimen juga dapat digunakan sebagai dasar dalam menentukan prioritas perbaikan maupun pengembangan fitur aplikasi.

Pada penelitian ini digunakan dua algoritma klasifikasi yang berbeda, yaitu **Long Short-Term Memory (LSTM)** sebagai representasi metode **Deep Learning** dan **Support Vector Machine (SVM)** sebagai representasi metode **Machine Learning**. Algoritma LSTM dipilih karena memiliki kemampuan dalam memahami hubungan antar kata pada suatu kalimat sehingga mampu menangkap konteks teks dengan lebih baik. Sementara itu, algoritma SVM dipilih karena memiliki performa yang baik dalam proses klasifikasi data teks, khususnya ketika dikombinasikan dengan metode ekstraksi fitur **Term Frequency–Inverse Document Frequency (TF-IDF)**.

Penelitian ini bertujuan untuk membangun model analisis sentimen terhadap ulasan aplikasi Wondr by BNI menggunakan kedua algoritma tersebut, kemudian membandingkan performanya berdasarkan metrik evaluasi **Accuracy**, **Precision**, **Recall**, dan **F1-Score**. Hasil penelitian diharapkan dapat membantu pengembang dalam memahami opini pengguna secara otomatis serta menjadi referensi dalam memilih algoritma yang paling sesuai untuk proses analisis sentimen pada data ulasan aplikasi mobile.

### Referensi

Latar belakang penelitian ini didukung oleh beberapa penelitian terdahulu mengenai analisis sentimen menggunakan metode Machine Learning dan Deep Learning. Damayanti dkk. (2024) menunjukkan bahwa algoritma Long Short-Term Memory (LSTM) dan Support Vector Machine (SVM) mampu memberikan performa yang baik dalam klasifikasi sentimen pada ulasan aplikasi mobile. Penelitian lain juga menunjukkan bahwa penggunaan metode ekstraksi fitur TF-IDF yang dipadukan dengan algoritma SVM mampu meningkatkan akurasi klasifikasi pada data teks berbahasa Indonesia. Selain itu, beberapa penelitian mengenai analisis sentimen ulasan aplikasi di Google Play Store menyatakan bahwa klasifikasi otomatis dapat membantu pengembang dalam memahami kebutuhan pengguna serta meningkatkan kualitas layanan aplikasi.

Referensi lengkap yang digunakan dalam penelitian ini akan disajikan pada bagian **Daftar Referensi**.

# 2. Business Understanding

Business Understanding merupakan tahap awal dalam pengembangan sistem kecerdasan buatan yang bertujuan untuk memahami permasalahan yang akan diselesaikan, menentukan tujuan penelitian, mengidentifikasi pengguna sistem, serta merancang solusi yang akan diterapkan. Pada penelitian ini, Business Understanding difokuskan pada analisis sentimen terhadap ulasan pengguna aplikasi **Wondr by BNI** yang diperoleh dari Google Play Store.

---

## 2.1 Permasalahan Dunia Nyata

Aplikasi mobile banking menjadi salah satu layanan digital yang paling banyak digunakan masyarakat dalam melakukan berbagai transaksi keuangan. Sebagai salah satu aplikasi mobile banking di Indonesia, Wondr by BNI terus menerima ulasan dari pengguna melalui Google Play Store. Ulasan tersebut berisi pengalaman pengguna terhadap kualitas layanan, kemudahan penggunaan aplikasi, performa sistem, hingga berbagai kendala yang dialami selama menggunakan aplikasi.

Banyaknya jumlah ulasan yang terus bertambah setiap hari menyebabkan proses analisis secara manual menjadi tidak efisien. Selain membutuhkan waktu yang lama, proses tersebut juga rentan terhadap kesalahan karena setiap pengguna memiliki gaya bahasa, kosakata, dan cara penyampaian opini yang berbeda-beda. Akibatnya, pengembang akan kesulitan memperoleh informasi yang akurat mengenai persepsi pengguna terhadap aplikasi.

Melalui penerapan analisis sentimen berbasis Artificial Intelligence (AI), ulasan pengguna dapat diklasifikasikan secara otomatis ke dalam kategori sentimen positif, netral, maupun negatif. Informasi tersebut dapat digunakan sebagai dasar dalam melakukan evaluasi serta pengembangan aplikasi sehingga kualitas layanan yang diberikan kepada pengguna dapat terus ditingkatkan.

---

## 2.2 Literature Review

Beberapa penelitian terdahulu menunjukkan bahwa analisis sentimen merupakan salah satu penerapan Natural Language Processing (NLP) yang efektif untuk mengidentifikasi opini pengguna terhadap suatu produk atau layanan digital.

Damayanti dkk. (2024) melakukan penelitian mengenai analisis sentimen ulasan aplikasi Alfagift menggunakan algoritma Long Short-Term Memory (LSTM) dan Support Vector Machine (SVM). Hasil penelitian menunjukkan bahwa kedua algoritma mampu melakukan klasifikasi sentimen dengan baik, namun LSTM memiliki kemampuan yang lebih baik dalam memahami konteks kalimat karena memanfaatkan hubungan antar kata dalam suatu urutan teks.

Zandroto dkk. (2025) melakukan analisis sentimen terhadap ulasan aplikasi BCA Mobile menggunakan algoritma K-Nearest Neighbor (K-NN) dan Support Vector Machine (SVM). Penelitian tersebut menunjukkan bahwa algoritma SVM mampu menghasilkan performa klasifikasi yang lebih baik dibandingkan algoritma pembanding pada data ulasan aplikasi mobile.

Penelitian lain mengenai analisis sentimen ulasan aplikasi berbasis Google Play Store juga menunjukkan bahwa penggunaan metode ekstraksi fitur TF-IDF yang dikombinasikan dengan algoritma Support Vector Machine mampu meningkatkan kualitas representasi data teks sehingga menghasilkan akurasi klasifikasi yang tinggi.

Berdasarkan penelitian-penelitian tersebut, penelitian ini menggunakan dua pendekatan yang berbeda, yaitu algoritma Long Short-Term Memory (LSTM) sebagai metode Deep Learning dan Support Vector Machine (SVM) sebagai metode Machine Learning. Kedua algoritma tersebut kemudian dibandingkan untuk mengetahui metode yang memiliki performa terbaik dalam mengklasifikasikan sentimen ulasan aplikasi Wondr by BNI.

---

## 2.3 Tujuan Proyek

Penelitian ini memiliki beberapa tujuan sebagai berikut.

1. Mengumpulkan data ulasan aplikasi Wondr by BNI dari Google Play Store menggunakan Google Play Scraper.

2. Melakukan proses preprocessing terhadap data ulasan agar siap digunakan pada proses pelatihan model.

3. Membangun model analisis sentimen menggunakan algoritma Long Short-Term Memory (LSTM).

4. Membangun model analisis sentimen menggunakan algoritma Support Vector Machine (SVM).

5. Membandingkan performa kedua algoritma berdasarkan nilai Accuracy, Precision, Recall, dan F1-Score.

6. Menentukan algoritma yang memiliki performa terbaik untuk klasifikasi sentimen ulasan aplikasi Wondr by BNI.

---

## 2.4 User/Pengguna Sistem

Sistem analisis sentimen yang dibangun pada penelitian ini ditujukan kepada beberapa pengguna, yaitu:

### 1. Pengembang Aplikasi

Pengembang dapat memanfaatkan hasil analisis sentimen untuk mengetahui opini pengguna terhadap aplikasi Wondr by BNI sehingga dapat menentukan prioritas perbaikan maupun pengembangan fitur berdasarkan kebutuhan pengguna.

### 2. Peneliti

Penelitian ini dapat dijadikan sebagai referensi dalam pengembangan sistem analisis sentimen menggunakan metode Machine Learning maupun Deep Learning.

### 3. Mahasiswa

Mahasiswa dapat memanfaatkan penelitian ini sebagai media pembelajaran mengenai penerapan Natural Language Processing (NLP), TensorFlow, dan Scikit-Learn dalam proses klasifikasi data teks.

---

## 2.5 Solusi dan Manfaat Implementasi AI

Solusi yang ditawarkan pada penelitian ini adalah pembangunan sistem analisis sentimen berbasis Artificial Intelligence menggunakan teknik Natural Language Processing (NLP). Sistem dikembangkan untuk mengklasifikasikan ulasan pengguna aplikasi Wondr by BNI secara otomatis ke dalam kategori sentimen positif, netral, dan negatif.

Tahapan penelitian dimulai dari proses pengumpulan data menggunakan Google Play Scraper, kemudian dilanjutkan dengan preprocessing data yang meliputi case folding, cleaning text, tokenizing, stopword removal, dan stemming. Setelah itu dilakukan proses pembentukan model menggunakan algoritma Long Short-Term Memory (LSTM) dan Support Vector Machine (SVM).

Kedua model dievaluasi menggunakan Confusion Matrix, Accuracy, Precision, Recall, dan F1-Score. Selanjutnya dilakukan perbandingan performa untuk menentukan algoritma terbaik yang dapat digunakan dalam analisis sentimen ulasan aplikasi Wondr by BNI.

Penerapan Artificial Intelligence pada penelitian ini diharapkan mampu membantu pengembang dalam menganalisis ribuan ulasan pengguna secara otomatis sehingga proses evaluasi kualitas aplikasi menjadi lebih cepat, efisien, dan objektif.

# 3. Data Understanding

Data Understanding merupakan tahapan untuk memahami karakteristik dataset yang akan digunakan dalam proses pembangunan model machine learning. Pada tahap ini dilakukan identifikasi terhadap sumber data, ukuran dataset, atribut yang digunakan, tipe data, serta target klasifikasi. Pemahaman terhadap dataset sangat penting karena akan mempengaruhi proses preprocessing, pemilihan algoritma, hingga evaluasi model.

---

## 3.1 Sumber Data

Dataset yang digunakan pada penelitian ini berasal dari **Google Play Store** dengan objek penelitian berupa ulasan pengguna aplikasi **Wondr by BNI**. Proses pengambilan data dilakukan menggunakan library **google-play-scraper** pada bahasa pemrograman Python.

Pengambilan data dilakukan secara otomatis (*web scraping*) dengan memanfaatkan API yang disediakan oleh library tersebut. Dataset yang diperoleh berupa ulasan pengguna beserta informasi pendukung seperti nama pengguna, rating, tanggal ulasan, dan isi ulasan.

Proses scraping dilakukan terhadap aplikasi dengan ID:

```python
id.bni.wondr
```

Data kemudian disimpan dalam format **CSV** untuk memudahkan proses analisis dan preprocessing.

---

## 3.2 Deskripsi Dataset

Dataset yang digunakan merupakan kumpulan ulasan pengguna aplikasi Wondr by BNI yang diperoleh dari Google Play Store.

Setiap data merepresentasikan satu ulasan yang ditulis oleh pengguna beserta nilai rating yang diberikan. Nilai rating kemudian digunakan sebagai dasar dalam proses pelabelan sentimen, yaitu:

- Rating 4–5 → Positif
- Rating 3 → Netral
- Rating 1–2 → Negatif

Setelah proses pelabelan selesai, dataset digunakan sebagai data utama pada proses pelatihan model LSTM maupun Support Vector Machine.

Jumlah dataset yang berhasil dikumpulkan adalah sekitar **13.000 ulasan**.

---

## 3.3 Ukuran dan Format Data

Dataset disimpan dalam format **Comma Separated Values (CSV)** dengan nama file:

```
wondrbyBNI.csv
```

Jumlah data yang digunakan pada penelitian ini adalah sekitar **13.000 baris data**, dimana setiap baris merepresentasikan satu ulasan pengguna.

Secara umum dataset memiliki beberapa atribut utama yang digunakan selama penelitian.

---

## 3.4 Deskripsi Atribut

Tabel berikut menunjukkan atribut yang digunakan pada penelitian.

| No | Nama Atribut | Tipe Data | Keterangan |
|----|--------------|-----------|------------|
| 1 | userName | String | Nama pengguna Google Play Store |
| 2 | score | Integer | Rating yang diberikan pengguna (1–5) |
| 3 | at | Datetime | Tanggal ulasan dibuat |
| 4 | content | String | Isi ulasan pengguna |
| 5 | sentimen | Kategori | Label hasil pelabelan sentimen |
| 6 | cleaning | String | Hasil proses cleaning text |
| 7 | tokenizing | List | Hasil tokenisasi |
| 8 | stopword | String | Hasil stopword removal |
| 9 | stemming | String | Hasil stemming menggunakan Sastrawi |

Atribut yang digunakan sebagai fitur utama pada proses pelatihan model adalah kolom **stemming**, sedangkan atribut **sentimen** digunakan sebagai target klasifikasi.

---

## 3.5 Tipe Data dan Target Klasifikasi

Penelitian ini merupakan kasus **multiclass classification**, yaitu proses klasifikasi yang memiliki lebih dari dua kelas.

Target klasifikasi terdiri atas tiga kategori sentimen, yaitu:

| Label | Deskripsi |
|--------|-----------|
| Positif | Ulasan dengan rating 4 dan 5 |
| Netral | Ulasan dengan rating 3 |
| Negatif | Ulasan dengan rating 1 dan 2 |

Sebelum proses pelatihan model dilakukan, target sentimen diubah menjadi bentuk numerik menggunakan **Label Encoding** sehingga dapat diproses oleh algoritma machine learning maupun deep learning.

Sedangkan data teks pada kolom **stemming** digunakan sebagai fitur utama karena telah melalui seluruh tahapan preprocessing, sehingga kualitas data menjadi lebih baik dan siap digunakan dalam proses klasifikasi.

---

## 3.6 Insight Awal Dataset

Berdasarkan hasil pengamatan awal terhadap dataset, diperoleh beberapa informasi sebagai berikut.

- Dataset didominasi oleh ulasan dengan sentimen positif karena sebagian besar pengguna memberikan rating 4 dan 5.
- Masih terdapat beberapa ulasan yang mengandung karakter khusus, emoji, URL, angka, dan tanda baca sehingga perlu dilakukan preprocessing.
- Terdapat variasi panjang kalimat pada setiap ulasan, mulai dari satu kata hingga beberapa kalimat.
- Dataset memiliki karakteristik data teks berbahasa Indonesia sehingga diperlukan proses stemming menggunakan library **Sastrawi**.
- Karena distribusi kelas tidak sepenuhnya seimbang, evaluasi model tidak hanya menggunakan Accuracy, tetapi juga Precision, Recall, dan F1-Score agar hasil evaluasi lebih representatif.

 # 4. Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) merupakan tahapan untuk memahami karakteristik dataset sebelum dilakukan proses pemodelan. Tahap ini bertujuan untuk mengetahui pola data, distribusi kelas, kualitas data, serta memperoleh insight awal yang dapat digunakan sebagai dasar dalam proses preprocessing dan pemilihan model klasifikasi.

Pada penelitian ini, EDA dilakukan menggunakan beberapa visualisasi data seperti diagram batang (bar chart), diagram lingkaran (pie chart/donut chart), histogram, serta visualisasi kata yang paling sering muncul pada ulasan pengguna.

---

## 4.1 Distribusi Sentimen

Distribusi sentimen dilakukan untuk mengetahui jumlah data pada setiap kelas sentimen, yaitu positif, netral, dan negatif.

> *<img width="569" height="427" alt="image" src="https://github.com/user-attachments/assets/c47a7600-cb69-4f6d-b35e-b0f6dd7f94ad" />*  
> *Gambar 4.1 Grafik Distribusi Sentimen (Bar Chart)*

Berdasarkan grafik distribusi sentimen, terlihat bahwa sebagian besar ulasan pengguna berada pada kategori **positif**. Hal ini menunjukkan bahwa mayoritas pengguna memberikan pengalaman yang baik terhadap penggunaan aplikasi Wondr by BNI.

Sementara itu, jumlah ulasan dengan sentimen negatif dan netral relatif lebih sedikit dibandingkan sentimen positif. Kondisi ini menunjukkan bahwa dataset memiliki distribusi kelas yang tidak sepenuhnya seimbang (imbalanced dataset).

---

## 4.2 Persentase Distribusi Sentimen

Selain menggunakan diagram batang, distribusi sentimen juga divisualisasikan menggunakan diagram lingkaran (pie chart/donut chart) untuk melihat persentase masing-masing kelas sentimen.

> *<img width="439" height="370" alt="image" src="https://github.com/user-attachments/assets/63a8b49c-4536-4a38-887b-dde94f15c86c" />*  
> *Gambar 4.2 Diagram Donut Distribusi Sentimen*

Visualisasi tersebut menunjukkan proporsi masing-masing kelas sentimen dalam dataset. Sentimen Netral memiliki persentase terbesar, lalu disusul dengan Sentimen Positif, setelah itu sentimen negatif memiliki jumlah paling sedikit.

Visualisasi ini membantu memberikan gambaran umum mengenai kondisi dataset sebelum dilakukan proses pelatihan model.

---

## 4.3 Distribusi Rating Pengguna

Distribusi rating dilakukan untuk mengetahui banyaknya ulasan berdasarkan rating yang diberikan pengguna pada Google Play Store.

> *<img width="582" height="381" alt="image" src="https://github.com/user-attachments/assets/d4275803-6880-449d-b89c-116e99c3e317" />*  
> *Gambar 4.3 Grafik Distribusi Rating*

Berdasarkan hasil visualisasi, rating 5 merupakan rating yang paling banyak diberikan oleh pengguna. Hal tersebut menunjukkan bahwa sebagian besar pengguna merasa puas terhadap layanan aplikasi Wondr by BNI.

Sebaliknya, rating 1 dan 2 memiliki jumlah yang lebih sedikit, namun tetap memberikan informasi penting mengenai berbagai kendala yang dialami pengguna.

---

## 4.4 Distribusi Panjang Ulasan

Analisis panjang ulasan dilakukan untuk mengetahui karakteristik teks yang digunakan oleh pengguna dalam memberikan ulasan.

> *<img width="581" height="371" alt="image" src="https://github.com/user-attachments/assets/b521e834-14a0-410a-8567-6019d78fa872" />*  
> *Gambar 4.4 Histogram Panjang Ulasan*

Hasil visualisasi menunjukkan bahwa sebagian besar pengguna menuliskan ulasan dengan panjang kalimat yang relatif pendek hingga sedang. Namun demikian, terdapat beberapa ulasan yang memiliki jumlah kata cukup panjang sehingga proses preprocessing diperlukan untuk menyeragamkan representasi data.

---

## 4.5 Kata yang Paling Sering Muncul

Analisis frekuensi kata dilakukan untuk mengetahui kata-kata yang paling sering muncul setelah proses preprocessing.

> *<img width="728" height="426" alt="image" src="https://github.com/user-attachments/assets/2e376929-acdd-487c-bfc4-d6f0e6b61d4d" />*
> *<img width="871" height="464" alt="image" src="https://github.com/user-attachments/assets/aa353dd6-84bd-46fc-9c75-1e313a5c2f46" />* 
> *Gambar 4.5 Top 20 Kata Terbanyak*

Berdasarkan hasil visualisasi, beberapa kata muncul dengan frekuensi yang tinggi pada dataset. Kata-kata tersebut menggambarkan topik utama yang sering dibahas oleh pengguna, seperti kualitas aplikasi, proses login, transaksi, maupun performa sistem.

Analisis ini membantu memahami konteks umum dari ulasan yang diberikan pengguna.

---

## 4.6 Analisis Korelasi Antar Fitur

Pada penelitian ini tidak dilakukan analisis korelasi menggunakan heatmap maupun pairplot.

Hal tersebut dikarenakan dataset yang digunakan merupakan **data teks (text mining)**, sehingga tidak memiliki banyak atribut numerik yang dapat dihitung hubungan korelasinya seperti pada kasus prediksi data tabular.

> *<img width="511" height="302" alt="image" src="https://github.com/user-attachments/assets/514f253a-e698-4738-8bb4-209d507e8a84" />*
> *Gambar 4.6 Heatmap Korelasi*

Sebagai gantinya, analisis dilakukan melalui distribusi sentimen, distribusi rating, serta frekuensi kemunculan kata yang lebih sesuai untuk karakteristik data teks.

---

## 4.7 Analisis Ketidakseimbangan Data (Imbalanced Dataset)

Distribusi sentimen menunjukkan bahwa jumlah data pada setiap kelas tidak sama.

Kelas sentimen positif memiliki jumlah data yang lebih banyak dibandingkan kelas netral maupun negatif. Kondisi ini disebut sebagai **imbalanced dataset**.

Dataset yang tidak seimbang dapat mempengaruhi performa model karena model cenderung lebih mudah mempelajari kelas mayoritas. Oleh karena itu, pada penelitian ini proses evaluasi tidak hanya menggunakan metrik Accuracy, tetapi juga Precision, Recall, dan F1-Score agar performa model dapat dinilai secara lebih objektif.

---

## 4.8 Insight Awal Dataset

Berdasarkan hasil Exploratory Data Analysis, diperoleh beberapa insight sebagai berikut.

- Sebagian besar ulasan pengguna memiliki sentimen positif.
- Rating 5 merupakan rating yang paling banyak diberikan oleh pengguna.
- Dataset memiliki distribusi kelas yang tidak sepenuhnya seimbang.
- Panjang ulasan cukup bervariasi sehingga diperlukan preprocessing sebelum proses pelatihan model.
- Kata-kata yang paling sering muncul menunjukkan bahwa pengguna banyak membahas performa aplikasi, proses transaksi, serta pengalaman penggunaan aplikasi.
- Dataset sudah memenuhi kebutuhan untuk digunakan dalam pembangunan model klasifikasi sentimen menggunakan algoritma Long Short-Term Memory (LSTM) dan Support Vector Machine (SVM).

# 5. Data Preparation

Data Preparation merupakan tahapan untuk mempersiapkan data sebelum digunakan dalam proses pelatihan model Machine Learning maupun Deep Learning. Tahapan ini bertujuan untuk meningkatkan kualitas data dengan menghilangkan informasi yang tidak diperlukan, menyeragamkan format teks, serta mengubah data menjadi representasi numerik yang dapat diproses oleh algoritma klasifikasi.

Pada penelitian ini dilakukan beberapa tahapan preprocessing, yaitu data cleaning, case folding, cleaning text, tokenizing, stopword removal, stemming, pelabelan sentimen, pembagian data latih dan data uji, serta transformasi data sesuai kebutuhan masing-masing algoritma.

---

## 5.1 Data Cleaning

Tahap pertama adalah melakukan pemeriksaan terhadap dataset hasil scraping dari Google Play Store. Proses ini bertujuan untuk memastikan bahwa data yang digunakan memiliki kualitas yang baik sebelum dilakukan preprocessing lebih lanjut.

Pada tahap ini dilakukan pengecekan terhadap:

- Missing value
- Data duplikat
- Struktur dataset
- Tipe data setiap atribut

Apabila ditemukan data yang kosong atau duplikat, maka data tersebut dihapus agar tidak mempengaruhi proses pelatihan model.

> *<img width="283" height="379" alt="image" src="https://github.com/user-attachments/assets/28817700-54ea-4a3a-8947-9127c76641db" />*
> *Gambar 5.1 Hasil pengecekan missing value dan data duplikat.*

---

## 5.2 Case Folding

Case Folding merupakan proses mengubah seluruh huruf pada teks menjadi huruf kecil (lowercase). Tahapan ini bertujuan agar kata yang memiliki penulisan berbeda, seperti **"Bagus"** dan **"bagus"**, dianggap sebagai kata yang sama.

Contoh:

| Sebelum | Sesudah |
|---------|----------|
| Aplikasi BAGUS Sekali | aplikasi bagus sekali |

Tahapan ini membantu mengurangi variasi kata yang sebenarnya memiliki makna yang sama.

---

## 5.3 Cleaning Text

Cleaning Text dilakukan untuk menghapus karakter yang tidak memiliki pengaruh terhadap analisis sentimen.

Karakter yang dihapus meliputi:

- URL
- Mention (@)
- Hashtag (#)
- Emoji
- Angka
- Tanda baca
- Karakter khusus
- Spasi berlebih

Contoh:

| Sebelum | Sesudah |
|---------|----------|
| Aplikasi bagus!!! 😍😍 | aplikasi bagus |

Dengan proses ini, data menjadi lebih bersih sehingga memudahkan proses analisis selanjutnya.

---

## 5.4 Tokenizing

Tokenizing merupakan proses memecah sebuah kalimat menjadi kumpulan kata atau token.

Contoh:

Kalimat:

```
aplikasi sangat membantu transaksi
```

Hasil tokenizing:

```
["aplikasi","sangat","membantu","transaksi"]
```

Tahapan ini diperlukan agar setiap kata dapat diproses secara individual pada tahap preprocessing berikutnya.

---

## 5.5 Stopword Removal

Stopword Removal bertujuan menghapus kata-kata umum yang tidak memberikan informasi penting terhadap proses klasifikasi sentimen.

Contoh stopword:

- yang
- dan
- di
- ke
- untuk
- dengan
- adalah

Contoh:

| Sebelum | Sesudah |
|---------|----------|
| aplikasi ini sangat bagus | aplikasi bagus |

Penghapusan stopword mampu mengurangi jumlah kata yang tidak memiliki kontribusi terhadap proses klasifikasi.

---

## 5.6 Stemming

Stemming merupakan proses mengubah kata berimbuhan menjadi kata dasar menggunakan library **Sastrawi**.

Contoh:

| Sebelum | Sesudah |
|---------|----------|
| menggunakan | guna |
| pembayaran | bayar |
| transaksi | transaksi |

Dengan proses stemming, variasi kata yang memiliki arti sama dapat disatukan sehingga ukuran kosakata menjadi lebih kecil.

Kolom hasil stemming digunakan sebagai fitur utama pada proses pelatihan model.

---

## 5.7 Pelabelan Sentimen

Setelah preprocessing selesai dilakukan, setiap ulasan diberikan label sentimen berdasarkan nilai rating yang diberikan pengguna pada Google Play Store.

Aturan pelabelan yang digunakan adalah sebagai berikut.

| Rating | Label Sentimen |
|---------|----------------|
| 4 – 5 | Positif |
| 3 | Netral |
| 1 – 2 | Negatif |

> *<img width="434" height="227" alt="image" src="https://github.com/user-attachments/assets/a306267f-10a5-493a-8986-c0afdeed6430" />*

Metode pelabelan ini dipilih karena rating dianggap mampu merepresentasikan kepuasan pengguna terhadap aplikasi.

---

## 5.8 Label Encoding

Label sentimen yang masih berbentuk kategori diubah menjadi nilai numerik menggunakan **Label Encoder**.

Contoh hasil encoding:

| Label | Nilai |
|--------|--------|
| Negatif | 0 |
| Netral | 1 |
| Positif | 2 |

Label Encoding diperlukan agar algoritma Machine Learning maupun Deep Learning dapat memproses target klasifikasi.

---

## 5.9 One Hot Encoding (LSTM)

Karena model LSTM menggunakan fungsi aktivasi **Softmax** dengan **Categorical Crossentropy**, maka target klasifikasi diubah menjadi bentuk One Hot Encoding.

Contoh:

| Label | One Hot |
|---------|----------------|
| Negatif | [1,0,0] |
| Netral | [0,1,0] |
| Positif | [0,0,1] |

Tahapan ini hanya diterapkan pada model LSTM.

---

## 5.10 Train Test Split

Dataset kemudian dibagi menjadi dua bagian, yaitu data latih dan data uji.

Pembagian data dilakukan menggunakan metode **Train-Test Split** dengan komposisi:

- Data Latih : **80%**
- Data Uji : **20%**

Pembagian data dilakukan secara **stratified** sehingga proporsi masing-masing kelas tetap terjaga pada data latih maupun data uji.

---

## 5.11 Tokenizer dan Padding Sequence (LSTM)

Pada model Long Short-Term Memory (LSTM), data teks tidak dapat langsung diproses sehingga perlu diubah menjadi representasi numerik menggunakan **Tokenizer**.

Tokenizer memberikan indeks pada setiap kata berdasarkan frekuensi kemunculannya dalam dataset.

Selanjutnya dilakukan **Padding Sequence** agar seluruh kalimat memiliki panjang yang sama.

Pada penelitian ini digunakan parameter sebagai berikut.

| Parameter | Nilai |
|------------|--------|
| Vocabulary Size | 10000 |
| Maximum Length | 100 |

Padding dilakukan menggunakan metode **post-padding**, sehingga nilai padding ditambahkan pada bagian akhir setiap kalimat.

---

## 5.12 TF-IDF Vectorization (SVM)

Berbeda dengan model LSTM, algoritma Support Vector Machine menggunakan representasi fitur berupa **Term Frequency – Inverse Document Frequency (TF-IDF)**.

TF-IDF memberikan bobot terhadap setiap kata berdasarkan frekuensi kemunculannya pada suatu dokumen serta keseluruhan dataset.

Melalui proses ini, setiap dokumen diubah menjadi sebuah vektor numerik yang kemudian digunakan sebagai input bagi algoritma SVM.

Representasi TF-IDF dipilih karena terbukti efektif dalam proses klasifikasi data teks dan mampu meningkatkan performa algoritma Machine Learning.

---

## 5.13 Hasil Data Preparation

Setelah seluruh tahapan preprocessing selesai dilakukan, dataset telah siap digunakan pada proses pembangunan model klasifikasi sentimen.

Tahapan Data Preparation menghasilkan dua jenis representasi data yang berbeda, yaitu:

- **Tokenizer + Padding Sequence** untuk model Long Short-Term Memory (LSTM).
- **TF-IDF Vectorization** untuk model Support Vector Machine (SVM).

Seluruh proses preprocessing dilakukan menggunakan bahasa pemrograman Python dengan bantuan beberapa library, di antaranya **Pandas**, **NLTK**, **Sastrawi**, **Scikit-Learn**, dan **TensorFlow**.


# 6. Modeling

Pada tahap Modeling dilakukan pembangunan model klasifikasi sentimen menggunakan dua algoritma yang berbeda, yaitu **Long Short-Term Memory (LSTM)** dan **Support Vector Machine (SVM)**. Kedua algoritma dipilih karena memiliki karakteristik yang berbeda sehingga dapat dibandingkan performanya dalam mengklasifikasikan sentimen ulasan aplikasi Wondr by BNI.

Model pertama menggunakan pendekatan **Deep Learning**, sedangkan model kedua menggunakan pendekatan **Machine Learning**. Seluruh model dibangun menggunakan bahasa pemrograman Python pada Google Colaboratory.

---

## 6.1 Long Short-Term Memory (LSTM)

Long Short-Term Memory (LSTM) merupakan salah satu pengembangan dari Recurrent Neural Network (RNN) yang dirancang untuk mengatasi permasalahan *vanishing gradient*. LSTM memiliki kemampuan menyimpan informasi jangka panjang sehingga sangat sesuai digunakan pada data teks yang memiliki hubungan antar kata.

Pada penelitian ini, model LSTM digunakan untuk mempelajari pola kalimat dari ulasan pengguna aplikasi Wondr by BNI sehingga mampu mengklasifikasikan sentimen menjadi tiga kelas, yaitu **Positif**, **Netral**, dan **Negatif**.

### Persiapan Data

Sebelum dilakukan pelatihan model, data teks diproses menggunakan beberapa tahapan sebagai berikut.

- Label Encoding
- Train-Test Split (80:20)
- Tokenizer
- Padding Sequence
- One-Hot Encoding

Tokenizer digunakan untuk mengubah kata menjadi indeks numerik, sedangkan Padding Sequence digunakan agar seluruh data memiliki panjang yang sama sehingga dapat diproses oleh jaringan saraf.

---

### Arsitektur Model

Arsitektur model LSTM yang digunakan pada penelitian ini terdiri dari beberapa lapisan sebagai berikut.

| Layer | Parameter |
|--------|-----------|
| Embedding | Input Dim = 10000, Output Dim = 128 |
| Bidirectional LSTM | 128 Unit |
| Dropout | 0.3 |
| Bidirectional LSTM | 64 Unit |
| Dropout | 0.3 |
| Dense | 64 Unit (ReLU) |
| Dropout | 0.3 |
| Output | 3 Unit (Softmax) |

Model dibangun menggunakan TensorFlow dan Keras dengan optimizer **Adam** serta fungsi loss **Categorical Crossentropy**.

---

### Parameter Training

Parameter pelatihan model ditunjukkan pada tabel berikut.

| Parameter | Nilai |
|-----------|-------|
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Epoch | 15 |
| Batch Size | 32 |
| Validation Split | Data Uji (20%) |
| EarlyStopping | Ya |
| ReduceLROnPlateau | Ya |
| ModelCheckpoint | Ya |

EarlyStopping digunakan untuk menghentikan proses pelatihan apabila model sudah tidak mengalami peningkatan performa sehingga dapat mengurangi risiko overfitting.

> *<img width="1142" height="268" alt="image" src="https://github.com/user-attachments/assets/1b73fec1-780d-4ad0-87b1-ff0f7d6edeac" />*
---

### Hasil Pelatihan

Setelah proses training selesai, model menghasilkan nilai Accuracy dan Loss pada data latih maupun data validasi.

> *<img width="1209" height="350" alt="image" src="https://github.com/user-attachments/assets/310b7301-e866-446a-8038-0a9d8b381d0e" />*

Grafik tersebut menunjukkan perubahan nilai Accuracy dan Loss selama proses pelatihan sehingga dapat digunakan untuk mengetahui apakah model mengalami overfitting atau underfitting.

---

## 6.2 Support Vector Machine (SVM)

Support Vector Machine (SVM) merupakan algoritma Machine Learning yang bekerja dengan mencari hyperplane terbaik untuk memisahkan setiap kelas.

Pada penelitian ini, algoritma SVM digunakan sebagai model pembanding terhadap LSTM karena dikenal memiliki performa yang baik pada klasifikasi data teks.

---

### Persiapan Data

Berbeda dengan model LSTM, model SVM menggunakan ekstraksi fitur **TF-IDF (Term Frequency–Inverse Document Frequency)**.

Tahapan yang dilakukan yaitu:

- Train-Test Split
- TF-IDF Vectorization
- Training SVM

TF-IDF digunakan untuk mengubah data teks menjadi representasi numerik sehingga dapat diproses oleh algoritma SVM.

---

### Parameter Model

Parameter model SVM yang digunakan adalah sebagai berikut.

| Parameter | Nilai |
|-----------|-------|
| Kernel | Linear |
| Random State | 42 |

Kernel Linear dipilih karena sesuai digunakan pada proses klasifikasi data teks yang memiliki dimensi tinggi.

---

### Hasil Pelatihan

Setelah proses training selesai, model SVM berhasil melakukan klasifikasi sentimen terhadap data uji menggunakan representasi fitur TF-IDF.

Model kemudian dievaluasi menggunakan Accuracy, Precision, Recall, F1-Score, dan Confusion Matrix.

> *<img width="416" height="132" alt="image" src="https://github.com/user-attachments/assets/294eada3-66c7-406f-a21c-4f7a1642737e" />*
> *<img width="410" height="370" alt="image" src="https://github.com/user-attachments/assets/4ce7156f-4fb8-47ef-93fe-5e1b81d6560f" />*
> *<img width="232" height="159" alt="image" src="https://github.com/user-attachments/assets/741a07f2-54e6-48f5-9c2b-0575b942d1ac" />*
---

## 6.3 Perbandingan Model

Setelah kedua model selesai dilatih, dilakukan perbandingan performa menggunakan metrik evaluasi yang sama sehingga hasil yang diperoleh dapat dibandingkan secara objektif.

Metrik evaluasi yang digunakan meliputi:

- Accuracy
- Precision
- Recall
- F1-Score

Hasil evaluasi kedua model kemudian ditampilkan dalam bentuk tabel dan grafik.

> *<img width="449" height="195" alt="image" src="https://github.com/user-attachments/assets/51fbdfe9-745a-4eca-b1c4-f77e04d02922" />*
> *<img width="560" height="377" alt="image" src="https://github.com/user-attachments/assets/5ce540d1-84a4-40a0-a7c8-a2bf9dc7d7d6" />*

---

## 6.4 Pemilihan Model Terbaik

Model terbaik ditentukan berdasarkan nilai Accuracy, Precision, Recall, dan F1-Score yang diperoleh pada data uji.

Apabila model LSTM memperoleh nilai evaluasi yang lebih tinggi dibandingkan SVM, maka model LSTM dipilih sebagai model terbaik. Sebaliknya, apabila model SVM menghasilkan performa yang lebih baik, maka model tersebut dipilih sebagai model utama.

Berdasarkan hasil pengujian pada penelitian ini, model dengan performa terbaik selanjutnya digunakan pada tahap implementasi sistem analisis sentimen.


# 7. Evaluation

Tahap Evaluation bertujuan untuk mengetahui performa model dalam mengklasifikasikan sentimen ulasan aplikasi Wondr by BNI. Pada penelitian ini digunakan dua algoritma klasifikasi, yaitu **Long Short-Term Memory (LSTM)** dan **Support Vector Machine (SVM)**.

Evaluasi dilakukan menggunakan beberapa metrik, yaitu **Accuracy**, **Precision**, **Recall**, **F1-Score**, **Classification Report**, serta **Confusion Matrix**. Selain itu, dilakukan pula perbandingan performa kedua algoritma untuk menentukan model terbaik.

---

## 7.1 Evaluasi Model Long Short-Term Memory (LSTM)

Model LSTM dievaluasi menggunakan data uji yang tidak pernah digunakan selama proses pelatihan. Hasil evaluasi diperoleh dari fungsi `model.evaluate()` serta `classification_report()` pada library Scikit-Learn.

### Accuracy, Precision, Recall, F1-Score

Accuracy merupakan persentase jumlah prediksi yang benar dibandingkan seluruh data uji. Precision digunakan untuk mengukur tingkat ketepatan model dalam memberikan prediksi terhadap suatu kelas.Recall digunakan untuk mengetahui kemampuan model dalam menemukan seluruh data yang benar pada setiap kelas. F1-Score merupakan rata-rata harmonik antara Precision dan Recall.

> *<img width="801" height="454" alt="image" src="https://github.com/user-attachments/assets/2c90dd9f-0aa1-4994-ba1e-b3256a556c32" />*
---

### Classification Report

Classification Report menampilkan nilai Precision, Recall, F1-Score, dan Support pada masing-masing kelas sentimen.

> *<img width="447" height="228" alt="image" src="https://github.com/user-attachments/assets/5586ba91-5116-4708-b4a5-7e95e7c33fc3" />*
---

### Confusion Matrix

Confusion Matrix digunakan untuk melihat jumlah prediksi yang benar maupun salah pada setiap kelas sentimen.

> *<img width="447" height="428" alt="image" src="https://github.com/user-attachments/assets/3ef3f6b1-68f0-43d9-8d27-f9e6fae324b9" />*

Berdasarkan Confusion Matrix dapat diketahui bahwa sebagian besar data berhasil diklasifikasikan dengan benar oleh model LSTM. Namun masih terdapat beberapa data yang salah diklasifikasikan terutama pada kelas yang memiliki jumlah data lebih sedikit.

---

## 7.2 Evaluasi Model Support Vector Machine (SVM)

Model Support Vector Machine dievaluasi menggunakan data uji yang sama sehingga hasil evaluasi dapat dibandingkan secara objektif dengan model LSTM.

### Accuracy, Precision, Recall, F1-Score

> *<img width="898" height="507" alt="image" src="https://github.com/user-attachments/assets/58f429b8-1790-4a2d-9de3-55287b44a3bd" />*

---

### Classification Report

> *<img width="391" height="130" alt="image" src="https://github.com/user-attachments/assets/2ff42faa-b2f4-4e63-8b10-0871946caec7" />*

---

### Confusion Matrix

> *<img width="403" height="360" alt="image" src="https://github.com/user-attachments/assets/9647fd6a-e8a2-4474-aa9f-951daca5b4a0" />*

Berdasarkan hasil evaluasi, model SVM mampu melakukan klasifikasi sentimen dengan baik menggunakan representasi fitur TF-IDF. Nilai evaluasi yang diperoleh kemudian dibandingkan dengan model LSTM untuk mengetahui algoritma yang memiliki performa terbaik.

---

## 7.3 Perbandingan Performa Algoritma

Perbandingan dilakukan menggunakan empat metrik utama, yaitu Accuracy, Precision, Recall, dan F1-Score.

| Metrik | LSTM | SVM |
|---------|------|-----|
| Accuracy | ... | ... |
| Precision | ... | ... |
| Recall | ... | ... |
| F1-Score | ... | ... |

> *<img width="471" height="296" alt="image" src="https://github.com/user-attachments/assets/956efdc4-f041-4b8f-96f5-b7d268962351" />
*

---

### Grafik Perbandingan

Selain menggunakan tabel, hasil evaluasi divisualisasikan menggunakan grafik batang agar perbedaan performa kedua algoritma dapat terlihat dengan lebih jelas.

> *<img width="623" height="383" alt="image" src="https://github.com/user-attachments/assets/b76566c6-9892-4286-a95a-ddd636275c1f" />*

---

## 7.4 Analisis Hasil

Berdasarkan hasil evaluasi diketahui bahwa kedua algoritma mampu melakukan klasifikasi sentimen terhadap ulasan aplikasi Wondr by BNI dengan performa yang baik. Namun demikian, terdapat perbedaan karakteristik antara kedua algoritma.

Model **Long Short-Term Memory (LSTM)** memiliki kemampuan yang lebih baik dalam memahami hubungan antar kata karena memanfaatkan struktur jaringan saraf berurutan (*sequence model*). Hal ini memungkinkan model mengenali konteks kalimat secara lebih mendalam sehingga menghasilkan performa yang tinggi pada data teks.

Di sisi lain, **Support Vector Machine (SVM)** memiliki proses pelatihan yang lebih cepat serta lebih ringan dibandingkan LSTM. Dengan bantuan ekstraksi fitur TF-IDF, model SVM mampu memberikan hasil klasifikasi yang cukup baik meskipun tidak mempertimbangkan urutan kata dalam suatu kalimat.

Perbedaan tersebut menunjukkan bahwa algoritma Deep Learning cenderung unggul dalam memahami konteks bahasa, sedangkan algoritma Machine Learning lebih efisien dari sisi komputasi.

---

## 7.5 Model Terbaik

Berdasarkan hasil perbandingan Accuracy, Precision, Recall, dan F1-Score, model dengan nilai evaluasi tertinggi dipilih sebagai model terbaik.

Model tersebut kemudian digunakan sebagai model utama pada implementasi sistem analisis sentimen karena memiliki kemampuan klasifikasi yang lebih baik dibandingkan model pembanding.

# 8. Kesimpulan dan Rekomendasi

## 8.1 Ringkasan Hasil Modeling dan Evaluasi

Penelitian ini berhasil membangun sistem analisis sentimen terhadap ulasan pengguna aplikasi **Wondr by BNI** menggunakan dua algoritma klasifikasi, yaitu **Long Short-Term Memory (LSTM)** dan **Support Vector Machine (SVM)**. Dataset penelitian diperoleh melalui proses scraping ulasan pengguna pada Google Play Store, kemudian dilakukan tahapan preprocessing yang meliputi data cleaning, case folding, cleaning text, tokenizing, stopword removal, stemming, pelabelan sentimen, serta transformasi data sesuai kebutuhan masing-masing algoritma.

Model LSTM dibangun menggunakan arsitektur **Bidirectional LSTM** dengan lapisan Embedding, Bidirectional LSTM, Dropout, Dense, dan Softmax. Sementara itu, model SVM dibangun menggunakan representasi fitur **TF-IDF** dengan kernel linear.

Berdasarkan hasil evaluasi menggunakan metrik Accuracy, Precision, Recall, dan F1-Score, kedua algoritma mampu melakukan klasifikasi sentimen dengan baik. Selain itu, evaluasi juga dilakukan menggunakan Classification Report dan Confusion Matrix untuk mengetahui kemampuan model dalam mengklasifikasikan setiap kelas sentimen.

Selanjutnya dilakukan perbandingan performa kedua algoritma untuk mengetahui model yang memberikan hasil terbaik terhadap dataset ulasan aplikasi Wondr by BNI.

---

## 8.2 Apakah Tujuan Proyek Tercapai?

Tujuan utama penelitian ini adalah membangun sistem analisis sentimen menggunakan dua algoritma berbeda serta membandingkan performanya dalam mengklasifikasikan ulasan aplikasi Wondr by BNI.

Berdasarkan hasil penelitian yang telah dilakukan, seluruh tujuan penelitian dapat tercapai, yaitu:

- Berhasil mengumpulkan dataset ulasan aplikasi Wondr by BNI dari Google Play Store.
- Berhasil melakukan preprocessing data menggunakan tahapan NLP.
- Berhasil membangun model klasifikasi sentimen menggunakan algoritma LSTM.
- Berhasil membangun model klasifikasi sentimen menggunakan algoritma SVM.
- Berhasil melakukan evaluasi model menggunakan Accuracy, Precision, Recall, F1-Score, Classification Report, dan Confusion Matrix.
- Berhasil membandingkan performa kedua algoritma sehingga diperoleh model dengan performa terbaik.

Dengan demikian, sistem yang dibangun telah mampu mengklasifikasikan sentimen pengguna ke dalam kategori **Positif**, **Netral**, dan **Negatif** secara otomatis.

---

## 8.3 Kelebihan dan Keterbatasan Model

### Kelebihan

Penelitian ini memiliki beberapa kelebihan, antara lain:

- Menggunakan dataset ulasan asli dari Google Play Store sehingga mencerminkan opini pengguna secara nyata.
- Menerapkan tahapan preprocessing NLP secara lengkap untuk meningkatkan kualitas data.
- Menggunakan dua pendekatan berbeda, yaitu Deep Learning (LSTM) dan Machine Learning (SVM), sehingga memungkinkan dilakukan perbandingan performa.
- Sistem mampu melakukan prediksi sentimen terhadap ulasan baru melalui implementasi aplikasi Streamlit.
- Hasil evaluasi disajikan menggunakan berbagai metrik sehingga performa model dapat dianalisis secara menyeluruh.

### Keterbatasan

Meskipun menghasilkan performa yang baik, penelitian ini masih memiliki beberapa keterbatasan, yaitu:

- Dataset hanya berasal dari satu aplikasi sehingga belum mewakili seluruh aplikasi mobile banking.
- Pelabelan sentimen dilakukan berdasarkan rating pengguna sehingga belum sepenuhnya menggambarkan isi teks ulasan.
- Model hanya mengklasifikasikan tiga kategori sentimen, yaitu Positif, Netral, dan Negatif.
- Penelitian belum mempertimbangkan aspek seperti ironi, sarkasme, atau bahasa gaul yang sering muncul pada ulasan pengguna.

---

## 8.4 Rekomendasi Pengembangan

Berdasarkan hasil penelitian, beberapa pengembangan yang dapat dilakukan pada penelitian selanjutnya antara lain:

- Menggunakan jumlah dataset yang lebih besar agar model memperoleh informasi yang lebih beragam.
- Menggunakan teknik pelabelan sentimen secara manual atau semi-otomatis sehingga kualitas label menjadi lebih akurat.
- Membandingkan performa dengan algoritma Deep Learning lainnya seperti GRU, BiLSTM, atau Transformer (BERT).
- Menggunakan teknik penyeimbangan data apabila distribusi kelas tidak seimbang.
- Mengembangkan sistem agar mampu melakukan analisis sentimen secara real-time dari berbagai sumber, seperti media sosial maupun platform ulasan lainnya.
- Menambahkan fitur visualisasi dashboard yang lebih interaktif sehingga memudahkan pengguna dalam memahami hasil analisis sentimen.


# 9. Referensi

Berikut merupakan referensi yang digunakan pada penelitian ini.
> 1. Zandroto, Y. Y., Vitianingsih, A. V., Maukar, A. L., Hikmawati, N. K., & Hamidan, R. (2025). Sentiment analysis of BCA Mobile app reviews using K-Nearest Neighbour and Support Vector Machine algorithm. Indonesian Journal of Artificial Intelligence and Data Mining, 8(2), 448–458. https://doi.org/10.24014/ijaidm.v8i2.37773
> 2. Pratama, J. A. (2023). Penerapan metode Support Vector Machine dan Naïve Bayes pada klasifikasi sentimen review aplikasi WhatsApp. Jurnal Komputer dan Informatika, 18(1), 38–45.
> 3. Santika, B., & Hidayah, A. K. (2025). Implementation of Support Vector Machine for sentiment analysis on Blibli app reviews on Play Store. Jurnal Vocational Teknik Elektronika dan Informatika, 13(2). https://doi.org/10.24036/voteteknika.v13i2.133666
> 4. Rizkiyanto, M. D., Purbolaksono, M. D., & Astuti, W. (2024). Sentiment analysis classification on PLN Mobile application reviews using Random Forest method and TF-IDF feature extraction. INTEK Jurnal Penelitian, 11(1), 37–43. https://doi.org/10.31963/intek.v11i1.4774
> 5. Damayanti, E., Vitianingsih, A. V., Kacung, S., Cahyono, D., & Maukar, A. L. (2024). Sentiment analysis of Alfagift application user reviews using Long Short-Term Memory (LSTM) and Support Vector Machine (SVM) methods. DECODE: Jurnal Pendidikan Teknologi Informasi, 4(2), 509–521. https://doi.org/10.51454/decode.v4i2.478
> 6. Indonesian sentiment analysis towards MyPertamina application reviews by utilizing machine learning algorithms. (2022).
> 7. Analisis sentimen Grab Indonesia pada ulasan Google Play Store menggunakan algoritma Naïve Bayes dan Support Vector Machine. (2025).


# 10. Lampiran

Lampiran berisi dokumentasi proses penelitian yang mendukung hasil analisis serta implementasi sistem.

## Lampiran A. Dataset

- Dataset hasil scraping Google Play Store.
- Jumlah data yang digunakan dalam penelitian.
- Contoh beberapa data ulasan pengguna.

> <img width="447" height="356" alt="image" src="https://github.com/user-attachments/assets/342c900a-2e38-4f8d-b88a-f2ce91d3a8a5" /> 
> <img width="1207" height="228" alt="image" src="https://github.com/user-attachments/assets/ca64c0e7-d5a9-4626-8b9f-f007ee600d04" />
---

## Lampiran B. Hasil Preprocessing

Tahapan preprocessing yang dilakukan meliputi:

- Data Cleaning
- Case Folding
- Cleaning Text
- Tokenizing
- Stopword Removal
- Stemming
- Pelabelan Sentimen

> <img width="301" height="377" alt="image" src="https://github.com/user-attachments/assets/e32a6711-c003-4039-afd4-f37a6624f2c1" />
>  <img width="528" height="193" alt="image" src="https://github.com/user-attachments/assets/987dc3c1-299b-4dde-826b-0efb393ad5f2" />
> <img width="517" height="198" alt="image" src="https://github.com/user-attachments/assets/27dbf622-58e9-4af0-9228-a1731c8b47fa" />
> <img width="506" height="192" alt="image" src="https://github.com/user-attachments/assets/c183f208-f8a7-429d-ab93-a2802d23bc79" />
> <img width="527" height="184" alt="image" src="https://github.com/user-attachments/assets/de63dca3-1c33-4145-896a-c983541c5a31" />
> <img width="519" height="196" alt="image" src="https://github.com/user-attachments/assets/b7388fc3-a981-4a4b-89db-a74fade2c85e" />
> <img width="495" height="353" alt="image" src="https://github.com/user-attachments/assets/ebf5b42a-91e3-41cd-a7f6-c021f536a688" />


---

## Lampiran C. Exploratory Data Analysis (EDA)

Lampiran ini berisi visualisasi hasil eksplorasi data, seperti:

- Distribusi Sentimen
- Distribusi Rating
- Panjang Teks Ulasan
- Top Frequent Words
- WordCloud

> <img width="442" height="434" alt="image" src="https://github.com/user-attachments/assets/28e17340-ee46-480d-9874-1fbdc3a4f50e" />
> <img width="530" height="374" alt="image" src="https://github.com/user-attachments/assets/e18cb9f8-f861-495f-b41a-5c17dbb9bff6" />
> <img width="594" height="375" alt="image" src="https://github.com/user-attachments/assets/769cf8a1-a9ba-4466-8648-4a13c6ff1b9b" />
> <img width="727" height="433" alt="image" src="https://github.com/user-attachments/assets/b5dbc2cd-d63d-4722-adf6-37f9970d25de" />
> <img width="886" height="476" alt="image" src="https://github.com/user-attachments/assets/ba29a542-6c78-4f75-9b81-f2392c251c62" />

---

## Lampiran D. Hasil Training Model

Lampiran ini berisi dokumentasi proses pelatihan model, antara lain:

- Arsitektur Model LSTM
- Grafik Training Accuracy
- Grafik Validation Accuracy
- Grafik Training Loss
- Grafik Validation Loss

> <img width="995" height="397" alt="image" src="https://github.com/user-attachments/assets/9af20f42-3edd-4e87-b50e-eba4e1470c43" />


---

## Lampiran E. Hasil Evaluasi

Lampiran evaluasi model meliputi:

- Classification Report LSTM
- Confusion Matrix LSTM
- Classification Report SVM
- Confusion Matrix SVM
- Tabel Perbandingan Accuracy, Precision, Recall, dan F1-Score
- Grafik Perbandingan LSTM dan SVM

---
