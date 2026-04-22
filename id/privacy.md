---
layout: default
title: Kebijakan Privasi — Abba
---

# Kebijakan Privasi

**Terakhir Diperbarui: 22 April 2026**

## 1. Pendahuluan

Abba ("kami", "aplikasi kami", "aplikasi") adalah aplikasi seluler pendamping doa dan Saat Teduh (Quiet Time) yang dibuat untuk umat Kristiani yang ingin berdoa lebih dalam. Kebijakan Privasi ini menjelaskan bagaimana Abba mengumpulkan, menggunakan, menyimpan, dan melindungi informasi Anda saat Anda menggunakan aplikasi iOS (Bundle ID: `com.ystech.abba`).

Abba saat ini dijalankan sebagai proyek pengembang independen. Ketika kami menyebut "kami" dalam kebijakan ini, yang kami maksud adalah tim Abba. Jika Abba menjadi perusahaan terdaftar di masa mendatang, kebijakan ini akan diperbarui sesuai dengan itu.

Kebijakan ini berlaku secara global. Kami mengikuti prinsip-prinsip Peraturan Perlindungan Data Umum Uni Eropa (GDPR), Undang-Undang Privasi Konsumen California (CCPA), dan Undang-Undang Perlindungan Informasi Pribadi Korea (PIPA) jika berlaku. Untuk pengguna di Indonesia, kami mengikuti semangat UU Perlindungan Data Pribadi (UU PDP).

## 2. Informasi yang Kami Kumpulkan

### 2.1 Informasi Akun
Abba **mengutamakan anonimitas**. Saat Anda membuka aplikasi untuk pertama kali, kami membuat ID pengguna anonim (UUID) agar doa dan pengaturan Anda dapat disinkronkan antar sesi. Anda tidak perlu memberikan nama, email, atau nomor telepon untuk menggunakan Abba.

Anda dapat secara opsional masuk dengan **Apple Sign-In** atau **Google Sign-In** untuk mencadangkan data Anda. Dalam hal itu, kami menerima alamat email Anda dan pengenal unik dari Apple atau Google. Anda dapat menggunakan "Sembunyikan Email Saya" dengan Apple Sign-In jika Anda mau.

### 2.2 Konten Doa (Data Inti)
Ketika Anda menggunakan Abba, kami mengumpulkan:
- **Rekaman audio** dari doa lisan Anda
- **Transkrip** yang dihasilkan dari rekaman tersebut
- **Teks renungan dan refleksi** yang Anda tulis atau hasilkan
- **Bagian Kitab Suci** yang Anda tandai

Ini adalah data paling sensitif yang ditangani Abba, dan kami memperlakukannya dengan hati-hati. Audio Anda disimpan di folder pribadi Anda sendiri di penyimpanan aman kami. Hanya Anda yang dapat mengaksesnya. Kami tidak mendengarkannya, membagikannya, atau menggunakannya untuk pemasaran.

### 2.3 Informasi Langganan
Jika Anda berlangganan Abba Pro, layanan pihak ketiga bernama **RevenueCat** mencatat status langganan Anda (aktif, kedaluwarsa, uji coba, dll.) bersama dengan ID anonim. Kami **tidak** menerima nomor kartu kredit Anda — itu tetap dengan Apple.

### 2.4 Informasi Teknis
- Bahasa perangkat (untuk mengatur bahasa default aplikasi)
- Log kerusakan dengan data pribadi yang disamarkan (melalui Sentry)
- Token notifikasi push (FCM, opsional — hanya jika Anda mengaktifkan notifikasi)
- Versi aplikasi dan versi iOS (untuk debugging)

## 3. Cara Kami Menggunakan Informasi Anda

Kami menggunakan informasi Anda untuk:
- **Memberikan analisis AI** untuk doa dan refleksi Saat Teduh Anda (Google Gemini)
- **Menyinkronkan data Anda** antar sesi dan perangkat
- **Mengelola langganan Anda** dan hak
- **Memperbaiki bug dan meningkatkan aplikasi** melalui laporan kerusakan
- **Mengirim notifikasi push opsional** (pengingat Saat Teduh harian) jika Anda memilih untuk ikut serta

Kami **tidak**:
- Menampilkan iklan apa pun
- Menjual data Anda kepada siapa pun
- Membagikan konten doa Anda dengan pihak ketiga (kecuali pemrosesan AI yang dijelaskan di bawah)
- Menggunakan konten Anda untuk melatih model AI

## 4. Layanan Pihak Ketiga

Abba mengandalkan sejumlah kecil layanan tepercaya untuk beroperasi.

| Layanan | Tujuan | Data Dikirim | Wilayah |
|---|---|---|---|
| **Supabase** | Basis data & autentikasi | ID anonim, doa, metadata | AS / UE |
| **Google Gemini API** | Analisis AI untuk doa | Hanya teks doa | Google Cloud |
| **RevenueCat** | Manajemen langganan | ID anonim, tanda terima pembelian | AS |
| **Sentry** | Pelaporan kerusakan (PII disamarkan) | Pelacakan kesalahan dengan email, transkrip panjang, JWT dihapus | AS / UE |
| **Firebase Cloud Messaging** | Notifikasi push (opsional) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Tautan akun opsional | Email, ID penyedia | Apple / Google |

**Google Gemini:** Sesuai kebijakan yang diterbitkan Google untuk penggunaan API berbayar, konten doa yang dikirim ke Gemini **tidak digunakan untuk melatih model AI Google**. Pemrosesan bersifat sementara.

**Penyamaran PII Sentry:** Kami menerapkan aturan penyamaran sebelum mengirim laporan kerusakan — email, transkrip lebih dari 50 karakter, JWT, dan pengenal lainnya dihapus.

## 5. Penyimpanan dan Keamanan Data

- Semua data dalam transit dienkripsi melalui HTTPS (TLS 1.2+).
- Data saat disimpan dilindungi oleh enkripsi penyedia basis data kami.
- **Keamanan Tingkat Baris (RLS)** di Supabase memastikan Anda hanya dapat mengakses data Anda sendiri.
- File audio disimpan dalam folder per pengguna dengan akses dikontrol oleh token autentikasi Anda.
- Token akses disimpan di Secure Enclave iOS (`flutter_secure_storage`), tidak pernah di preferensi biasa.

Kami menyimpan data Anda selama akun Anda aktif. Jika Anda menghapus akun Anda, kami akan menghapus data Anda dalam waktu **30 hari**, kecuali di mana kami secara hukum diwajibkan untuk menyimpan catatan (seperti catatan pajak untuk pembelian langganan, yang disimpan Apple/RevenueCat berdasarkan kebijakan mereka sendiri).

## 6. Hak Anda

Anda memiliki hak-hak berikut atas data pribadi Anda:

- **Akses** — meminta salinan data yang kami simpan tentang Anda
- **Koreksi** — meminta kami memperbaiki informasi yang tidak akurat
- **Penghapusan** — meminta kami menghapus akun dan data Anda (tersedia di aplikasi: Pengaturan → Akun → Hapus Akun, atau melalui email)
- **Portabilitas** — meminta ekspor data Anda dalam format yang dapat dibaca mesin
- **Keberatan** — keberatan terhadap pemrosesan tertentu
- **Menarik persetujuan** — Anda dapat menarik persetujuan untuk notifikasi push, pemrosesan AI, atau penautan akun kapan saja

Untuk penduduk GDPR (UE) dan CCPA (California), hak-hak ini dijamin oleh hukum. Untuk menggunakan hak apa pun, kirim email ke **rrallvv@gmail.com**. Kami merespons dalam waktu 30 hari.

## 7. Privasi Anak-Anak

Abba dinilai 4+ di App Store. Kami tidak secara sadar mengumpulkan informasi dari anak-anak di bawah 13 (COPPA) atau di bawah 16 (GDPR, di beberapa negara UE) tanpa persetujuan orang tua yang dapat diverifikasi. Jika Anda yakin seorang anak telah memberikan informasi pribadi, silakan hubungi kami dan kami akan menghapusnya segera.

## 8. Transfer Data Internasional

Infrastruktur kami di-host di Amerika Serikat dan Uni Eropa. Dengan menggunakan Abba, Anda menyetujui data Anda ditransfer ke dan diproses di wilayah tersebut. Kami mengandalkan Klausa Kontrak Standar (SCCs) jika diperlukan.

## 9. Permintaan Pemerintah dan Hukum

Kami mengungkapkan data pengguna hanya ketika diwajibkan secara hukum (panggilan pengadilan yang sah, perintah pengadilan, atau yang setara). Kami belum menerbitkan laporan transparansi, tetapi kami berkomitmen untuk memberi tahu pengguna yang terkena dampak bila diizinkan secara hukum.

## 10. Perubahan pada Kebijakan Ini

Kami dapat memperbarui Kebijakan Privasi ini seiring Abba berkembang. Ketika kami membuat perubahan materiil, kami akan memberi tahu Anda di aplikasi dan memperbarui tanggal "Terakhir Diperbarui" di bagian atas. Penggunaan Abba yang berkelanjutan setelah perubahan berarti Anda menerima kebijakan yang diperbarui.

## 11. Hubungi Kami

Pertanyaan, permintaan, atau keluhan?

- **Email:** rrallvv@gmail.com
- **Waktu respons:** dalam 30 hari (biasanya lebih cepat)

Anda juga memiliki hak untuk mengajukan keluhan kepada otoritas perlindungan data lokal Anda (misalnya, DPA negara anggota UE Anda, Jaksa Agung California, atau PIPC Korea).

---
⚠️ **Pemberitahuan Terjemahan**: Ini adalah terjemahan yang disediakan untuk kemudahan.
Dalam hal terjadi perbedaan, [versi Bahasa Inggris](../privacy.html) yang berlaku.
