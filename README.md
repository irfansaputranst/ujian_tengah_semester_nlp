# UJIAN TENGAH SEMESTER NLP

## Deskripsi
Dokumen ini menjelaskan penerapan teknik Natural Language Processing (NLP) dalam pengolahan dan analisis data teks. Proyek ini melibatkan berbagai teknik pembersihan data, representasi teks, dan klasifikasi menggunakan pembelajaran mesin. Tujuannya adalah untuk mencapai hasil analisis teks yang optimal dengan menggunakan berbagai metode.

## Struktur Proyek

### **BAB I: DATA PREPROCESSING**

- **Eksplorasi Data**: 
  Pada tahap ini, data diperiksa secara menyeluruh untuk memahami karakteristik dan kualitas data sebelum proses analisis lebih lanjut. Beberapa teknik eksplorasi yang digunakan termasuk pemeriksaan distribusi kata, panjang kalimat, dan potensi masalah seperti data yang hilang atau tidak relevan.

- **Library yang Digunakan**:
  - **pandas**: Untuk manipulasi data tabular.
  - **numpy**: Untuk operasi komputasi numerik dan matriks.
  - **seaborn** & **matplotlib**: Untuk visualisasi data, seperti grafik distribusi kata dan visualisasi frekuensi kata.
  - **nltk**, **re**, dan **string**: Untuk pembersihan teks, termasuk penghapusan stopwords, tanda baca, dan karakter tidak relevan dari data teks.
  - **TfidfVectorizer**: Untuk mengonversi teks menjadi representasi numerik berbasis frekuensi kata (TF-IDF).
  - **train_test_split**: Untuk membagi data menjadi data latih (training) dan uji (testing).
  - **KNeighborsClassifier**: Untuk klasifikasi teks menggunakan algoritma K-Nearest Neighbors (KNN).
  
- **Pembersihan Data**: 
  Pada tahap ini, dilakukan penghapusan stopwords menggunakan **nltk** dan proses pembersihan lain seperti normalisasi teks dan penghapusan tanda baca yang tidak perlu.

---

### **BAB II: REPRESENTASI TEKS**

- **Tokenisasi**: 
  Proses ini memecah teks menjadi bagian-bagian yang lebih kecil yang disebut token, seperti kata atau frasa. Tokenisasi adalah langkah pertama dalam pengolahan teks untuk membangun model NLP.

- **Tokenisasi TF-IDF**:
  Setelah tokenisasi, teks diubah menjadi representasi numerik menggunakan **TF-IDF**. Teknik ini menilai seberapa penting suatu kata dalam sebuah dokumen relatif terhadap seluruh korpus, memberikan bobot yang lebih besar pada kata-kata yang lebih relevan dalam konteks dokumen tertentu.

---

### **BAB IV: KESIMPULAN**

- **Model Terbaik**: 
  Berdasarkan hasil evaluasi, model **K-Means** dengan **Word2Vec** menghasilkan performa terbaik. Model ini menggunakan K=5 (jumlah kluster) dan pembagian data 80:20 antara data latih dan data uji.

- **Akurasi**: 
  Model terbaik mencapai **96.19%** akurasi.

- **Precision**: 
  Precision model dinilai tinggi, meskipun nilai spesifik tidak disebutkan dalam analisis ini.

- **Recall**: 
  Recall model juga dinilai tinggi, tanpa nilai spesifik yang disebutkan.

- **F1-Score**: 
  F1-Score dari model ini adalah **0.967**, yang menunjukkan keseimbangan antara precision dan recall.

---

### **Hasil Analisis Lainnya**

1. **Performa Naive Bayes dengan TF-IDF**:
   - Model **Naive Bayes** yang menggunakan **TF-IDF** menunjukkan performa lebih baik pada pembagian data 70:30 dibandingkan dengan pembagian data 80:20. Hal ini menunjukkan bahwa pembagian data yang lebih besar untuk data uji (70%) memberikan hasil yang lebih optimal untuk model ini.

---

## Installasi dan Penggunaan

### 1. Install Dependensi
Pastikan Anda sudah menginstal library yang dibutuhkan dengan menjalankan perintah berikut:

```bash
pip install pandas numpy seaborn matplotlib nltk scikit-learn
