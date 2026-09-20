# Tugas 1 — Analisis Pitfall FoodGo

**Kelompok:** [Yang penting happy]

| Nama | NIM | Kontribusi |
|---|---|---|
| [Bagas Bintang Saputro] | [103072400078] | [The Network is Realible] |
| [Wahyu Puji Riski Purwanto] | [103072400050] | [Latency is Zero] |
| [Andi Muh. Arief alfaizi ilham] | [103072400082] | [Single Point Of Failure ] |

## Pitfall 1: [the network is reliable] — ditulis oleh [Bagas Bintang Saputro]

**Bukti di skenario:** [Kami menemukan bahwa code mereka menulis asumsi seperti # network is realible, for need to retry]

**Kenapa ini keliru:** [Dalam dunia nyata jaringan fisik maupun virtual sangat rentan terhadap gangguan. Paket data bisa hilang (packet loss),lalu router bisa mengalami restart atau terjadinya fluktuasi sinyal pada sisi pengguna aplikasi seluler. Sistem terdistribusi yang tangguh harus berasumsi bahwa kegagalan jaringan adalah hal yang pasti terjadi (meskipun jarang) dan termasuk hal yang bukan mustahil untuk terjadi]

**Dampak ke FoodGo:** [Ketika terjadi kegagalan jaringan sementara asaat aplikasi mengirim data pesanan ke backend, sistem langsung menyerah dan gagal karena tidak memilii mekanisme retry. Hal ini menyebabkan pengguna mengalami error secara tiba-tiba meskipun server sebenarnya masih menyala]

**Solusi desain awal:** [Bisa diterapkan pola Retry dengan Exponential Backoff & Jitter. Jika terjadi kegagalan koneksi, sistem akan mencoba ulang pengiriman dengan jeda waktu yang bertambah secara eksponensial misalnya jeda 1 detik,lalu 2 detik, lalu 5 detik yang ditambah sedikit waktu acak (Jitter) agar tidak terjadi penumpukan request pada detik yang sama]

**Trade-off:** [Meskipun retry berguna untuk mengatasi kegagalan jaringan sementara, jika tidak dikonfigurasi dengan hati-hati, retry justru bisa menjadi pisau bermata dua. jika server backend sedang sangat lambat karena kelebihan beban trafik sungguhan, ratusan hingga ribuan user yang melakukan entry serentak akan memberikan beban tambahan yang eksponensial. Hal ini dapat menyebabkan cascading failure dimana server yang awalnya hanya sekedar lambat akhirnya hancur dihantam request ulang]

---

## Pitfall 2: [nama pitfall] — ditulis oleh [nama]

(ulangi struktur di atas)

---

## Pitfall 3: [Single Point Of Failure ] — ditulis oleh [Andi Muh Arief Alfaizi Ilham]

**Bukti di skenario:** [satu server yang menangani semua modul (pesanan, pembayaran, notifikasi kurir) kewalahan karena semuanya berjalan di satu proses monolitik yang sama.]

**Kenapa ini keliru:** [karena beberapa modul berada dalam 1 server yang dapat menyebabkan lag dan sistemnya mati]

**Dampak ke FoodGo:** [server kemungkinan akan mengalami crash akibat terlalu banyak request yang terpaksa melakukan restart terhadap server]

**Solusi desain awal:** [Melakukan pemisahan setiap modul yang menjadi layanan tepisah]

**Trade-off:** [Komunikasi Antar modul menjadi lebih rumit karena harus bergantung pada jaringan internet/internal, dan merawat banyak layanan terpisah membutuhkan biaya serta usaha yang lebih besar di bandingkan satu server]

## Kesimpulan Kelompok

[Ringkasan: jika FoodGo memperbaiki ketiga pitfall ini, apa arsitektur yang disarankan secara garis besar? Kaitkan dengan Tugas 2.]
