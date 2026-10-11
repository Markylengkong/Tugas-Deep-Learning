
# Tugas Take-Home Sesi 05: Advanced CNNs and Transfer Learning

Repositori ini dikembangkan untuk memenuhi penugasan mata kuliah Pembelajaran Mesin / Computer Vision[cite: 1]. Proyek ini berfokus pada perbandingan performa model Convolutional Neural Networks (CNN) menggunakan teknik *Transfer Learning*, *Fine-Tuning*, dan *Data Augmentation* pada dataset citra terbatas (*small-data regime*)[cite: 2, 4].

## 👤 Informasi Mahasiswa
* **Nama:** Mark Philip Lengkong
* **NIM:** 2802491715
* **Program Studi:** Computer Science - BINUS University

## 📂 Struktur Berkas Repositori
* `Tugas05_2802491715_MarkPhilipLengkong.ipynb`: Berkas Jupyter Notebook utama yang berisi seluruh kode pelatihan dari kondisi B1 hingga B5, evaluasi model, dan *failure analysis*[cite: 1, 5, 7, 8].
* `metrics_summary.csv`: Berkas log metrik mentah hasil pencatatan eksperimen pelatihan[cite: 8, 10].
* `requirements.txt`: Daftar pustaka dependensi Python yang dibutuhkan.
* ''
* `README.md`: Dokumentasi penjelasan repositori[cite: 8].

## 📊 Rangkuman Kondisi Eksperimen (Oxford-IIIT Pet Dataset)
Eksperimen dilakukan menggunakan subset 10 kelas target (5 ras kucing dan 5 ras anjing) dengan arsitektur utama **ResNet-18** dan pembanding **EfficientNet-B0**[cite: 4, 5]:
* **B1 (Baseline From Scratch):** Pelatihan bobot acak dari nol[cite: 5].
* **B2 (Feature Extraction):** Pembekuan seluruh lapisan *backbone* dan pelatihan pada *classifier head* baru[cite: 5].
* **B3 (Progressive Fine-Tuning):** Pembukaan pembekuan pada `layer4` dengan *differential learning rate*[cite: 5].
* **B4 (Control Data Augmentation):** Pengujian dampak isolasi data augmentasi[cite: 5].
* **B5 (EfficientNet-B0):** Evaluasi arsitektur modern berorientasi efisiensi[cite: 5].

## 🚀 Cara Menjalankan Kode
1. Unggah berkas `Tugas05_NIM_Nama.ipynb` ke **Google Colab**[cite: 1].
2. Pastikan *Runtime type* diatur menggunakan **GPU T4**[cite: 1].
3. Jalankan seluruh sel secara berurutan (*Run All*). Dataset Oxford-IIIT Pet akan diunduh secara otomatis melalui `torchvision`[cite: 4].
