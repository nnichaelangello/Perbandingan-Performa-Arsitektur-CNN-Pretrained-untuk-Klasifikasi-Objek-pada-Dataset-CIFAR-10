# Perbandingan Arsitektur CNN untuk Klasifikasi Citra CIFAR-10

## Deskripsi Proyek
Proyek ini bertujuan untuk mengevaluasi performa dan efisiensi enam arsitektur Convolutional Neural Network (CNN) pretrained—VGG16, ResNet50, MobileNetV2, EfficientNetB0, DenseNet121, dan InceptionV3—dalam tugas klasifikasi citra pada dataset CIFAR-10. Proyek ini mencakup preprocessing citra, pelatihan model, evaluasi menggunakan metrik seperti akurasi, precision, recall, dan F1-score, serta analisis dampak arsitektur terhadap kinerja dan efisiensi komputasi. Hasil disajikan dalam laporan ringkas dan visualisasi seperti grafik akurasi, loss, dan confusion matrix.

## Fitur Utama
- **Preprocessing Citra**: Resizing ke 224x224, normalisasi, dan augmentasi sederhana (rotasi, flip, pergeseran).
- **Arsitektur CNN**: Implementasi model pretrained dengan lapisan tambahan untuk klasifikasi 10 kelas CIFAR-10.
- **Evaluasi Kinerja**: Perbandingan akurasi, precision, recall, F1-score, dan confusion matrix.
- **Analisis Efisiensi**: Pengukuran jumlah parameter, ukuran model, waktu pelatihan per epoch, dan waktu inferensi per batch.
- **Visualisasi**: Grafik akurasi/loss, confusion matrix, dan prediksi model terbaik.

## Dataset
Dataset CIFAR-10 digunakan, terdiri dari 60.000 citra berwarna (32x32 piksel) dalam 10 kelas (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck). Untuk efisiensi, subset digunakan: 2.000 sampel pelatihan dan 1.000 sampel pengujian.  
**Sumber Dataset**: [CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)

## Prasyarat
- Python 3.8+
- Library Python:
  - TensorFlow
  - NumPy
  - Pandas
  - Matplotlib
  - Seaborn
  - Scikit-learn
- Google Colab (opsional, untuk menjalankan kode dengan GPU)

## Instalasi
1. Clone repository ini:
   ```bash
   git clone https://github.com/nnichaelangello/Perbandingan-Performa-Arsitektur-CNN-Pretrained-untuk-Klasifikasi-Objek-pada-Dataset-CIFAR-10.git
   cd <repo-name>
   ```
2. Instal dependensi:
   ```bash
   pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
   ```
3. Unduh dataset CIFAR-10 (`cifar-10-python.tar.gz`) dari [sumber resmi](https://www.cs.toronto.edu/~kriz/cifar.html) dan tempatkan di direktori proyek.

## Cara Menjalankan
1. Pastikan `cifar-10-python.tar.gz` ada di direktori proyek.
2. Jalankan skrip utama:
   ```bash
   python main.py
   ```
3. Hasil pelatihan, evaluasi, dan visualisasi akan disimpan di folder hasil.
4. Laporan ringkas tersedia di `report.pdf`.

## Hasil
- **Model Terbaik**: InceptionV3 (akurasi 78,60%).
- **Keseimbangan Terbaik**: MobileNetV2 (akurasi 76,00%, efisien dengan 2,59 juta parameter).
- **Kinerja Buruk**: ResNet50 (10,90%) dan EfficientNetB0 (8,70%) memerlukan fine-tuning.
- Visualisasi dan metrik lengkap tersedia di folder hasil.

## Laporan
Laporan ringkas (3 halaman) mencakup:
- Deskripsi arsitektur CNN (VGG16, ResNet50, MobileNetV2, EfficientNetB0, DenseNet121, InceptionV3).
- Perbandingan performa (tabel akurasi, precision, recall, F1-score).
- Analisis kekuatan dan kelemahan setiap arsitektur berdasarkan kinerja dan efisiensi.

## Kontribusi
Kontribusi sangat diterima! Silakan buat *issue* untuk melaporkan bug atau *pull request* untuk perbaikan kode.
