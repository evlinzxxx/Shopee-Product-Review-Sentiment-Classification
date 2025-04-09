## Proyek Analisis Sentimen Ulasan Produk di Shopee  
**Nama:** Evlin Sitanggang  

### 1. **Persiapan Library & Dataset**
- Mengimpor berbagai library penting seperti `pandas`, `re`, `Sastrawi`, `nltk`, `scikit-learn`, dan `TensorFlow`.
- Membaca dataset `review_shopee.csv` yang berisi ulasan produk dari aplikasi Shopee.

### 2. **Pembersihan Data (Data Cleaning)**
- Menghapus nilai kosong (missing value) pada kolom review.
- Menghapus data duplikat agar analisis lebih akurat.
- Menyimpan hanya kolom yang relevan: `content` diubah menjadi `review`.

### 3. **Preprocessing Teks**
Melibatkan beberapa tahapan penting, yaitu:
- **Cleaning text**: Menghapus mentions, hashtag, RT, angka, link, newline, dan tanda baca.
- **Case folding**: Mengubah semua huruf menjadi huruf kecil.
- **Slang word normalization**: Mengubah kata tidak baku menjadi bentuk baku.
- **Tokenisasi**: Memecah kalimat menjadi kata-kata.
- **Stopword removal**: Menghapus kata-kata umum yang tidak membawa makna penting.
- **Stemming Bahasa Indonesia** menggunakan **Sastrawi**.

### 4. **Labeling Sentimen**
- Memberikan label sentimen berdasarkan data atau aturan tertentu (misalnya: dari konteks atau rating).
- Label: **Positif**, **Netral**, dan **Negatif**.

### 5. **Ekstraksi Fitur**
- Menggunakan teknik **TF-IDF Vectorizer** untuk mengubah teks menjadi fitur numerik.
- Data dibagi menjadi data latih dan data uji (train-test split).

### 6. **Pembangunan Model**
- Model yang digunakan: **Naive Bayes** (BernoulliNB).
- Melatih model dengan data yang telah diproses.
- Menghitung akurasi dan precision sebagai metrik evaluasi model.

### 7. **Visualisasi & Analisis Hasil**
- Menampilkan WordCloud dari kata-kata yang sering muncul di ulasan.
- Membandingkan jumlah masing-masing kategori sentimen dengan diagram batang atau pie chart.
- Menganalisis kata-kata yang sering muncul di masing-masing kategori sentimen.
