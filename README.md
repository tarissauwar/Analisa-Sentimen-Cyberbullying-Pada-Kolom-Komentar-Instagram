# 📊 Analisis Sentimen Komentar Instagram untuk Deteksi Cyberbullying

**Dataset**: [Dataset Komentar Instagram - Cyberbullying](https://raw.githubusercontent.com/rizalespe/Dataset-Sentimen-Analisis-Bahasa-Indonesia/master/dataset_komentar_instagram_cyberbullying.csv)  

---

## 📖 Deskripsi

Proyek ini bertujuan untuk menganalisis sentimen komentar pada platform media sosial, khususnya Instagram, untuk mendeteksi kemungkinan adanya **cyberbullying**. Dataset yang digunakan mencakup komentar dalam Bahasa Indonesia yang diambil dari platform Instagram dan diklasifikasikan berdasarkan sentimen, yaitu apakah komentar tersebut mengandung unsur cyberbullying atau tidak.

Analisis ini diharapkan dapat membantu dalam pengembangan model deteksi cyberbullying, yang dapat digunakan oleh platform media sosial atau pihak terkait untuk memantau dan menangani kasus cyberbullying dengan lebih efektif.

---

## 📂 Struktur Dataset

Dataset terdiri dari kolom-kolom berikut:

- **Komentar**: Teks komentar dalam Bahasa Indonesia yang diambil dari Instagram.
- **Label**: Kategori atau kelas sentimen dari komentar, yang menunjukkan apakah komentar tersebut tergolong cyberbullying atau bukan.

Label terdiri dari dua kategori utama:
- **Bullying**: Komentar yang mengandung unsur cyberbullying.
- **Non-Bullying**: Komentar yang tidak mengandung unsur cyberbullying.

---

## 🔍 Metodologi

1. **Preprocessing Data**  
   - *Text Cleaning*: Menghapus tanda baca, angka, dan karakter yang tidak relevan dari teks.
   - *Tokenization*: Memisahkan teks menjadi kata-kata individu (token) untuk memudahkan analisis.
   - *Stopword Removal*: Menghapus kata-kata umum (seperti "dan", "yang", dll.) yang tidak memberikan informasi penting untuk deteksi sentimen.
   - *Stemming*: Mengonversi kata ke bentuk dasarnya untuk mengurangi jumlah kata yang perlu dianalisis.

2. **Algoritma Klasifikasi**  
   Berbagai model klasifikasi dapat digunakan untuk menganalisis sentimen pada dataset ini, seperti:
   - **Naive Bayes**: Sering digunakan dalam analisis teks dan memberikan hasil yang baik pada klasifikasi sentimen.
   - **Support Vector Machine (SVM)**: Algoritma kuat yang cocok untuk klasifikasi teks dengan data biner.
   - **Random Forest**: Algoritma berbasis pohon yang dapat digunakan untuk klasifikasi sentimen dengan kinerja yang cukup baik.

3. **Evaluasi Model**  
   Menggunakan metrik seperti akurasi, presisi, recall, dan F1-score untuk menilai kinerja model dalam mendeteksi komentar yang mengandung cyberbullying.

---

## 🚀 Cara Menggunakan

1. **Download** dataset dari URL berikut: [Dataset Komentar Instagram - Cyberbullying](https://raw.githubusercontent.com/rizalespe/Dataset-Sentimen-Analisis-Bahasa-Indonesia/master/dataset_komentar_instagram_cyberbullying.csv).
2. **Lakukan Preprocessing** pada teks menggunakan teknik yang telah dijelaskan di atas.
3. **Latih Model Klasifikasi** menggunakan algoritma pilihan Anda untuk mendeteksi komentar yang termasuk dalam kategori cyberbullying.
4. **Evaluasi Hasil** untuk menilai akurasi dan performa model dalam mendeteksi komentar yang mengandung cyberbullying.

---
