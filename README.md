# 1. Tema: Memprediksi Skor Kredit Dari Aplikasi Pinjaman Konsumen
Project ini merupakan Tugas Final dari Virtual Internship Experience pada Home Credit dengan posisi Data Science yang diselengggarakan oleh Rakamin Academy
## A. Problem:
Jumlah peminjam yang gagal bayar yang relative banyak
## B. Goal:
Meningkatkan tingkat kelancaran pembayaran
## C. Objective
Membuat sebuat model meachine learning yang mampu memprediksi skor kredit untuk melihat tingkat kelancaran pembayaran calon peminjam.
Model Machine Learning yang akan diuji adalah Supervised Machine Learning karena target alaha kategori dengan 2 nilai.
## D. Business Metric
Menurunkan tingkat gagal bayar dan menaikan tingkat kelancaran pembayaran
# 2. Source Code File
Untuk menghemat penggunaan memori, source code file untuk membuat model machine learning dibuat menjadi 2 yaitu:
1. vix1_homecredit.ipynb
   Dalam file ini berisi kode-kode untuk memnggabungkan dataset dan melakukan feature slection menggunakan anova
2. vix1_homecredit_2.ipynb
   Dalam file ini berisi kode-kode Deskripsi Statistik, Exploration Data Analisis (EDA), Data Preprocessing, Model Machone Learning, Evaluasi, Feature Importance
# 3. Dataset
Terdapat 8 Dataset. Beberapa kolom dari datset tersebut digabung dan juga ada yang dikurangi menggunakan feature selection ANOVA sehingga diperoleh sebuah tabel yang terdiri dari beberapa kolom.
# 4. Exploration Data Analysis (EDA)
Dalam proses EDA ini dilakukan Deskripsi Statistik, melakukan visualisasi data dengan univariate analysis, bivariate analysisi, multivariate analysis untuk melihat gambaran data mentah sebelum dilakukan preprocessing.
Dalam proses ini dikethui kolom antar feature yang memiliki korelasi tinggi (>0,7) yang artinya redundan sehingga salah satu perlu dihapus
# 5. Preprocessing Data
a. Menghapus kolom redundan
Terdapa kolom antar feature yang berkorelasi sehingga kolom yang berkolerasi dihapus.
b. Handling Missing Value/Data Null
Terdapat beberapa kolom yang mengandung data null/missing value. Kolom yang memiliki data null yang besar dihapus. Kolom yang memiliki data null sedikit dilakukan imputasion atau diisi dengan nilai. Selain itu juga kolom ayng mengandung sedikit data null dihapus baris yang mengandung da null.
c. Handling Duplicate Data
Tidak terdapat data yang duplikat
d. Handling Outlier
Terdapat data outlier. Baris-Baris yang mengandung data outlier dihapus.
e. Train Test Split
Membagi data menjadi 80% untuk data training dan 30% untuk data test.
f. Encoding
Dalam proses ini kolom yang nilainya bertype kategori diubah menjadi angka.
g. Feature Transformation
Merubah scala nilai pada kolom numerik agar variasi data relative seragam dan distribusi mendekati normal.
h. Class Imbalance
Nilai pada kolom target tidak seimbang sehingga dilakukan class imbalance agar nilai pada kolom target seimbang menggunakan SMOTE.
# 6. Memilih Model Machine Learning Terbaik
Model Meachine Learninng yang akan diuji adalah Supervised Machine Learning karena data target berupa kategori dengan 2 nilai. Dalam pengujian ini dilakukan uji model dengan Logistic Regression dan Decision Tree.
Berdasarkan hasil pengujian diperoleh model machine learning terbaik adalah Logistic Regression dengan nilai Accuracy sebesar 61% dan ROC AUC Score sebesar 60%.
# 7. Feature Importance
Terdapat beberapa feature yang paling berpengaruh terhadap target:
 - Semakin memiliki mobil semakin besar peluang lancar pembayarannya
 - Semakin aktif credit semakin besar peluang lancar pembayarannya
 - Semakin tinggi harga barang semakin besar peluang lancar pembayarannya
 - Semakin besar rumah semakin besar peluang lancar pembayarannya
 - Semakin tinggi jabatan atau pekerjaan semakin besar peluang lancar pembayarannya
 - Semakin lama bekerja semakin besar peluang lancar pembayarannya
 - Semakin muda usia pada saat mengajukan pinjaman maka semakin tidak lancar
 - Semakin tinggi angka rating kota maka semakin tidak lancer
 - Pelamar ayng baru saja merubah nomor telp cenderung lebih besar gagal bayarnya






