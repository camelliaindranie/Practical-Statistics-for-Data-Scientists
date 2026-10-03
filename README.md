# Practical Statistics for Data Scientists

Repositori ini berisi reproduksi kode dan pembahasan teori dari buku **_Practical Statistics for Data Scientists_ (O'Reilly)** karya Peter Bruce, Andrew Bruce, dan Peter Gedeck.

Repositori ini dibuat untuk tugas individu pengayaan mata kuliah Machine Learning dan Deep Learning. Untuk setiap bab di buku, saya membuat satu notebook Jupyter yang berisi:

1. **Ringkasan bab.**
2. **Reproduksi kode** dari buku, lengkap dengan output dan grafik yang sudah dijalankan.
3. **Penjelasan teori** untuk setiap bagian kode, dengan bahasa saya sendiri.

---

## Struktur Repositori

```
Practical-Statistics-for-Data-Scientists/
├── README.md
├── requirements.txt
├── data/                      # dataset dari repositori kode pendamping buku
├── notebooks/
│   ├── Chapter_01_Exploratory_Data_Analysis.ipynb
│   ├── Chapter_02_Data_and_Sampling_Distributions.ipynb
│   ├── Chapter_03_Statistical_Experiments_and_Significance_Testing.ipynb
│   ├── Chapter_04_Regression_and_Prediction.ipynb
│   ├── Chapter_05_Classification.ipynb
│   ├── Chapter_06_Statistical_Machine_Learning.ipynb
│   └── Chapter_07_Unsupervised_Learning.ipynb
```

## Cara Menjalankan

```bash
git clone https://github.com/<username-github-kamu>/Practical-Statistics-for-Data-Scientists.git
cd Practical-Statistics-for-Data-Scientists
python -m venv .venv && source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/
```

Notebook membaca data dari folder `../data/`, jadi buka notebook dari dalam folder `notebooks/` (Jupyter sudah melakukannya secara otomatis).

Dataset di folder `data/` berasal dari repositori kode pendamping buku: <https://github.com/gedeck/practical-statistics-for-data-scientists>.

---

## Ringkasan Tiap Bab

### Bab 1: Exploratory Data Analysis
Bab ini membahas langkah pertama dalam proyek data, yaitu melihat dan memahami data sebelum membuat model. Isinya meliputi jenis data terstruktur (numerik dan kategorikal, data persegi panjang), ukuran lokasi (mean, trimmed mean, mean berbobot, median, median berbobot), ukuran variabilitas (varians, simpangan baku, MAD, persentil, IQR), grafik distribusi (boxplot, histogram, density plot), data biner dan kategorikal, korelasi (Pearson, matriks korelasi, scatterplot), serta eksplorasi banyak variabel (hexagonal binning, contour plot, tabel kontingensi, violin plot, facet). Bab ini menekankan pentingnya statistik yang robust terhadap outlier.
Dataset: `state`, `dfw_airline`, `sp500_data`, `kc_tax`, `lc_loans`, `airline_stats`.

### Bab 2: Data and Sampling Distributions
Bab ini menjelaskan bahwa cara data dikumpulkan lebih penting daripada banyaknya data. Topiknya adalah random sampling dan bias sampel, selection bias (data snooping, vast search effect, regression to the mean), distribusi sampling, Central Limit Theorem dan standard error, bootstrap, confidence interval, serta distribusi-distribusi penting: normal (QQ-plot), long-tailed, t Student, binomial, chi-square, F, Poisson, eksponensial, dan Weibull.
Dataset: `loans_income`, `sp500_data`.

### Bab 3: Statistical Experiments and Significance Testing
Bab ini membahas cara menilai apakah perbedaan yang teramati itu nyata atau hanya kebetulan. Isinya A/B testing, uji hipotesis (hipotesis nol dan alternatif, satu arah dan dua arah), resampling lewat permutation test, signifikansi statistik dan p-value (alpha, error tipe 1 dan 2), uji t, multiple testing, derajat bebas, ANOVA dan statistik F, uji chi-square dan uji eksak Fisher, multi-armed bandit, serta power dan ukuran sampel.
Dataset: `web_page_data`, `four_sessions`, `click_rates`.

### Bab 4: Regression and Prediction
Bab ini membahas cara mengukur hubungan antara outcome numerik dan prediktor. Isinya regresi linear sederhana dan berganda (kuadrat terkecil, RMSE, R², statistik t), pemilihan model (AIC, stepwise), regresi berbobot, prediction interval, variabel faktor (dummy coding, penggabungan level), masalah interpretasi (prediktor berkorelasi, multikolinearitas, confounder, interaksi), diagnostik regresi (outlier, pengaruh/Cook's distance, heteroskedastisitas, partial residual plot), serta regresi polinomial, spline, dan GAM. Ada juga bagian tambahan tentang ridge dan lasso.
Dataset: `LungDisease`, `house_sales`.

### Bab 5: Classification
Bab ini membahas prediksi outcome kategorikal. Isinya Naive Bayes, discriminant analysis (LDA), regresi logistik (logit, odds ratio, GLM, spline), evaluasi model (confusion matrix, precision, recall, specificity, ROC, AUC, lift), strategi untuk data tidak seimbang (undersampling, oversampling dan pembobotan, SMOTE/ADASYN), serta perbandingan decision boundary antar model.
Dataset: `loan_data`, `loan3000`, `full_train_set`.

### Bab 6: Statistical Machine Learning
Bab ini membahas metode prediksi yang fleksibel dan berbasis data. Isinya K-Nearest Neighbors (ukuran jarak, standarisasi, KNN sebagai pembuat fitur), decision tree (recursive partitioning, Gini/entropi, pruning), bagging dan random forest (OOB error, variable importance), serta boosting (AdaBoost, gradient boosting, XGBoost, regularisasi, dan cross-validation untuk hyperparameter).
Dataset: `loan200`, `loan3000`, `loan_data`.

### Bab 7: Unsupervised Learning
Bab ini membahas cara menemukan struktur dalam data tanpa label. Isinya PCA (scree plot, loading, correspondence analysis), K-means (metode elbow), hierarchical clustering (dendrogram, metode linkage), model-based clustering dengan Gaussian mixture (EM, BIC), serta penskalaan dan variabel kategorikal (standarisasi, variabel dominan, jarak Gower, one-hot encoding).
Dataset: `sp500_data`, `housetasks`, `loan_data`.

---

## Referensi
Bruce, P., Bruce, A., & Gedeck, P. (2020). *Practical Statistics for Data Scientists* (2nd ed.). O'Reilly Media. Kode pendamping: <https://github.com/gedeck/practical-statistics-for-data-scientists>.
