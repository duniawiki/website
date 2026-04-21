---
layout: post
title:  "Sistem AI baru akurat petakan ruang hijau kota, ungkap kesenjangan lingkungan"
author: dewek
categories: [ Tekno, Lingkungan, Urban ]
tags: [ AI, Inderaja ]
image: assets/img/rumichunara1.avif
lat: 24.860966
long: 66.990501
---


Sebuah tim peneliti yang dipimpin oleh [Rumi Chunara](https://engineering.nyu.edu/faculty/rumi-chunara), seorang _associate professor_ di NYU yang pernah bekerja di Tandon School of Engineering dan School of Global Public Health, telah meluncurkan sistem kecerdasan buatan (AI) baru yang menggunakan citra satelit untuk melacak ruang hijau perkotaan dengan lebih akurat dibandingkan metode sebelumnya, yang sangat penting untuk memastikan kota yang sehat.

Untuk memvalidasi pendekatan mereka, para peneliti [menguji sistem tersebut di Karachi](https://chunaralab.github.io/GreenSpaceAnalysis/), kota terbesar di Pakistan tempat beberapa anggota tim berasal. Karachi terbukti menjadi tempat uji coba yang ideal karena perpaduan wilayah perkotaan yang padat dan kondisi vegetasi yang bervariasi.

Analisis tim yang diterima untuk dipublikasikan oleh [ACM Journal on Computing and Sustainable Societies](https://dl.acm.org/toc/acmjcss/2025/3/1) ini mengungkap kesenjangan lingkungan yang mencolok: beberapa daerah menikmati jalanan yang ditumbuhi pepohonan, sementara banyak lingkungan yang hampir tidak memiliki vegetasi sama sekali.

Kota-kota telah lama kesulitan untuk melacak ruang hijau mereka dengan tepat, mulai dari taman hingga pepohonan di jalan, dimana analisis satelit tradisional kehilangan sekitar 37% vegetasi perkotaan.

Ketika kota-kota menghadapi perubahan iklim dan urbanisasi yang pesat, terutama di Asia dan Afrika, pengukuran yang akurat menjadi hal yang penting. Ruang hijau dapat membantu mengurangi suhu perkotaan, menyaring polusi udara, dan menyediakan ruang penting untuk berolahraga dan kesehatan mental.

Namun ruang hijau ini mungkin tidak terdistribusi secara merata. Daerah berpendapatan rendah sering kali kekurangan vegetasi, sehingga menjadikan daerah tersebut lebih panas dan lebih tercemar dibandingkan daerah kaya yang banyak pepohonannya.

Tim peneliti mengembangkan solusi mereka dengan meningkatkan arsitektur segmentasi AI, seperti DeepLabV3+. Dengan menggunakan citra satelit resolusi tinggi dari Google Earth, mereka melatih sistem dengan menambah data pelatihan mereka untuk memasukkan beragam versi vegetasi hijau dalam kondisi pencahayaan dan musiman yang berbeda – sebuah proses yang mereka sebut 'augmentasi hijau'. Teknik ini meningkatkan akurasi pendeteksian vegetasi sebesar 13,4% dibandingkan metode AI yang sudah ada – sebuah kemajuan signifikan di bidangnya.

Saat mengukur seberapa sering sistem mengidentifikasi vegetasi dengan benar, sistem ini mencapai akurasi 89,4% dengan keandalan 90,6%, jauh lebih baik dibandingkan metode tradisional yang hanya mencapai akurasi 63,3% dengan keandalan 64,0%. 

“Metode sebelumnya mengandalkan pengukuran panjang gelombang cahaya sederhana,” kata Chunara, yang menjabat sebagai Direktur Pusat Ilmu Data Kesehatan NYU dan anggota [Pusat Pencitraan Visual dan Analisis Data (_Visualization Imaging and Data Analysis Center_, VIDA)](https://engineering.nyu.edu/research-innovation/centers/visualization-imaging-and-data-analysis-center-vida) NYU Tandon. “Sistem kami belajar untuk mengenali pola yang lebih halus yang membedakan pohon dan rumput, bahkan di lingkungan perkotaan yang menantang. Jenis data ini diperlukan bagi perencana kota untuk mengidentifikasi lingkungan yang kekurangan vegetasi sehingga mereka dapat mengembangkan ruang hijau baru yang akan memberikan manfaat semaksimal mungkin. Tanpa pemetaan yang akurat, kota tidak dapat mengatasi kesenjangan secara efektif.”

Analisis di Karachi menemukan bahwa rata-rata kota ini hanya memiliki 4,17 meter persegi ruang hijau per orang, kurang dari setengah rekomendasi Organisasi Kesehatan Dunia (WHO) yaitu minimal 9 meter persegi per kapita. Kesenjangan dalam lingkungan sangat dramatis: meskipun beberapa dewan serikat pekerja di wilayah terpencil – yang merupakan badan pemerintah daerah terkecil di Pakistan, dengan total 173 orang yang dilibatkan dalam penelitian ini – memiliki luas lebih dari 80 meter persegi per orang, lima dewan serikat pekerja memiliki luas kurang dari 0,1 meter persegi per kapita.

Studi tersebut mengungkapkan bahwa daerah dengan lebih banyak jalan beraspal – yang biasanya merupakan penanda pembangunan ekonomi – cenderung memiliki lebih banyak pohon dan rumput. Yang lebih penting lagi, dalam delapan dewan serikat pekerja berbeda yang diteliti, wilayah dengan lebih banyak vegetasi menunjukkan suhu permukaan yang jauh lebih rendah, yang menunjukkan peran ruang hijau dalam mendinginkan kota.

Singapura menawarkan kontras, menunjukkan apa yang mungkin terjadi jika dilakukan perencanaan yang matang. Meskipun memiliki kepadatan penduduk yang serupa dengan Karachi, kota ini menyediakan 9,9 meter persegi ruang hijau per orang, melebihi target WHO.

Para peneliti telah mempublikasikan metodologi mereka, meskipun penerapannya di kota-kota lain memerlukan pelatihan ulang sistem pada citra satelit lokal.

Studi ini menambah upaya Chunara dalam mengembangkan metode komputasi dan statistik, termasuk _data mining_ dan _machine learning_, untuk memahami faktor penentu sosial dari kesehatan dan kesenjangan kesehatan. Penelitian sebelumnya mencakup [penggunaan postingan media sosial untuk memetakan rasisme dan homofobia sistemik di tingkat lingkungan dan menilai dampaknya terhadap kesehatan mental](https://engineering.nyu.edu/news/twitter-reveals-nyc-neighborhoods-racism-and-homophobia-nyu-tandon-school-engineering), serta menganalisis catatan kesehatan elektronik untuk memahami [kesenjangan akses telemedis selama COVID-19](https://engineering.nyu.edu/news/telemedicine-and-healthcare-disparities-cohort-study-large-healthcare-system-new-york-city).

Selain Chunara, penulis makalah ini adalah Miao Zhang, seorang kandidat Ph.D. di [Departemen Ilmu dan Teknik Komputer NYU Tandon](https://engineering.nyu.edu/academics/departments/computer-science-and-engineering) dan VIDA; dan Hajra Arshad, Manzar Abbas, Hamzah Jehanzeb, Izza Tahir, Javerya Hassan dan Zainab Samad dari Departemen Kedokteran Universitas Aga Khan di Karachi. Samad juga bekerja di Pusat Ilmu Data Kesehatan CITRIC Universitas Aga Khan.

Penelitian ini terselenggara berkat pendanaan yang disediakan oleh National Science Foundation dan National Institutes of Health.

Sumber: <https://doi.org/10.1145/3716370>