# Review Produk E-Commerce Dataset (ML Dataset)

Repository berisi dataset mengenai review produk yang ada pada e-commerce berbahasa indonesia. Review diambil dari tiap kategori produk yang ada di e-commerce. Tiap kategori memiliki rata-rata 200 lebih  produk yang berkaitan dengan kategori tersebut. Jumlah dataset saat ini sudah melebihi 3 Juta review dengan perkiraan mungkin akan ada lebih dari 5 Juta dataset setelah proses Crawling dilakukan.

Machine learning adalah pendekatan yang sangat populer untuk memperoleh knowledge berdasarkan pola yang ada pada dataset. Kali ini saya tidak akan menerangkan mengenai Machine learning melainkan bagaimana kita dapat mendapatkan dataset untuk model machine learning yang ingin kita buat.

Kendala utama yang ada pada Machine learning adalah kualitas dan juga kuantitas pada dataset yang digunakan untuk melatih model machine learning kita. Sering kita mendengar konsep "Garbage-in Garbage out". Jadi apabila yang kita masukan adalah sampah maka model yang terbentuk menghasilkan sampah juga. Oleh karena itu kita perlu melakukan serangkaian pemrosesan sebelum kita melatih model machine learning.

Dataset berdasarkan hak aksesnya dibagi menjadi dua yaitu open source dan juga closed source. Data yang open source atau bersifat public umumnya dapat kita peroleh di portal portal penyedia dataset public seperti kaagle ataupun public repository dari universitas seperti repository milik UCI. Sedangkan data yang closed source atau bersifat private hanya dimiliki oleh suatu organisasi ataupun perusahaan dan hanya dapat dikelola oleh organisasi atau perusahaan tersebut.

Data sentimen analisis berbahasa indonesia yang bersifat public masih sangat sedikit. Terlebih lagi jumlah pada dataset tersebut umumnya tidak begitu banyak rata-rata berkisar diantara 1000-15000 berdasarkan pengalaman penulis. Tentu hal ini menjadi problem yang apabila kita menggunakan metode deep learning ataupun machine learning yang membutuhkan data dalam jumlah yang sangat banyak.

Repository ini menjadi alternatif dalam mencari dataset untuk penelitian sentimen analisis dengan pendekatan machine learning maupun deep learning

## Bagaimana Pemerolehan Dataset

**Akses API review pada platform e-commerce**
Setelah dianalisis, Banyak dari platform e-commerce menggunakan API yang cukup sederhana dimana kita hanya memerlukan product ID untuk mendapatkan data review pada produk tersebut. Cara mengetahui alamat API yang digunakan sangatlah mudah yaitu kita dapat membuka developer tools pada browser (disini saya menggunakan Chrome). Lalu kita buka salah satu produk pada lazada dan kita klik halaman pagination review yang ada pada produk tersebut. Saat kita mengklik halaman pagination selanjutnya disini misal mengklik halaman dua kita sebelumnya harus membuka tabel network untuk melihat data apa saja yang didapatkan oleh browser kita. Dan nanti setelah kita mengklik halaman dua maka akan muncul alamat API tersebut
  
**Dapatkan setiap produk ID**
Bagaimana cara mendapatkan produk ID ? Tentu kita dapat memanfaatkan fitur pencarian yang ada pada lazada dan shopee disini kita perlu menentukan barang apa saja yang ingin kita cari lalu kita dapat mengekstrak product id dengan melihat struktur HTMLnya. Hal ini bisa kalian pelajari menggunakan tools beautifulsoup ataupun menggunakan regex. Disini saya menggunakan python dan sudah ada juga code khusus untuk mendapatkan setiap produk ID berdasarkan pencarian.

**Crawl setiap komentar yang ada pada produk ID tersebut**
Proses ini sangatlah memakan banyak waktu. Hal ini dikarenakan dataset yang kita ambil jumlahnya sangat banyak dan mekanisme server yang membatasi hak akses. Apabila kita melakukan request terlalu banyak maka akan langsung diblock oleh server tidak hanya itu banyak sekali mekanisme keamanan sistem yang membuat kita harus membatasi kecepatan pengaksesan, IP address (disini saya sarankan menggunakan VPN apabila IP kita sudah diblokir), menggunakan selenium (mengapa selenium karena selenium dapat mengatasi permasalahan apabila http header kita diblock oleh server). Saya menggunakan selenium dalam melakukan crawl data. 



## Dataset masih dalam pengembangan

Dataset ini masih dalam proses crawling dan belum dilakukan serangkaian proses pra pengolahan kata sehingga tidak menjamin menghasilkan performansi yang baik dalam membangun model. 
Beberapa fenomena yang perlu dilakukan pra pengolahan kata
1. Simbol
2. Kode Gambar
3. Kata Gaul
4. Kata Tidak Baku
5. Kata dengan huruf berulang
6. Angka
7. Tanda Baca 

> **Note:** Jika anda ingin berkontribusi membangun dataset ini saya sangat mengapresiasi :)


## Publikasi

Untuk saat ini anda bisa menghubungi saya terkait dengan sitasi dan penggunaan dari dataset ini. Dataset ini bersifat publik dan dapat digunakan secara gratis namun untuk feedback saya anda dapat menginformasikan paper atau penelitian yang menggunakan dataset ini. Terima kasih
