---
layout: default
title: Dasar Privasi — Abba
---

# Dasar Privasi

**Dikemas Kini Terakhir: 22 April 2026**

## 1. Pengenalan

Abba ("kami", "aplikasi kami", "aplikasi") ialah aplikasi mudah alih rakan doa dan Masa Tenang (Quiet Time) yang dibina untuk orang Kristian yang ingin berdoa dengan lebih mendalam. Dasar Privasi ini menerangkan bagaimana Abba mengumpul, menggunakan, menyimpan dan melindungi maklumat anda apabila anda menggunakan aplikasi iOS (Bundle ID: `com.ystech.abba`).

Abba pada masa ini dikendalikan sebagai projek pembangun bebas. Apabila kami merujuk kepada "kami" dalam dasar ini, kami bermaksud pasukan Abba. Jika Abba menjadi syarikat berdaftar pada masa hadapan, dasar ini akan dikemas kini dengan sewajarnya.

Dasar ini terpakai di seluruh dunia. Kami mengikut prinsip Peraturan Perlindungan Data Umum EU (GDPR), Akta Privasi Pengguna California (CCPA), dan Akta Perlindungan Maklumat Peribadi Korea (PIPA) jika berkenaan. Untuk pengguna di Malaysia, kami juga mengambil kira semangat Akta Perlindungan Data Peribadi (PDPA).

## 2. Maklumat yang Kami Kumpul

### 2.1 Maklumat Akaun
Abba adalah **mengutamakan tanpa nama**. Apabila anda membuka aplikasi buat kali pertama, kami mencipta ID pengguna tanpa nama (UUID) supaya doa dan tetapan anda boleh disegerakkan merentas sesi. Anda tidak perlu memberikan nama, e-mel atau nombor telefon untuk menggunakan Abba.

Secara pilihan, anda boleh log masuk dengan **Apple Sign-In** atau **Google Sign-In** untuk menyandarkan data anda. Dalam kes itu, kami menerima alamat e-mel anda dan pengecam unik dari Apple atau Google. Anda boleh menggunakan "Sembunyikan E-mel Saya" dengan Apple Sign-In jika anda mahu.

### 2.2 Kandungan Doa (Data Teras)
Apabila anda menggunakan Abba, kami mengumpul:
- **Rakaman audio** doa lisan anda
- **Transkrip** yang dijana daripada rakaman tersebut
- **Teks renungan dan refleksi** yang anda tulis atau jana
- **Petikan Kitab Suci** yang anda tandakan

Ini adalah data paling sensitif yang dikendalikan Abba, dan kami mengendalikannya dengan berhati-hati. Audio anda disimpan di folder peribadi anda sendiri pada storan selamat kami. Hanya anda yang boleh mengaksesnya. Kami tidak mendengarnya, berkongsinya atau menggunakannya untuk pemasaran.

### 2.3 Maklumat Langganan
Jika anda melanggan Abba Pro, perkhidmatan pihak ketiga yang dipanggil **RevenueCat** merekodkan status langganan anda (aktif, tamat tempoh, percubaan, dsb.) bersama dengan ID tanpa nama. Kami **tidak** menerima nombor kad kredit anda — itu kekal dengan Apple.

### 2.4 Maklumat Teknikal
- Bahasa peranti (untuk menetapkan bahasa lalai aplikasi)
- Log ranap dengan data peribadi ditutup (melalui Sentry)
- Token pemberitahuan tolak (FCM, pilihan — hanya jika anda mengaktifkan pemberitahuan)
- Versi aplikasi dan versi iOS (untuk penyahpepijatan)

## 3. Cara Kami Menggunakan Maklumat Anda

Kami menggunakan maklumat anda untuk:
- **Memberikan analisis AI** bagi doa dan refleksi Masa Tenang anda (Google Gemini)
- **Menyegerakkan data anda** merentas sesi dan peranti
- **Menguruskan langganan anda** dan kelayakan
- **Membetulkan pepijat dan menambah baik aplikasi** melalui laporan ranap
- **Menghantar pemberitahuan tolak pilihan** (peringatan Masa Tenang harian) jika anda memilih untuk ikut serta

Kami **tidak**:
- Memaparkan sebarang iklan
- Menjual data anda kepada sesiapa
- Berkongsi kandungan doa anda dengan pihak ketiga (kecuali pemprosesan AI yang diterangkan di bawah)
- Menggunakan kandungan anda untuk melatih model AI

## 4. Perkhidmatan Pihak Ketiga

Abba bergantung pada sebilangan kecil perkhidmatan yang dipercayai untuk beroperasi.

| Perkhidmatan | Tujuan | Data Dihantar | Wilayah |
|---|---|---|---|
| **Supabase** | Pangkalan data & pengesahan | ID tanpa nama, doa, metadata | AS / EU |
| **Google Gemini API** | Analisis AI untuk doa | Hanya teks doa | Google Cloud |
| **RevenueCat** | Pengurusan langganan | ID tanpa nama, resit pembelian | AS |
| **Sentry** | Pelaporan ranap (PII ditutup) | Jejak ralat dengan e-mel, transkrip panjang, JWT dialih keluar | AS / EU |
| **Firebase Cloud Messaging** | Pemberitahuan tolak (pilihan) | Token FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Pautan akaun pilihan | E-mel, ID pembekal | Apple / Google |

**Google Gemini:** Menurut dasar yang diterbitkan Google untuk penggunaan API berbayar, kandungan doa yang dihantar ke Gemini **tidak digunakan untuk melatih model AI Google**. Pemprosesan adalah sementara.

**Penutupan PII Sentry:** Kami menggunakan peraturan penutupan sebelum menghantar laporan ranap — e-mel, transkrip lebih 50 aksara, JWT, dan pengecam lain dialih keluar.

## 5. Penyimpanan Data dan Keselamatan

- Semua data dalam transit disulitkan melalui HTTPS (TLS 1.2+).
- Data semasa berehat dilindungi oleh penyulitan penyedia pangkalan data kami.
- **Keselamatan Peringkat Baris (RLS)** dalam Supabase memastikan anda hanya boleh mengakses data anda sendiri.
- Fail audio disimpan dalam folder setiap pengguna dengan akses dikawal oleh token pengesahan anda.
- Token akses disimpan dalam iOS Secure Enclave (`flutter_secure_storage`), tidak pernah dalam keutamaan biasa.

Kami menyimpan data anda selagi akaun anda aktif. Jika anda memadam akaun anda, kami akan mengalih keluar data anda dalam **30 hari**, kecuali di mana kami dikehendaki secara undang-undang untuk menyimpan rekod (seperti rekod cukai untuk pembelian langganan, yang Apple/RevenueCat simpan mengikut dasar mereka sendiri).

## 6. Hak Anda

Anda mempunyai hak berikut ke atas data peribadi anda:

- **Akses** — minta salinan data yang kami simpan tentang anda
- **Pembetulan** — minta kami membetulkan maklumat yang tidak tepat
- **Pemadaman** — minta kami memadam akaun dan data anda (tersedia dalam aplikasi: Tetapan → Akaun → Padam Akaun, atau melalui e-mel)
- **Kemudahalihan** — minta eksport data anda dalam format boleh dibaca mesin
- **Bantahan** — membantah pemprosesan tertentu
- **Tarik balik kebenaran** — anda boleh menarik balik kebenaran untuk pemberitahuan tolak, pemprosesan AI, atau pautan akaun pada bila-bila masa

Untuk penduduk GDPR (EU) dan CCPA (California), hak ini dijamin oleh undang-undang. Untuk melaksanakan sebarang hak, e-mel **rrallvv@gmail.com**. Kami membalas dalam tempoh 30 hari.

## 7. Privasi Kanak-kanak

Abba dinilai 4+ di App Store. Kami tidak mengumpul maklumat dengan sengaja daripada kanak-kanak di bawah umur 13 (COPPA) atau di bawah umur 16 (GDPR, di beberapa negara EU) tanpa persetujuan ibu bapa yang boleh disahkan. Jika anda percaya seorang kanak-kanak telah memberikan maklumat peribadi, sila hubungi kami dan kami akan memadamkannya dengan segera.

## 8. Pemindahan Data Antarabangsa

Infrastruktur kami dihoskan di Amerika Syarikat dan Kesatuan Eropah. Dengan menggunakan Abba, anda bersetuju data anda dipindahkan ke dan diproses di kawasan ini. Kami bergantung pada Klausa Kontrak Standard (SCCs) jika diperlukan.

## 9. Permintaan Kerajaan dan Undang-undang

Kami mendedahkan data pengguna hanya apabila diperlukan secara undang-undang (sepina yang sah, perintah mahkamah, atau setara). Kami belum menerbitkan laporan ketelusan lagi, tetapi kami berjanji untuk memberitahu pengguna yang terjejas apabila dibenarkan secara undang-undang.

## 10. Perubahan pada Dasar Ini

Kami boleh mengemas kini Dasar Privasi ini apabila Abba berkembang. Apabila kami membuat perubahan material, kami akan memberitahu anda dalam aplikasi dan mengemas kini tarikh "Dikemas Kini Terakhir" di bahagian atas. Penggunaan berterusan Abba selepas perubahan bermakna anda menerima dasar yang dikemas kini.

## 11. Hubungi Kami

Soalan, permintaan atau aduan?

- **E-mel:** rrallvv@gmail.com
- **Masa respons:** dalam 30 hari (biasanya lebih cepat)

Anda juga mempunyai hak untuk memfailkan aduan dengan pihak berkuasa perlindungan data tempatan anda (cth., DPA negara anggota EU anda, Peguam Negara California, atau PIPC Korea).

---
⚠️ **Notis Terjemahan**: Ini adalah terjemahan yang disediakan untuk kemudahan.
Sekiranya terdapat sebarang percanggahan, [versi Bahasa Inggeris](../privacy.html) akan diutamakan.
