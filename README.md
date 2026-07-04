# 🌸 Lifa Flora — Online Flower Bouquet Store

**Business Overview**

| | |
|---|---|
| **Nama** | Alifah Salma Fauziah |
| **NIM** | 209250117 |
| **Program Studi** | Administrasi Bisnis 6 |
| **Mata Kuliah** | Komputer Aplikasi IT-II (KAIT-II) |
| **Semester** | Genap 2026 |

🔗 **Repository:** https://github.com/alifahsalmafauziah-coder/Lifa-Flora-Online-Store-bouquettt

🛍️ **Live site (customer):** https://alifahsalmafauziah-coder.github.io/Lifa-Flora-Online-Store-bouquettt/

🔐 **Live site (admin):** https://alifahsalmafauziah-coder.github.io/Lifa-Flora-Online-Store-bouquettt/admin/admin_login.html

---

## 1. Profil Bisnis

**Nama Bisnis:** Lifa Flora

**Deskripsi:**
Lifa Flora adalah toko bunga online yang menjual buket bunga segar dan buket custom untuk berbagai momen spesial seperti ulang tahun, anniversary, wisuda, hingga hadiah personal. Pelanggan dapat memilih, memesan, dan membayar buket sepenuhnya secara online melalui website, tanpa perlu datang ke toko fisik.

**Value Proposition:**
- Buket bunga segar dengan desain estetik dan siap kirim di hari yang sama (same-day delivery area Bandung)
- Pemesanan online yang mudah mulai dari katalog, keranjang, sampai checkout dalam satu alur
- Harga transparan, tanpa biaya tersembunyi, plus promo gratis ongkir area Bandung
- Pilihan buket custom untuk momen personal (anniversary, wisuda, ulang tahun)

---

## 2. Target Market & Segmentasi Pelanggan

**Target utama:** Usia 12–35 tahun, berdomisili di Bandung dan sekitarnya, aktif berbelanja online, dan sering mencari hadiah untuk momen spesial.

Segmentasi pelanggan:
1. **Pasangan muda / anniversary buyer** — mencari buket romantis (mawar, tulip, lavender) untuk hari jadi.
2. **Mahasiswa & keluarga wisuda** — mencari buket wisuda dengan aksen pita/boneka bunga.
3. **Pemberi hadiah ulang tahun** — mencari buket ceria, warna-warni, dengan harga terjangkau.
4. **Pembeli custom/korporat** — perusahaan atau individu yang butuh buket khusus untuk acara formal.

---

## 3. Analisis Pasar Singkat & Kompetitor

Industri florist online di Indonesia tumbuh seiring naiknya kebiasaan belanja hadiah lewat marketplace dan media sosial, terutama menjelang momen seperti Hari Valentine, wisuda, dan ulang tahun.

**Kompetitor tidak langsung/langsung:**
- Toko bunga lokal Bandung dengan pemesanan via WhatsApp (proses manual, tidak ada katalog online terstruktur)
- Platform florist nasional (mis. layanan kirim bunga berbasis app) — jangkauan lebih luas tapi harga lebih tinggi dan kurang personal
- Marketplace umum (Shopee/Tokopedia) — banyak pilihan tapi kualitas dan kesegaran bunga tidak terjamin

**Peluang Lifa Flora:** menggabungkan pengalaman belanja online yang rapi (katalog, keranjang, checkout otomatis) dengan sentuhan lokal Bandung dan kecepatan pengiriman, sesuatu yang jarang ditawarkan toko bunga tradisional.

---

## 4. Strategi Manajemen Produk & Katalog

Katalog produk dikelola melalui panel admin khusus (terpisah dari halaman customer) dan tersinkronisasi otomatis ke halaman utama via Firebase.

**Kategori produk:**
- 💐 Anniversary
- 🎂 Ulang Tahun
- 🎓 Wisuda
- 🎨 Custom

**Strategi konten produk:**
- Setiap produk memiliki nama yang catchy (mis. "Sapphire Wishes", "Sweet Romance"), deskripsi naratif yang menonjolkan simbolisme warna/bunga, dan emoji identitas kategori
- Foto produk asli dan konsisten (rasio & pencahayaan seragam) untuk membangun kepercayaan visual
- Label dinamis seperti 🔥 "Hot/Terlaris" berdasarkan data penjualan, untuk mendorong social proof
- Halaman detail produk menampilkan harga, deskripsi lengkap, dan tombol tambah ke keranjang

**Pengelolaan stok:** admin dapat menambah, mengedit, menghapus, dan memantau stok tiap produk lewat dashboard admin (`admin_produk.html`, `admin_tambah_produk.html`, `admin_edit_produk.html`), serta memantau pesanan masuk lewat `admin_pesanan.html`.

---

## 5. Model Bisnis & Revenue Stream

**Model bisnis:** B2C e-commerce langsung (D2C — direct to consumer), penjualan buket fisik dengan pemesanan online.

**Sumber pendapatan (revenue stream):**
1. Penjualan buket reguler (katalog tetap)
2. Buket custom/personalisasi (harga premium karena request khusus)
3. Add-on/upsell — kartu ucapan, boneka bunga, wrapping premium
4. Potensi kerja sama korporat (pengadaan buket untuk acara kantor, seminar, wisuda massal)

---

## 6. Strategi Harga, Promosi, dan Diskon

**Strategi harga:** penetapan harga per produk berdasarkan kompleksitas rangkaian dan jenis bunga (kisaran Rp 145.000 – Rp 260.000), dengan positioning harga menengah — lebih terjangkau dari florist premium, namun kualitas di atas toko bunga pasar biasa.

**Promosi yang berjalan di situs:**
- 🎟️ Kode voucher promo (contoh: `LIFA10`) yang bisa dimasukkan langsung saat checkout
- 🚚 Gratis ongkir untuk area Bandung, ditampilkan sebagai running banner di halaman utama
- Badge "Promo terbatas hari ini" untuk menciptakan urgensi (scarcity marketing)

**Rencana promosi lanjutan:** diskon musiman (menjelang wisuda, Valentine), program referral, dan bundling produk (buket + kartu ucapan).

---

## 7. Proses Checkout & Simulasi Payment Gateway

Alur belanja pelanggan: **Katalog → Detail Produk → Keranjang → Checkout → Konfirmasi Pembayaran → Order Success → Tracking**.

**Simulasi payment gateway:** situs ini menggunakan simulasi pembayaran berbasis **QRIS (dummy)** — pelanggan diarahkan ke tampilan kode QRIS statis (`images/qris.jpg` / `images/qris.png`) di halaman checkout untuk mensimulasikan proses scan-and-pay, tanpa transaksi finansial nyata (cocok untuk keperluan demo/prototipe).

**Rencana pengembangan ke depan:** integrasi payment gateway sungguhan seperti **Midtrans** atau **Xendit**, yang mendukung QRIS resmi, transfer bank, dan e-wallet (GoPay, OVO, Dana) sekaligus verifikasi pembayaran otomatis dan notifikasi real-time ke pelanggan & admin.

---

## 8. Rencana SEO, Keamanan, dan Pemeliharaan

**SEO:**
- Optimasi judul & meta description tiap halaman produk dengan kata kunci relevan ("buket bunga Bandung", "kado wisuda", "bunga anniversary")
- Struktur URL dan heading yang deskriptif
- Alt text pada gambar produk untuk pencarian gambar
- Pendaftaran ke Google Search Console dan Google Business Profile (khusus lokal Bandung)

**Keamanan:**
- Data produk dan pesanan disimpan di Firebase Firestore (lihat `firebase-config.js` dan `admin/firebase-config.js`) dengan rencana penerapan **Firestore Security Rules** agar hanya admin terautentikasi yang bisa menulis/menghapus data
- Rencana migrasi login admin dari sistem password sederhana (`admin_login.html`) ke **Firebase Authentication** agar lebih aman dari akses tidak sah
- Koneksi situs menggunakan HTTPS (otomatis dari GitHub Pages)

**Pemeliharaan:**
- Update katalog & harga berkala oleh admin melalui dashboard
- Monitoring bug dan feedback pengguna secara rutin
- Backup data produk/pesanan secara berkala

---

## 9. Rencana Penggunaan Data Analytics

Data yang dikumpulkan dari aktivitas situs (jumlah terjual per produk, kategori terlaris, kunjungan halaman) akan dimanfaatkan untuk:

1. **Keputusan stok** — memprioritaskan produksi/stok buket dengan penjualan tertinggi (field `sold` pada tiap produk)
2. **Keputusan harga & promo** — mengevaluasi efektivitas kode voucher dan menyesuaikan diskon berdasarkan periode ramai (musim wisuda, Valentine)
3. **Pengembangan katalog** — menambah varian pada kategori yang paling diminati, mengurangi/menghentikan produk yang kurang laku
4. **Optimasi marketing** — memanfaatkan data sumber kunjungan (nantinya via Google Analytics) untuk menentukan kanal promosi paling efektif

Rencana lanjutan: integrasi **Google Analytics** untuk memantau perilaku pengunjung (halaman paling sering dibuka, tingkat drop-off di checkout) sebagai dasar perbaikan pengalaman pengguna (UX).

### Script Google Analytics (Dummy)

Setiap halaman customer (`index.html`, `detail_produk.html`, `keranjang.html`, `checkout.html`, `order_success.html`, `tracking.html`, `login.html`, `register.html`, `profile.html`) sudah dipasangi script `gtag.js` dengan ID **`G-DUMMY123456`** — bukan ID akun Google Analytics asli, sehingga tidak mengirim data sungguhan ke Google. Script ini dipasang untuk mendemonstrasikan cara integrasi teknis, sekaligus metrik yang akan dipantau ketika ID asli dipasang saat website live:

| Metrik | Kegunaan |
|---|---|
| **Bounce rate** | Persentase pengunjung yang keluar tanpa interaksi — indikator relevansi konten halaman |
| **Conversion rate** | Persentase pengunjung yang berhasil checkout — mengukur efektivitas funnel penjualan |
| **Page views per halaman** | Mengetahui produk/kategori mana yang paling sering dilihat |
| **Drop-off funnel** | Titik pengunjung berhenti (keranjang → checkout → order sukses) — untuk perbaikan UX |
| **Traffic source** | Asal pengunjung (pencarian, media sosial, langsung) — untuk optimasi kanal marketing |

---

## 📁 Struktur Proyek

```
LIFA_FLORA/
├── README.md                      # Dokumentasi proyek (file ini)
├── index.html                     # Halaman utama & katalog produk
├── detail_produk.html             # Halaman detail satu produk
├── keranjang.html                 # Halaman keranjang belanja
├── checkout.html                  # Checkout & simulasi payment (QRIS)
├── order_success.html             # Halaman konfirmasi pesanan berhasil
├── tracking.html                  # Halaman lacak status pesanan
├── login.html                     # Login customer
├── register.html                  # Registrasi customer
├── profile.html                   # Profil/akun customer
├── business-overview.html         # Versi HTML dari business overview
├── firebase-config.js             # Konfigurasi & sinkronisasi Firebase (sisi customer)
├── script.js                      # Logic utama sisi customer (katalog, cart, checkout, dll.)
├── style.css                      # Stylesheet utama sisi customer
│
├── images/                        # Aset foto produk & QRIS (sisi customer)
│   ├── Blue_Serenity_Bouquest.jpeg
│   ├── Chocolate_Lily.jpeg
│   ├── Elegant_Matcha_Edition_.jpeg
│   ├── Midnight_Dusk_Premium.jpeg
│   ├── Pink_Harmony.jpeg
│   ├── Sapphire_Wishes.jpeg
│   ├── Summer_Sunshine_Garden.jpeg
│   ├── Sunshine_Birthday_Blooms.jpeg
│   ├── Sweet_Bloom_Wisuda.jpeg
│   ├── Sweet_Romance_.jpeg
│   ├── chery blosoom.jpeg
│   ├── lavender kiss.jpeg
│   ├── mix garden.jpeg
│   ├── pastel tulip.jpeg
│   ├── qris.jpg
│   ├── qris.png
│   ├── rose.jpg
│   ├── sunflower glow.jpeg
│   ├── white lili.jpeg
│   └── wisuda.jpeg
│
└── admin/                         # Panel admin (terpisah dari sisi customer)
    ├── admin.html                 # Entry point / shell panel admin
    ├── admin.js                   # Logic admin berbasis localStorage (sinkron dgn toko)
    ├── admin_login.html           # Login admin
    ├── admin_dashboard.html       # Dashboard ringkasan admin
    ├── admin_produk.html          # Daftar & kelola produk
    ├── admin_tambah_produk.html   # Form tambah produk baru
    ├── admin_edit_produk.html     # Form edit produk
    ├── admin_pesanan.html         # Kelola & pantau pesanan masuk
    ├── admin_script.js            # Logic utama panel admin (CRUD produk & pesanan)
    ├── admin_style.css            # Stylesheet panel admin
    ├── firebase-config.js         # Konfigurasi & sinkronisasi Firebase (sisi admin)
    └── images/                    # Salinan aset foto produk & QRIS untuk sisi admin
        ├── Blue_Serenity_Bouquest.jpeg
        ├── Chocolate_Lily.jpeg
        ├── Elegant_Matcha_Edition_.jpeg
        ├── Midnight_Dusk_Premium.jpeg
        ├── Pink_Harmony.jpeg
        ├── Sapphire_Wishes.jpeg
        ├── Summer_Sunshine_Garden.jpeg
        ├── Sunshine_Birthday_Blooms.jpeg
        ├── Sweet_Bloom_Wisuda.jpeg
        ├── Sweet_Romance_.jpeg
        ├── chery blosoom.jpeg
        ├── lavender kiss.jpeg
        ├── mix garden.jpeg
        ├── pastel tulip.jpeg
        ├── qris.jpg
        ├── qris.png
        ├── rose.jpg
        ├── sunflower glow.jpeg
        ├── white lili.jpeg
        └── wisuda.jpeg
```

**Catatan struktur:**
- Folder `images/` di root dan `admin/images/` berisi set file yang identik (foto produk digandakan agar masing-masing sisi — customer & admin — bisa memuat asetnya sendiri tanpa saling bergantung path).
- Ada dua file `firebase-config.js` (root & `admin/`) dan dua "otak" logic terpisah untuk admin: `admin.js` (versi berbasis `localStorage`, dipakai oleh `admin.html`) dan `admin_script.js` (dipakai oleh halaman-halaman `admin_*.html` lain seperti dashboard, produk, dan pesanan).
- Data produk secara realtime disinkronkan antara sisi customer dan admin melalui Firebase Firestore (koleksi `products`).

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3, vanilla JavaScript (tanpa framework)
- **Font & Icon:** Google Fonts (Playfair Display, DM Sans), Lucide Icons (CDN)
- **Backend/Database:** Firebase Firestore (sinkronisasi data produk realtime)
- **Analytics:** Google Analytics (`gtag.js`) — dummy ID untuk simulasi, belum terhubung ke akun asli
- **Hosting:** GitHub Pages
- **Payment:** Simulasi QRIS statis (belum terintegrasi payment gateway sungguhan)

---

## 🚀 Cara Menjalankan Proyek

1. Clone atau download repository ini.
2. Buka `index.html` langsung di browser, atau jalankan lewat local server (mis. ekstensi *Live Server* di VS Code) agar modul JavaScript (`type="module"` pada `firebase-config.js`) berjalan normal.
3. Untuk masuk ke panel admin, buka `admin/admin_login.html` masukan kata sandi nya.
4. Pastikan koneksi internet aktif karena data produk memakai Firebase Firestore (bukan data statis lokal).
