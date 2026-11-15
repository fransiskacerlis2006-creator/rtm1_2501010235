# AKUISISI DATA DESTINASI WISATA BALI MENGGUNAKAN OPENSTREETMAP API

## A. Identitas Mahasiswa

| Keterangan | Identitas |
|---|---|
| Nama | Fransiska Cerlis Oda |
| Program Studi | Informatika |
| Angkatan | 2025 |
| Mata Kuliah | Akuisisi dan Manajemen Data |
| NIM | Tercantum dalam `docs/provenance.json` |

## B. Deskripsi Proyek

Proyek ini merupakan kegiatan akuisisi data destinasi wisata di Bali dengan memanfaatkan OpenStreetMap melalui Overpass API.

Tujuan proyek ini adalah mengumpulkan data tempat wisata di wilayah Bali, kemudian mengolahnya menjadi dataset berbentuk CSV menggunakan Python di Google Colab.

## C. Sumber Data

- Nama sumber: OpenStreetMap
- API: Overpass API
- Website: https://www.openstreetmap.org/
- Endpoint API: https://overpass-api.de/api/interpreter
- Lisensi: Open Database License (ODbL)
- Atribusi: © OpenStreetMap contributors

## D. Metode Akuisisi Data

Pengambilan data dilakukan menggunakan metode API dengan bahasa pemrograman Python melalui Google Colab.

Data diperoleh menggunakan HTTP POST request ke Overpass API dengan wilayah pencarian Bali.

Kategori objek wisata yang diambil:
1. Attraction
2. Viewpoint
3. Museum
4. Gallery
5. Zoo
6. Theme Park

## E. Hasil Akuisisi Data

Hasil pengambilan dan pengolahan data:

- Jumlah objek mentah dari API: 756 objek.
- Jumlah record setelah pengolahan: 553 record.
- Jumlah kolom dataset: 6 kolom.
- Format data mentah: JSON.
- Format dataset: CSV.

## F. Penjelasan Kolom Dataset

| No. | Nama Kolom | Keterangan |
|---|---|---|
| 1 | nama_destinasi | Nama tempat wisata |
| 2 | jenis_wisata | Kategori wisata |
| 3 | jenis_objek | Jenis objek OpenStreetMap |
| 4 | latitude | Koordinat garis lintang |
| 5 | longitude | Koordinat garis bujur |
| 6 | sumber_data | Sumber data destinasi |

## G. Pemeriksaan Kualitas Data

Pemeriksaan dilakukan untuk mengetahui:
- Data kosong (missing values).
- Data duplikat berdasarkan seluruh kolom.
- Jumlah baris dan kolom.
- Distribusi kategori wisata.

Hasil pemeriksaan menunjukkan:
- Jumlah record: 553.
- Jumlah kolom: 6.
- Tidak terdapat nilai kosong.
- Tidak ditemukan baris duplikat secara keseluruhan.

## H. Etika dan Lisensi Data

Pengambilan data memperhatikan penggunaan sumber data publik, lisensi, dan atribusi OpenStreetMap.

Hal-hal yang diperhatikan:
- Menggunakan sumber data publik.
- Mencantumkan lisensi ODbL dan atribusi OpenStreetMap.
- Menggunakan User-Agent yang mencantumkan identitas tugas dan email kampus.
- Pengambilan data dilakukan dengan satu request.
- Tidak menggunakan API key atau kata sandi.

## I. Struktur Folder

```text
rtm1_<NIM>/
│
├── notebooks/
│   └── akuisisi_openstreetmap_bali.ipynb
│
├── data/
│   └── raw/
│       ├── openstreetmap_bali_20261114.json
│       └── openstreetmap_bali_20261114.csv
│
├── docs/
│   ├── provenance.json
│   └── data_ethics_checklist.csv
│
└── README.md
```

## J. Perangkat yang Digunakan

- Python
- Google Colab
- Requests
- Pandas
- JSON
- OpenStreetMap Overpass API
- GitHub

## K. Cara Menjalankan

1. Buka file notebook menggunakan Google Colab.
2. Pastikan koneksi internet tersedia.
3. Periksa dan sesuaikan email kampus pada bagian User-Agent.
4. Jalankan setiap sel kode secara berurutan.
5. Data hasil akuisisi akan disimpan dalam folder `data/raw`.

## L. Kesimpulan

Melalui proyek ini, berhasil diperoleh dataset destinasi wisata Bali sebanyak 553 record dengan 6 kolom. Data diperoleh dari OpenStreetMap melalui Overpass API dan diolah menggunakan Python di Google Colab.

Proyek ini memberikan pengalaman dalam proses pengambilan, pengolahan, pemeriksaan, dan penyimpanan data untuk keperluan pembelajaran.
