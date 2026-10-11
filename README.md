
# Tugas Take-Home Sesi 05: Advanced CNNs and Transfer Learning

Repositori ini dikembangkan untuk memenuhi penugasan mata kuliah Pembelajaran Mesin / Computer Vision. Proyek ini berfokus pada perbandingan performa model Convolutional Neural Networks (CNN) menggunakan teknik *Transfer Learning*, *Fine-Tuning*, dan *Data Augmentation* pada dataset citra terbatas (*small-data regime*).

## 👤 Informasi Mahasiswa
* **Nama:** Mark Philip Lengkong
* **NIM:** 2802491715
* **Program Studi:** Computer Science - BINUS University

## 📂 Struktur Berkas Repositori
* `BagA&C_2802491715_MarkPhilipLengkong.pdf`: Jawaban Bagian A dan Laporan(Bagian C)
* `README.md`: Dokumentasi penjelasan repositori.
* `Tugas05_2802491715_MarkPhilipLengkong.ipynb`: Berkas Jupyter Notebook utama yang berisi seluruh kode pelatihan dari kondisi B1 hingga B5, evaluasi model, dan *failure analysis.
* `metrics_summary.csv`: Berkas log metrik mentah hasil pencatatan eksperimen pelatihan.
* `requirements.txt`: Daftar pustaka dependensi Python yang dibutuhkan.

## 📊 Rangkuman Kondisi Eksperimen (Oxford-IIIT Pet Dataset)
Eksperimen dilakukan menggunakan subset 10 kelas target (5 ras kucing dan 5 ras anjing) dengan arsitektur utama **ResNet-18** dan pembanding **EfficientNet-B0**:
* **B1 (Baseline From Scratch):** Pelatihan bobot acak dari nol.
* **B2 (Feature Extraction):** Pembekuan seluruh lapisan *backbone* dan pelatihan pada *classifier head* baru.
* **B3 (Progressive Fine-Tuning):** Pembukaan pembekuan pada `layer4` dengan *differential learning rate*.
* **B4 (Control Data Augmentation):** Pengujian dampak isolasi data augmentasi.
* **B5 (EfficientNet-B0):** Evaluasi arsitektur modern berorientasi efisiensi.

## 🚀 Cara Menjalankan Kode
1. Unggah berkas `Tugas05_2802491715_MarkPhilipLengkong.ipynb` ke **Google Colab**.
2. Pastikan *Runtime type* diatur menggunakan **GPU T4**.
3. Jalankan seluruh sel secara berurutan (*Run All*). Dataset Oxford-IIIT Pet akan diunduh secara otomatis melalui `torchvision`.
