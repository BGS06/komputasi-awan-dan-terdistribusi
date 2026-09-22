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
| ... | ... | ... | ... | ... |