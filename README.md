# 📊 Financial Statements of Major Companies (2009–2023) Executive Dashboard

## 📌 Project Overview
Proyek ini menganalisis data historis Laporan Keuangan (*Financial Statements*) dari 12 perusahaan multinasional raksasa periode **2009–2023** (161 baris data transaksi) serta membangun **Executive Financial Performance Dashboard** yang terstruktur, otomatis, dan interaktif menggunakan Microsoft Excel.

Analisis ini melacak indikator keuangan utama (*Revenue*, *Gross Profit*, *Net Income*, dan *Net Profit Margin*) pada Kartu KPI, membedah alur pembentukan laba bersih melalui *Profit Bridge Waterfall Chart*, memetakan tren pertumbuhan keuangan 15 tahun (2009–2023), memetakan kontribusi kinerja per sektor industri, serta menyajikan perbandingan performa antar-perusahaan secara presisi

---

## 🗂️ Data Source & Attribution
* **Dataset:** Financial Statements of Major Companies (2009–2023)
* **Publisher:** Kaggle (Rishabh Patil)
* **Link Source:** [Kaggle - Financial Statements of Major Companies (2009-2023)](https://www.kaggle.com/datasets/rish59/financial-statements-of-major-companies2009-2023/data)

---

## 🛠️ Excel Features & Techniques Used

* **Data Cleaning & Standardisation:**
  * **Text to Columns Parsing:** Mengubah dan memisahkan struktur data mentah format CSV menjadi kolom-kolom terpisah yang terstruktur sesuai variabel laporan keuangan.
  * **Missing Value Handling & Median Imputation:** Melakukan inspeksi keberadaan sel kosong (*blank cells*) pada data keuangan dan menerapkan penanganan nilai hilang dengan mengisikan nilai median berdasarkan kelompoknya (*group median imputation*) untuk menjaga integritas dan distribusi data.
  * **Data Transformation & Unit Scale Verification:** Memastikan tipe data tiap kolom valid serta memverifikasi bahwa header `Market Cap(in B USD)` tertulis dalam skala *Billion USD ($B)*, sementara indikator `Revenue`, `Gross Profit`, dan `Net Income` merupakan nilai nominal murni.
  * **Custom Number Formatting:** Menerapkan pemformatan kustom presisi (`$#,##0;-$#,##0;"-"`) pada Pivot Table dan (`$#,##0,"K"`) pada sumbu chart agar pembagian angka ribuan/jutaan tidak mengerosi kerugian nyata perusahaan (seperti PCG Net Income `-$3,985`) menjadi `$0`.
* **Data Staging Architecture & Dynamic Slicers:**
  * **Dedicated Staging Sheet (`Staging KPI`):** Memisahkan area logika *backend* dan 5 Pivot Tables dari lembar kerja tampilan utama untuk menjaga kestabilan *file* dan struktur pengolahan data.
  * **Single-Click Dynamic Slicers (`Report Connections`):** Menghubungkan **Slicer Year**, **Slicer Company**, dan **Slicer Category** secara eksplisit ke seluruh Pivot Table. Mematikan fitur *Multi-Select* (`Alt + S`) serta mengaktifkan *Slicer Settings* `Hide items with no data` untuk pengalaman navigasi yang intuitif dan responsif.
* **Advanced Visualizations & UI/UX Design:**
  * **Profit Bridge Waterfall Chart:** Merancang grafik *Waterfall* dari tabel perantara (*Staging Link*) dengan memberikan nilai negatif pada pengurang biaya (*COGS* & *OPEX*) serta mengkonfigurasi properti *Set as Total* pada pilar `Revenue`, `Gross Profit`, dan `Net Income`.
  * **Company Performance Bar Chart:** Memetakan 12 perusahaan secara hierarkis dari kontributor pendapatan terbesar hingga terkecil dengan label nilai yang disesuaikan.
  * **Multi-Year Trend Combo Chart:** Mengintegrasikan grafik batang vertikal (*Revenue*) dengan grafik garis (*Net Income*) untuk melacak tren pertumbuhan keuangan 15 tahun.
  * **Clean Executive Dark Layout:** Menyusun tata letak *Clean Dark Dashboard* (`#1E293B`) yang simetris dan pas dalam 1 layar *view* tanpa mengorbankan keterbacaan data.

---

## 📈 Interactive Dashboard Showcase

### 1. Executive Profit Bridge Waterfall (USD)
*Waterfall Chart* yang membedah alur pembentukan laba bersih dari total pendapatan (*Revenue*) dikurangi Harga Pokok Penjualan (*COGS*) menghasilkan *Gross Profit*, kemudian dikurangi Beban Operasional & Pajak (*OPEX_Other*) hingga menyisakan *Net Income*.
* **Key Insight:** Dari akumulasi *Total Revenue* sebesar **$12,213,879**, perusahaan menghabiskan **$6,195,141** untuk *COGS* (50.7%) dan **$4,042,204** untuk *OPEX_Other* (33.1%), sehingga menyisakan akumulasi *Net Income* bersih sebesar **$1,976,534** dengan *Net Profit Margin* rata-rata sebesar **13.7%**.

---

### 2. Company Performance & Industry Category Breakdown
*Horizontal Bar Charts* yang memetakan perbandingan *Revenue* vs *Net Income* antar-perusahaan serta kontribusi performa berdasarkan 8 sektor industri.
* **Key Insight:** Sektor **IT** memimpin kontribusi pendapatan secara mutlak sebesar **$6,189,902** dengan *Net Income* **$1,514,327**, disusul oleh **LOGI** ($2,635,460) dan **Bank** ($1,342,743). **Apple (AAPL)** memimpin sebagai perusahaan paling menguntungkan dengan *Revenue* **$2,965,609** dan *Net Income* **$680,563**. Sebaliknya, sektor **Manufacturing / PCG** (-$3,985) dan sektor **Finance / SHLDQ** (-$10,429) mencatatkan akumulasi *Net Income* negatif.

---

### 3. Multi-Year Financial Growth Trend (2009–2023)
*Combo Line & Column Chart* deret waktu yang melacak laju pertumbuhan pendapatan dan laba bersih selama periode 15 tahun.
* **Key Insight:** Terjadi akselerasi pertumbuhan yang sangat signifikan menuju masa puncak pandemi, di mana **Net Income tertinggi dicapai pada tahun 2021 ($319,285)** dan **Revenue tertinggi dicapai pada tahun 2022 ($1,639,071)**, sebelum mengalami koreksi penyesuaian pasar pada tahun 2023 ($238,889 Revenue / $76,729 Net Income).

---

![Financial Statements Analysis Dashboard Preview](Financial%20Dashboard%20Image.jpeg)

📄 **[Download / Lihat Dashboard versi PDF Beresolusi Tinggi](./Financial%20Dashboard%20PDF.pdf)**

---

## 📁 Repository Structure

* `Financial_Statements_Analysis_Dashboard.xlsx` : File kerja utama Excel.
* **`Financial Data`** : Sheet data mentah (*raw data*) laporan keuangan 12 perusahaan dari Kaggle.
* **`Data Cleaning`** : Sheet tempat pengolahan data awal, verifikasi tipe data sel, dan penyesuaian format angka.
* **`Staging KPI`** : Sheet *backend logic* yang memuat 5 Pivot Tables interaktif dan kalkulasi *Waterfall Chart Link*.
* **`Dashboard`** : Sheet tampilan utama (*User Interface*) berisi KPI Scorecards, Slicers interaktif, Profit Bridge Waterfall Chart, Combo Trend Chart, dan Bar Charts.
* 📝 **Medium Article:** [Link Medium Kamu Akan Ditaruh Di Sini]

---

## 👤 Author
- **Name:** Alena Mansika
- **GitHub:** [@alenamansika](https://github.com/alenamansika)
- **LinkedIn:** [LinkedIn Alena Mansika](https://www.linkedin.com/in/alenamansika)
