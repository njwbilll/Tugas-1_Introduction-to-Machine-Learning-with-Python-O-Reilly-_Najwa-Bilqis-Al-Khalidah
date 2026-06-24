# Introduction to Machine Learning with Python
 
Repositori ini berisi reproduksi kode dan penjelasan teori dari buku
**"Introduction to Machine Learning with Python"** karya Andreas C. Muller dan Sarah Guido (O'Reilly).
 
Setiap chapter direpresentasikan sebagai satu Jupyter Notebook terpisah,
lengkap dengan penjelasan konsep dalam Bahasa Indonesia, implementasi kode,
dan visualisasi hasil.
 
---
 
## Identifikasi
 
| Field | Detail |
|-------|--------|
| Nama | Najwa Bilqis Al Khalidah |
| NIM | 101032300186 |
| Kelas | TK-46-GAB |
| Mata Kuliah | Machine Learning |
| Referensi | Introduction to Machine Learning with Python by Andreas C. Muller & Sarah Guido (O'Reilly) |
 
---
 
## Deskripsi Proyek
 
Tugas ini merupakan bagian dari enrichment course Machine Learning dan Deep Learning.
Tujuannya adalah memperdalam pemahaman dan keterampilan praktis dalam
mengimplementasikan konsep-konsep inti Machine Learning melalui reproduksi kode
dan penjelasan teori terstruktur.
 
Setiap notebook mencakup:
- Penjelasan teori konsep yang dibahas (dalam Bahasa Indonesia)
- Reproduksi dan adaptasi kode dari buku referensi
- Visualisasi hasil eksperimen
- Ringkasan dan panduan praktis di akhir setiap chapter
 
---
 
## Struktur Repository
 
```
IntroductionMachineLearningwithPython/
|
|-- 01_Introduction.ipynb
|-- 02_Supervised_Learning.ipynb
|-- 03_Unsupervised_Learning_and_Preprocessing.ipynb
|-- 04_Representing_Data_and_Engineering_Features.ipynb
|-- 05_Model_Evaluation_and_Improvement.ipynb
|-- 06_Algorithm_Chains_and_Pipelines.ipynb
|-- 07_Working_with_Text_Data.ipynb
|-- 08_Wrapping_Up.ipynb
|-- README.md
```
 
---
 
## Deskripsi Setiap Chapter
 
### Chapter 1: Introduction
**File:** `01_Introduction.ipynb`
 
Chapter pembuka yang memperkenalkan ekosistem Python untuk Machine Learning
dan membangun model klasifikasi pertama dari nol.
 
Topik utama:
- Apa itu machine learning dan mengapa dibutuhkan
- Library inti: NumPy, SciPy, matplotlib, pandas, scikit-learn
- Dataset Iris sebagai studi kasus pertama
- Train-test split dan pentingnya evaluasi yang jujur
- k-Nearest Neighbors (kNN) sebagai classifier pertama
- Pengaruh hyperparameter k terhadap akurasi
 
---
 
### Chapter 2: Supervised Learning
**File:** `02_Supervised_Learning.ipynb`
 
Chapter terpanjang dan terpenting. Membahas hampir semua algoritma
supervised learning yang tersedia di scikit-learn secara menyeluruh.
 
Topik utama:
- Klasifikasi vs. Regresi
- Generalisasi, overfitting, dan underfitting
- k-Nearest Neighbors untuk klasifikasi dan regresi
- Linear Models: Ridge, Lasso, Logistic Regression
- Regularisasi L1 dan L2 dan pengaruhnya terhadap koefisien
- Naive Bayes: GaussianNB dengan visualisasi distribusi per kelas
- Decision Trees: visualisasi struktur, pruning, feature importance
- Ensemble Methods: Random Forest dan Gradient Boosted Trees
- Kernelized SVM: pentingnya scaling dan pengaruh C serta gamma
- Neural Networks (MLP): pengaruh arsitektur hidden layer
- Estimasi ketidakpastian: decision_function vs predict_proba
- Perbandingan semua model dalam satu benchmark
 
---
 
### Chapter 3: Unsupervised Learning dan Preprocessing
**File:** `03_Unsupervised_Learning_and_Preprocessing.ipynb`
 
Membahas dua topik besar: cara mempersiapkan data sebelum training (preprocessing)
dan cara menemukan struktur dalam data tanpa label (unsupervised learning).
 
Topik utama:
- Jenis-jenis unsupervised learning dan tantangan evaluasinya
- Preprocessing: StandardScaler, MinMaxScaler, RobustScaler, Normalizer
- Aturan emas: fit scaler hanya pada training data
- PCA (Principal Component Analysis): explained variance, loading, visualisasi 2D
- NMF (Non-Negative Matrix Factorization): representasi parts-based pada digit
- t-SNE: visualisasi cluster pada digits dataset, pengaruh perplexity
- k-Means: algoritma, metode elbow, silhouette score
- Agglomerative Clustering: linkage methods, dendrogram
- DBSCAN: core/border/noise points, pengaruh eps dan min_samples
- Perbandingan ketiga algoritma clustering pada berbagai bentuk data
 
---
 
### Chapter 4: Merepresentasikan Data dan Rekayasa Fitur
**File:** `04_Representing_Data_and_Engineering_Features.ipynb`
 
Membahas teknik-teknik untuk mengubah data mentah menjadi representasi
yang lebih bermakna bagi algoritma machine learning.
 
Topik utama:
- Variabel kategorikal: nominal vs ordinal
- One-Hot Encoding dengan pandas dan scikit-learn OneHotEncoder
- Ordinal Encoding untuk variabel berurutan
- Binning (KBinsDiscretizer): uniform, quantile, kmeans strategy
- Polynomial Features dan Interaction Features
- Pengaruh degree polynomial terhadap overfitting/underfitting
- Transformasi non-linear: log1p dan sqrt untuk distribusi skewed
- Seleksi fitur otomatis: Univariate (f_classif), Model-Based (RF), RFE
- Menggabungkan semua preprocessing dalam Pipeline
 
---
 
### Chapter 5: Evaluasi Model dan Peningkatan Performa
**File:** `05_Model_Evaluation_and_Improvement.ipynb`
 
Membahas cara mengevaluasi model secara jujur dan cara mencari
hyperparameter terbaik tanpa overfitting pada test set.
 
Topik utama:
- Masalah dengan single train-test split
- k-Fold dan Stratified k-Fold Cross-Validation
- Pentingnya stratifikasi pada imbalanced dataset
- GridSearchCV: exhaustive search dengan cross-validation
- RandomizedSearchCV: sampling dari distribusi kontinu
- GridSearchCV dalam Pipeline (mencegah data leakage)
- Confusion Matrix: TP, TN, FP, FN
- Precision, Recall, F1 Score, Specificity
- ROC Curve dan AUC
- Precision-Recall Curve dan Average Precision
- Trade-off precision-recall dengan threshold
- Metrik multiclass: macro, weighted, micro averaging
- Metrik regresi: R2, MSE, RMSE, MAE, residual plot
- Panduan memilih metrik sesuai konteks bisnis
 
---
 
### Chapter 6: Algorithm Chains dan Pipelines
**File:** `06_Algorithm_Chains_and_Pipelines.ipynb`
 
Membahas cara merangkai langkah-langkah preprocessing dan model
menjadi satu objek Pipeline yang aman dan efisien.
 
Topik utama:
- Masalah data leakage pada preprocessing manual
- Demonstrasi kuantitatif: leakage vs tidak pada scaling dan feature selection
- Membangun Pipeline dengan Pipeline() dan make_pipeline()
- Mengakses atribut setiap step setelah fitting
- GridSearchCV + Pipeline: naming convention dengan double underscore
- Grid search atas parameter preprocessing sekaligus (PCA n_components + SVM C)
- Grid search atas pilihan scaler yang berbeda
- ColumnTransformer untuk data dengan fitur numerik dan kategorikal campuran
- Perbandingan berbagai pipeline menggunakan cross-validation
 
---
 
### Chapter 7: Bekerja dengan Data Teks
**File:** `07_Working_with_Text_Data.ipynb`
 
Membahas cara mengubah data teks mentah menjadi representasi numerik
yang bisa digunakan oleh algoritma machine learning.
 
Topik utama:
- Jenis data teks dan tantangan representasinya
- Bag-of-Words dengan CountVectorizer
- Parameter penting: min_df, max_df, max_features
- Stopwords bahasa Inggris dan custom bahasa Indonesia
- tf-idf (Term Frequency -- Inverse Document Frequency): formula dan intuisi
- TfidfVectorizer vs CountVectorizer: perbandingan performa
- n-Grams: unigram, bigram, trigram dan pengaruhnya
- Pipeline teks + GridSearchCV
- Topic Modeling dengan LDA: menemukan topik tersembunyi dalam corpus
- Perbandingan Logistic Regression, LinearSVC, dan Multinomial Naive Bayes
 
---
 
### Chapter 8: Penutup -- Pendekatan ML di Dunia Nyata
**File:** `08_Wrapping_Up.ipynb`
 
Chapter penutup yang memberikan panduan praktis untuk mendekati
masalah machine learning di dunia nyata dari awal sampai production.
 
Topik utama:
- Workflow ML end-to-end 8 langkah sistematis
- Baseline dummy classifier sebagai lower bound
- Perbandingan dan tuning model terbaik
- Evaluasi final yang jujur (test set hanya disentuh sekali)
- Humans in the Loop: identifikasi prediksi dengan kepercayaan rendah
- Simulasi active learning dan zone otomasi vs review manusia
- Model serialization dengan joblib
- Fungsi prediksi siap production dengan validasi input
- Deteksi data drift dengan Kolmogorov-Smirnov test
- Monitoring performa model di production dengan alerting
- Final benchmark semua model dengan ROC curves
- Panduan langkah selanjutnya: XGBoost, LightGBM, Deep Learning, MLOps
 
---
 
## Library yang Digunakan
 
| Library | Versi | Kegunaan |
|---------|-------|----------|
| Python | 3.8+ | Bahasa pemrograman utama |
| scikit-learn | terbaru | Algoritma ML, preprocessing, evaluasi |
| NumPy | terbaru | Operasi array dan matematika |
| pandas | terbaru | Manipulasi data tabular |
| matplotlib | terbaru | Visualisasi dasar |
| seaborn | terbaru | Visualisasi statistik |
| scipy | terbaru | Sparse matrix, statistical tests |
 
---
 
## Cara Menjalankan
 
### Prasyarat
 
```bash
pip install scikit-learn numpy pandas matplotlib seaborn scipy jupyter
```
 
### Menjalankan Notebook
 
```bash
git clone https://github.com/njwbilll/Tugas-1_Introduction-to-Machine-Learning-with-Python-O-Reilly-_Najwa-Bilqis-Al-Khalidah.git
cd Tugas-1_Introduction-to-Machine-Learning-with-Python-O-Reilly-_Najwa-Bilqis-Al-Khalidah
jupyter notebook
```
 
Kemudian buka notebook sesuai urutan chapter (01 hingga 08) di browser.
 
### Urutan yang Disarankan
 
Notebook dirancang untuk dibaca secara berurutan karena konsep dari
chapter sebelumnya sering digunakan di chapter berikutnya.
 
```
01 Introduction
   |
   v
02 Supervised Learning     <-- Chapter terpanjang, paling penting
   |
   v
03 Unsupervised + Preprocessing
   |
   v
04 Feature Engineering
   |
   v
05 Model Evaluation        <-- Sangat penting untuk praktik yang benar
   |
   v
06 Pipelines               <-- Wajib dipahami sebelum project nyata
   |
   v
07 Text Data
   |
   v
08 Wrapping Up
```
 
---
 
## Dataset yang Digunakan
 
Semua dataset diambil dari built-in scikit-learn, tidak perlu download terpisah.
 
| Dataset | Chapter | Deskripsi |
|---------|---------|-----------|
| Iris | 1, 2 | 150 sampel bunga iris, 3 kelas, 4 fitur |
| Breast Cancer Wisconsin | 2, 3, 4, 5, 6, 8 | 569 sampel tumor, biner, 30 fitur |
| Digits | 3 | 1797 gambar digit 8x8, 10 kelas |
| Make Blobs / Moons / Circles | 2, 3 | Dataset sintetis untuk visualisasi |
| Ulasan Film (sintetis) | 7 | 40 ulasan sentimen bahasa Indonesia |
| Corpus Topik (sintetis) | 7 | 20 dokumen 4 topik untuk LDA |
 
---
 
## Referensi
 
Muller, A. C., & Guido, S. (2016).
*Introduction to Machine Learning with Python: A Guide for Data Scientists*.
O'Reilly Media.
 
ISBN: 978-1-449-36941-5
