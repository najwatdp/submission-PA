# Laporan Submission Predictive Analytics - Najwa Tiara Djunaedy Putri

## Domain Proyek
### Latar belakang
Industri telekomunikasi mengalami persaingan yang sangat ketat, dengan banyaknya penyedia layanan yang menawarkan paket serupa. Perusahaan telekomunikasi perlu mempertahankan tingkat loyalitas pelanggan agar tetap bertahan. Churn customer menjadi indikator penting yang dapat memengaruhi pendapatan perusahaan.

Churn customer menunjukkan jumlah pelanggan lama yang hilang, baik karena alasan apa pun, selama periode tertentu. Kemungkinan pelanggan berhenti atau lanjut berlangganan dapat dipengaruhi oleh perilaku dan karakteristik pelanggan. Data historis pelanggan memungkinkan perusahaan untuk membangun model prediktif guna mengidentifikasi pelanggan yang berisiko churn.
### Mengapa Masalah Churn Harus Diselesaikan?
1. Berdampak langsung pada pendapatan perusahaan. Perusahaan cenderung mengeluarkan lebih banyak dana untuk mendapatkan pelanggan baru.
2. Indikator kepuasan pelanggan. Churn yang tinggi mencerminkan rendahnya kepuasan pelanggan.
3. Meningkatkan nilai jangka panjang pelanggan.
4. Bertahan pada persaingan perusahaan yang ketat.
### Bagaimana Masalah Churn Diselesaikan?
1. Menggunakan data historis pelanggan untuk memahami pola pelanggan yang churn.
2. Menggunakan model machine learning untuk mengklasifikasi pelanggan berdasarkan kemungkinan churn
3. Pelanggan yang terdeteksi akan churn diberikan perhatian khusus, seperti peningkatan layanan, promo, dan kontak personal.
### Hasil Riset Referensi
1. Pentingnya pendekatan data-driven pada perusahaan telekomunikasi untuk memahami kebutuhan dan preferensi pelanggan
2. Tidak ada umpan balik real-time dari pelanggan
3. Prototipe sistem umpan balik langsung
4. Perusahaan menekan jumlah churn dengan memanfaatkan data umpan balik dari pengguna.
Referensi: Saliu, A. (2025). Development of a Data-Driven Prototype for Consumer-Centric Product Development and Issue Resolution in the Telecommunications Industry (Case Study: Smartphones). *International Journal of Research and Innovation in Social Science*, 9(4), 1715-1718. https://dx.doi.org/10.47772/IJRISS.2025.90400128

## Business Understanding
### Problem Statements
1. Fitur apa yang paling berpengaruh terhadap keputusan pelanggan untuk melakukan churn?
Perusahaan harus mengetahui fitur atau faktor yang paling memengaruhi angka churn pelanggan agar perusahaan fokus pada faktor-faktor kritis.
2. Bagaimana karakteristik pelanggan yang cenderung melakukan churn?
Pola demografi dan perilaku pelanggan yang sering churn dapat membantu perusahaan dalam memahami segemn mana yang paling rentan dan mengapa mereka berhenti menggunakan layanan.
3. Model machine learning apa yang paling efektif dalam meprediksi pelanggan yang berpotensi melakukan churn?
Membandingkan beberapa model machine learning klasifikasi untuk menentkan model yang paling akurat dan andal dalam memprediksi churn. Model yang dapat digunakan seperti Logistic Regression, Decision Tree, dan Random Forest.
4. Strategi apa yang dapat diterapkan perusahaan telekomunikasi untuk mengurangi angka churn pelanggan?
Berdasarkan hasil analisis, perusahaan dapat menyusun strategi agar pelanggan tetap loyal terhadap perusahaan dan angka churn menurun.
### Goals
1. Mengetahui fitur yang paling berpengaruh terhadap churn pelanggan.
Tujuan ini bertujuan untuk mengidentifikasi fitur-fitur utama dalam data yang secara signifikan memengaruhi keputusan pelanggan untuk berhenti berlangganan.
2. Mengetahui karakteristik pelanggan yang churn.
Menganalisis pola dan profil pelanggan yang melakukan churn, seperti lama berlangganan, jenis layanan, dan tingkat pembayaran, untuk memahami perilaku mereka.
3. Membuat model machine learning klasifikasi yang dapat memprediksi pelanggan berpotensi akan churn seakurat mungkin berdasarkan fitur-fitur yang ada.
Tujuan ini fokus pada pembangunan dan evaluasi model prediktif menggunakan algoritma machine learning agar dapat mengenali pelanggan yang berisiko churn.
4. Menentukan strategi yang dapat diterapkan perusahaan telekomunikasi untuk mengurangi angka churn pelanggan.
Berdasarkan hasil analisis, ditujukan untuk merumuskan tindakan atau kebijakan retensi yang tepat guna mempertahankan pelanggan dan menurunkan churn.
### Solution Statements
1. Melakukan Exploratory Data Analysis dan visualisasi fitur terhadap target churn.
2. Menggunakan teknik feature importance untuk mengetahui kontribusi masing-masing fitur terhadap prediksi.
3. Membandingkan distribusi pelanggan churn dan tidak churn pada setiap fitur menggunakan visualisasi.
4. Membangun 3 model klasifikasi, yang kemudian akan dibandingkan berdasarkan metrik evaluasi(Accuracy, Precision, Recall, F1-Score). Model terbaik akan digunakan untuk memprediksi pelanggan berpotensi churn.

## Data Understanding
Customer Churn Dataset memberikan gambaran menyeluruh tentang perilaku pelanggan dan churn dalam industri telekomunikasi. Kumpulan data ini mencakup informasi terperinci tentang demografi pelanggan, penggunaan layanan, dan berbagai indikator yang penting untuk menganalisis retensi dan churn pelanggan. Terdapat 1000 sampel data, yang terdiri dari 9 fitur dan 1 target. Dataset: https://www.kaggle.com/datasets/abdullah0a/telecom-customer-churn-insights-for-analysis/data
### Variabel-variabel Pada Customer Churn Dataset
- CustomerID: Pengenal unik untuk setiap pelanggan.
- Age: Usia pelanggan, mencerminkan profil demografis mereka.
- Gender: Jenis Kelamin pelanggan (Male atau Female).
- Tenure: Durasi (dalam bulan) pelanggan telah menggunakan layanan penyedia layanan.
- MonthlyCharges: Biaya bulanan yang dibebankan kepada pelanggan.
- ContractType: Jenis kontrak yang diikuti pelanggan (Month-to-Month, One-Year, Two-Year).
- InternetService: Jenis layanan internet yang dipakai (DSL, Fiber Optik, None).
- TechSupport: Apakah pelanggan memiliki dukungan teknis (Yes atau No).
- TotalCharges: Jumlah total yang dibebankan kepada pelanggan (dihitung dengan MonthlyCharges * Tenure).
- Churn: Variabel target yang menunjukkan apakah pelanggan telah berhenti berlangganan (Yes atau No).
### Tahapan Data Understanding
- Exploratory Data Understanding:
  1. info(): Mengetahui tipe data setiap fitur
  2. describe(): Mengetahui statistik deskriptif pada dataset, seperti jumlah data, rata-rata, standar deviasi, nilai minimum, maksimun, dan kuartil(25%, 50%, 75%)
  3. duplicated(): Mengidentifikasi apakah terdapat baris duplikat
  4. Boxplot: Visualisasi fitur numerikal untuk mengidentifikasi apakah terdapat outlier
  5. Bar chart: Visualisasi distribusi fitur kategorikal
  6. Histogram: Visulisasi distribusi fitur numerikal
  7. Pairplot: Visualisasi hubungan antar fitur numerikal
  8. Heatmap: Visualisasi hubungan antar fitur numerikal

## Data Preparation
### Encoding Fitur Kategori
Proses: Fitur kategorikal diubah ke bentuk numerik menggunakan LabelEncoder. Setiap kategori unik dalam suatu kolom diubah menjadi angka (Misalnya: Female = 0, Male = 1).

Alasan: 
### Standarisasi
StandardScaler
### Pembagian dataset
Pemisahan fitur menjadi X dan target (Churn) menjadi Y. Split dataset dengan train_test_split. test_size=0.2
