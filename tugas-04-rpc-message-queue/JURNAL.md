# Jurnal Proses — Tugas 4

## Jalur yang dipilih
- Kami memutuskan menggunakan keduanya. RPC kami gunakan untuk operasi sinkron yang wajib menunggu respons seketika, seperti mengecek status saldo. Sedangkan MQ kami terapkan untuk asynchronous decoupling pada operasi yang tidak perlu ditunggu hasilnya, seperti mengirim notifikasi ke modul kurir. agar modul pembayaran tidak tertahan dan tetap responsif walau modul penerima sedang down.

## Kendala teknis
- Error saat setup (mis. koneksi RabbitMQ ditolak, port bentrok): ...

## Uji "pesan tidak hilang" (khusus Jalur B)
- Langkah uji: matikan consumer → jalankan publisher → nyalakan consumer
- Hasil yang diamati: ...

## Log Penggunaan AI (Level 2)

> Wajib diisi sesuai kebijakan Level 2 di [`../RUBRIK-UMUM.md`](../RUBRIK-UMUM.md). Tulis "Tidak memakai AI" pada baris pertama jika memang tidak dipakai. Hanya untuk brainstorming ide/outline — bukan untuk kode/analisis/teks akhir.

| Tanggal | Tool AI | Prompt yang diberikan | Ringkasan saran/ide AI | Bagaimana diolah jadi tulisan/kode sendiri |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |
