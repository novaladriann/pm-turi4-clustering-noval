# TuRi 4 — Clustering dengan K-Means

Repositori ini berisi hasil praktikum **Pertemuan 9: Clustering dengan K-Means** pada mata kuliah Pembelajaran Mesin.

## Identitas

| | |
|---|---|
| **Nama** | Noval Adrian |
| **NIM** | 2488010018 |
| **Kelas** | 5B |
| **Program Studi** | S1 Informatika |
| **Universitas** | UIN Siber Syekh Nurjati Cirebon |
| **Mata Kuliah** | Pembelajaran Mesin (INF62325, 3 SKS) |
| **Pertemuan / Praktikum** | 9 / TuRi 4 |
| **Sub-CPMK** | SCPMK0401-003 |
| **Dosen Penyusun Modul** | Ardi Susanto, S.Kom., M.Cs. |

## Ringkasan Temuan

### 1. Scaling
Rentang fitur sangat berbeda: `pendapatan` sekitar 3 juta sampai 21 juta, sedangkan `usia` 18–65 dan `skor_belanja` 15–95. Setelah `StandardScaler`, setiap fitur memiliki rata-rata 0 dan standar deviasi 1 sehingga semua fitur berkontribusi setara pada perhitungan jarak.

### 2. Metode Elbow
Inertia turun tajam dari K=1 (±450) ke K=2 (±167) dan K=3 (±71), lalu melandai (K=4 ±56, K=5 ±49). Siku berada di **K = 3**.

### 3. Hasil K-Means (K=3)
Terbentuk tiga cluster dengan jumlah anggota hampir seimbang: 51, 50, dan 49 pelanggan.

### 4. Silhouette Score
Silhouette score K=3 sebesar **0,600**, artinya cluster terpisah dengan baik.

### 5. Profil dan Penamaan Cluster

| Cluster | Nama | Rata-rata usia | Rata-rata pendapatan | Rata-rata skor belanja |
|---|---|---|---|---|
| 0 | **Muda & Boros** | 24,5 tahun | Rp5.053.000 | 79,7 |
| 1 | **Mapan & Hemat** | 42,3 tahun | Rp13.642.157 | 29,9 |
| 2 | **Senior & Moderat** | 57,2 tahun | Rp8.318.163 | 51,5 |
