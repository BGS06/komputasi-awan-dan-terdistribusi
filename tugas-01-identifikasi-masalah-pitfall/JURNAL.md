# Jurnal Proses — Tugas 1

> Isi jurnal ini selama proses diskusi berlangsung, bukan ditulis ulang rapi di akhir. Tulis dengan gaya bebas — poin diskusi, kebuntuan, perubahan pikiran.

## [Tanggal diskusi 1]
- Peserta: [Bagas Bintang Saputro] | [103072400078]
           [Wahyu Puji Riski Purwanto] | [103072400050]
           [Andi Muh. Arief alfaizi ilham] | [103072400082]
- Poin diskusi: ...
- Perbedaan pendapat (jika ada): ...

## [Tanggal diskusi 2]
- ...

## Review Silang
- [Nama] mengomentari analisis [Nama lain]: ...

## Log Penggunaan AI (Level 2)

> Wajib diisi sesuai kebijakan Level 2 di [`../RUBRIK-UMUM.md`](../RUBRIK-UMUM.md). Tulis "Tidak memakai AI" pada baris pertama jika memang tidak dipakai. Hanya untuk brainstorming ide/outline — bukan untuk kode/analisis/teks akhir.

| Tanggal | Tool AI | Prompt yang diberikan | Ringkasan saran/ide AI | Bagaimana diolah jadi tulisan/kode sendiri |
| Tanggal | Tool AI | Prompt yang diberikan | Ringkasan saran/ide AI | Bagaimana diolah jadi tulisan/kode sendiri |
|---|---|---|---|---|
| 21/09/2026 | ChatGPT | Saya sedang menganalisis studi kasus FoodGo dalam mata kuliah Komputasi Awan dan Terdistribusi. Saya memilih salah satu Fallacies of Distributed Computing, yaitu "Latency Is Zero". Dalam skenario FoodGo disebutkan bahwa aplikasi menjadi sangat lambat dan beberapa permintaan mengalami timeout. Selain itu, tidak ada timeout pada pemanggilan antar-service; modul pesanan memanggil modul pembayaran dan dapat menunggu tanpa batas waktu. Ketika trafik meningkat, server menjadi kewalahan dan terkadang mengalami crash. Bantu saya menganalisis masalah "Latency Is Zero" berdasarkan skenario tersebut. Jangan berikan jawaban langsung, coba jelaskan kenapa dan berikan sebuah analogi atau contoh yang mudah saya pahami sebagai mahasiswa atau pemula yang baru belajar tentang komputasi awan dan sistem terdistribusi. Jelaskan materi ini dan berikan juga contoh kasusnya. | AI menjelaskan bahwa Latency Is Zero adalah asumsi bahwa komunikasi antar-service selalu berlangsung cepat atau tanpa jeda. Pada FoodGo, modul pesanan menunggu respons dari modul pembayaran tanpa adanya timeout. Ketika trafik meningkat atau modul pembayaran lambat merespons, permintaan dapat menumpuk dan menambah beban server. AI juga memberikan analogi antrean kasir untuk mempermudah pemahaman. | Saya menggunakan AI untuk membantu memahami konsep Latency Is Zero. Dari penjelasan tersebut, saya memahami bahwa tidak adanya timeout dapat membuat proses terus menunggu dan membebani server. Solusi yang saya usulkan adalah menerapkan timeout agar proses tidak menunggu tanpa batas saat modul pembayaran terlambat merespons. |
|21/09/2026| Gemini | Fallacies of Distributed Computing (referensi: "the network is reliable", "latency is zero", "bandwidth is infinite", "the network is secure", "topology doesn't change", "there is one administrator", "transport cost is zero", "the network is homogeneous") DAN/ATAU masalah desain sistem terdistribusi lain yang relevan (mis. single point of failure karena arsitektur monolitik).
jelaskan materi ini dan berikan juga contoh kasus nya  | Membangun sistem terdistribusi dengan asumsi bahwa infrastruktur jaringan akan selalu berjalan sempurna adalah kesalahan fatal. Berikut adalah ringkasan dari 8 Fallacies of Distributed Computing (asumsi keliru) dan masalah arsitektur yang wajib diantisipasi:

Jaringan selalu dapat diandalkan (The network is reliable): Jaringan fisik dan sinyal bisa terputus; sistem yang tidak memiliki mekanisme timeout atau retry akan mengalami hang.
Latensi adalah nol (Latency is zero): Komunikasi antar-server membutuhkan waktu; melakukan request data berulang-ulang melalui jaringan akan menciptakan jeda operasional yang sangat lama.
Bandwidth tidak terbatas (Bandwidth is infinite): Mengirim ukuran data yang terlalu besar atau tidak efisien akan menyumbat kapasitas jaringan (bottleneck).
Jaringan sepenuhnya aman (The network is secure): Ancaman keamanan bisa datang dari dalam jaringan internal; perlindungan firewall luar tidak cukup sehingga data tetap wajib dienkripsi.
Topologi tidak berubah (Topology doesn't change): Infrastruktur cloud selalu berubah secara dinamis; menanamkan (hardcode) IP Address secara statis akan membuat sistem gagal terkoneksi saat server diubah.
Hanya ada satu administrator (There is one administrator): Sistem sering bergantung pada komponen atau API pihak ketiga yang kebijakan dan pengaturannya bisa berubah di luar kendali tim Anda.
Biaya transportasi data adalah nol (Transport cost is zero): Proses transfer data memakan sumber daya komputasi (CPU) dan tagihan finansial dari penyedia layanan cloud.
Jaringan bersifat homogen (The network is homogeneous): Setiap komponen mungkin menggunakan bahasa pemrograman atau perangkat keras yang berbeda, sehingga komunikasi data memerlukan format standar yang universal (seperti JSON atau Protobuf).
Selain asumsi keliru di atas, terdapat kerentanan desain arsitektur yang sering terjadi:
Titik Kegagalan Tunggal (Single Point of Failure / SPOF): Mengandalkan satu komponen sentral (misalnya satu database utama untuk seluruh layanan). Jika komponen ini mati, seluruh aplikasi akan lumpuh total.
Kegagalan Beruntun (Cascading Failures): Efek domino yang terjadi ketika satu layanan melambat, menyebabkan antrean panjang yang pada akhirnya membuat layanan lain yang memanggilnya ikut crash.
Meranang sistem terdistribusi yang tangguh berarti menerapkan prinsip designing for failure—membangun arsitektur sejak awal dengan kesadaran penuh bahwa kegagalan jaringan, gangguan komponen, dan perubahan sistem pasti akan terjadi.| setelah memahami penjelasan dan contoh kasus yang di berikan ai saya memahami bahwa salah satu masalah desain sistem terdistribusi "yaitu Single Point Of Failure" di karena kana salah satu gejala mirip dengan penjelasan dari ai yaitu 1 server yang sama(monolitik) jadi memudahkan saya untuk menganalisis |
| ... | ... | ... | ... | ... |
