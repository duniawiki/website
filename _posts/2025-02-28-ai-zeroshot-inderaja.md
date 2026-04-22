---
layout: post
title:  "AI Zero-Shot penginderaan jauh: Sebuah pipeline baru untuk segmentasi citra otomatis"
author: dewek
categories: [ Tekno ]
tags: [ AI, Inderaja ]
image: assets/img/ai-zeroshot.avif
lat: 45.4781552 
long: 9.227272
---

Jumlah citra udara dan satelit yang diambil di seluruh dunia terus meningkat dengan kecepatan luar biasa. Namun, mengidentifikasi dan memberi label fitur dalam citra-citra ini, seperti atap, mobil, atau pohon, secara efisien dapat menjadi tantangan. Sebuah alur kerja baru yang dikembangkan oleh para peneliti di Politecnico di Milano dan Universitas Teknik Nasional Athena mengatasi masalah ini dengan menggabungkan model AI canggih dengan strategi penanganan data yang cerdas.

“Model AI serbaguna sangat ampuh, tetapi seringkali kesulitan ketika diminta untuk menemukan objek yang tidak dikenal tanpa pelatihan eksplisit,” kata Profesor Maria Antonia Brovelli dari Politecnico di Milano. “Dengan menggunakan pendekatan hyper inference jendela geser untuk memotong citra besar menjadi bagian-bagian yang lebih kecil dan lebih mudah dikelola, dan dengan menerapkan langkah penolakan outlier untuk menghilangkan deteksi yang salah, kami sangat mengurangi beban komputasi model dan meningkatkan akurasi dalam mengidentifikasi fitur-fitur spesifik.”

Alur kerja mereka memanfaatkan model dasar _open source_ seperti Segment Anything Model (SAM) dan Grounding DINO dalam proses dua langkah yang strategis. Pertama, secara sengaja mendeteksi objek secara berlebihan untuk memastikan bahkan detail terkecil pun dapat ditangkap. Hal ini dicapai melalui pendekatan jendela geser (sliding window), yang menerapkan model deteksi pada bagian gambar yang lebih kecil. Metode ini tidak hanya mengurangi beban komputasi — yang sangat penting untuk citra penginderaan jauh skala besar — tetapi juga meningkatkan akurasi deteksi.

Selanjutnya, sistem menyempurnakan hasilnya dengan menyaring kotak pembatas yang tidak relevan, seperti yang terlalu besar atau posisinya buruk, menggunakan teknik statistik dan berbasis data. Kotak pembatas berkualitas tinggi yang tersisa kemudian diteruskan ke SAM, yang menghasilkan masker segmentasi yang tepat.

Pipeline ini beroperasi secara zero-shot, artinya model digunakan secara langsung, mempertahankan parameter pelatihan aslinya tanpa penyempurnaan atau pelatihan ulang tambahan pada data eksternal. Pada citra udara dengan resolusi spasial kurang dari 1 meter, pipeline yang dikembangkan mencapai hasil segmentasi yang luar biasa, mencapai akurasi hingga 99%.

“Pada dasarnya, kami memanfaatkan fleksibilitas model AI skala besar yang siap pakai, dengan membangun alur pemrosesan yang kuat yang dikembangkan oleh Mohanad Diab untuk mencapai hasil terbaik,” tambah Kolokoussis. Para peneliti berharap alur ini akan membuat analisis citra penginderaan jauh otomatis lebih mudah diakses, mempercepat segala hal mulai dari survei lingkungan hingga perencanaan kota.

Sumber: <https://doi.org/10.1016/j.aiig.2025.100105>