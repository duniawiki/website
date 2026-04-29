---
title: "Berkontribusi di Dunia.Wiki"
permalink: "/join"
layout: page-about
# comments: false
search: exclude
image: assets/images/contribution.avif
---

Terima kasih telah meluangkan waktu untuk berkontribusi pada proyek ini! Kami sangat menghargai bantuan Anda untuk membuat dokumentasi atau konten kami menjadi lebih baik.

Kontribusi bisa dilakukan dengan menulis artikel baru, memperbaiki artikel yang sudah ada, memberikan kritik dan saran, atau dengan donasi.

## Menulis Artikel Baru atau Menyunting Yang Sudah Ada

Berikut adalah panduan langkah demi langkah agar proses kontribusi Anda berjalan lancar.

1. **Persiapan Awal**

    Sebelum memulai, pastikan Anda memiliki akun [**GitHub**](https://github.com) dan memahami dasar-dasar [**Markdown**](https://www.markdownguide.org/). Karena website ini dibangun menggunakan [**Jekyll**](https://jekyllrb.com/), struktur folder dan _front matter_ sangatlah penting.
    
    **Struktur Utama Folder:**
    
    - `_posts/`:  Tempat menyimpan artikel atau berita (format: `TAHUN-BULAN-TANGGAL-judul.md`).
    - `assets/`: Tempat menyimpan gambar atau file pendukung lainnya.

2. **Alur Kerja Git (Workflow)**

    Kami menggunakan model *Fork & Pull Request*. Ikuti langkah berikut:

    - **Fork** repositori ini ke akun GitHub Anda.

    - **Clone** hasil fork tersebut ke komputer lokal Anda:

        ````bash
        git clone https://github.com/duniawiki/website.git
        ````

    - Buat **Branch** baru untuk perubahan Anda agar tetap rapi:
    
        ````bash
        git checkout -b fitur-atau-artikel-baru
        ````

    - Lakukan perubahan atau tambahkan konten baru.
 
    - **Commit** dan **Push** perubahan Anda:

        ````bash
        git add .
        git commit -m "Menambah artikel tentang X"
        git push origin fitur-atau-artikel-baru
        ````

    - Buka repositori asli di GitHub dan klik "**Compare & pull request**".


3. **Menulis Artikel Baru**

    Semua artikel harus diletakkan di dalam folder `_posts/`. Nama file wajib mengikuti format:`YYYY-MM-DD-judul-singkat.md`
    
    Contoh: `2026-04-22-elnino-mengancam-pertanian.md`
    
    **Front Matter**
    
    Di bagian paling atas file, Anda harus menyertakan **Front Matter** dalam format YAML yang diapit oleh dua garis putus-putus (`---`). Ini digunakan Jekyll untuk mengatur metadata artikel.
    ````YAML
    ---
    layout: post
    title: "Judul Artikel Anda"
    date: 2026-04-22 09:00:00 +0700
    categories: [ Iklim ]
    tags: [ Pemanasan Global ]
    author: "Nama Anda"
    image: assets/img/nama-file-gambar.webp
    lat: yy.yyyyy
    long: xx.xxxx
    ---
    ````

    Contoh format penulisan artikel lengkap, bisa dilihat pada berkas artikel yang ada dalam folder `_posts`.

4. **Kategori dan Kata Kunci ( *categories & tags* )**

    Kategori utama disebutkan dalam `categories`. Saat ini tersedia kategori: `Lingkungan`, `Iklim`, `Tekno`, `Urban`, `Alam Liar`, `Energi Baru`, `Semesta`, `Peta` dan `Sejarah`. Mohon untuk menulis artikel dalam kategori yang sudah disediakan ini, atau hubungi kami jika dirasa perlu ada kategori baru.

    Sedangkan untuk kata kunci (*tags*), Anda dibebaskan untuk memasukkan kata kunci yang sesuai dengan artikel kiriman Anda, tetapi disarankan tidak lebih dari tiga kata kunci.

5. **Lintang dan Bujur ( *lat & long* )**

    Gunakan jika artikel anda memuat informasi lokasi tentang dimana kejadian atau artikel itu berasal. Ditulis dengan format [_decimal degree_](https://id.wikipedia.org/wiki/Derajat_desimal). 
    
    Jika ada lebih dari satu lokasi pada artikel, gunakan lokasi utama dalam artikel. Abaikan jika tidak ada (tidak perlu menuliskan baris `lat` dan `long`).
    

6. **Panduan Penulisan Markdown**

    Gunakan format Markdown standar untuk menjaga konsistensi tampilan:
    
    - **Heading**
    
        Gunakan `#` untuk judul besar dan `##` atau `###` untuk sub-judul. Jangan gunakan `#` tunggal di dalam artikel karena sudah digunakan untuk judul utama oleh sistem (sudah ada `title` pada _Front Matter_).
    
    - **Gambar**
    
        Simpan gambar di folder `assets/img/`. Panggil dengan cara:

        `![Deskripsi Gambar](/assets/img/nama-file.jpg)`

        Gambar utama artikel tidak perlu dipanggil ulang karena akan otomatis ditambahkan di bagian atas artikel oleh sistem (sudah ada `image` pada _Front Matter_).

        Lakukan optimasi pada gambar yang akan digunakan untuk menghemat ruang penyimpanan dan mempercepat akses pengunjung, [TinyPNG](https://www.tinypng.com) bisa sangat membantu dalam mengecilkan ukuran berkas gambar.
    
    - **Kode (*Code Blocks*)**
    
        Untuk menampilkan potongan kode, gunakan _backticks_:
    
        ````
        ```python
        def hello_world():
        print("Halo kontributor!")
        ```
        ````

        Akan menghasilkan:

        ```python
        def hello_world():
        print("Halo kontributor!")
        ```

    - **Tabel**

        Gunakan tiga atau lebih tanda minus/penghubung (`---`) untuk memisahkan kepala kolom dan gunakan karakter pipa (`|`) untuk memisahkan tiap kolom. 

        Contoh: 
    
        ````YAML
        |Nama Komponen |Fungsi |
        |--------------|-------|
        |`_config.yml` |Pengaturan utama website|
        |`_layouts  `  |Template tampilan halaman|
        ````

        Untuk mendapatkan hasil seperti ini:

        |Nama Komponen |Fungsi |
        |-------|-------|
        |`_config.yml` |Pengaturan utama website|
        |`_layouts`    |Template tampilan halaman|


7. **Hal-hal yang Perlu Diperhatikan**
    - **Gunakan Bahasa yang Jelas**: Pastikan tulisan mudah dipahami karena meskipun situs ini banyak memuat sari artikel ilmiah tetapi tujuan utamanya adalah pembaca umum, dan bebas dari kesalahan ketik (_typo_).
    - **Lisensi**: Dengan mengirimkan Pull Request, Anda setuju bahwa kontribusi Anda akan dilisensikan di bawah lisensi yang sama dengan proyek ini.
    - **Review**: Tim kami akan meninjau perubahan Anda. Jika ada saran perbaikan, kami akan meninggalkan komentar di halaman Pull Request Anda.

## Kritik, Saran dan Komentar

Kritik, saran dan komentar membangun akan sangat membantu menjaga kualitas situs dan tulisan yang ada. Silakan layangkan komentar atas tulisan di bagian bawah tiap halaman artikel. Sedangkan [kritik dan saran](/about#graphcomment) bisa diajukan di bagian bawah halaman "Tentang Kami".

Untuk kejelasan identitas, kritik, saran dan komentar ini mengguanakan sistem dari GraphComment. Identitas anda diperjelas dengan login ke GraphComment, atau menggunakan akun Facebook, X/Twitter dan Google.

## Donasi

Donasi bisa dilakukan lewat [saweria.co](/sawer) untuk keperluan teknis pemeliharan dan kelangsungan situs ini. 

**Selamat berkontribusi!** Jika ada pertanyaan, jangan ragu untuk membuka [Issue](https://github.com/duniawiki/website/issues) baru, atau [hubungi kami](/contact).