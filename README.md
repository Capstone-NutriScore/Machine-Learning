# NutriScore – Machine Learning Module

Modul ini merupakan inti dari sistem kecerdasan buatan dalam aplikasi **NutriScore**, yang bertugas untuk mengenali jenis makanan dari gambar dan menganalisis kandungan gizinya. Model dilatih menggunakan kombinasi dataset gambar makanan, informasi gizi, dan resep masakan Indonesia.

## Dataset yang Digunakan

1. **🍽️ Food Images Dataset**

   * Dikumpulkan dari berbagai sumber terbuka di Kaggle
   * Terdiri dari **40 kelas makanan**
   * Total **12.000 gambar**
   * Telah dibagi menjadi data training dan testing
   * 📎 [Link Dataset](#)

2. **🥗 Nutrition Dataset**

   * Berisi detail gizi untuk setiap jenis makanan
   * Meliputi kalori, lemak, protein
   * Digunakan untuk analisis kandungan gizi
   * 📎 [Link Dataset](#)

3. **🍛 Indonesian Recipes Dataset**

   * Berisi resep dan bahan makanan khas Indonesia
   * Digunakan untuk memberikan rekomendasi makanan yang lebih sehat
   * Dibagi untuk keperluan analisis dan saran masakan
   * 📎 [Link Dataset](#)

---

## Arsitektur Model

| Komponen     | Teknologi                   |
| ------------ | --------------------------- |
| Framework ML | TensorFlow                  |
| Model CNN    | MobileNetV2                 |
| Bahasa       | Python                      |
| Input Model  | Gambar makanan (image)      |
| Output Model | Label jenis makanan (kelas) |

Model ini dibangun dengan pendekatan **transfer learning**, menggunakan arsitektur **MobileNetV2** yang ringan dan optimal untuk aplikasi berbasis mobile atau web.

---

## Cara Menjalankan

Untuk menjalankan proses pelatihan, evaluasi, dan inferensi model, Anda dapat menggunakan dua cara:

### 1. **Menggunakan Google Colab**

* **Langkah-langkah**:

  1. Buka file notebook `.ipynb` yang tersedia di Google Colab.
  2. Jalankan sel secara berurutan.
  3. Seluruh proses sudah dituliskan secara lengkap di dalam notebook, termasuk:

     * Preprocessing data
     * Augmentasi gambar
     * Training model
     * Evaluasi akurasi
     * Prediksi dan visualisasi hasil

> **Tidak diperlukan setup khusus** — cukup gunakan Google Colab untuk menjalankan notebook ini secara langsung.

### 2. **Menjalankan Secara Lokal**

* **Langkah-langkah**:

  1. Clone repository ini ke komputer Anda menggunakan Git:

     ```bash
     git clone https://github.com/yourusername/nutriscore.git
     cd nutriscore
     ```
  2. Pastikan Anda telah menginstal semua pustaka yang dibutuhkan:

     ```bash
     pip install tensorflow matplotlib seaborn scikit-learn kaggle
     ```
  3. Siapkan file `kaggle.json` dengan API key Kaggle Anda, kemudian salin ke folder `.kaggle`:

     ```bash
     mkdir -p ~/.kaggle
     cp kaggle.json ~/.kaggle/
     chmod 600 ~/.kaggle/kaggle.json
     ```
  4. Unduh dataset dari Kaggle:

     ```bash
     kaggle datasets download -d feniakarenina/nutriscore-dataset
     unzip nutriscore-dataset.zip
     ```
  5. Pastikan struktur folder dataset sesuai dengan yang dijelaskan di notebook dan lanjutkan untuk menjalankan sel notebook secara berurutan.

---

## Hasil

Model menunjukkan akurasi tinggi dalam mengenali jenis makanan, dan dapat diintegrasikan dengan komponen web (frontend/backend) untuk menampilkan skor gizi dan rekomendasi sehat secara real-time.

---

Dengan panduan ini, Anda dapat menjalankan proyek **NutriScore** baik menggunakan Google Colab untuk kemudahan akses atau secara lokal jika Anda ingin mengontrol lebih banyak aspek dari proses pelatihan. Jika ada langkah lain yang perlu disesuaikan, beri tahu saya!
