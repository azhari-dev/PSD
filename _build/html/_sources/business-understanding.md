# Business Understanding

**Business Understanding** adalah fase awal dalam siklus hidup proyek sains data di mana fokus utamanya adalah memahami tujuan dan kebutuhan proyek dari perspektif bisnis. Tujuannya adalah untuk mengubah masalah bisnis yang seringkali abstrak ("Kita ingin meningkatkan penjualan") menjadi definisi masalah sains data yang jelas, terukur, dan dapat ditindaklanjuti ("Buat model untuk memprediksi produk mana yang kemungkinan besar akan dibeli oleh pelanggan X jika kita mengirimkan email promosi").

## Komponen Inti dan Pertanyaan Kunci dalam Business Understanding
Fase ini dapat dipecah menjadi beberapa langkah atau komponen utama. Untuk setiap komponen, ada serangkaian pertanyaan kunci yang harus dijawab.

Mari kita gunakan studi kasus agar lebih mudah dipahami: **Sebuah perusahaan telekomunikasi (Telco) mengalami tingkat perpindahan pelanggan (churn rate)** yang tinggi.

## 1. Menentukan Tujuan Bisnis (Determine Business Objectives)
Ini adalah gambaran besar. Apa yang ingin dicapai oleh perusahaan secara strategis?

*   **Apa masalah utama yang dihadapi bisnis?**
    *   Contoh Telco: "Kami kehilangan terlalu banyak pelanggan ke pesaing setiap bulannya, yang menggerus pendapatan dan pangsa pasar kami."

*   **Apa tujuan akhir dari proyek ini dari sudut pandang bisnis?**
    *   Contoh Telco: "Tujuan utamanya adalah **mengurangi tingkat churn pelanggan sebesar 20%** dalam enam bulan ke depan."

*   **Bagaimana solusi dari proyek ini akan membantu perusahaan?**
    *   Contoh Telco: "Dengan mempertahankan lebih banyak pelanggan, kita dapat meningkatkan Customer Lifetime Value (CLV), menstabilkan pendapatan, dan mengurangi biaya akuisisi pelanggan baru yang mahal."

## 2. Menilai Situasi Saat Ini (Assess Situation)
Ini adalah inventarisasi: apa yang kita miliki, apa yang kita ketahui, dan apa kendalanya?

*   **Sumber Daya:** Aset apa yang kita miliki? (manusia, data, infrastruktur)
    *   Contoh Telco: "Kita memiliki tim analis data, akses ke data warehouse yang berisi data demografi pelanggan, riwayat panggilan, penggunaan data internet, data tagihan, dan log keluhan pelanggan."

*   **Batasan (Constraints):** Apa saja batasan yang ada? (anggaran, waktu, regulasi)
    *   Contoh Telco: "Proyek ini harus memberikan hasil awal dalam 3 bulan. Kita juga harus mematuhi regulasi privasi data pelanggan (GDPR/UU PDP) dan tidak boleh menggunakan data pribadi yang sensitif."

*   **Asumsi:** Asumsi apa yang kita buat?
    *   Contoh Telco: "Kami berasumsi bahwa data yang ada cukup untuk mengidentifikasi pola perilaku pelanggan yang akan churn. Kami juga berasumsi bahwa tim marketing memiliki kapasitas untuk menindaklanjuti hasil dari model."

*   **Risiko:** Apa saja potensi masalah yang bisa menggagalkan proyek?
    *   Contoh Telco: "Risikonya adalah kualitas data yang buruk (banyak data hilang), atau model yang dihasilkan terlalu rumit untuk dijelaskan kepada tim marketing."

## 3. Menerjemahkan Tujuan Bisnis menjadi Tujuan Sains Data (Data Mining/Data Science Goals)
Ini adalah langkah penerjemahan krusial. Bagaimana kita menggunakan data untuk mencapai tujuan bisnis?
*   **Tujuan Bisnis:** Mengurangi churn pelanggan.
*   **Tujuan Sains Data:** Ini harus lebih spesifik dan teknis.
    *   Contoh Telco (Terjemahan):
    1.  **"Membangun sebuah model klasifikasi** yang dapat memprediksi probabilitas setiap pelanggan akan churn dalam 30 hari ke depan."
    2.  **"Mengidentifikasi faktor-faktor utama (key drivers)** yang paling berpengaruh terhadap keputusan pelanggan untuk churn (misalnya, jumlah keluhan, kenaikan tagihan, kualitas jaringan)."
    3.  **"Melakukan segmentasi pelanggan** berdasarkan risiko churn mereka (risiko tinggi, sedang, rendah) untuk tindakan marketing yang lebih tertarget."

## 4. Mendefinisikan Kriteria Kesuksesan (Define Success Criteria)
Bagaimana kita mengukur keberhasilan? Ini harus didefinisikan dari dua sisi: bisnis dan teknis.
*   **Kriteria Kesuksesan Bisnis:** Harus terukur dan terkait langsung dengan tujuan bisnis awal.
    *   Contoh Telco:
        *   "Tingkat churn bulanan berkurang setidaknya 15% pada kelompok pelanggan yang diberi perlakuan khusus berdasarkan hasil model."
        *   "Tingkat keberhasilan kampanye retensi (misalnya, pelanggan menerima tawaran diskon dan tetap bertahan) meningkat sebesar 25%."

*   **Kriteria Kesuksesan Teknis/Sains Data:** Metrik untuk mengevaluasi performa model.
    *   Contoh Telco:
        *   "Model prediksi harus mencapai akurasi lebih dari 85%."
        *   "Model harus memiliki **Recall (Sensitivity)** setidaknya 80% untuk kelas 'churn', yang berarti model harus mampu mengidentifikasi setidaknya 80 dari 100 pelanggan yang sebenarnya akan churn. Ini penting karena lebih merugikan jika kita gagal mengidentifikasi pelanggan yang akan pergi daripada salah mengira pelanggan setia akan pergi."
        *   "Model harus dapat memberikan skor risiko untuk seluruh basis pelanggan dalam waktu kurang dari 24 jam."

## Siapa Saja yang Terlibat?
Fase ini sangat kolaboratif dan melibatkan berbagai pihak:
*   **Pemangku Kepentingan Bisnis (Business Stakeholders):** Manajer produk, kepala departemen marketing, direktur, dll. Mereka adalah pemilik masalah.
*   **Pakar Domain (Subject Matter Experts - SMEs):** Orang yang sangat memahami seluk-beluk operasional bisnis, misalnya staf layanan pelanggan senior yang tahu persis keluhan apa yang sering memicu churn.
*   **Tim Sains Data (Data Scientists & Analysts):** Bertugas menerjemahkan masalah bisnis, memahami kelayakan teknis, dan merumuskan rencana proyek.
*   **Tim IT/Data Engineering:** Memberikan informasi mengenai ketersediaan, akses, dan kualitas data.

## Output/Deliverable dari Fase Business Understanding
Hasil akhir dari fase ini biasanya adalah sebuah dokumen formal yang disebut Project Charter atau **Dokumen Lingkup Proyek**. Dokumen ini merangkum semua poin di atas, termasuk:
1.  **Latar Belakang Masalah (Background)**
2.  **Tujuan Bisnis (Business Objectives)**
3.  **Tujuan & Ruang Lingkup Proyek Sains Data (Data Science Goals & Scope)**
4.  **Kriteria Kesuksesan (Business & Technical Success Criteria)**
5.  **Rencana Proyek Awal (Initial Project Plan):** Garis besar tahapan, estimasi waktu, dan sumber daya yang dibutuhkan.
6.  **Identifikasi Risiko dan Rencana Mitigasi (Risks & Mitigation Plan)**
7.  **Asumsi dan Batasan (Assumptions & Constraints)**

Dokumen ini menjadi "kontrak" dan panduan yang disetujui bersama oleh semua pihak sebelum proyek benar-benar melangkah ke fase pengumpulan data.

Secara ringkas, fase **Business Understanding** adalah tentang bertanya "mengapa", "apa", dan "bagaimana" dari perspektif bisnis sebelum terjun ke dalam lautan data. Ini adalah proses investigasi yang memastikan bahwa pada akhir proyek, solusi yang dihasilkan tidak hanya canggih secara teknis, tetapi juga memberikan dampak nyata bagi bisnis.