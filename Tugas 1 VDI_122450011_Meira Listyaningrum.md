| *Field*          | *Details*                                                                         |
|--------------------|-------------------------------------------------------------------------------------|
| **Article Title**  | Making data visualization more efficient and effective: a survey                    |
| **Writer**       | Xuedi Qin, Yuyu Luo, Nan Tang, Guoliang Li                                           |
| **Publisher**       | The VLDB Journal                                                                     |
| **Date of issue** | 19 November 2019                                                                     |
| **DOI**            | [https://doi.org/10.1007/s00778-019-00588-3](https://doi.org/10.1007/s00778-019-00588-3) |

**Meira Listyaningrum || 122450011 || RB**

---
## Latar Belakang
Artikel yang digunakan membahas mengenai teknik-teknik yang membuat visualisasi data lebih efisien dan efektif. Artikel tersebut juga memberikan ringkasan tentang berbagai teknik yang digunakan untuk meningkatkan proses visualisasi data. Visualisasi data ini sangat bermanfaat dalam era digital sekarang. Karena hal itu visualisasi data penting untuk membantu memberikan gambaran umum yang baik mengenai data yang besar, dan mempermudah interpretasi hasil analisis data. Selain itu visualisasi data jugaa telah digunakan dalam berbagai aplikasi yang berhubungan dengan database, seperti Excel, Google Spreadsheet, Dekstop Visualisasi Daya Oracle, IBM DB2 dan lainnya. 

---

## Meningkatkan Efisiensi dan Efektivitas Visualisasi Data
Dijelaskan pada artikel, terdapat tiga pendekatan umum yang dapat membantu meningkatkan efisiensi dan efektivitas visualisasi data, seperti yang disebutkan sebagai berikut:

1. Visualization Specification -> Spesifikasi visualisasi ini menjelaskan bagaimana pengguna dapat menentukan kebutuhan dalam membuat visualisasi.

2. Efficient Approaches for Data Visualization -> Pendekatan ini dapat menghasilkan visualisasi dengan tujuan utama untuk efisiensi dan kemampuan skala pada kecepatan yang interaktif. Proses pembuatan visualisasi data ini harus efisien dan terukur, terutama untuk dua komponen yaitu 'Manupulasi Data' dan 'Pemetaan'.

3. Data Visualization Recomendation -> Rekomendasi ini berfokus pada pengisian spesifikasi yang tidak lengkap atau menemukan serta memandu pengguna secara cerdas berdasarkan visualisasi referensi atau visualisasi yang direkomendasikan.

---

## The Pipeline of Data Visualization 
1. Data Import -> Mengambil data yang diperlukan dari suatu sumber data.

2. Data Preparation -> Mempersiapkan data yang diimpor untuk visualisasi (seperti normalisasi, interpolasi, atau memeriksa data yang hilang dll.)

3. Data Manipulation -> Memilih data yang akan divisualisasikan

4. Mapping -> Memetakan data yang diperoleh dari proses di atas ke primitif geometris (misal titik dan garis), beserta dengan atributnya (misal warna, posisi, ukuran dll.).

5. Rendering -> Mengubah data geometris menjadi representasi visual.

---


## Spesifikasi Visualisasi Data
Dijelaskan pada jurnal bahwa bahasa Viasualisasi data terdiri dari tiga buah bagian sebegai berikut:
1. Data
   - Records -> data yang perlu divisualisasikan
   - Transformasi -> Operasi, seperti grup, bin, filter, dan pengurutan untuk mengubah rekaman data tertentu.
  
2. Tanda/Isyarat Visual
    - Jenis -> Representasi visual untuk rekaman data (seperti batang, garis, atau titik)
    - Ukuran -> Lebar, tinggi visualisasi
    - Legenda -> Informasi dari legenda
    - Aneka ragam -> seperti 

3. Pemetaan -> Memetakan data ke dalam tanda yang sesuai

---

## Kategori Bahasa Visualisasi Data
Bahasa visualisasi data didasarkan pada ekspresifnya. Bahasa tingkat tinggi merangkum beberapa detail tingkat rendah dengan memberikan default yang masuk akal dan menambahkan lebih banyak batasan. Cara lain untuk memahami berbagai tingkat spesifikasi visualisasi bahasa adalah memalui aksebilitas, semakin tinggi tingkat bahasanya, maka akan semakin mudah digunakan.

  - Bahasa Tingkat Rendah -> Bahasa untuk menentukan semua elemen pemetaan
  - Bahasa tingkat tinggi -> Untuk merangkum detail konstruksi visualisasi, seperti fungsi dari pemetaan, serta beberapa properti untuk tanda seperti ukuran kanvas, legenda, dan lainnya.

---

## Spesifikasi yang Tidak Ditentukan
Visualisasi ini tidak ada artinya jika tidak dapat memberi gambaran mengenai data. Namun, terdapat banyak kasus di mana pengguna tidak benar-benar mengerti semua aspek data. Karena itu, hal ini menimbulkan persyaratan untuk mendukung spesifikasi yang tidak ditentukan. Secara umum, pengguna hanya memberikan beberapa petunjuk dan merupakan tugas sistem visualisasi untuk menafsir masukan yang tidak ditenntukan tersebut, dengan cara yang mungkin berbeda seperti berikut

  1. Berbasis Referensi -> Dimana penggunan memberi visualisasi referensi sebagai benih dan sistem akan menyarankan visualisasi berdasarkan referensi tersebut.
  2. Berbasis Kata Kunci -> Dimana APT akan menentukan kolom untuk divisualisasikan dan kemudian merekomendasikan visualisasi yang memenuhi tujuan berdasarkan kata kunci yang diberikan.
  3. Berbasis alam -> Dimana akan mempertimbangkan konteks masukan pengguna dan status sistem dalam siklus eksplorasi data.

---

## Pendekatan Efisien untuk Visualisasi Data
Ada beberapa pendekatan yang efisien untuk visualisasi data, sebagai berikut:
  1. Visualisasi data yang tepat
  2. Mengintegrasikan sistem visualisasi dengan DBMS
  3. Column Stores
  4. Indeks
  5. Perhitungan Pararel
  6. Prediksi dan Pengambilan Awal

---

## Perkiraan Visualisasi Data
Ada beberapa perkiraan visualisasi data yang dituliskan pada artikel, yaitu sebagai berikut:

1. Berbasis AQP
   
   Cara mundah untuk menghasilkan periraan visualisasi dalam waktu interaktif adalah dengan memanfaatkan teknik AQP. Dengan teknik AQP ini kita akan menggunakan sekumpulan data yang representatif dapat memberikan perkiraan visualisasi interaktif secara online kepada pengguna dengan mengorbankan kualitas.

2. Berbasis Pengambilan Sampel

    Sistem akan menghasilkan visualisasi perkiraan berdasarkan sampel kumpulan data yang representatif dengan cepat. Kemudia, sistem akan meningkatkan ukuran sampel dari waktu ke waktu untuk terus meningkatkan kualitas visualisasi. Penggu biasanya akan memperoleh beberapa wawasan untuk terus meningkatkan kualitas visualisasi dan memutuskan menghentikannya jika kualitas visualisasi cukup untuk memverifikasi wawasan ini.

3. Berbasis Persepsi Manusia

    Memperkirakan sistem visualisasi untuk menghasilkan hasil perkiraan berdasarkan sampel yang representatif tetapi dengan dampak minimal terhadap kualitas visualisasi. Pendekatan berbasis persepsi manusia menghentikan pengambilan sampel ketika tidak ada perbedaan nyata pada persepsi manusia antara perkiraan visualisasi saat ini dan visualisasi yang diperbolehkan dengan pengambilan sampel lebih lanjut.

---
## Rekomendasi Berdasarkan Spesifikasi
Terdapat beberapa rekomendasi visualisasi, diantaranya adalah sebagai berikut:

  1. Rekomendasi berbasis spesifikasi -> Rekomendasi ini terbagi menjadi dua, yaitu spesifikasi tidak lengkap di mana spesifikasi elemen visualisasi kosong atau kosong sebagian. Spesifikasi kedua yaitu spesifikasi berbasis referensi di mana sistem ini akan merekomendasikan visualisasi yang mirip atau berbeda dari referensi yang diberikan. 

  2. Rekomendasi berbasis perilaku -> Sistem ini menangkap perilaku pengguna sebagai input. 

  3. Rekomendasi yang dipersonalisasi -> Sistem rekomendasi ini menangkap perilaku historis pengguna sebagai input. 

  4. Ringkasan -> Sistem rekomendasi dengan spesifikasi kosong digunakan pengguna untuk menjelajahi data dengan cepat ketika pengguna tidak begitu mengenal data dan visualisasi yang diinginkan. 

---
## Kesimpulan

Isi artikel secara keseluruhan adalah untuk memberitahu pentingnya visualisasi data terutama dalam membantu pengambilan keputusan dan mempermudah interpretasi dalam analisis data. Tiga bahasan utama yang menjadi pembahasan utama disini adalah bagaimana membuat visualisasi data menjadi efisien dan efektif, spesifikasi visualisasi, pendekatan efisien, serta rekomendasi visualisasi.


