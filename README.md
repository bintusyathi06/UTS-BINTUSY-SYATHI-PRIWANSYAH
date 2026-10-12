# UTS Coding Akuntansi - Purwarupa Voucher Kas Keluar

Repositori ini dibuat untuk memenuhi Ujian Tengah Semester (UTS) mata kuliah **Pengkodean dan Pemrograman / Coding Akuntansi** Semester Gasal 2026/2027.

## 👤 Identitas Mahasiswa
- **Nama:** Bintusy Syathi Priwansyah
- **NIM:** 12030124140286
- **Kelas:** Akuntansi D
- **Dosen Pengampu:** Totok Dewayanto
- **Universitas:** Fakultas Ekonomika dan Bisnis, Universitas Diponegoro

## 📖 Deskripsi Proyek
Proyek ini merupakan purwarupa (prototype) modul **Voucher Entri Transaksi Kas Keluar** berbasis web yang terintegrasi dengan database cloud PostgreSQL (Supabase). Sistem ini dirancang untuk memastikan asas *zero-discrepancy* (Total Debit = Total Kredit) sebelum transaksi disimpan, serta dilengkapi dengan mekanisme jejak audit (*audit trail*).

## ✨ Fitur Utama
1. **Formulir Dinamis:** Entri header voucher (Nomor, Tanggal, Penerima, Keterangan) dan baris jurnal yang dapat ditambah/hapus.
2. **Live Balanced Indicator:** Kalkulasi otomatis Total Debit dan Kredit. Tombol "Simpan" hanya aktif jika status **BALANCED** (Debit = Kredit > 0).
3. **Validasi Ganda:** Mencegah pengisian Debit dan Kredit secara bersamaan dalam satu baris.
4. **Integrasi Database (3NF):** Data disimpan ke tabel `journal_headers` dan `journal_lines` di Supabase untuk menjaga normalisasi data.
5. **Audit Trail & Immutability:** Mencegah perubahan/penghapusan jurnal yang sudah berstatus `POSTED` (harus melalui jurnal pembalik).

## 🛠️ Teknologi yang Digunakan
- **Frontend:** HTML5, Tailwind CSS, Vanilla JavaScript
- **Backend/Database:** Supabase (PostgreSQL)
- **Tools AI:** Gemini Canvas (Pembuatan UI), NotebookLM (Verifikasi Aturan Bisnis PSAK)

## 🔗 Tautan Penting
- **Live Demo (GitHub Pages):** [Klik di sini untuk membuka Web Voucher](https://bintusyathi06.github.io/UTS-BINTUSY-SYATHI-PRIWANSYAH/)
- **Database:** Supabase (PostgreSQL)

## 📂 Struktur Database (Soal 1 & 2)
Proyek ini mengimplementasikan skema database relasional yang mencakup:
- `chart_of_accounts` (Master Akun)
- `journal_headers` (Header Jurnal)
- `journal_lines` (Baris Jurnal)
- `inventory_items` & `inventory_transactions` (Modul Persediaan Perpetual dengan Trigger Otomatis)

---
*Dibuat untuk keperluan akademik. Seluruh artefak kode dan logika bisnis telah diverifikasi sesuai dengan kaidah akuntansi berpasangan.*
