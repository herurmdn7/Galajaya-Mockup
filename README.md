# Galajaya Mockup Dashboard Guideline

> **Disclaimer & Data Privacy Notice:**  
> Berikut hasil analisa gembel cepat yang menjadi Dashboard dan dokumentasi. File ini dibuat *not fully AI* karena token saya ga sebanyak enterprise. si AI di sini hanya membantu *filling the missing pieces* dalam penyusunan struktur kode frontend, visualisasi grafik,*Phrasing readme ini*, dan logika kalkulasi backend. **Data asli perusahaan di dalam Google Spreadsheet tidak pernah dibaca atau disimpan oleh AI.** AI hanya membaca struktur kolom dan contoh format *prompt* dari saya sehingga kerahasiaan data operasional maupun komersial tetap aman. Saya Jamin wok sebagai creator 

---

## 1. Master Summary (Top KPI Cards)

Bagian paling atas dari *Executive Command Center* yang merangkum kesehatan bisnis secara keseluruhan dalam empat metrik utama. Seluruh kartu bersifat interaktif dan dapat diklik untuk langsung masuk ke bagian analitik terkait.

### A. Pipeline Forecast

![Insert Screenshot Pipeline Forecast Card](Images/Pipeline%20Forecast.png)

* **Fungsi:** Menampilkan total potensi kas masuk (*unbilled / ongoing pipeline*) dari penawaran yang statusnya masih **Belum**, **Berlangsung**, atau **6 bulan lagi**.
* **Cara Membaca:** Memberikan gambaran langsung mengenai estimasi dana yang akan masuk ke perusahaan dalam waktu dekat hingga menengah.

### B. Realized Revenue

![Insert Screenshot Realized Revenue Card](Images/Realized%20Revenue.png)

* **Fungsi:** Menampilkan total nilai transaksi yang statusnya sudah **Selesai** (*realized cash-in*).
* **Cara Membaca:** Menggunakan warna hijau solid (*Emerald*) sebagai indikator pendapatan bersih yang sudah aman tercatat.

### C. Service Action (< 100 Hours)

![Insert Screenshot Service Action Card](Images/Service%20Action.png)

* **Fungsi:** Menghitung jumlah unit genset yang sisa jam operasionalnya menuju jadwal *Plan Service* berada di bawah batas toleransi **100 jam**.
* **Cara Membaca:** Jika angka ini tinggi, tim teknis harus segera menyiapkan jadwal *maintenance* dan stok *sparepart* sebelum mesin melewati batas servis.

### D. Fleet Utilization Rate

![Insert Screenshot Fleet Utilization Rate Card](Images/Fleet%20Utilization.png)

* **Fungsi:** Mengukur persentase keaktifan seluruh armada genset di lapangan dalam satu bulan (total hari beroperasi aktif dibagi total hari tersedia).
* **Cara Membaca:** Indikator efisiensi aset. Semakin tinggi persentasenya, semakin produktif armada yang disewakan.

---

## 2. Commercial & Yield Analytics

Bagian ini membedah performa penjualan, margin layanan, profil klien, dan potensi perpanjangan kontrak dari sheet **Penawaran Deal**.

### A. Gross Volume (Service vs Parts Breakdown)

![Insert Screenshot Gross Volume Card](Images/Gross%20Volume.png)

* **Fungsi:** Menunjukkan total nilai transaksi pada periode terpilih sekaligus membandingkan proporsi pendapatan dari **Jasa** melawan penjualan **Sparepart**.
* **Cara Membaca:** Membantu manajemen melihat apakah pendapatan bulan tersebut lebih banyak ditopang oleh ongkos kerja teknisi atau margin penjualan komponen.

### B. Revenue Growth & Peak Detection

![Insert Screenshot Revenue Growth Chart](Images/Revenue%20Growth.png)

* **Fungsi:** Grafik area yang melacak pergerakan total nilai deal dari bulan ke bulan, dilengkapi penanda otomatis (**Peak Revenue**) pada bulan dengan pencapaian tertinggi.
* **Cara Membaca:** Memudahkan identifikasi tren kenaikan atau penurunan omzet secara historis tanpa harus mengecek tabel satu per satu.

### C. Asset Yield (Revenue per kVA) <kbd>🟢 Planned</kbd>

![Insert Screenshot Asset Yield Chart](Images/Asset%20Yield.png)

* **Fungsi:** Menggabungkan data nilai deal dengan kapasitas mesin di sheet **Daftar Genset** untuk menghitung rata-rata pendapatan yang dihasilkan per 1 kVA.
* **Cara Membaca:** Menjawab pertanyaan unit mana yang paling menguntungkan secara rasio kapasitas, sehingga membantu keputusan investasi pembelian unit baru.

### D. Top Channel Performance (Via)

![Insert Screenshot Top Channel Chart](Images/Top%20Channel%20Performances.png)

* **Fungsi:** Mengurutkan kontribusi nilai transaksi berdasarkan nama sales atau kanal masuknya penawaran (*Via*).
* **Cara Membaca:** Evaluasi performa tim komersial dalam menutup nilai kontrak terbesar.

### E. Deal Breakdown (Jenis Pekerjaan)

![Insert Screenshot Deal Breakdown Chart](Images/Deal%20Breakdown.png)

* **Fungsi:** Memecah nilai transaksi berdasarkan kategori pekerjaan seperti *Service Rutin*, *Overhoul*, *Rental*, *Psg Panel*, hingga *Maintenance Check Genset*.
* **Cara Membaca:** Menunjukkan lini layanan apa yang paling mendominasi pemasukan perusahaan pada periode berjalan.

### F. Contract Expiry Radar

![Insert Screenshot Contract Expiry Radar](Images/Contract%20Status.png)

* **Fungsi:** Grafik donat yang mengelompokkan status penyelesaian proyek (*Selesai*, *Berlangsung*, *Belum*, dan *6 bulan lagi*).
* **Cara Membaca:** Berfungsi sebagai radar pengingat bagi tim sales untuk melakukan *follow-up* proyek yang akan habis masa berlakunya dalam 6 bulan ke depan.

### G. Client Concentration (VIP Risk)

![Insert Screenshot Client Concentration Chart](Images/Client%20Concentration.png)

* **Fungsi:** Membandingkan porsi pendapatan dari **Top 3 Customer Terbesar** melawan gabungan seluruh customer lainnya (*Others*).
* **Cara Membaca:** Mitigasi risiko bisnis. Jika porsi 1 atau 3 klien terlalu mendominasi di atas 60-70%, perusahaan perlu memperluas basis klien baru agar tidak bergantung pada satu pihak.

---

## 3. Predictive Maintenance & Hour Meter Analytics <kbd>🟢 Planned</kbd>

Bagian ini menarik log harian dari sheet **Hour Meter** untuk mendeteksi beban kerja mesin dan mencegah keterlambatan servis.

### A. Full Standby Month (Interactive Card) 

![Insert Screenshot Full Standby Card](Images/Full%20Standby%20Months.png)

* **Fungsi:** Menghitung jumlah unit genset yang statusnya tercatat `STBY` penuh sepanjang bulan tanpa satu hari pun beroperasi.
* **Cara Membaca:** Kartu ini dapat diklik untuk membuka daftar detail unit beserta lokasinya. Unit yang terlalu lama *standby* di lokasi proyek perlu dievaluasi apakah kontraknya masih berjalan atau unit perlu ditarik kembali ke gudang.

### B. Overall Fleet Health Gauge <kbd>🟢 Planned</kbd>

![Insert Screenshot Fleet Health Gauge](Images/OVeral%20Fleet%20Operational%20Health.png)

* **Fungsi:** Visualisasi *speedometer* yang merangkum tingkat utilitas operasional seluruh genset yang tercatat di log Hour Meter.
* **Cara Membaca:** Warna biru menandakan utilitas di bawah 50% (banyak unit menganggur), sedangkan hijau menandakan armada bekerja optimal di atas 50%.

### C. Average Usage / Day (Top 5 & Least 5 Toggle)

![Insert Screenshot Average Usage Per Day Chart](Images/Average%20usage%20per%20Day%20Top.png)

* **Fungsi:** Menampilkan rata-rata jam nyala mesin per hari aktif (di luar hari `STBY`). Dilengkapi tombol *toggle* untuk beralih antara **Top 5** (paling berat) dan **Least 5** (paling ringan).
* **Cara Membaca:** Mesin di daftar *Top 5* memiliki tingkat keausan paling cepat dan wajib diprioritaskan untuk inspeksi rutin.

### D. Total HM Usage (Top 5 & Least 5 Toggle)

![Insert Screenshot Total HM Usage Chart](Images/Total%20Monthly%20HM%20Usage%20Top.png)

* **Fungsi:** Menampilkan akumulasi total jam operasional mesin dalam satu periode penuh, lengkap dengan *toggle* **Top 5** dan **Least 5**.
* **Cara Membaca:** Mengidentifikasi mesin mana yang paling produktif dan mesin mana yang kapasitasnya terlalu besar untuk kebutuhan lokasi (*underutilized*).

### E. Predictive Burn-Down & Estimated Service Date Table

![Insert Screenshot Predictive Burn-Down Table](Images/Predictive%20Service.png)

* **Fungsi:** Tabel pemantauan jadwal servis yang dilengkapi batang progres visual (*Burn-Down Progress*) dan kalkulasi otomatis **Estimasi Tanggal Servis** berdasarkan rata-rata pemakaian harian.
* **Cara Membaca:** Bar yang semakin penuh dan berwarna merah menandakan sisa jam semakin tipis. Jika estimasi tanggal servis jatuh dalam 7 hari ke depan, sistem otomatis memberi label **Urgent**, serta menandai unit yang data *Terakhir Service*-nya masih kosong.

---

## 4. Fleet Composition & Geospatial Mapping

Bagian ini memetakan master aset dari sheet **Daftar Genset** berdasarkan kepemilikan, tipe unit, dan sebaran wilayahnya.

### A. Total Registered Fleet (Galajaya vs Customer)

![Insert Screenshot Total Registered Fleet Card](Images/Total%20Registered%20Fleet.png)

* **Fungsi:** Menampilkan total keseluruhan unit genset yang terdaftar di sistem, dibagi menjadi unit milik internal (**GALAJAYA**) dan unit milik klien (**CUSTOMER**).
* **Cara Membaca:** Memudahkan pemisahan antara aset investasi perusahaan sendiri dengan unit milik luar yang hanya menggunakan jasa perawatan.

### B. Type Distribution (Open vs Silent Type)

![Insert Screenshot Type Distribution Chart](Images/Enclosire%20Distrib.png)

* **Fungsi:** Grafik donat yang membandingkan jumlah genset bertipe *Silent Type* dengan *Open Type*.
* **Cara Membaca:** Memberikan gambaran kesiapan spesifikasi armada untuk kebutuhan proyek perkotaan/perkantoran (yang mewajibkan *Silent Type*) dibandingkan area terbuka/perkebunan.

### C. Top Locations (Unit Count)

![Insert Screenshot Top Locations Chart](Images/Top%20Site%20Loc.png)

* **Fungsi:** Menampilkan 5 lokasi atau *site* dengan konsentrasi penempatan genset terbanyak.
* **Cara Membaca:** Membantu tim logistik memetakan area kerja terpadat dan memantau berapa banyak unit yang sedang menumpuk di *Gudang Platinum* maupun *Kantor*.

### D. Indonesia Archipelago Choropleth Map <kbd>🟢 Planned</kbd>

![Insert Screenshot Indonesia Archipelago Map](Images/Geo.png)

* **Fungsi:** Peta vektor interaktif kepulauan Indonesia yang secara otomatis menyalakan provinsi dengan warna oranye (*Accent Orange*) apabila terdapat unit genset yang beroperasi di wilayah tersebut, sementara provinsi kosong dibiarkan redup.
* **Cara Membaca:** Arahkan kursor ke provinsi yang menyala untuk melihat rincian kota/site, atau klik provinsi untuk membuka daftar unit di wilayah tersebut. Jika terdapat lokasi umum yang belum terpetakan ke provinsi (seperti nama jalan tanpa nama kota), notifikasi peringatan kuning akan muncul tepat di bawah peta.

---

## 5. Future Roadmap & Database Restructuring Plan <kbd>🟢 Planned</kbd>

Agar potensi analitik dashboard ini bisa berkembang jauh lebih dalam di versi berikutnya (*Version 3*), struktur pencatatan di Google Spreadsheet disarankan untuk dirombak secara bertahap dengan poin-poin berikut:

1. **Standardisasi Kode Unit sebagai Primary Key (`NO. Unit` / `Kode Genset`):**
   * Saat ini, penulisan nama unit di sheet *Penawaran Deal* masih sering dicampur dengan deskripsi bebas (contoh: `Fawde 20kva (ST)`), sedangkan di *Daftar Genset* dan *Hour Meter* menggunakan kode baku (contoh: `GJP-05-030-MW`).
   * **Target:** Menggunakan dropdown kode unit baku di sheet *Penawaran Deal* agar sistem dapat menghitung **Profitabilitas Bersih per Unit** (Total Pemasukan Sewa/Jasa dikurangi Biaya Sparepart & Overhaul per masing-masing mesin).
2. **Pemisahan Kolom Kota/Provinsi di Sheet Daftar Genset:**
   * Menambahkan kolom terpisah untuk **Provinsi** dan **Kota/Kabupaten** di samping kolom alamat detail (*Lokasi*).
   * **Target:** Menghilangkan data lokasi yang tidak terpetakan (*unmapped*) pada peta geospasial dan membuka fitur filter wilayah per provinsi secara otomatis.
3. **Arsip Log Hour Meter Berbasis Periode (Bulan & Tahun):**
   * Menambahkan kolom `Periode (YYYY-MM)` pada sheet *Hour Meter* atau memisahkan tab per bulan dengan format header yang seragam.
   * **Target:** Membuat filter bulan di pojok kanan atas dashboard dapat memfilter data historis pemakaian mesin secara akurat dari bulan ke bulan, bukan hanya membaca bulan berjalan.
4. **Penambahan Kolom Tanggal Mulai & Berakhir Kontrak Sewa:**
   * Menambahkan kolom `Start Date` dan `End Date` pada transaksi yang berjenis *Rental* di sheet *Penawaran Deal*.
   * **Target:** Mengubah *Contract Expiry Radar* menjadi sistem peringatan otomatis berbasis tanggal jatuh tempo kontrak (misalnya peringatan 30 hari sebelum kontrak berakhir).
5. **Pencatatan Biaya Aktual Maintenance & Sparepart:**
   * Menambahkan kolom `HPP / Biaya Aktual` di samping harga penawaran pada sheet *Penawaran Deal*.
   * **Target:** Menampilkan metrik **Gross Profit Margin (%)** secara langsung di halaman *Master Summary* untuk melengkapi angka *Realized Revenue*.

