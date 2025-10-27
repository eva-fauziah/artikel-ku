# Mengenal MNIST dan Penerapan CNN Menggunakan PyTorch 🚀


Di era digital saat ini, kemampuan komputer untuk "melihat" dan memahami dunia melalui gambar, atau yang dikenal sebagai **Klasifikasi Citra (*Image Classification*)**, telah menjadi salah satu bidang paling revolusioner dalam Kecerdasan Buatan (AI). Klasifikasi citra adalah fondasi bagi banyak teknologi canggih, mulai dari diagnosis medis otomatis, kendaraan otonom, hingga pengenalan wajah. Kunci di balik akurasi dan keajaiban ini adalah **Jaringan Saraf Tiruan Konvolusional (*Convolutional Neural Network* atau CNN)**.


Artikel ini bertujuan untuk mengenalkan **MNIST**, yang sering dijuluki sebagai *dataset* "Hello World" bagi para peneliti dan pengembang *deep learning*. Selanjutnya, kita akan mengupas tuntas penerapan model CNN yang efektif untuk mengklasifikasikan digit-digit tulisan tangan ini, dengan menggunakan salah satu *framework* *deep learning* terpopuler saat ini: **PyTorch**.

---

## A. Mengenal Dataset MNIST

### 1. Apa itu MNIST?

**MNIST** merupakan singkatan dari **Modified National Institute of Standards and Technology**. Dataset ini adalah koleksi klasik yang berisi **70.000 gambar digit tulisan tangan** (angka 0 hingga 9). Secara spesifik, setiap gambar dalam MNIST memiliki **resolusi rendah $28 \times 28$ piksel**, dan disajikan dalam format **Grayscale** (hanya memiliki 1 kanal warna).  Kesederhanaan, namun kompleksitasnya yang cukup, menjadikannya titik awal yang sempurna untuk mempelajari dan menguji model klasifikasi.

### 2. Peran MNIST

Sejak dirilis, MNIST telah menjadi **tolok ukur (*benchmark*)** standar dalam komunitas *machine learning*. Ketika seorang peneliti mengembangkan arsitektur jaringan saraf atau algoritma pelatihan yang baru, hasil kinerjanya pada MNIST sering kali menjadi bukti awal efektivitas model tersebut. Mencapai akurasi di atas 99% pada MNIST menjadi target awal yang menandakan bahwa sebuah model klasifikasi siap untuk diuji pada dataset yang lebih kompleks dan beragam.

---

## B. Dasar-Dasar Convolutional Neural Network (CNN)

### 1. Prinsip Kerja CNN

**Convolutional Neural Network (CNN)** adalah jenis Jaringan Saraf Tiruan (JST) yang dirancang khusus untuk memproses data visual. Prinsip kerjanya meniru cara **korteks visual otak manusia** mengidentifikasi objek, yaitu dengan memecah gambar menjadi hierarki fitur yang semakin kompleks. CNN secara otomatis dapat mempelajari dan mengekstrak fitur penting (tepi, garis, bentuk) langsung dari data piksel, tanpa perlu rekayasa fitur manual.

### 2. Komponen Utama CNN

Sebuah arsitektur CNN umumnya terdiri dari tiga jenis lapisan inti:

* **Lapisan Konvolusi (*Convolutional Layer*):** Ini adalah jantung dari CNN. Lapisan ini menggunakan filter atau *kernel* untuk melakukan operasi konvolusi pada gambar *input*, menghasilkan peta fitur (*feature map*) yang menyoroti fitur-fitur penting seperti tepi atau tekstur.
* **Lapisan *Pooling* (*Pooling Layer*):** Biasanya menggunakan **Max-Pooling** untuk mengurangi dimensi spasial (*width* dan *height*) dari peta fitur. Tujuannya adalah mengurangi jumlah parameter dan komputasi, sekaligus membuat model lebih tangguh terhadap variasi posisi (translasi) pada citra.
* **Lapisan *Fully Connected* (*Dense Layer*):** Setelah lapisan konvolusi dan *pooling* berhasil mengekstrak fitur, data di-*flatten* (diratakan) dan dimasukkan ke lapisan *fully connected* di akhir jaringan. Lapisan ini bertanggung jawab untuk melakukan klasifikasi akhir berdasarkan fitur-fitur yang telah dipelajari.

---

## C. PyTorch: Pilihan Framework Modern

### 1. Mengapa PyTorch?

**PyTorch** adalah *framework* *deep learning* sumber terbuka yang dikembangkan oleh Facebook (Meta AI) dan kini menjadi pilihan utama dalam lingkungan penelitian dan pengembangan akademik. Keunggulan utamanya terletak pada sifat **grafik komputasi dinamis (*dynamic computation graph*)**-nya, yang memberikan fleksibilitas tinggi kepada pengembang untuk memodifikasi dan men-debug model dengan mudah selama proses pelatihan.

### 2. Struktur Dasar PyTorch

Untuk mengimplementasikan model *deep learning*, PyTorch menyediakan beberapa modul utama:

| Modul PyTorch | Deskripsi Singkat |
| :--- | :--- |
| `torch.Tensor` | Struktur data dasar, mirip array NumPy, namun mendukung akselerasi GPU. |
| `torch.nn` | Modul yang berisi semua blok bangunan (lapisan) untuk membangun jaringan saraf, seperti `Conv2d`, `MaxPool2d`, dan `Linear`. |
| `torch.optim` | Menyediakan berbagai algoritma optimasi (*optimizer*) seperti SGD dan Adam, yang digunakan untuk menyesuaikan bobot model. |
| `torch.utils.data.DataLoader` | Alat penting untuk pemuatan data (*loading*) dan pengelompokan data dalam bentuk *batch* secara efisien selama pelatihan. |

---
## D. Contoh Implementasi MNIST
## Klasifikasi Angka Tulisan Tangan Menggunakan PyTorch dan Dataset MNIST
## ⚙️ Arsitektur CNN untuk MNIST di PyTorch
<!-- Heading kedua (gunakan ## untuk H2). -->

Struktur model yang digunakan dalam eksperimen ini meliputi dua lapisan konvolusi, dua lapisan fully connected, serta fungsi aktivasi ReLU dan Softmax.  
Model diimplementasikan menggunakan framework **PyTorch** dengan optimizer **Adam**.

Berikut tabel ringkas parameternya:

| Komponen | Detail |
|:--|:--|
| Framework | PyTorch |
| Dataset | MNIST |
| Arsitektur | 2 Conv Layer + 2 Fully Connected Layer |
| Optimizer | Adam |
| Epoch | 3 |
| Batch Size | 64 |

---

## 🔗 Lihat Hasil Eksperimen

<!-- Format link: [teks tampil](alamat tautan) -->
Kamu bisa melihat hasil eksperimen dan kode lengkap pada notebook berikut:

👉 [**MNIST CNN Notebook**](https://github.com/eva-fauziah/artikel-ku/blob/main/Klasifikasi_Angka_Tulisan_Tangan_Menggunakan_PyTorch_dan_Dataset_MNIST.ipynb)

---

## 📊 Hasil Pelatihan
<!-- Tabel hasil training -->

Model dilatih selama tiga epoch dengan hasil sebagai berikut:

| Epoch | Loss |
|:--:|:--:|
| 1 | 0.1616 |
| 2 | 0.0294 |
| 3 | 0.0023 |

Penurunan *loss* menandakan bahwa model semakin baik mengenali pola angka.

---

## 💡 Insight

Hasil eksperimen ini menunjukkan bahwa kemampuan Convolutional Neural Network (CNN) dalam mengenali pola visual sederhana sangatlah kuat, bahkan pada arsitektur yang minimalis. Nilai loss yang menurun drastis dan akurasi yang mencapai sekitar 98% membuktikan bahwa model mampu belajar representasi fitur angka dengan efektif tanpa perlu rekayasa fitur manual. Hal ini menegaskan bahwa deep learning  khususnya CNN  dapat mengekstraksi informasi visual secara otomatis dan efisien, sehingga menjadi fondasi penting bagi aplikasi computer vision yang lebih kompleks seperti deteksi objek, pengenalan wajah, maupun analisis citra medis.

---

## 🔗 Coba Sendiri di Google Colab
<!-- Cara menambahkan link aktif -->

Kamu bisa mencoba kode latihan langsung di Colab melalui tautan di bawah ini:

👉 [**Buka Notebook di Google Colab**](https://colab.research.google.com/)

---

## 📚 Referensi
<!-- Daftar pustaka atau sumber jurnal -->

### 2. Daftar Pustaka

[1]  Fitriati, D. "PERBANDINGAN KINERJA CNN LeNet 5 DAN EXTREME LEARNING MACHINE PADA PENGENALAN CITRA TULISAN TANGAN ANGKA," *Jurnal Teknologi Terpadu*, Vol. [2], No. [1], [2016]. Tersedia daring: [https://journal.nurulfikri.ac.id/index.php/JTT/article/view/45](https://journal.nurulfikri.ac.id/index.php/JTT/article/view/45)

[2] Al-Hafizh F., Alamsyah A. (2024). Penerapan model deep-CNN untuk meningkatan akurasi klasifikasi bahasa isyarat alfabet menggunakan algoritma convolutional neural network. Indonesian Journal of Mathematics and Natural Sciences, 47(1), 1-11. Tersedia daring: [https://journal.unnes.ac.id/journals/JM/article/download/4560/319/10187](https://journal.unnes.ac.id/journals/JM/article/download/4560/319/10187)

---

✍️ **Ditulis oleh:** Eva Fauziah  
📅 **Tanggal:** 27 Oktober 2025  
🔗 **Repo:** [GitHub Repo](https://github.com/eva-fauziah/artikel-ku)
