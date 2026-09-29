# Analisis Sentimen Ulasan Google Maps – Cafe C28 Group

Analisis sentimen terhadap ulasan pelanggan Google Maps pada **6 cabang Cafe C28 Group** menggunakan Python dan teknik Natural Language Processing (NLP). Proyek ini membandingkan distribusi sentimen, rating, kata kunci, serta karakteristik ulasan pada masing-masing cabang.

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk mengolah dan menganalisis ulasan pelanggan secara terstruktur sehingga dapat memberikan gambaran mengenai persepsi pelanggan terhadap setiap cabang.

Data yang dianalisis mencakup sekitar **5,393 review hasil analisis** dari 6 cabang:

- 1009 Palagan
- C28 Malioboro
- C28 Urip Sumoharjo
- Machia Palagan
- Machia Seturan
- Michael Kreme Gelato Palagan

Analisis dilakukan melalui beberapa tahapan, mulai dari eksplorasi data, pembersihan teks, normalisasi bahasa informal, analisis sentimen, hingga analisis kata dan perbandingan antar-cabang.

## 🔎 Tahapan Analisis

### 1. Data Loading & Exploratory Data Analysis
- Menggabungkan data ulasan dari 6 cabang.
- Memeriksa struktur data dan missing values.
- Menganalisis distribusi rating.
- Membandingkan jumlah review dan rating antar-cabang.

### 2. Text Preprocessing
Proses preprocessing meliputi:
- Penanganan missing values.
- Case normalization.
- Pembersihan karakter dan teks.
- Penghapusan stopwords Bahasa Indonesia.
- Normalisasi kata slang, singkatan, dan typo.
- Stemming menggunakan **Sastrawi**.

### 3. Sentiment Analysis
Ulasan diklasifikasikan menjadi tiga kategori:
- 🟢 **Positif**
- 🟡 **Netral**
- 🔴 **Negatif**

Hasil analisis kemudian dibandingkan berdasarkan masing-masing cabang.

### 4. Text & Keyword Analysis
Analisis teks mencakup:
- Top positive keywords.
- Top negative keywords.
- Word cloud berdasarkan sentimen.
- Word cloud berdasarkan cabang.
- Analisis **4-gram**.
- Analisis **TF-IDF**.

### 5. Comparative Analysis
Dilakukan perbandingan antar-cabang berdasarkan:
- Jumlah review.
- Rata-rata rating.
- Persentase sentimen.
- Distribusi sentimen.
- Kata dan frasa yang paling sering muncul.

### 6. IndoBERT Preparation
Notebook juga memuat tahap persiapan klasifikasi sentimen menggunakan model:

`indobenchmark/indobert-base-p1`

Tahapan mencakup:
- Pembagian data training dan testing.
- Tokenisasi.
- Pembuatan dataset PyTorch.
- Training dengan Hugging Face Trainer.
- Evaluasi menggunakan Accuracy, Precision, Recall, dan F1-Score.
- Fungsi prediksi sentimen untuk teks baru.

> **Catatan:** bagian IndoBERT membutuhkan environment Python dengan library Transformer dan PyTorch serta model yang perlu diunduh saat dijalankan.

## 📂 Struktur Repository

```text
Mini_Proyek/
├── perbandingan.ipynb
│
├── data_1009_palagan.csv
├── data_c28_malioboro.csv
├── data_c28_urip_sumoharjo.csv
├── data_machia_palagan.csv
├── data_machia_seturan.csv
├── data_michael_kreme_gelato_palagan.csv
│
├── analisis_keywords.csv
├── hasil_analisis_sentimen_lengkap.csv
└── ringkasan_sentimen_per_cabang.csv
```

### Keterangan File

| File | Keterangan |
|---|---|
| `perbandingan.ipynb` | Notebook utama seluruh proses analisis |
| `data_*.csv` | Dataset ulasan Google Maps masing-masing cabang |
| `hasil_analisis_sentimen_lengkap.csv` | Dataset hasil preprocessing dan klasifikasi sentimen |
| `ringkasan_sentimen_per_cabang.csv` | Ringkasan metrik sentimen per cabang |
| `analisis_keywords.csv` | Ringkasan keyword positif dan negatif |

## 🛠️ Teknologi yang Digunakan

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Sastrawi
- WordCloud
- PyTorch
- Hugging Face Transformers
- IndoBERT
- Jupyter Notebook

## 🚀 Cara Menjalankan

### 1. Clone repository

```bash
git clone https://github.com/USERNAME/NAMA-REPOSITORY.git
cd NAMA-REPOSITORY
```

### 2. Buat virtual environment (opsional tetapi disarankan)

```bash
python -m venv .venv
```

Aktifkan environment:

**Windows:**
```bash
.venv\Scripts\activate
```

**macOS/Linux:**
```bash
source .venv/bin/activate
```

### 3. Install library

Untuk analisis utama:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn wordcloud Sastrawi jupyter
```

Untuk bagian IndoBERT:

```bash
pip install torch transformers
```

### 4. Jalankan Jupyter Notebook

```bash
jupyter notebook
```

Kemudian buka:

```text
perbandingan.ipynb
```

> Pastikan file CSV berada pada direktori yang sama dengan notebook agar proses pembacaan data berjalan dengan benar.

## 📊 Output Analisis

Hasil analisis yang tersedia dalam repository antara lain:

- Distribusi rating per cabang.
- Jumlah review per cabang.
- Distribusi sentimen positif, netral, dan negatif.
- Word cloud berdasarkan sentimen.
- Word cloud berdasarkan cabang.
- Top keyword positif dan negatif.
- Top 4-gram.
- Top kata berdasarkan TF-IDF.
- Heatmap perbandingan sentimen.
- Ringkasan statistik dan metrik setiap cabang.

## 🎯 Tujuan Penggunaan

Proyek ini dapat digunakan sebagai contoh penerapan **Natural Language Processing (NLP)** untuk:

- Memahami persepsi pelanggan berdasarkan ulasan.
- Membandingkan karakteristik ulasan antar-cabang.
- Mengidentifikasi kata atau topik yang sering muncul.
- Mengidentifikasi area yang memperoleh respons positif maupun negatif.
- Menjadi dasar eksplorasi lebih lanjut menggunakan model NLP berbasis Transformer.

## ⚠️ Catatan Data

Data dalam repository merupakan data ulasan pelanggan yang digunakan untuk kebutuhan analisis proyek. Interpretasi hasil sentimen perlu mempertimbangkan kualitas data, konteks ulasan, preprocessing, serta metode klasifikasi yang digunakan.

Hasil analisis sentimen tidak selalu merepresentasikan keseluruhan pengalaman pelanggan dan sebaiknya digunakan sebagai salah satu sumber informasi dalam analisis lebih lanjut.

## 👤 Author

**ADI PRABU JAYANEGARA**  
NIM: **5220411346**

---

⭐ Jika repository ini bermanfaat, silakan berikan **Star** pada repository.
