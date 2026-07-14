# Olist Ecommerce Analysis
_Olist_ merupakan platform _e-commerce_ yang menghubungkan para pedagang dengan pelanggan di seluruh wilayah Brazil. Platform ini berfungsi sebagai _marketplace_ yang memfasilitasi para pedagang dalam memasarkan dan menjual produk mereka, sekaligus memudahkan pelanggan untuk mencari, memilih, dan membeli produk secara online.
## Project Overview
Project ini bertujuan untuk mengeksplorasi data transaksi dari platform _Olist_ untuk memperoleh insight mengenai kinerja bisnis secara keseluruhan. Analisis dilakukan dengan mengolah data ke dalam beberapa dashboard yang menyajikan informasi dari berbagai perspektif untuk menjawab berbagai pertanyaan bisnis serta mengidentifikasi insight tambahan yang mendukung pengambilan keputusan.
## Business Problem
Platform _e-commerce_ menghasilkan data transaksi dalam jumlah besar yang mencakup berbagai aspek operasional, seperti penjualan, pelanggan, penjual, produk, pembayaran, dan pengiriman. Tanpa proses analisis, data tersebut sulit dimanfaatkan untuk memperoleh informasi yang mendukung pengambilan keputusan. Oleh karena itu, diperlukan analisis yang mampu memberikan gambaran menyeluruh mengenai kinerja bisnis, memahami perilaku pelanggan, mengevaluasi performa penjual dan produk, serta mengevaluasi proses operasional seperti pembayaran dan pengiriman untuk mengidentifikasi peluang peningkatan efisiensi dan kualitas layanan.
## Dataset Description
Project ini menggunakan Brazilian E-Commerce Public Dataset by Olist, yaitu kumpulan data yang mencakup sekitar 100.000 pesanan selama periode 2016–2018. Dataset ini terdiri atas beberapa tabel yang saling berelasi, meliputi data pelanggan _(customers)_, penjual _(sellers)_, pesanan _(orders)_, rincian item pesanan _(order_items)_, pembayaran _(order_payments)_, ulasan pelanggan _(order_reviews)_, produk _(products)_, kategori produk _(product_category_name_translation)_, serta data geolokasi _(geolocation)_. Selain itu, dataset juga memuat informasi mengenai status pesanan, waktu pemesanan dan pengiriman, harga produk, biaya pengiriman _(freight)_, serta penilaian dan ulasan yang diberikan pelanggan setelah transaksi selesai.
## Data Cleaning & Transformation
Sebelum proses analisis dilakukan, dataset terlebih dahulu melalui tahap data cleaning dan data transformation untuk memastikan kualitas dan konsistensi data yang digunakan. Tahapan ini mencakup penanganan nilai yang hilang, standarisasi format data, pembersihan data yang tidak valid, serta transformasi data ke dalam struktur yang sesuai untuk kebutuhan analisis. Penjelasan lebih rinci mengenai proses tersebut dapat dilihat pada proyek [Olist Data Warehouse].
## Data Modeling
Data yang digunakan dalam analisis ini telah dimodelkan pada proyek Olist Data Warehouse menggunakan skema dimensional (dimensional modeling). Proses tersebut menghasilkan struktur data yang terdiri atas tabel fakta dan tabel dimensi yang telah dioptimalkan untuk kebutuhan analisis dan visualisasi data. Detail mengenai model data serta hubungan antartabel dapat dilihat pada proyek [Olist Data Warehouse].
## Dashboard Overview
### Business Overview Dashboard
![Business Dashboard](images/1_Business_Overview_Dashboard.png)
### Key Insights & Business Recommendation
- Terdapat pertumbuhan bisnis yang signifikan dibanding tahun sebelumnya (lebih dari $95%$), baik dari aspek total pendapatan, total orders maupun total items yang terjual.
  - _Mempertahankan strategi pemasaran dan akuisisi pelanggan yang telah mendorong pertumbuhan bisnis yang signifikan tersebut._
- Meskipun total pendapatan meningkat, nilai _Average Order Value (AOV)_ justru menurun $1.1%$ dibandingkan tahun sebelumnya, yang menunjukkan bahwa peningkatan pendapatan lebih banyak berasal dari bertambahnya jumlah transaksi dibandingkan peningkatan nilai belanja per transaksi.
  - _Meningkatkan nilai transaksi rata-rata melalui strategi cross-selling, bundling produk, atau rekomendasi produk yang relevan._
- Rata-rata waktu pengiriman adalah $12$ hari, sedikit lebih cepat dibanding tahun sebelumnya. Selain itu, $91,48%$ pesanan berhasil dikirim tepat waktu, menunjukkan performa logistik yang baik. Namun, tidak menutup fakta bahwa masih cukup banyak pengiriman yang telat.
  - _Mempertahankan kerja sama dengan mitra logistik yang memiliki performa tinggi, serta mengidentifikasi wilayah atau seller yang masih sering mengalami keterlambatan untuk dilakukan evaluasi lebih lanjut._
- Rata-rata rating pelanggan mencapai $4,07$ dari $5$, dengan mayoritas ulasan termasuk kategori positif. Namun, masih terdapat sekitar $7.750$ ulasan negatif yang menunjukkan adanya ruang untuk perbaikan.
  - _Analisis isi ulasan negatif untuk mengidentifikasi penyebab utama, seperti keterlambatan pengiriman, kualitas produk, atau masalah layanan._
- Sekitar $76%$ transaksi menggunakan kartu kredit, sedangkan pembayaran melalui boleto sekitar $19%$. Metode pembayaran lainnya hanya digunakan oleh sebagian kecil pelanggan.
  - _Optimalkan pengalaman pembayaran menggunakan kartu kredit karena merupakan metode pembayaran utama pelanggan._
- Sebagian besar pesanan telah berstatus _Delivered_, sedangkan jumlah pesanan yang dibatalkan maupun masih diproses relatif kecil dibandingkan total transaksi.
  - _Pantau penyebab pembatalan pesanan agar dapat diminimalkan, serta meningkatkan efisiensi proses pemenuhan pesanan untuk mengurangi pesanan yang masih berada pada tahap pemrosesan._

### Customer Insights Dashboard
![Customer Dashboard](images/2_Customer_Insights_Dashboard.png)
### Key Insights & Business Recommendation
- Jumlah pelanggan mencapai $52,56$ ribu, dengan $51,89$ ribu di antaranya merupakan pelanggan baru, sedangkan pelanggan lama hanya sekitar 2%.
  - Diperlukan pengembangan strategi lebih lanjut untuk menyeimbangkan fokus antara memperoleh pelanggan baru dan mempertahankan pelanggan lama.
- Rata-rata spending customer sebesar $$131.80$ dengan frekuensi berbelanja didominasi $96.6%$ oleh pelanggan yang hanya melakukan satu kali pembelian sedangkan pelanggan yang melakukan pembelian berulang hanya sekitar $3.4%$.
  - Meningkatkan frekuensi pembelian serta nilai belanja pelanggan melalui rekomendasi produk yang dipersonalisasi, pengingat pembelian ulang, dan program loyalitas serta gunakan produk dengan potensi pembelian berulang untuk dijadikan target promosi pada pelanggan yang relevan.
- Customer terdistribusi cukup merata diseluruh wilayah brazil, namun terdapat satu wilayah dengan total customer terbanyak, yaitu Sao Paulo.
  - Mempertahankan strategi pemasaran di wilayah dengan jumlah pelanggan tinggi serta di wilayah yang masih memiliki jumlah pelanggan rendah namun berpotensi berkembang.
- Terdapat pelanggan dengan kontribusi pendapatan sangat tinggi sekitar $6.7$ ribu, sedangkan pelanggan lainnya dalam daftar teratas menyumbang sekitar $3.7-4.6$ ribu.
  - Identifikasi dan pertahankan pelanggan bernilai tinggi melalui program VIP Customer atau layanan eksklusif untuk meningkatkan loyalitas dari pelanggan.

### Product Performance Dashboard
![Product Dashboard](images/2_Customers_Insights_Dashboard.png)
### Key Insights
blabla
### Business Recommendations
blabla

### Seller Performance Dashboard
![Seller Dashboard](images/2_Customers_Insights_Dashboard.png)
### Key Insights
blabla
### Business Recommendations
blabla



