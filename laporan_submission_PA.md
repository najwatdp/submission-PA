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
Melakukan Exploratory Data Understanding:
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

Alasan: Model machine learning seperti Logistic Regression, Random Forest, dan Decision Tree tidak dapat memproses data dalam bentuk teks. Encoding diperlukan agar fitur kategorikal dapat diinterpretasikan secara numerik oleh algoritma.
### Standarisasi
Proses: Fitur numerik distandarisasi menggunakan StandardScaler agar memiliki mean=0 dan standar deviasi=1

Alasan: Model machine learning seperti Logistic Rgression sangat sensitif terhadap skala fitur. Fitur dengan nilai besar (seperti TotalCharges) bisa mendominasi model jika tidak distandarisasi. Standarisasi membuat semua fitur berada pada skala yang sama, sehingga model bisa belajar dengan lebih adil dari semua fitur.
### Pembagian dataset
Proses: Dataset dibagi menjadi 2 bagian, yaitu X = semua fitur kecuali 'Churn' dan y = kolom target 'Churn'. Untuk melatih model, dataset dibagi menggunakan train_test_split dengan pembagian 80% untuk train set dan 20% untuk test set.

Alasan: Pembagian dataset penting untuk melatih model pada train set dan mengukur performa model pada data yang belum pernah dilihat (test set). Hal itu dilakukan agar terhindar dari overfitting dan memastikan model bisa generalisasi ke data baru.
Pemisahan fitur menjadi X dan target (Churn) menjadi Y. Split dataset dengan train_test_split. test_size=0.2

## Modeling
Model yang dibangun untuk meprediksi pelanggan yang berpotensi akan churn ada 3, yaitu Random Forest, Logistic Regression, dan Decision Tree.
### Random Forest
- Tahapan: Latih model dengan RandomForestClassifier(), evaluasi performa menggunakan metrik klasifikasi.
- Parameter: n_estimators=100, criterion='gini', max_depth=None, min_samples_split=2, min_samples_leaf=1, bootstrap=True, random_state=None
- Kelebihan: Lebih akurat dan stabil dibanding single tree, mengurangi overfitting dengan rata-rata dari banyak pohon, Menangani data yang kompleks, non-linear, dan dengan banyak fitur, Memberikan feature importance otomatis.
- Kekurangan: Lebih lambat dibanding Decision Tree dan Logistic Regression (karena ensemble), kurang interpretatif dibanding model sederhana, bisa terlalu besar dan lambat saat prediksi jika dataset besar.
### Logistic Regression
- Tahapan: Latih model dengan LogisticRegression(), evaluasi performa menggunakan metrik klasifikasi.
- Parameter: penalty='12', solver='lbfgs', C=1.0, max_iter=100, random_state=None
- Kelebihan: Sederhana dan cepat dilatih, hasil model mudah diinterpretasikan (koefisien menunjukkan arah dan kekuatan pengaruh fitur), cocok untuk baseline model, tidak mudah overfitting jika data tidak kompleks.
- Kekurangan: Kurang cocok untuk data yang sangat kompleks dan non-linear, sensitif terhadap fitur yang memiliki skala berbeda, tidak menangani interaksi antar fitur secara otomatis.
### Decision Tree
- Tahapan: Latih model dengan DecisionTreeClassifier(), evaluasi performa menggunakan metrik klasifikasi.
- Parameter: criterion='gini', max_depth=None, min_samples_split=2, min_samples_leaf=1, random_state=None
- Kelebihan: Mudah dipahami dan divisualisasikan, tidak memerlukan normalisasi atau standarisasi fitur, menangani data kategorikal dan numerik dengan baik, menangani fitur non-linear dan interaksi antar fitur.
- Kekurangan: Cenderung overfitting jika tidak dilakukan pruning, Sensitif terhadap perubahan kecil pada data, Performa bisa buruk dibanding model ensemble.

### Model Terbaik: Random Forest
- Dalam konteks deteksi churn pelanggan, Random Forest menjadi model terbaik berdasarkan hasil evaluasi kinerja pada test set. Hal ini didukung oleh performa metrik yang sangat tinggi, khususnya dalam hal accuracy, precision, dan recall.
- Hasil evaluasi pada test set: Accuracy 99.45%, Precision 99.38%, Recall 100%, F1-Score 99.69%.
- Tahan overfitting dengan accuracy 100% pada train set dan 99.45% pada test set. Rndom forest tetap generalizable dan tidak mudah overfit terhadap train set.
- Model ini memberikan informasi penting tentang fitur mana yang paling berpengaruh terhadap keputusan prediksi. Ini sangat berguna bagi perusahaan untuk memahami faktor utama penyebab churn dan menyusun strategi retensi pelanggan.

## Evaluation
Metrik evaluasi yang digunakan adalah Accuracy, Precision, Recall, F1-Score.
