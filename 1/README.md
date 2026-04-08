# MATERI PERTEMUAN 1: 
# Pengantar Manajemen Proyek Perangkat Lunak di Era Modern

## 1. Pengantar: Apa itu Proyek?
Sebelum membahas perangkat lunak, kita harus menyamakan persepsi mengenai esensi "proyek".
* **Definisi:** Proyek adalah usaha sementara (temporer) yang dilakukan untuk menciptakan produk, jasa, atau hasil yang unik.
* **Karakteristik Utama Proyek:**
    * **Sementara:** Memiliki awal dan akhir yang jelas. Proyek selesai ketika tujuannya tercapai, atau dihentikan jika tujuannya tidak lagi relevan.
    * **Unik:** Berbeda dengan kegiatan operasional yang rutin dan berulang.
* **The Triple Constraint (Segitiga Kendala):** Setiap proyek selalu dibatasi oleh tiga elemen yang saling tarik-menarik:
    1.  **Waktu (Jadwal):** Kapan proyek harus selesai?
    2.  **Biaya (Anggaran):** Berapa *budget* yang dialokasikan?
    3.  **Ruang Lingkup (*Scope*):** Apa saja fitur atau batasan yang harus dikerjakan?
    * *Catatan:* Jika klien meminta tambahan fitur (*scope* bertambah), maka waktu atau biaya pasti harus ikut bertambah. Kualitas produk berada di tengah-tengah segitiga ini.

## 2. Mengapa Proyek Perangkat Lunak Itu Unik dan Berbeda?
Membangun sistem perangkat lunak (misalnya membangun API backend dengan Golang atau model *machine learning* dengan Python) sangat berbeda dengan membangun jembatan atau gedung fisik.
* **Invisibility (Tidak Kasat Mata):** Progres fisik tidak terlihat. Kita tidak bisa melihat kerangka gedung yang sudah setengah jadi. Kemajuan proyek hanya bisa diukur dari artefak seperti dokumentasi, diagram, atau *working software* yang sudah di-*deploy*.
* **Complexity (Kompleksitas Tinggi):** Terdiri dari ribuan baris kode. Perubahan pada satu modul fungsional dapat merusak modul lain secara tak terduga (*bug*).
* **Flexibility (Sangat Fleksibel):** Karena wujudnya digital, perangkat lunak sangat mudah diubah kapan saja. Hal ini sering menjadi bumerang berupa *Scope Creep* (ruang lingkup proyek yang melebar terus-menerus karena klien meminta perubahan).

## 3. Realita Pengembangan Perangkat Lunak Saat Ini (Konteks Terkini)
Manajemen proyek tidak bisa lagi dijalankan dengan gaya tahun 2000-an. Industri saat ini bergerak sangat cepat dengan standar baru:
* **Era *Generative AI* dan *Copilot*:** Penulisan kode saat ini menjadi sangat cepat dengan bantuan AI. Tantangan manajer proyek bukan lagi "berapa lama *developer* mengetik kode", melainkan pada fase perancangan arsitektur, integrasi, *review* kelayakan kode, dan pemenuhan logika bisnis klien.
* **Keamanan Sejak Awal (*DevSecOps*):** Dulu, uji keamanan jaringan atau *penetration testing* baru dilakukan di akhir proyek. Sekarang, keamanan harus dipikirkan sejak fase perencanaan (*Shift-Left Security*). Proyek bisa dianggap gagal jika di akhir fase rilis ditemukan celah keamanan fatal (misalnya injeksi SQL atau kebocoran data).
* ***Agile* Sebagai Standar Fundamental:** Pendekatan kaku yang menolak perubahan di tengah jalan sudah banyak ditinggalkan. Industri menggunakan *Agile/Scrum* untuk bisa beradaptasi dengan cepat terhadap perubahan permintaan pasar atau *feedback* dari *user*.
* **Tim yang Terdistribusi (*Remote Working*):** Sangat umum anggota tim tidak berada di satu kantor. Manajemen komunikasi beralih dari rapat tatap muka menjadi pengelolaan *repository* (Git), *sprint board* (Jira/Trello), dan dokumentasi yang asinkron namun disiplin.

## 4. Faktor Kegagalan dan Keberhasilan Proyek
Menurut data industri (seperti *CHAOS Report*), banyak proyek perangkat lunak yang gagal (melebihi *budget*, terlambat, atau dibatalkan). 
* **Mengapa Proyek Gagal?**
    * Kebutuhan klien (*requirements*) yang ambigu, tidak jelas, atau terus berubah tanpa kontrol.
    * Estimasi waktu dan biaya yang terlalu optimis dan tidak rasional.
    * Kurangnya komunikasi dan keterlibatan langsung dari pengguna akhir (*end-user*).
    * Manajemen risiko dan keamanan yang buruk.
* **Faktor Penentu Keberhasilan:**
    * Keterlibatan klien secara intens untuk memberikan *feedback* berkelanjutan.
    * Pendefinisian ruang lingkup yang jelas sejak awal, dengan toleransi perubahan yang dikelola (menggunakan *Agile*).
    * Komunikasi tim yang transparan, meskipun bekerja secara *remote*.

## 5. Manajemen Proyek vs SDLC (*System Development Life Cycle*)
Mahasiswa sering bingung membedakan antara mengelola proyek dan membuat aplikasinya.
* **Siklus Hidup Proyek (Fokus pada Manajerial):**
    1.  *Initiating* (Menentukan tujuan awal dan kelayakan).
    2.  *Planning* (Membuat jadwal, anggaran, alokasi sumber daya).
    3.  *Executing* (Menjalankan rencana).
    4.  *Monitoring & Controlling* (Memantau apakah eksekusi sesuai dengan rencana dan mengendalikan perubahan).
    5.  *Closing* (Serah terima produk dan evaluasi akhir).
* **SDLC (Fokus pada Teknis Rekayasa Perangkat Lunak):**
    Analisis Kebutuhan $\rightarrow$ Desain Arsitektur $\rightarrow$ Pemrograman (*Coding*) $\rightarrow$ Pengujian (*Testing*) $\rightarrow$ Rilis & Pemeliharaan (*Deployment & Maintenance*).
* **Kesimpulan:** Manajemen proyek adalah payung besar yang mengawal dan mengatur jadwal serta sumber daya dari seluruh fase SDLC tersebut agar berjalan selaras.

---

## 6. Sesi Diskusi Interaktif (Tugas Pemantik di Kelas)
*(Tampilkan di slide terakhir untuk memancing partisipasi mahasiswa)*

**Studi Kasus Ringan:**
"Bayangkan kalian adalah seorang Manajer Proyek. Tim *developer* kalian saat ini bisa menggunakan AI untuk men-*generate* kode aplikasi dengan sangat cepat, memangkas waktu *coding* hingga 50%. 

Namun, klien kalian adalah sebuah bank yang sangat ketat soal regulasi dan keamanan data. 

**Pertanyaan:**
Apakah dengan adanya AI ini, proyek kalian dijamin pasti selesai lebih cepat dan sukses? Jika tidak, aspek manajemen proyek apa saja yang justru harus kalian perketat pengawasannya?"