# Jurnal Proses — Tugas 2

## [28/09/2026]
- Opsi arsitektur yang dipertimbangkan: kami memutuskan memakai Kombinasi Service-Oriented Architecture (SOA) dan Publish-Subscribe (Event-Driven).
- Kenapa akhirnya pilih [SOA/Pub-Sub]:  Karena kebutuhan tiap modul di FoodGo itu beda-beda. Interaksi pemesanan dan pembayaran membutuhkan kepastian validasi yang instan atau real-time sehingga pendekatan SOA yang sinkron lebih tepat. Tapi buat urusan nyari kurir dan notif ke resto, bakal lebih optimal kalau dijalanin di background secara asinkron pakai Pub-Sub
- Revisi diagram (versi 1 → versi 2, apa yang berubah dan kenapa): Sejak awal diskusi, kelompok kami sudah sepakat untuk langsung merancang arsitektur kombinasi. menggunakan SOA, akan berisiko menyebabkan antrean atau bottleneck pada layanan kurir. Sebaliknya, jika memaksakan Publish-Subscribe murni untuk semua layanan, sangat berisiko memunculkan masalah Eventual Consistency pada modul pembayaran, di mana pelanggan bisa mengira pesanan sukses padahal pembayaran gagal di latar belakang.


## Log Penggunaan AI (Level 2)

> Wajib diisi sesuai kebijakan Level 2 di [`../RUBRIK-UMUM.md`](../RUBRIK-UMUM.md). Tulis "Tidak memakai AI" pada baris pertama jika memang tidak dipakai. Hanya untuk brainstorming ide/outline — bukan untuk kode/analisis/teks akhir.

| Tanggal | Tool AI | Prompt yang diberikan | Ringkasan saran/ide AI | Bagaimana diolah jadi tulisan/kode sendiri |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |
