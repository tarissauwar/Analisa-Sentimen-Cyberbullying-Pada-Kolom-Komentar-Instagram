# 🧠 Analisis Sentimen Komentar Instagram Menggunakan NLP

Proyek ini berfokus pada **analisis sentimen komentar Instagram** menggunakan pendekatan **Natural Language Processing (NLP)**. Dataset yang digunakan berisi komentar dengan label **positif** dan **negatif**, yang merepresentasikan opini pengguna terhadap suatu topik atau akun.

Tahapan utama dalam proyek ini meliputi **pembersihan teks (text preprocessing)** seperti *lowercasing*, penghapusan tanda baca, tokenisasi, *stopword removal*, dan *stemming* menggunakan **Sastrawi**. Setelah teks dibersihkan, data direpresentasikan menggunakan **Bag of Words (BoW)** agar dapat dianalisis lebih lanjut.

Proyek ini juga menampilkan berbagai **visualisasi data**, seperti distribusi komentar positif dan negatif, serta kata yang paling sering muncul di setiap kategori. Hasil analisis ini diharapkan dapat memberikan gambaran umum mengenai opini publik di media sosial.

---

## 📂 Dataset

Dataset yang digunakan:

```
dataset_komentar_instagram_cyberbullying.csv
```

Berisi dua kolom utama:

* `comment` → teks komentar dari pengguna
* `label` → kategori sentimen (`positive` atau `negative`)

---

## ⚙️ Instalasi dan Dependensi

Sebelum menjalankan notebook, pastikan semua dependensi berikut sudah terinstal:

```bash
pip install contractions
pip install Sastrawi
pip install nltk
pip install seaborn
pip install scikit-learn
pip install pandas
pip install matplotlib
```

Atau langsung jalankan di notebook:

```python
!pip install contractions
!pip install Sastrawi
```

---

## 🧹 Tahapan Preprocessing

Langkah-langkah utama pembersihan teks:

1. **Lowercasing** → mengubah seluruh teks menjadi huruf kecil.
2. **Menghapus tanda baca dan angka** → agar teks lebih bersih.
3. **Tokenization** → memecah kalimat menjadi kata-kata.
4. **Stopword Removal** → menghapus kata umum yang tidak bermakna penting.
5. **Stemming (Sastrawi)** → mengubah kata ke bentuk dasarnya.

Contoh fungsi pembersihan teks:

```python
def clean_text(text):
    text = text.lower()
    text = re.sub(r'[^a-z\s]', '', text)
    tokens = word_tokenize(text)
    tokens = [stemmer.stem(word) for word in tokens if word not in stopwords]
    return ' '.join(tokens)
```

---

## 🧮 Representasi Teks

Teks yang telah dibersihkan diubah menjadi representasi numerik menggunakan **Bag of Words (BoW)**:

```python
from sklearn.feature_extraction.text import CountVectorizer

vectorizer = CountVectorizer()
X = vectorizer.fit_transform(df_comments['cleaned_text'])
```

---

## 📊 Visualisasi

Beberapa visualisasi yang dihasilkan:

* Distribusi komentar positif dan negatif
* Frekuensi kata terbanyak per kategori
* Word frequency analysis dengan Matplotlib dan Seaborn

Contoh visualisasi:

```python
sns.countplot(x='label', data=df_comments)
plt.title('Distribusi Sentimen Komentar Instagram')
plt.show()
```

---
