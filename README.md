# Laporan Proyek Machine Learning - Rizka Indah Puspita
---

## Domain Proyek

### Latar Belakang
---
Stroke merupakan masalah kesehatan global yang terjadi akibat terhentinya suplai darah ke otak, baik karena sumbatan (stroke iskemik) maupun pecahnya pembuluh darah (stroke hemoragik). Penyakit ini menjadi penyebab kematian tertinggi kedua di negara maju dan ketiga di negara berkembang, dengan sekitar 15 juta kasus baru setiap tahunnya (WHO).

Stroke terjadi akibat gangguan aliran darah ke otak, yang dapat disebabkan oleh penyumbatan pembuluh darah (stroke iskemik) atau pecahnya pembuluh darah (stroke hemoragik). Faktor risiko utama stroke meliputi usia, tekanan darah tinggi (hipertensi), diabetes, penyakit jantung, obesitas, merokok, serta pola hidup yang tidak sehat. Deteksi dini sangat penting untuk mencegah komplikasi yang lebih serius, karena penanganan yang cepat dapat meningkatkan peluang pemulihan pasien.

Dengan berkembangnya teknologi di bidang kecerdasan buatan (Artificial Intelligence) dan machine learning, berbagai algoritma dapat digunakan untuk memprediksi risiko stroke berdasarkan faktor-faktor kesehatan individu. Beberapa model prediksi seperti K-Nearest Neighbors (KNN), Decision Tree (DT), Random Forest (RF), Support Vector Machine (SVM), Naïve Bayes (NB), dan XGBoost (XGB) telah menunjukkan tingkat akurasi yang tinggi dalam mengidentifikasi potensi stroke pada pasien.

**Rubrik/Kriteria Tambahan (Opsional)**:
- Jelaskan mengapa dan bagaimana masalah tersebut harus diselesaikan
- Menyertakan hasil riset terkait atau referensi. Referensi yang diberikan harus berasal dari sumber yang kredibel dan author yang jelas.
  
  Format Referensi: [Judul Referensi](https://scholar.google.com/) 

## Business Understanding
-----
Stroke merupakan salah satu penyakit yang memiliki dampak besar terhadap kesehatan masyarakat dan sistem layanan kesehatan. Penyakit ini menjadi penyebab utama kecacatan dan kematian di dunia, dengan tingkat kejadian yang terus meningkat akibat pola hidup tidak sehat dan faktor risiko seperti hipertensi, diabetes, penyakit jantung, obesitas, dan merokok.

Deteksi dini stroke sangat penting untuk mengurangi risiko komplikasi dan meningkatkan efektivitas pengobatan. Namun, banyak kasus stroke baru teridentifikasi setelah kondisi pasien memburuk, yang menyebabkan penanganan terlambat dan biaya perawatan yang tinggi. Oleh karena itu, diperlukan model prediksi berbasis data dan machine learning yang dapat membantu dalam mengidentifikasi individu dengan risiko tinggi terkena stroke secara lebih cepat dan akurat.

Dengan penerapan model prediksi ini, rumah sakit, klinik, dan tenaga medis dapat mengoptimalkan strategi pencegahan, memberikan diagnosis yang lebih cepat, serta mengurangi beban ekonomi akibat perawatan jangka panjang bagi pasien stroke.

### Problem Statements
-----
Problem Statements
Berdasarkan latar belakang diatas, permasalahan yang dapat diselesaikan pada proyek ini adalah sebagai berikut:

Saat ini, diagnosis stroke sering dilakukan setelah pasien mengalami gejala yang signifikan, yang mengurangi peluang intervensi dini. Beberapa permasalahan yang dihadapi dalam prediksi stroke adalah:

- Bagaimana cara melakukan pra-pemrosesan data lahan sehingga dapat digunakan untuk membuat model yang baik?
- Bagaimana membangun model machine learning yang dapat memprediksi risiko stroke dengan akurasi tinggi berdasarkan data pasien?
- Algoritma apa yang paling efektif dan optimal dalam mendeteksi risiko stroke?
- Bagaimana model ini dapat membantu tenaga medis dalam memprediksi stroke terhadap pasien?


### Goals
Tujuan dibuatnya proyek ini adalah sebagai berikut :

- Melakukan pra-pemrosesan data preiksi stroke agar dapat digunakan dalam membangun model.
- Mengembangkan model machine learning yang mampu mengklasifikasikan pasien dengan risiko stroke dan non-stroke secara akurat dengan tingkat akurasi > 85%.
-  Membandingkan performa berbagai algoritma seperti K-Nearest Neighbors (KNN), Decision Tree (DT), Random Forest (RF), Support Vector Machine (SVM), Naïve Bayes (NB), dan XGBoost (XGB) dalam mendeteksi risiko stroke.
-  Mengembangkan model yang dapat menganalisis faktor risiko dan mendeteksi potensi stroke lebih awal, sehingga tenaga medis dapat melakukan intervensi sebelum kondisi memburuk.

### Solution Statements
1. Analisis Data untuk Pemahaman Mendalam
- Melakukan univariate dan multivariate analysis untuk memahami pola distribusi data, hubungan antar fitur, serta mengetahui faktor-faktor yang memiliki pengaruh signifikan terhadap risiko stroke.
- Menggunakan visualisasi data seperti heatmap korelasi, boxplot untuk deteksi outlier, dan distribusi fitur untuk memahami tren yang ada dalam dataset.
2. Proses Data Cleaning dan Normalisasi
- Menangani data yang hilang dengan metode imputasi yang sesuai.
- Menghilangkan atau menangani outlier untuk meningkatkan stabilitas model.
- Melakukan normalisasi dan standarisasi fitur agar model lebih optimal dalam melakukan prediksi.
3. Pemilihan dan Pengujian Model Machine Learning
Untuk mendapatkan model terbaik dalam memprediksi stroke, beberapa algoritma machine learning yang akan digunakan adalah:
    - K-Nearest Neighbors (KNN)
    Algoritma berbasis jarak yang mengklasifikasikan data berdasarkan tetangga terdekatnya. KNN dapat membantu dalam mengenali pola pasien dengan karakteristik serupa yang memiliki risiko stroke. [[Referensi]](https://www.geeksforgeeks.org/k-nearest-neighbours/)
    - Decision Tree (DT)
    Algoritma berbasis pohon keputusan yang bekerja dengan membagi data menjadi cabang berdasarkan fitur yang paling berpengaruh terhadap target. Decision Tree mudah diinterpretasikan dan dapat menangani data dengan hubungan non-linear. Namun, algoritma ini rentan terhadap overfitting jika tidak dilakukan pruning. [[Referensi]](https://www.geeksforgeeks.org/decision-tree/)
    - Random Forest (RF)
    Algoritma ensemble yang menggabungkan banyak decision tree untuk meningkatkan akurasi prediksi. Random Forest efektif dalam menangani data dengan banyak variabel dan mengurangi overfitting. [[Referensi]](https://www.geeksforgeeks.org/random-forest-algorithm-in-machine-learning/)
    - Support Vector Machine (SVM)
    Algoritma yang mencari hyperplane optimal untuk memisahkan data dalam ruang multidimensi. SVM cocok untuk menangani dataset dengan distribusi kompleks dalam prediksi stroke. [[Referensi]](https://www.geeksforgeeks.org/support-vector-machine-algorithm/)
    - Naive Bayes (NB)
    Model berbasis probabilitas yang cepat dan efisien untuk klasifikasi. Cocok untuk data medis yang memiliki pola distribusi tertentu berdasarkan faktor risiko stroke. [[Referensi]](https://binus.ac.id/bandung/2019/12/algoritma-naive-bayes/)
    - XGBoost (XGB)
    Algoritma berbasis gradient boosting yang sangat kuat untuk meningkatkan akurasi prediksi. XGBoost sering digunakan dalam kompetisi machine learning karena kemampuannya dalam menangani dataset dengan jumlah fitur yang besar.[[Referensi]](https://www.geeksforgeeks.org/xgboost/)


## Data Understanding


## Data Preparation


## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

-https://repository.unism.ac.id/66/4/12%20BAB%20I.pdf

