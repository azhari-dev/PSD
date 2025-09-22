# Data Understanding

## Deskripsi Dataset

Data Understanding adalah fase dalam siklus hidup proyek sains data yang berfokus pada pengumpulan data awal, familiarisasi melalui analisis eksplorasi, identifikasi masalah kualitas data, dan penemuan wawasan pertama yang mungkin menarik. Tujuannya adalah untuk mendapatkan pemahaman yang mendalam tentang kekuatan dan kelemahan data sebelum melangkah ke fase persiapan data yang lebih intensif.

Mengapa Fase Ini Sangat Penting?
Menghindari Asumsi yang Salah: Tanpa memahami data, kita mungkin membuat asumsi yang keliru tentang isinya, yang akan mengarahkan pemodelan ke arah yang salah.

Deteksi Dini Masalah: Menemukan masalah seperti data yang hilang (missing values) atau outlier di awal akan menghemat banyak waktu dan tenaga di kemudian hari.

Memberi Inspirasi untuk Feature Engineering: Eksplorasi data seringkali memunculkan ide-ide tentang bagaimana menggabungkan atau mengubah variabel yang ada untuk membuat fitur prediktif yang lebih kuat.

Mengelola Ekspektasi: Pemahaman data membantu kita menilai apakah tujuan bisnis yang telah ditetapkan realistis untuk dicapai dengan data yang tersedia.

Aktivitas Kunci dalam Fase Data Understanding
Fase ini melibatkan empat aktivitas utama:

Pengumpulan Data Awal (Collect Initial Data)

Tujuan: Mengumpulkan data dari berbagai sumber yang diidentifikasi pada fase sebelumnya.

Proses: Ini bisa melibatkan penarikan data dari database, mengakses API, atau membaca file seperti CSV, JSON, dll. Hasilnya adalah kumpulan data "mentah" pertama.

Deskripsi Data (Describe Data)

Tujuan: Memeriksa "fakta-fakta" dasar tentang data.

Proses: Ini adalah pemeriksaan permukaan untuk menjawab pertanyaan seperti:

Berapa volume data? (Jumlah baris dan kolom)

Apa saja nama kolomnya?

Apa format dan tipe data setiap kolom? (misalnya, integer, float, string, datetime)

Apakah ada data yang tampak salah format secara kasat mata?

Eksplorasi Data (Explore Data / EDA - Exploratory Data Analysis)

Tujuan: Menyelam lebih dalam untuk menemukan pola, hubungan, dan anomali.

Proses: Ini adalah inti dari data understanding. Kita menggunakan statistik dan visualisasi untuk bertanya pada data:

Analisis Univariat: Menganalisis setiap variabel secara individual. (Bagaimana distribusi harga? Apa saja kategori produk yang ada?)

Analisis Bivariat/Multivariat: Menganalisis hubungan antara dua atau lebih variabel. (Apakah ada korelasi antara suhu dan penjualan es krim? Bagaimana harga rumah bervariasi berdasarkan lokasi dan jumlah kamar?)

Visualisasi: Membuat plot seperti histogram, box plot, scatter plot, dan bar chart untuk mempermudah pemahaman pola.

Verifikasi Kualitas Data (Verify Data Quality)

Tujuan: Mengidentifikasi secara sistematis masalah-masalah dalam data.

Proses: Memeriksa dan mendokumentasikan isu-isu seperti:

Nilai yang Hilang (Missing Values): Apakah ada sel yang kosong? Seberapa banyak?

Data Duplikat: Apakah ada baris data yang identik?

Inkonsistensi: Apakah data dimasukkan dengan format yang berbeda (misalnya, "Jakarta", "JKT", "Dki Jakarta")?

Outliers (Pencilan): Apakah ada nilai yang sangat ekstrem dan tidak masuk akal?

Output Fase Ini: Sebuah laporan atau ringkasan yang mendokumentasikan semua temuan di atas. Laporan ini akan menjadi panduan utama untuk fase berikutnya, yaitu Data Preparation.

Bagian 2: Analisis Dataset btc.csv
Berikut adalah hasil dari fase Data Understanding yang saya terapkan pada file btc.csv yang Anda berikan.

1. Deskripsi Umum Dataset
   Dataset ini berisi data deret waktu (time-series) historis yang tampaknya merupakan data harga dan volume perdagangan Bitcoin (BTC). Setiap baris data merepresentasikan informasi perdagangan dalam interval waktu tertentu (kemungkinan per menit atau jam, dilihat dari pola timestamp). Ini adalah format data OHLCV (Open, High, Low, Close, Volume) yang sangat umum digunakan dalam analisis pasar finansial.

2. Struktur Dataset
   Berdasarkan analisis file, berikut adalah struktur dari dataset Anda:

Jumlah Baris: 4,857,377 baris

Jumlah Kolom: 7 kolom

Nama Kolom: id, timestamp, open, high, low, close, volume

3. Tipe Data dan Contoh Nilai
   Berikut adalah rincian setiap kolom, tipe datanya, contoh nilainya, dan deskripsi singkatnya.

(tabel)

4. Kualitas Data
   Setelah melakukan pemeriksaan awal terhadap kualitas data, berikut temuannya:

Nilai yang Hilang (Missing Values): Tidak ada nilai yang hilang di seluruh kolom dalam dataset ini. Setiap sel memiliki nilainya masing-masing. Ini menunjukkan kualitas data yang sangat baik dari segi kelengkapan.

Duplikasi: Tidak ditemukan adanya baris data yang terduplikasi secara penuh. Setiap baris adalah unik.

Konsistensi:

Nama kolom sudah konsisten (menggunakan huruf kecil).

Tipe data di setiap kolom tampak konsisten (semua numerik).

Secara keseluruhan, kualitas data awal terlihat sangat baik dan bersih, siap untuk analisis lebih lanjut.

5. Statistik Univariat
   Analisis univariat melihat setiap variabel secara individual.

a. Variabel Kategorikal

Dalam dataset ini, tidak ada variabel yang murni kategorikal. Kolom id dan timestamp meskipun numerik, berfungsi sebagai pengidentifikasi dan tidak dianalisis distribusinya seperti variabel harga.

b. Variabel Numerik

Berikut adalah ringkasan statistik deskriptif untuk kolom-kolom numerik utama:

(tabel)

Interpretasi dari Statistik:

Rentang Harga yang Ekstrem: Harga Bitcoin (open, high, low, close) memiliki rentang yang sangat besar, dari $3.80 hingga $69,000. Ini menunjukkan volatilitas yang sangat tinggi selama periode waktu yang dicakup oleh dataset.

Standar Deviasi Tinggi: Nilai standar deviasi yang lebih besar dari nilai rata-rata pada semua kolom harga mengkonfirmasi adanya fluktuasi harga yang sangat ekstrem.

Volume Perdagangan: Volume perdagangan memiliki rata-rata sekitar 9.21 BTC per interval waktu, namun nilai mediannya hanya 2.1 volume. Ini menunjukkan bahwa sebagian besar waktu, volume perdagangannya rendah, tetapi sesekali terjadi lonjakan volume yang sangat tinggi (terlihat dari nilai maksimum 5,853).

Distribusi Miring (Skewed): Perbedaan besar antara nilai rata-rata (mean) dan median (50%) pada semua variabel menunjukkan bahwa distribusinya tidak simetris (kemungkinan miring ke kanan atau right-skewed). Ini umum terjadi pada data finansial.
