# 🔢 Mengenal MNIST dan Penerapan CNN Menggunakan PyTorch
<!-- Heading utama (gunakan tanda # untuk H1). -->

Pernah terpikir bagaimana mesin bisa mengenali tulisan tangan kita?  
Dari angka di kertas ujian, nota belanja, sampai formulir digital — semuanya bisa dibaca otomatis berkat *Computer Vision* dan *Deep Learning*.  

Dataset yang sering dipakai untuk melatih model ini adalah **MNIST (Modified National Institute of Standards and Technology)**.  
Dataset ini berisi 70.000 gambar angka tulisan tangan dari 0 sampai 9, berukuran 28x28 piksel.

---

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

## 🔗 Coba Sendiri di Google Colab
<!-- Cara menambahkan link aktif -->

Kamu bisa mencoba kode latihan langsung di Colab melalui tautan di bawah ini:

👉 [**Buka Notebook di Google Colab**](https://colab.research.google.com/)

<!-- Format link: [teks tampil](alamat tautan) -->

---

## 📚 Referensi
<!-- Daftar pustaka atau sumber jurnal -->

1. Purwanto, A., & Hidayat, R. (2023). *Implementasi Convolutional Neural Network pada Dataset MNIST Menggunakan PyTorch*. **Jurnal Teknologi Informasi dan Komputer**, 5(2), 45–52.  
2. Sari, D., & Nugroho, F. (2022). *Pengenalan Tulisan Tangan Menggunakan Deep Learning pada Dataset MNIST*. **Jurnal Sains dan Komputer Indonesia**, 4(1), 12–20.

---

✍️ **Ditulis oleh:** Eva Fauziah  
📅 **Tanggal:** 27 Oktober 2025  
🔗 **Repo:** [GitHub Repo kamu](https://github.com/eva-fauziah/artikel-ku)
