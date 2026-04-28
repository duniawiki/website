---
layout: post
title:  "Deep Learning perluas riwayat Cahaya Malam global"
author: dewek
categories: [ Tekno ]
tags: [ AI, Inderaja ]
image: assets/img/remotesensing.0874.fig.003.avif
lat: 26.0747 
long: 119.2005
---




Pengamatan cahaya malam (*night time light*, NTL) telah menjadi proksi penting untuk mengukur aktivitas manusia, pertumbuhan perkotaan, dan dinamika sosial ekonomi. Namun, dua sumber utama data NTL berbeda secara substansial. Sistem Pemindaian Garis Operasional Program Satelit Meteorologi Pertahanan (*Defense Meteorological Satellite Program Operational Line Scanning System*, DMSP-OLS) menyediakan catatan historis yang lebih panjang tetapi memiliki resolusi spasial yang lebih kasar, sensitivitas radiometrik yang lebih rendah, dan masalah saturasi yang serius, sementara Rangkaian Radiometer Pencitraan Inframerah Tampak Kemitraan Polar-orbiting Nasional Suomi (*Suomi National Polar-orbiting Partnership’s Visible Infrared Imaging Radiometer Suite*, NPP-VIIRS) menawarkan pengamatan yang lebih halus dan lebih sensitif tetapi baru memulai cakupan tahunan pada tahun 2012. Upaya sebelumnya untuk menyelaraskan kumpulan data ini sering mengorbankan detail atau memperkenalkan bias, terutama di pusat kota yang terang benderang. Berdasarkan tantangan ini, penelitian mendalam diperlukan tentang rekonstruksi cahaya malam jangka panjang, resolusi tinggi, dan konsisten lintas sensor.

Sebuah tim dari Universitas Fuzhou, Universitas Normal Tiongkok Timur, Universitas Normal Anhui, dan Universitas Normal Yunnan melaporkan pada 31 Maret 2026 di Journal of Remote Sensing ([DOI: 10.34133/remotesensing.0874](https://doi.org/10.34133/remotesensing.0874)), merekonstruksi dataset cahaya malam global baru yang memperluas pengamatan tahunan seperti NPP-VIIRS hingga tahun 1992. Studi ini mengatasi keterbatasan utama dalam pengamatan bumi: kurangnya catatan cahaya malam tunggal, berkelanjutan secara temporal, dan konsisten secara radiometrik yang cocok untuk pemantauan jangka panjang urbanisasi, guncangan ekonomi, dan dinamika pemukiman manusia di seluruh dunia.

Studi ini menggabungkan indeks vegetasi yang ditingkatkan (*enhanced vegetation index*, EVI) Landsat tahunan, data DMSP-OLS yang diselaraskan, data NPP-VIIRS bulanan, dan dataset masking dan validasi tambahan untuk merekonstruksi catatan cahaya yang lebih panjang dan lebih tajam. Pertama, tim membangun indeks cahaya malam yang disesuaikan dengan EVI (*EVI-adjusted nighttime light index*, EANTLI) untuk mengurangi efek saturasi pada citra DMSP-OLS. Mereka kemudian mengembangkan dan melatih Attention U-Net dengan Skip connection untuk super resolution (*Attention U-Net with Skip connection for Super Resolution*, ASSR) menggunakan data NTL tahunan NPP-VIIRS 2013 sebagai label dan data 2012 untuk validasi. Akhirnya, data NTL versi 2 yang menyerupai NPP-VIIRS direkonstruksi berdasarkan model ASSR. Dataset ini mencakup periode 1992–2024, memperluas catatan versi 1 sebelumnya yang dimulai pada tahun 2000, dan mempertahankan satuan NPP-VIIRS yaitu nanowatt per sentimeter persegi per steradian (nW·cm⁻²·sr⁻¹) dan resolusi spasial 15 detik busur.

Data NTL versi 2 yang menyerupai NPP-VIIRS mencapai kesesuaian yang kuat dengan data tahunan resmi NPP-VIIRS, dengan nilai R² sebesar 0,66 pada tingkat piksel, 0,91 pada tingkat kota, dan 0,93 pada tingkat provinsi. Di wilayah dengan tingkat saturasi DMSP-OLS yang sulit, dataset ini juga mengungguli tolok ukur SVNTL, mencapai R² = 0,54 dan root mean square error (RMSE) = 20,18, dibandingkan dengan R² = 0,22 dan RMSE = 31,47 untuk SVNTL. Selain akurasi, dataset ini mempertahankan detail spasial yang lebih jelas dan menunjukkan kontinuitas temporal yang lebih halus selama transisi kritis 2011–2013. Pemeriksaan temporal lebih lanjut menunjukkan bahwa dataset ini dapat mencerminkan perubahan ekonomi besar, termasuk perlambatan ekonomi Eropa tahun 2004, resesi global tahun 2008, dan gangguan baru-baru ini di Ukraina. Kesesuaian global dengan produk domestik bruto (PDB) dan populasi mencapai nilai R² masing-masing 0,91 dan 0,92.

Dataset ini membuka kemungkinan baru untuk melacak ekspansi perkotaan multi-dekade, ketahanan ekonomi, pertumbuhan infrastruktur, dan perubahan demografis pada skala global. Dataset ini dapat mendukung aplikasi dalam pemantauan pembangunan, penilaian bencana, perencanaan regional, dan perbandingan sosial ekonomi antar negara. Para penulis juga mencatat bahwa produk saat ini bersifat tahunan, bukan bulanan atau harian, sehingga pekerjaan di masa mendatang dapat berfokus pada resolusi temporal yang lebih halus untuk menangkap perubahan cepat dengan lebih baik. Meskipun demikian, catatan baru ini memberikan dasar yang kuat untuk analisis cahaya malam jangka panjang generasi berikutnya.

**Keterangan Gambar:**

Peta (A) data cahaya malam (NTL) Versi 2 dengan tren kumulatif (bin 1°) intensitas NTL pada arah (B) bujur dan (C) lintang dari tahun 1992 hingga 2024.

Sumber: <https://doi.org/10.34133/remotesensing.0874>