# **Strukturisasi Data dan Arsip Digital dengan OCR**

## **Deskripsi Proyek**

Proyek ini bertujuan untuk mengonversi dokumen tanah yang telah dipindai ke format digital yang dapat dicari, menggunakan pipeline OCR. Proses ini mencakup preprocessing gambar, deteksi struktur tabel, ekstraksi teks, hingga penyimpanan hasil dalam format CSV.

## **Fitur Utama**

- **Preprocessing Gambar:** Meningkatkan kualitas gambar untuk hasil OCR yang lebih baik.
- **Deteksi dan Ekstraksi Teks:** Menggunakan Tesseract OCR untuk mendeteksi teks dari dokumen.
- **Penyimpanan Hasil:** Hasil OCR disimpan dalam format CSV yang terstruktur.
- **User-Friendliness:** Disertai dengan panduan dalam bentuk video dan manual.

## **Struktur Folder yang Dibutuhkan**

```plaintext
|-- BERKAS LETTER C/
|   |-- berkas 0-100.pdf
|   |-- berkas 100-200.pdf
|   |-- ...
|   |-- berkas 900-968.pdf
|   |-- berkas sisa sobekan 400-500.pdf
```

## **Hirarki Folder Output yang Diharapkan**

```plaintext
|-- file png berkas 0-100/
|   |-- langkah 1.1 konversi ke grayscale
|   |-- |-- halaman_1.png
|   |-- |-- halaman_2.png
|   |-- |-- ...
|   |-- |-- halaman_100.png
|   |-- langkah 1.2 meningkatkan kontras menggunakan CLAHE
|   |-- |-- halaman_1.png
|   |-- |-- halaman_2.png
|   |-- |-- ...
|   |-- |-- halaman_100.png
|   |-- langkah 1.3 menghapus noise menggunakan median blurring
|   |-- |-- halaman_1.png
|   |-- |-- halaman_2.png
|   |-- |-- ...
|   |-- |-- halaman_100.png
|   |-- langkah 1.4 normalisasi dimensi
|   |-- |-- halaman_1.png
|   |-- |-- halaman_2.png
|   |-- |-- ...
|   |-- |-- halaman_100.png
|   |-- langkah 2.1 mendeteksi struktur tabel
|   |-- |-- halaman_1.png
|   |-- |-- halaman_2.png
|   |-- |-- ...
|   |-- |-- halaman_100.png
|   |-- langkah 2.2 menghapus struktur tabel untuk mengekstraksi teks
|   |-- |-- halaman_1.png
|   |-- |-- halaman_2.png
|   |-- |-- ...
|   |-- |-- halaman_100.png
|   |-- langkah 3.1 menerapkan OCR untuk mengekstrak teks
|   |-- |-- halaman_1.txt
|   |-- |-- halaman_2.txt
|   |-- |-- ...
|   |-- |-- halaman_100.txt
|   |-- langkah 3.2 membersihkan hasil OCR
|   |-- |-- halaman_1.txt
|   |-- |-- halaman_2.txt
|   |-- |-- ...
|   |-- |-- halaman_100.txt
|   |-- langkah 3.3 menyimpan hasil OCR dengan header yang benar
|   |-- |--berkas 0-100_OCR_results.csv
|-- file png berkas 100-200/
|-- file png berkas 200-300/
|-- ...
|-- file png berkas 900-968/
|-- file png berkas sisa sobekan 400-500/
```

## **Prasyarat**

- **Python 3.9 atau lebih baru**
- **Tesseract OCR:** Pastikan Tesseract OCR telah diinstal dan dapat diakses melalui PATH sistem.
- **IDE (Integrated Development Environment):** Pastikan sudah diinstal IDE seperti Virtual Studio Code.

## **Cara Menjalankan Proyek**

- Pastikan Tesseract OCR telah diinstal dan tersedia di PATH sistem.
- Siapkan file PDF dalam folder Berkas Files.
- Buka file notebook ocr.ipynb di VSCode atau Jupyter Notebook.
- Jalankan langkah-langkah sesuai urutan pipeline.

## **Panduan Pengguna**

- Manual pengguna tersedia dalam file `PANDUAN PENGGUNAAN PIPELINE OCR.pdf`.

## **Troubleshooting**

- **Tesseract tidak terdeteksi:** Pastikan Tesseract telah diinstal dan PATH sistem mengarah ke direktori Tesseract.
- **Hasil OCR kosong:** Periksa kualitas gambar input, pastikan dokumen tidak buram atau terlalu gelap. Pastikan konfigurasi OCR sudah benar.

## **Kontribusi**

Jika Anda ingin memperbaiki atau meningkatkan proyek ini, silakan fork repository ini dan ajukan pull request. Kami terbuka untuk ide-ide baru.
