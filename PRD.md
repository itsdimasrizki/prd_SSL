# PRD.md --- Poster Edukasi Semi-Supervised Learning (SSL)

## 1. Ringkasan Proyek

**Nama proyek:** Seri Poster Edukasi Semi-Supervised Learning\
**Format:** 12 poster berurutan, masing-masing terdiri dari 4-5 panel
berbentuk kotak\
**Bahasa:** Bahasa Indonesia\
**Audiens:** Mahasiswa Informatika dan pembaca yang baru mengenal
Machine Learning\
**Tujuan utama:** Menjelaskan konsep Semi-Supervised Learning (SSL) dari
dasar hingga contoh penerapannya pada rekomendasi kategori pekerjaan,
dengan studi kasus utama berdasarkan paper *An Improved Heterogeneous
Graph Convolutional Network for Job Recommendation* (2023).

Seri poster harus menghubungkan teori SSL dengan paper utama tanpa
mengubah klaim, metode, kategori pekerjaan, atau hasil eksperimen yang
dilaporkan paper. Adaptasi untuk kategori seperti Web Development, Data
Science, dan IoT hanya boleh disebut sebagai **contoh pengembangan
hipotetis**, bukan kategori asli atau hasil eksperimen paper.

## 2. Latar Belakang dan Masalah

Dalam Machine Learning, data berlabel membantu model mempelajari
hubungan antara masukan dan target, tetapi pemberian label dapat
membutuhkan waktu dan tenaga ahli. Sementara itu, data tanpa label dapat
tersedia dalam jumlah lebih besar. SSL memanfaatkan kombinasi data
berlabel dan tidak berlabel untuk membantu proses pembelajaran.

Dalam konteks rekomendasi pekerjaan, profil atau resume dapat memuat
informasi pendidikan, keterampilan, dan pengalaman. Paper utama mengkaji
pendekatan berbasis graf untuk mengklasifikasikan resume ke kategori
pekerjaan dengan memanfaatkan hubungan antardokumen, bukan hanya
memproses satu resume secara terisolasi.

## 3. Tujuan

1.  Menjelaskan definisi, motivasi, asumsi, dan keluarga pendekatan SSL.
2.  Membedakan contoh pendekatan SSL, seperti self-training, consistency
    regularization, dan graph-based learning.
3.  Menyajikan alur kerja SSL secara visual dan akurat.
4.  Menjelaskan studi kasus rekomendasi kategori pekerjaan berdasarkan
    paper utama.
5.  Menyajikan metode IHGCN dan hasil yang dilaporkan paper tanpa
    mengubah atau menggeneralisasikannya.
6.  Menghasilkan materi yang ringkas, konsisten, mudah dipahami, dan
    siap dipresentasikan.

## 4. Batasan dan Ketentuan Akurasi

-   Paper utama: Hao Wang, Wenchuan Yang, Jichao Li, Junwei Ou, Yanjie
    Song, dan Yingwu Chen, "An Improved Heterogeneous Graph
    Convolutional Network for Job Recommendation," *Engineering
    Applications of Artificial Intelligence*, Vol. 126, 2023, artikel
    107147.
-   DOI: `10.1016/j.engappai.2023.107147`
-   Tautan: https://doi.org/10.1016/j.engappai.2023.107147
-   Metode utama paper adalah **Improved Heterogeneous Graph
    Convolutional Network (IHGCN)**, pendekatan pembelajaran berbasis
    graf.
-   Jangan menggambarkan IHGCN sebagai metode self-training atau
    FixMatch. Keduanya boleh dibahas sebagai keluarga pendekatan SSL
    lain, dengan penegasan bahwa bukan metode utama paper.
-   Jangan menyatakan bahwa semua metode SSL menggunakan
    pseudo-labeling. Teknik SSL berbeda-beda.
-   Paper menggunakan enam kategori pekerjaan: **Technical, Management,
    Operational, Marketing, Functional, dan Research & Development**.
-   Kategori Web Development, Data Science, dan IoT bukan kategori asli
    paper. Jika digunakan untuk menjelaskan kemungkinan pengembangan
    sistem, beri label jelas sebagai contoh hipotetis.
-   Hasil eksperimen paper bukan hasil dari sistem yang sedang dirancang
    oleh kelompok.
-   Jangan membuat angka, grafik, dataset, kutipan, atau detail
    eksperimen yang tidak didukung sumber.
-   Jika suatu detail tidak dapat diverifikasi dari paper, hilangkan
    atau beri catatan "tidak dijelaskan dalam sumber yang digunakan".
-   Pisahkan informasi yang berasal dari paper dengan penjelasan umum
    tentang teori SSL.

## 5. Audiens dan Gaya Komunikasi

**Audiens utama:** Mahasiswa yang memahami dasar pemrograman tetapi
belum tentu memahami SSL atau graph neural network.

**Gaya penulisan:** 
- Bahasa Indonesia yang lugas, informatif, dan formal. 
- Satu gagasan utama per panel. 
- Istilah teknis bahasa Inggris boleh dipertahankan, lalu diberi penjelasan singkat dalam Bahasa Indonesia. 
- Hindari paragraf panjang, jargon tanpa definisi, dan klaim
berlebihan. 
- Gunakan contoh sederhana sebelum memperkenalkan istilah
teknis. 
- Jangan menyamakan "rekomendasi pekerjaan" dengan keputusan
perekrutan final. Sistem membantu mengklasifikasikan atau
merekomendasikan kategori; keputusan manusia tetap diperlukan.

## 6. Struktur Seri Poster

Setiap poster memiliki 4 panel utama. Panel kelima boleh digunakan jika
diperlukan untuk catatan, contoh, atau ringkasan. Urutan poster
membentuk alur belajar dari masalah, konsep, metode, penerapan, hingga
evaluasi.

### Poster 1 --- Mengapa Semi-Supervised Learning Dibutuhkan?

**Tujuan:** Memperkenalkan masalah data berlabel dan tidak berlabel.

1.  **Masalah label:** Label berkualitas dapat membutuhkan waktu, biaya,
    dan tenaga ahli.
2.  **Dua jenis data:** Data berlabel memiliki target; data tidak
    berlabel belum memiliki target.
3.  **Ide SSL:** Pembelajaran memanfaatkan data berlabel dan tidak
    berlabel.
4.  **Contoh intuitif:** Banyak resume tersedia, tetapi hanya sebagian
    yang sudah dikategorikan oleh ahli.

**Visual utama:** Dua kelompok dokumen, satu berlabel dan satu belum
berlabel.

### Poster 2 --- Apa Itu SSL dan Di Mana Posisinya?

**Tujuan:** Menjelaskan definisi SSL dan membedakannya dari paradigma ML
lain.

1.  **Definisi:** SSL menggunakan data berlabel dan tidak berlabel dalam
    proses pembelajaran.
2.  **Supervised learning:** Belajar dari data yang memiliki label.
3.  **Unsupervised learning:** Mencari struktur pada data tanpa label
    target.
4.  **Perbandingan:** SSL berada di antara keduanya dalam hal penggunaan
    label, tetapi bukan sekadar rata-rata dari dua metode tersebut.

**Visual utama:** Diagram perbandingan tiga paradigma. Hindari
menyatakan bahwa SSL selalu lebih baik.

### Poster 3 --- Intuisi dan Asumsi dalam SSL

**Tujuan:** Menjelaskan asumsi yang sering digunakan dalam sejumlah
metode SSL.

1.  **Smoothness assumption:** Contoh yang berdekatan atau mirip
    cenderung memiliki target yang mirip.
2.  **Cluster assumption:** Contoh dalam kelompok yang sama cenderung
    berbagi label.
3.  **Manifold assumption:** Struktur intrinsik data dapat membantu
    pembelajaran.
4.  **Catatan penting:** Asumsi ini tidak selalu berlaku dan tidak semua
    algoritma menggunakannya dengan cara yang sama.

**Visual utama:** Titik data dalam beberapa kelompok dengan label yang
ditandai.

### Poster 4 --- Self-Training dan Pseudo-Labeling

**Tujuan:** Menjelaskan salah satu keluarga pendekatan SSL, bukan
mengklaimnya sebagai metode paper utama.

1.  **Model awal:** Latih model menggunakan data berlabel.
2.  **Prediksi data baru:** Model memprediksi label untuk data yang
    belum berlabel.
3.  **Pseudo-label:** Prediksi dengan tingkat keyakinan yang memenuhi
    kriteria dapat dipakai sebagai label sementara.
4.  **Risiko:** Prediksi yang salah dapat masuk kembali ke pelatihan dan
    memperkuat kesalahan.

**Visual utama:** Alur data berlabel → model → pseudo-label → pelatihan
ulang.

### Poster 5 --- Consistency Regularization

**Tujuan:** Menjelaskan gagasan konsistensi prediksi pada variasi input.

1.  **Ide inti:** Model dipaksa untuk menghasilkan prediksi yang konsisten dan stabil meskipun data *input* sengaja di perturbasi atau modifikasi.
2.  **Dua versi augmentasi atau perturbasi:** Input diubah secara terkontrol menjadi dua versi untuk menguji prediksi model.
    *    *Augmentasi Lemah:* Perubahan kecil/halus (Misal pada CV: Pemograman Web menjadi Web Dev)
    *    *Augmentasi Kuat:* Perubahan yang lebih drastis atau kompleks namun tetap mempertahankan esensi keahliannya.
4.  **Mekanisme Konsistensi:** Model memproses data *augmentasi lemah* untuk membuat tebakan sementara (*pseudo-label*). Jika tebakan ini diyakini benar, label tersebut akan dijadikan 'kunci jawaban' (target pengawasan) untuk melatih data versi *augmentasi kuat*.
5.  **Contoh Metode (FixMatch):** FixMatch adalah algoritma populer di keluarga ini yang menggunakan ambang batas keyakinan (*confidence threshold*) untuk menyaring *pseudo-label*. 
    *(Catatan: Berikan penegasan visual bahwa FixMatch HANYA contoh komparasi dari keluarga SSL berbasis konsistensi, BUKAN metode utama dari paper rekomendasi pekerjaan IHGCN).*

**Visual utama:** 1 dokumen CV orisinal ditarik menjadi dua arah (CV Variasi Lemah & CV Variasi Kuat) → masuk ke dalam Model AI → menghasilkan *output* prediksi kategori pekerjaan yang identik (timbangan seimbang).


### Poster 6 --- Graph-Based Semi-Supervised Learning

**Tujuan:** Menyiapkan pembaca memahami pendekatan dasar berbasis graf dan GCN sebelum masuk ke metode spesifik paper utama.

1.  **Konsep Dasar Graf:** 
    *   **Node (Titik):** Mewakili entitas atau objek data tunggal. Dalam konteks kita, satu node adalah satu profil/resume pelamar.
    *   **Edge (Garis):** Mewakili hubungan atau koneksi antara dua objek (misal: kesamaan riwayat tontonan/kunjungan profil).
2.  **Mengubah Gambar Menjadi Angka:** Agar komputer memahami struktur graf ini, koneksi antar-*node* dicatat dalam sebuah tabel atau matriks yang disebut **Adjacency Matrix** (Matriks Ketetanggaan), sedangkan informasi isi CV disimpan dalam **Feature Matrix**.
3.  **Ide Inti GCN (Graph Convolutional Network):** Menggunakan *Neighborhood Aggregation*. Sebuah *node* memperbarui informasi fitur dirinya sendiri dengan cara mengumpulkan dan merangkum informasi dari *node-node* tetangga yang terhubung langsung dengannya (tetangga orde-pertama).
4.  **Aliran Label dalam SSL:** Dalam *Graph-based SSL*, informasi dari sebagian kecil *node* yang sudah memiliki label pekerjaan akan "mengalir" melalui *edge* untuk membantu memprediksi *node* lain yang belum memiliki label.

**Visual utama:** 
Ilustrasi titik-titik (node) yang saling terhubung garis (edge). Sebagian *node* sudah memiliki warna (berlabel kategori), dan menunjukkan visualisasi warna tersebut mengalir ke *node* abu-abu (tidak berlabel) di sekitarnya. 
*(Catatan Akurasi: Tambahkan keterangan bahwa ini adalah ilustrasi GCN standar, arsitektur IHGCN yang lebih lengkap akan dibahas di Poster 10).*

### Poster 7 --- Alur Umum SSL

**Tujuan:** Menampilkan proses umum tanpa menyiratkan semua algoritma
identik.

1.  **Siapkan data:** Kumpulkan data berlabel dan tidak berlabel.
2.  **Pra-pemrosesan:** Bersihkan dan ubah data menjadi representasi
    yang sesuai.
3.  **Latih model:** Gunakan pendekatan SSL yang dipilih untuk
    memanfaatkan kedua jenis data.
4.  **Evaluasi:** Ukur performa pada data evaluasi dengan label acuan
    yang tidak digunakan untuk melatih model.

**Visual utama:** Flowchart umum. Tambahkan catatan: detail proses
bergantung pada algoritma; alur IHGCN dijelaskan lebih khusus pada
Poster 10.

### Poster 8 --- Studi Kasus: Kategori Pekerjaan dari Resume

**Tujuan:** Mengaitkan teori SSL dengan masalah yang diteliti paper.

1.  **Input:** Informasi resume, seperti pendidikan dan keterampilan,
    sesuai fitur yang dibahas dalam paper.
2.  **Tantangan:** Mengategorikan banyak resume membutuhkan data dan
    label yang memadai.
3.  **Target paper:** Klasifikasi ke enam kategori pekerjaan yang
    digunakan penelitian.
4.  **Batas interpretasi:** Sistem menghasilkan klasifikasi/rekomendasi
    kategori, bukan keputusan final penerimaan kerja.

**Visual utama:** Resume → pemrosesan/representasi → kategori pekerjaan.

**Kategori asli paper:** Technical, Management, Operational, Marketing,
Functional, Research & Development.

### Poster 9 --- Paper Utama dan Masalah yang Dipecahkan

**Tujuan:** Mengenalkan paper dan kontribusinya secara tepat.

1.  **Identitas paper:** Judul, penulis, jurnal, tahun, dan DOI.
2.  **Masalah:** Rekomendasi atau klasifikasi pekerjaan berdasarkan
    resume, dengan perhatian pada pemanfaatan hubungan antardokumen.
3.  **Pendekatan:** Improved Heterogeneous Graph Convolutional Network
    (IHGCN).
4.  **Gambaran data:** Paper membahas profil publik LinkedIn dan dataset
    eksperimen; bedakan jumlah sumber profil dari jumlah sampel
    eksperimen.

**Visual utama:** Ringkasan masalah → pendekatan → keluaran. Angka
dataset hanya boleh dicantumkan setelah dicocokkan langsung dengan
bagian paper yang relevan.

### Poster 10 --- Cara Kerja IHGCN

**Tujuan:** Menjelaskan pipeline metode utama paper.

1.  **Representasi resume:** Informasi resume diproses menjadi
    representasi yang dapat digunakan model.
2.  **Pembentukan graf heterogen:** Resume dihubungkan berdasarkan
    relasi yang ditentukan dalam penelitian.
3.  **Meta-path dan konvolusi graf:** Struktur relasi digunakan untuk
    membantu representasi dan pembelajaran node.
4.  **Klasifikasi:** Model menghasilkan prediksi kategori pekerjaan.

**Visual utama:** Resume → graf heterogen → IHGCN/graph convolution →
classifier → kategori pekerjaan.

**Catatan akurasi:** Nama dan makna meta-path harus mengikuti paper.
Paper membahas RDR (tingkat pendidikan yang sama), RSR (jenis
keterampilan yang sama), RUR (peringkat universitas yang sama), dan RMR
(kategori jurusan yang sama). Jelaskan hanya jika istilah tersebut sudah
diverifikasi pada naskah yang digunakan.

### Poster 11 --- Hasil Eksperimen dan Cara Membacanya

**Tujuan:** Merangkum hasil paper tanpa melebih-lebihkan kesimpulan.

1.  **Metrik:** Jelaskan Accuracy, Precision, Macro-F1, dan AUC secara
    ringkas.
2.  **Hasil IHGCN:** Accuracy 85,91%; Precision 90,11%; Macro-F1 82,18%;
    AUC 84,75%, sesuai angka yang dilaporkan paper.
3.  **Perbandingan:** Paper melaporkan accuracy GCN 73,50%, GAT 66,44%,
    dan SVM 57,45%.
4.  **Interpretasi dan batasan:** Hasil berlaku pada eksperimen dan
    setup paper; tidak menjamin performa yang sama pada dataset lain.

**Visual utama:** Grafik batang sederhana untuk metrik yang benar-benar
sebanding. Jangan menaruh metrik berbeda dalam satu grafik seolah-olah
setara. Periksa ulang angka dan nama baseline pada naskah final sebelum
publikasi.

### Poster 12 --- Kesimpulan, Batasan, dan Referensi

**Tujuan:** Menutup seri dengan rangkuman dan bahan diskusi.

1.  **Ringkasan SSL:** SSL memanfaatkan data berlabel dan tidak
    berlabel, dengan cara yang bergantung pada algoritmanya.
2.  **Pelajaran dari IHGCN:** Struktur hubungan antarresume dapat
    dimanfaatkan dalam pendekatan graph-based learning.
3.  **Batasan:** Kualitas data, kualitas relasi graf, distribusi
    kategori, dan perbedaan domain dapat memengaruhi hasil.
4.  **Referensi dan diskusi:** Cantumkan sitasi lengkap paper utama dan
    2--3 pertanyaan diskusi.

**Pertanyaan diskusi yang disarankan:** - Mengapa hubungan antarresume
dapat membantu klasifikasi kategori pekerjaan? - Apa risiko jika relasi
antardokumen yang dibentuk ternyata tidak relevan? - Apa yang perlu
diuji sebelum pendekatan ini diterapkan pada kategori pekerjaan lain?

## 7. Ketentuan Desain Visual

-   **Jumlah:** 10 poster maksimal 12 poster.
-   **Panel:** 4 panel per poster sebagai standar; maksimal 5.
-   **Format:** Gunakan rasio dan ukuran kanvas yang sama untuk seluruh
    poster. Pilih format A3 vertikal jika akan dicetak; untuk presentasi
    digital, gunakan rasio konsisten yang mudah dibaca.
-   **Grid:** Susun panel secara konsisten; gunakan judul poster, nomor
    poster, dan indikator progres.
-   **Palet:** mengikuti template poster. Pastikan
    kontras teks terbaca.
-   **Tipografi:** Maksimal dua keluarga font.
-   **Teks:** Judul singkat, isi berupa poin pendek, dan definisi
    istilah teknis seperlunya.
-   **Diagram:** Utamakan flowchart, node-edge, perbandingan, dan
    ilustrasi konseptual. Hindari kode program.
-   **Konsistensi:** Gunakan gaya ikon, garis, panah, radius panel, dan
    jarak yang sama.
-   **Sumber:** Tambahkan sitasi singkat pada poster yang memuat klaim
    dari paper. Cantumkan referensi lengkap pada Poster 12.
-   **Aksesibilitas:** Jangan mengandalkan warna saja untuk membedakan
    label atau kategori; gunakan teks/ikon yang jelas.
-   **Grafik data:** Gunakan hanya angka yang diverifikasi dari paper.
    Beri judul, label sumbu, dan konteks eksperimen.

## 8. Kebutuhan Konten dan Pemeriksaan Fakta

Sebelum poster dirender, lakukan pemeriksaan berikut:

-   [ ] Definisi SSL konsisten di semua poster.
-   [ ] Self-training, consistency regularization, dan graph-based
    learning dijelaskan sebagai pendekatan yang berbeda.
-   [ ] IHGCN disebut sebagai metode utama paper, bukan FixMatch atau
    self-training.
-   [ ] Enam kategori pekerjaan ditulis sesuai paper.
-   [ ] Kategori contoh buatan kelompok tidak diklaim sebagai kategori
    asli paper.
-   [ ] Angka eksperimen, metrik, baseline, dan detail dataset diperiksa
    ulang terhadap naskah.
-   [ ] Grafik membandingkan metrik yang sejenis.
-   [ ] Semua sitasi dan DOI benar.
-   [ ] Tidak ada klaim bahwa model menggantikan keputusan HR.
-   [ ] Flowchart membedakan alur SSL umum dari pipeline khusus IHGCN.

## 9. Kriteria Penerimaan

Materi dianggap selesai jika:

1.  Terdapat 12 poster dengan urutan yang logis.
2.  Setiap poster memiliki 4--5 panel dan satu tujuan pembelajaran
    utama.
3.  Isi dapat dipahami mahasiswa yang baru mengenal SSL.
4.  Poster teori membahas definisi, asumsi, pendekatan, dan flowchart.
5.  Studi kasus terhubung jelas dengan paper utama.
6.  Metode IHGCN dan hasil eksperimennya tidak salah atribusi.
7.  Desain konsisten dan teks dapat dibaca pada ukuran target.
8.  Seluruh klaim berbasis paper memiliki rujukan yang memadai.
9.  Tidak ada angka atau hasil yang diciptakan oleh AI.
10. File akhir diperiksa manusia sebelum dikumpulkan atau
    dipresentasikan.

## 10. Alur Produksi yang Disarankan

1.  Verifikasi isi dan angka dari paper.
2.  Finalisasi naskah 4 panel untuk setiap poster.
3.  Buat sketsa tata letak dan diagram.
4.  Gunakan AI untuk membantu ilustrasi atau layout, bukan untuk
    menentukan fakta akademik.
5.  Periksa ulang teks yang dirender, terutama istilah teknis, nama,
    angka, dan sitasi.
6.  Koreksi konsistensi visual seluruh seri.
7.  Ekspor ke format yang dibutuhkan dan lakukan pemeriksaan
    keterbacaan.

## 11. Referensi Utama

Wang, H., Yang, W., Li, J., Ou, J., Song, Y., & Chen, Y. (2023). *An
Improved Heterogeneous Graph Convolutional Network for Job
Recommendation*. **Engineering Applications of Artificial Intelligence,
126**, 107147. https://doi.org/10.1016/j.engappai.2023.107147

**Catatan:** Gunakan naskah paper sebagai sumber utama untuk seluruh
detail metode, dataset, dan hasil. Jika ada ketidaksesuaian antara
ringkasan PRD ini dan naskah asli, naskah asli yang menjadi acuan.
