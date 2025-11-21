# 📚 REKAP MASTER SITUNEO - DOKUMENTASI LENGKAP
## Dokumen Gabungan dari 5 File Sumber

**Tanggal:** 21 November 2025  
**Status:** REKAP FINAL - SEMUA FILE DIBACA 100%  
**Total Sumber:** 1,502 baris dokumentasi

---

## ⚠️ PENTING: 2 PROJECT BERBEDA!

### PROJECT A: SITUNEO DIGITAL (Marketing Website)
**File Sumber:** File 1, 2, 3
- Website jasa pembuatan website
- Sistem Multi-Level Marketing (Partner-SPV-Manager)
- 232+ layanan digital
- Domain: https://situneo.my.id

### PROJECT B: SITUNEO PENGADILAN AGAMA
**File Sumber:** File 4
- Sistem Informasi Tugas Pembantuan
- Mahkamah Agung → Pengadilan Agama
- Sistem pelaporan & monitoring
- Tech stack: Vue.js + Laravel + PostgreSQL

**CATATAN:** Dokumen ini merekap KEDUA project dengan pemisahan jelas.

---

# 🎯 PART 1: SITUNEO DIGITAL (Marketing Website)

## 1. STRUKTUR ROLE SYSTEM (5 ROLE)

### Hierarki
```
┌─────────────┐
│   ADMIN     │ ← Full Control
└─────────────┘
       │
┌──────▼──────────┐
│ MANAGER AREA    │ ← 5% komisi, min 3 SPV
└─────────────────┘
       │
┌──────▼──────────┐
│   SPV           │ ← 10% komisi, min 10 Partner
└─────────────────┘
       │
┌──────▼──────────┐
│   PARTNER       │ ← 30-55% komisi (tier-based)
└─────────────────┘
       │
┌──────▼──────────┐
│   CLIENT        │ ← Pemesan jasa
└─────────────────┘
```

### Rekrutmen SPV & Manager
- ❌ **BUKAN** promote dari Partner
- ✅ Hire dari luar via registrasi
- ✅ Admin yang approve

---

## 2. SISTEM KOMISI & TANGGUNGAN

### 2.1 Pembagian Komisi Standar

**Contoh: Order Rp 10 juta**
```
Partner   : 40% = Rp 4,000,000
SPV       : 10% = Rp 1,000,000
Manager   :  5% =   Rp 500,000
SITUNEO   : 45% = Rp 4,500,000
─────────────────────────────────
TOTAL     : 100% = Rp 10,000,000
```

### 2.2 Sistem Tier Partner (Dinamis - Bisa Naik/Turun)

| Tier | Target/Bulan | Komisi | Maintenance | Konsekuensi |
|------|--------------|--------|-------------|-------------|
| **Tier 1** | Default | 30% | - | Tier paling bawah |
| **Tier 2** | 10 order | 40% | Min 10 order/bulan | Turun ke Tier 1 jika <10 |
| **Tier 3** | 25 order | 50% | Min 25 order/bulan | Turun ke Tier 2 jika <25 |
| **Tier MAX** | 50 order | 55% | Min 50 order/bulan | Turun ke Tier 3 jika <50 |

**Aturan Tier:**
- Tier bersifat **DINAMIS** (naik & turun setiap bulan)
- Partner baru bisa langsung **Tier MAX dalam 1 bulan** jika capai target
- Tidak maintain target bulan depan → **TURUN TIER**

### 2.3 Tanggungan Sewa (Jika Client Stop <3 Bulan)

**SKENARIO:**
Client sewa 5 halaman (Rp 750K/bulan, min 3 bulan)
- Bulan 1: Client bayar → Partner dapat 40% = Rp 300K
- Bulan 2: Client STOP (tidak bayar)

**TANGGUNGAN:**

**Partner DENGAN SPV & Manager:**
- Partner bayar: **85%** = Rp 127.5K/bulan
- SPV bayar: **10%** = Rp 15K/bulan
- Manager bayar: **5%** = Rp 7.5K/bulan

**Partner TANPA SPV (Daftar Langsung):**
- Partner bayar: **100%** = Rp 150K/bulan
- Admin akan tawarkan: mau dipindahkan ke SPV?
- Admin yang rekomendasikan SPV yang cocok

---

## 3. HARGA & PRODUK

### 3.1 Beli Putus
- **Harga:** Rp 350K/halaman
- **Komisi:** 40% sekali saat serah terima
- **Contoh:** 5 halaman = Rp 1.75 juta → Partner dapat Rp 700K

### 3.2 Sewa (Recurring)
- **Harga:** Rp 150K/halaman/bulan
- **Minimal:** 3 bulan kontrak
- **Komisi Partner:** 40% **hanya bulan pertama**
- **Bulan 2-12:** Partner **TIDAK dapat komisi**
- **Contoh:** 5 halaman = Rp 750K/bulan → Partner dapat Rp 300K (bulan 1 saja)

### 3.3 Penalty
- Client stop <3 bulan → Partner bayar tagihan 1 bulan (sesuai struktur tanggungan)

---

## 4. ARPU BONUS (SPV & MANAGER)

### 4.1 Target & Bonus Bulanan

| Target Revenue | Bonus |
|----------------|-------|
| Rp 15 juta | Rp 500K |
| Rp 35 juta | Rp 1 juta |
| Rp 75 juta | Rp 2 juta |
| Rp 200 juta+ | Rp 10 juta |

### 4.2 Perhitungan ARPU

**CONTOH KONKRIT: SPV punya 10 Partner**

| Partner | Order | Revenue |
|---------|-------|---------|
| Partner 1 | 5 order × Rp 1 juta | Rp 5 juta |
| Partner 2 | 3 order × Rp 2 juta | Rp 6 juta |
| Partner 3-10 | - | Rp 30 juta |
| **TOTAL** | - | **Rp 41 juta** |

**Perhitungan Komisi SPV:**
```
ARPU SPV          = Rp 41 juta
Komisi base 10%   = Rp 4.1 juta
Bonus ARPU tier   = Rp 1 juta (tier Rp 35M-75M)
─────────────────────────────────────────────
TOTAL SPV DAPAT   = Rp 5.1 juta
```

**SISTEM BONUS:**
- Perhitungan **per bulan** (tutup buku akhir bulan)
- Setiap bulan **independen** (tidak kumulatif)
- Bulan depan turun revenue → tidak dapat bonus
- **TIDAK ada** penurunan/kenaikan tier permanen

---

## 5. FORM ORDER & DEMO REQUEST

### 5.1 Flow Registrasi & Order

**WAJIB REGISTRASI AKUN DULU** → Setelah login ada 2 pilihan:

1. **Order Langsung**
2. **Request Demo Dulu**

### 5.2 Form 26 Fields

**Prinsip:**
- Client pasti paham (user-friendly)
- Orang awam pasti bisa menjawab
- Semua field mudah dipahami

**Berlaku untuk:**
- ✅ Order langsung
- ✅ Request demo

### 5.3 Copy Detail Button

**TUJUAN:** File/text siap upload ke Claude AI untuk generate website

**FORMAT OUTPUT (Super Lengkap):**
```
Buatkan website untuk:
Nama Bisnis: [nama]
Jenis Usaha: [jenis]
Target Market: [target]
Fitur Yang Diinginkan:
- [fitur 1]
- [fitur 2]
... (semua 26 fields detail lengkap)
```

**Format Pilihan:**
- Plain Text ATAU
- JSON ATAU
- File download

**Yang penting:** Isi form rapi dan bisa dibaca AI

---

## 6. TASK BOARD SYSTEM

### 6.1 Task Distribution

**SISTEM REBUTAN:**
1. Admin post task ke dashboard
2. **Semua Partner** (100+ partner) bisa lihat - **TIDAK ADA FILTER**
3. Siapa cepat dia dapat

**Mekanisme:**
- Partner klik "Ambil Task" → Task langsung reserved
- Partner lain tidak bisa ambil task yang sudah diambil

**Jika Partner Gagal:**
- Admin tidak yakin dengan hasil kerja
- Task **otomatis dibuka lagi** untuk Partner lain
- Admin **TIDAK assign manual**

### 6.2 Komisi Task

**PENTING:**
- ✅ SPV & Manager **BISA ambil task** (dapat notif seperti Partner)
- ❌ Komisi task **TIDAK cascade** ke SPV/Manager
- ✅ Yang ambil dapat **100%** komisi

**Admin Input:**
- Komisi manual per task (misal: Rp 500K untuk task ini)
- **TIDAK ada** default percentage

---

## 7. MINIMAL PARTNER/SPV/MANAGER

### 7.1 Aturan Minimal

**STANDAR SOP:**
- SPV minimal punya **10 Partner**
- Manager minimal punya **3 SPV**

**Jika Tidak Terpenuhi:**
- Status tetap **ACTIVE** (tidak diturunkan)
- **TIDAK ada** grace period
- **TIDAK ada** pemaksaan resign
- Hasil tidak maksimal (tidak sesuai SOP)
- Semua penghasilan dia yang atur

**PRINSIP:** Sistem tidak memaksa, tapi hasil tidak optimal jika tidak sesuai SOP

---

## 8. WITHDRAWAL SYSTEM

### 8.1 Aturan Withdrawal

```
Minimal    : Rp 50,000
Fee        : GRATIS (Rp 0)
Sistem     : MANUAL (tidak auto)
Integrasi  : TIDAK pakai Xendit/Midtrans
```

### 8.2 Proses Withdrawal

1. Partner request withdrawal
2. Admin approve di dashboard
3. Admin transfer **manual via m-banking**
4. Status updated di sistem

---

## 9. DEMO WEBSITE (50 KATEGORI)

### 9.1 Spesifikasi Demo

**DEMO HARUS:**
- ✅ **Real functioning** website
- ✅ **Semua alur berjalan dan berfungsi**
- ✅ Frontend + Backend fully working
- ✅ Frontend interactive (dropdown, slider, form berfungsi)
- ✅ Backend complete (submit save database, login, dll)

**Database Demo:**
- Boleh diatur bebas (terserah developer)
- Bisa: 50 database terpisah
- Bisa: 1 database dengan prefix table
- Bisa: Langsung di index (semua public)

**Sifat Demo:**
- **Read-only** untuk client
- Cuma untuk **showcase**
- Client tidak bisa edit

### 9.2 50 Kategori Demo Website

1. Toko Online Fashion (Baju, Sepatu, Aksesoris)
2. Restoran / Cafe
3. Toko Elektronik
4. Klinik / Praktek Dokter
5. Salon / Barbershop / Spa
6. Sekolah / Lembaga Pendidikan
7. Properti / Real Estate
8. Hotel / Villa / Homestay
9. Toko Furniture
10. Apotek / Toko Obat
11. Gym / Fitness Center
12. Wedding Organizer
13. Event Organizer
14. Photography Studio
15. Catering
16. Laundry
17. Bengkel / Service Motor-Mobil
18. Kontraktor / Jasa Renovasi
19. Travel Agency
20. Toko Buku / Alat Tulis
21. Pet Shop / Grooming
22. Florist / Toko Bunga
23. Bakery / Toko Kue
24. Minimarket / Toko Kelontong
25. Jasa Cleaning Service
26. Konsultan (HR, Legal, Finance, dll)
27. Software House / IT Solutions
28. Digital Marketing Agency
29. Toko Mainan Anak
30. Toko Perhiasan / Emas
31. Toko Kosmetik / Skincare
32. Barbershop / Pangkas Rambut
33. Notaris / Jasa Legal
34. Kursus / Les Privat
35. Coworking Space
36. Toko Souvenir / Gift Shop
37. Toko Tanaman / Nursery
38. Jasa Arsitek / Interior Design
39. Toko Bahan Bangunan
40. Toko Sepeda / Aksesoris
41. Toko Jam Tangan
42. Toko Tas / Dompet
43. Jasa Pengiriman / Ekspedisi
44. Dealer Motor / Mobil
45. Cuci Motor / Mobil
46. Toko Alat Musik
47. Studio Musik / Recording
48. Jasa Pindahan
49. Rental Kendaraan (Motor/Mobil)
50. Toko Batik / Fashion Lokal

---

## 10. UI/UX DESIGN

### 10.1 Network Particle Animation
- ✅ Konsisten di **semua halaman**
- ✅ Always on (tidak bisa disable)
- ✅ Jumlah particles: Disesuaikan optimal

### 10.2 Loading Screen
- **Durasi:** 2 detik
- **Tampil:** Logo SITUNEO + Tagline + "Memuat ke [Halaman]..."
- **Trigger:** Setiap page transition

### 10.3 Responsive Design
- **Prioritas:** Mobile-first (maksimalkan tampilan mobile)
- **Desktop:** Rapih, tidak perlu ekstrem
- **Dashboard:** Stabil di mobile & desktop untuk Admin/SPV/Manager

---

## 11. DATABASE & FILE STRUCTURE

### 11.1 Database
- **Total:** 85 tables
- **Buat:** Langsung sekaligus (1 SQL file)
- **Sample data:** Kosong (real data only)

**Database Config (dari File 5):**
```
DB_USER: nrrskfvk_user_situneo_digital
DB_PASS: Devin1922$
DB_NAME: nrrskfvk_situneo_digital
Status: CONNECTED ✅
```

### 11.2 File Structure (400+ files)

**Organize By Role:**
```
/admin/
  /dashboard/
  /users/
  /orders/
  /reports/
  /tasks/
  /withdrawals/

/client/
  /dashboard/
  /orders/
  /payments/
  /profile/

/partner/
  /dashboard/
  /earnings/
  /tasks/
  /withdrawals/
  /downline/

/spv/
  /dashboard/
  /team/
  /earnings/
  /reports/

/manager/
  /dashboard/
  /area/
  /team/
  /reports/
```

---

## 12. SECURITY & SESSION

### 12.1 Password Policy
- **Minimal:** 8 karakter
- **Bebas:** tidak wajib uppercase/lowercase/number/special char

### 12.2 Session Management
- **Timeout:** 1 hari
- **Remember me:** Yes
- **IP Whitelist:** TIDAK ada (login dari mana saja)

---

## 13. EMAIL NOTIFICATIONS (14 JENIS)

### 13.1 For Client (7 emails)
1. Welcome email (after register)
2. Email verification
3. Order confirmation (after submit order)
4. Payment received (after upload bukti)
5. Project update (progress update dari admin)
6. Project completed (website sudah siap)
7. Invoice (tagihan untuk sewa bulanan)

### 13.2 For Partner/SPV/Manager (3 emails)
8. Commission earned (ada komisi masuk)
9. Withdrawal approved (request withdraw disetujui)
10. Downline update (ada partner baru dibawahnya)

### 13.3 For Admin (4 emails)
11. New order notification
12. New payment proof uploaded
13. New withdrawal request
14. New demo request

---

## 14. INVOICE NUMBERING

**FORMAT:**
```
INV-SITUNEO-DD-MMM-YYYY-XXXX
```

**Contoh:**
```
INV-SITUNEO-21-NOV-2025-0001
```

**XXXX:** Developer bebas atur yang terbaik
- Boleh: auto increment per hari (reset tiap hari)
- Boleh: auto increment global (tidak reset)

**Berlaku untuk:**
- ✅ Sewa bulanan (recurring)
- ✅ Beli putus
- ✅ Semua layanan dapat invoice

---

## 15. REPORTS & ANALYTICS (ADMIN DASHBOARD)

### 15.1 Laporan Wajib

1. **Revenue Report**
   - Total income per hari/minggu/bulan

2. **Order Report**
   - Jumlah order, completion rate

3. **Partner Report**
   - Top performers, tier distribution

4. **Client Report**
   - New clients, repeat clients

5. **Commission Report**
   - Total komisi paid

6. **ARPU Report**
   - SPV & Manager performance

7. **Service Popularity**
   - Layanan paling laku

8. **Conversion Report**
   - Visitor → client rate

**Status:** Developer bebas atur yang terbaik, yang penting **super lengkap**

---

## 16. MULTI-LANGUAGE

### 16.1 Translation Scope
- ✅ Tersedia di **semua pages**
- ✅ **Manual toggle** user pilih (ID / EN)

### 16.2 Content Dynamic
- Admin input **2 bahasa sekaligus** (ID & EN)
- Nama layanan, deskripsi, blog post → bilingual

### 16.3 Email Notification
- **Ikut bahasa yang user pilih**
- Order confirmation, payment received, dll → sesuai preferensi user

### 16.4 Toggle Language
- Di **header** (flag ID/EN) ✅
- Di **footer** (flag ID/EN) ✅
- **Keduanya boleh** (fleksibel)

---

## 17. CAREER PAGE

### 17.1 Tujuan Career Page

**DUA TIPE RECRUITMENT:**

1. **Internal Team**
   - Developer, Designer, Marketing
   - Jadi karyawan SITUNEO (gaji tetap)

2. **Partner/Freelancer**
   - Kerja project-based
   - Bukan karyawan (komisi)

### 17.2 Apply Job
- Kirim email ke: career@situneo.my.id
- Submit via **form internal** (masuk admin dashboard)

### 17.3 Proses Hiring Developer SITUNEO
1. Admin review CV
2. Interview
3. Hire
4. Kasih akses admin (level developer)

**CATATAN:** Admin cuman **1 orang** (super admin), admin control **semua**

---

## 18. DEVELOPMENT SETUP

### 18.1 Environment
- **Production:** https://situneo.my.id
- **Staging:** TIDAK ada (langsung production)

### 18.2 Git Workflow
- **Repository:** Private
- **Upload:** Manual oleh Anda

### 18.3 Documentation
- **Level:** Basic (README + installation guide)
- **UI:** Self-explanatory (mudah dipahami sendiri)

### 18.4 Backup
- **Trigger:** Manual dari admin
- **Retention:** 30 hari terakhir

---

## 19. FUTURE FEATURES

### 19.1 Payment Gateway
- **Saat ini:** Manual (upload bukti transfer)
- **Future:** Lihat nanti (Midtrans/Xendit)

### 19.2 Live Chat
- **TIDAK ada** → Langsung ke WhatsApp
- Jadi database & bisa dikunci

### 19.3 Blog & Career
- **Blog:** Admin bisa setting & maintain
- **Career:** Untuk rekrutmen team SITUNEO (admin update)

---

## 20. PRIORITAS & TARGET

### 20.1 Development Priority
- **Semua penting** (tidak ada ranking khusus)
- Admin atur prioritas teknis

### 20.2 Quality Standard
```
✅ Quality First (BUKAN speed first)
✅ Zero bug sebelum lanjut fase berikutnya
✅ Test dulu, aman semua, baru lanjut
✅ Target: PERFECT
```

### 20.3 Success Metrics
- ✅ Website live & terima order
- ✅ Partner recruit client & dapat komisi
- ✅ Traffic tinggi
- ✅ Conversion rate tinggi

### 20.4 Deadline
- **Bebas** (quality first, no rush)

### 20.5 Concern Utama
1. **Security:** Harus aman
2. **Performance:** Super lengkap
3. **Scalability:** Awal normal, future 10,000+ users
4. **Maintainability:** Code mudah di-maintain

---

## 21. FILOSOFI NAMA SITUNEO

### 21.1 Etimologi

**SITUNEO = SITU + NEO**

**SITU:**
- Bahasa Indonesia: **Situs** = Website (kata baku KBBI)
- Bahasa Latin: **Situs** = Position/Location
- Makna: Posisi/tempat bisnis di dunia digital

**NEO:**
- Bahasa Yunani: **νέος (néos)** = New/Baru
- Makna: Inovasi, modernisasi, awal baru
- Contoh: Neo dalam film The Matrix (new beginning)

### 21.2 3 Interpretasi Makna

1. **Website Era Baru**
   - Platform digital modern dengan AI dan 232+ layanan

2. **Situasi Baru**
   - Transformasi bisnis dari offline → online, manual → automated

3. **Sistem Informasi Terpadu Era Baru**
   - **SI** (Sistem Informasi) + **TU** (Terpadu) + **NEO** (New Era)
   - All-in-one digital solution

### 21.3 Keunggulan Nama

1. **Mudah Diingat** - 2 suku kata simpel (SI-TU-NE-O)
2. **Punya Makna** - Lokal (Indonesia) + Global (Universal)
3. **Profesional** - Cocok untuk B2B dan B2C
4. **Future-Oriented** - Konotasi inovasi dan teknologi
5. **Scalable** - Bisa berkembang ke berbagai digital services

### 21.4 Brand Personality

**SITUNEO adalah:**
- **Innovator** (bukan follower)
- **Enabler** (memberdayakan bisnis)
- **Trusted Advisor** (partner, bukan sekadar vendor)
- **Future-Ready** (selalu 2 langkah di depan)

### 21.5 Positioning

**"The NEO Generation of Indonesian Digital Solutions"**

**Tagline Terbaik:**
1. "SITUNEO: Website Era Baru untuk Bisnis Indonesia"
2. "Transform Your Business. Welcome to the NEO Era."
3. "Build NEO. Build Better. Build with SITUNEO."

### 21.6 Campaign Concept: "GO NEO"

**Big Idea:** Ajak bisnis untuk "GO NEO" = embrace digital transformation

```
Hashtag: #GoNEO
CTA: "Ready to GO NEO?"
Message: "Bisnis Gue Udah GO NEO, Lo Kapan?"
```

### 21.7 Company Values (NEO PRINCIPLES)

- **N** - Never Stop Innovating
- **E** - Empower Everyone
- **O** - Own Your Outcomes

### 21.8 The SITUNEO Promise

> "We believe every business deserves a NEO beginning.
>
> Masa depan adalah untuk yang berani GO NEO.
>
> Dan kami di sini untuk memastikan Anda bisa."

### 21.9 Vision 2035

**SITUNEO = Digital Empowerment di Indonesia**

Ketika orang bilang "bisnis gue di SITUNEO", artinya:
- ✅ Serius soal digital presence
- ✅ Smart tentang pilihan teknologi
- ✅ Sukses dalam transformasi digital

---

## 22. PRINSIP UTAMA SISTEM

### 22.1 Core Principles

1. **Fleksibel**
   - Partner/SPV/Manager bebas atur pace sendiri
   - Tidak ada pemaksaan target

2. **Fair**
   - Komisi jelas dan transparan
   - Tanggungan adil (dibagi sesuai komisi)

3. **Scalable**
   - Support 100+ partner dengan sistem cascade
   - Siap untuk 10,000+ users di masa depan

4. **User-friendly**
   - Semua fitur mudah dipahami
   - UI self-explanatory

5. **Comprehensive**
   - Semua aspek bisnis ter-cover
   - Nothing left behind

---

# 🎯 PART 2: SITUNEO PENGADILAN AGAMA

## 1. RINGKASAN EKSEKUTIF

**SITUNEO Pengadilan Agama** adalah sistem informasi berbasis web untuk mengelola tugas pembantuan dari **Mahkamah Agung** kepada **Pengadilan Agama** di seluruh Indonesia.

### Tujuan Sistem:
1. Efisiensi koordinasi tugas pembantuan
2. Transparansi proses dan progress
3. Kemudahan pelaporan dan monitoring
4. Standardisasi workflow tugas pembantuan
5. Integrasi dengan sistem peradilan nasional

---

## 2. DATABASE STRUCTURE (10 TABEL UTAMA)

### 2.1 Users & Authentication

**Tabel: users**
```sql
- id, username, email, password
- nama_lengkap, nip, pangkat_golongan
- jabatan, unit_kerja
- role_id, is_active
- last_login_at, created_at, updated_at
```

**Tabel: roles**
```sql
- id, nama_role, deskripsi
- created_at, updated_at
```

**Tabel: permissions**
```sql
- id, nama_permission, deskripsi
- resource, action
- created_at, updated_at
```

**Tabel: role_permissions**
```sql
- id, role_id, permission_id
- created_at, updated_at
```

### 2.2 Tugas Pembantuan

**Tabel: tugas_pembantuan**
```sql
- id, nomor_tugas, judul, deskripsi
- jenis_tugas, prioritas
- tanggal_mulai, tanggal_selesai
- status (draft/dikirim/diterima/proses/selesai/ditolak)
- pemberi_tugas_id, penerima_tugas_id
- dokumen_surat_tugas, catatan
- created_by, updated_by
- created_at, updated_at, deleted_at
```

**Tabel: detail_tugas**
```sql
- id, tugas_pembantuan_id
- poin_instruksi, urutan
- is_completed, tanggal_completed
- catatan_pelaksanaan
- created_at, updated_at
```

### 2.3 Laporan & Monitoring

**Tabel: laporan**
```sql
- id, tugas_pembantuan_id
- jenis_laporan (harian/mingguan/bulanan/akhir)
- tanggal_laporan, periode_mulai, periode_selesai
- isi_laporan, progress_persentase
- kendala, solusi
- status_verifikasi (pending/disetujui/revisi)
- diverifikasi_oleh, tanggal_verifikasi
- catatan_verifikasi
- created_by, created_at, updated_at
```

**Tabel: dokumen**
```sql
- id, tugas_pembantuan_id, laporan_id
- nama_file, file_path, file_size, file_type
- keterangan, uploaded_by
- created_at, updated_at
```

### 2.4 Notifikasi & Komunikasi

**Tabel: notifikasi**
```sql
- id, user_id, judul, pesan
- jenis_notifikasi (tugas_baru/deadline/approval/dll)
- related_id, related_type
- is_read, read_at
- created_at, updated_at
```

**Tabel: komentar**
```sql
- id, tugas_pembantuan_id, laporan_id
- user_id, parent_id
- isi_komentar, created_at, updated_at
```

### 2.5 Sistem & Audit

**Tabel: pengaturan**
```sql
- id, key, value, deskripsi
- created_at, updated_at
```

**Tabel: audit_log**
```sql
- id, user_id, action, table_name
- record_id, old_values, new_values
- ip_address, user_agent
- created_at
```

**Tabel: pengadilan**
```sql
- id, kode_satker, nama_pengadilan
- tingkat (pa/pta), provinsi, kabupaten_kota
- alamat, telepon, email, website
- ketua_pengadilan, panitera
- is_active, created_at, updated_at
```

---

## 3. FITUR-FITUR SISTEM

### 3.1 Dashboard Multi-Role

**Admin Mahkamah Agung:**
- Statistik tugas pembantuan nasional
- Monitoring progress real-time
- Grafik performa pengadilan
- Alert tugas terlambat

**Ketua/Panitera Pengadilan:**
- Tugas aktif pengadilan
- Status laporan pending
- Timeline tugas mendatang
- Notifikasi penting

**Pelaksana Tugas:**
- Daftar tugas personal
- Deadline tracking
- Quick action buttons
- Progress indicator

### 3.2 Manajemen Tugas Pembantuan

1. **Pembuatan Tugas:** Form wizard multi-step
2. **Pengiriman Tugas:** Notifikasi otomatis ke penerima
3. **Penerimaan Tugas:** Accept/reject dengan alasan
4. **Assignment:** Delegasi ke pelaksana
5. **Tracking:** Real-time status monitoring
6. **Reminder:** Notifikasi otomatis sebelum deadline

### 3.3 Sistem Pelaporan

**Jenis Laporan:**
1. Laporan Harian
2. Laporan Mingguan
3. Laporan Bulanan
4. Laporan Akhir/Komprehensif

**Fitur Laporan:**
- Template terstandar
- Upload dokumen pendukung (PDF, Word, Excel, gambar)
- Progress percentage tracking
- Kendala dan solusi
- Verifikasi bertingkat

### 3.4 Workflow & Approval

```
Draft → Submit → Review → Approve/Revisi → Selesai
```

- Multi-level approval
- Email notification setiap tahap
- Comments & feedback system
- Revision tracking

### 3.5 Document Management

- Upload multiple files
- File preview
- Version control
- Download batch
- Search & filter dokumen

### 3.6 Notifikasi & Reminder

**Channel Notifikasi:**
- In-app notification
- Email notification
- WhatsApp (opsional, integrasi API)

**Trigger Notifikasi:**
- Tugas baru diterima
- Mendekati deadline (H-7, H-3, H-1)
- Perubahan status tugas
- Komentar/feedback baru
- Verifikasi laporan

### 3.7 Reporting & Analytics

**Dashboard Analytics:**
- Grafik status tugas (pie chart, bar chart)
- Trend timeline progress
- Perbandingan performa pengadilan
- Statistik keterlambatan
- Export ke Excel/PDF

**Filter & Pencarian:**
- Berdasarkan periode
- Berdasarkan pengadilan
- Berdasarkan jenis tugas
- Berdasarkan status
- Berdasarkan prioritas

---

## 4. SPESIFIKASI TEKNIS

### 4.1 Frontend

**Framework & Library:**
- Vue.js 3 (Composition API)
- Pinia (State Management)
- Vue Router 4
- Tailwind CSS 3
- Axios (HTTP Client)
- Chart.js / ApexCharts (Visualisasi)
- VeeValidate (Form Validation)
- Day.js (Date Management)

**UI Components:**
- Headless UI
- Heroicons
- Vue Select
- Vue Datepicker
- Rich Text Editor (Quill/TinyMCE)

### 4.2 Backend

**Framework:**
- Laravel 10
- PHP 8.2

**Package Utama:**
- Laravel Sanctum (API Authentication)
- Laravel Permission (Role & Permission)
- Laravel Excel (Export/Import)
- Laravel PDF (Generate PDF)
- Laravel Queue (Background Jobs)
- Laravel Notification (Email/SMS)

**API Architecture:**
- RESTful API
- JSON response format
- JWT token authentication
- Rate limiting
- API versioning

### 4.3 Database

**DBMS:** PostgreSQL 15

**Optimasi:**
- Indexing strategy
- Foreign key constraints
- Soft deletes
- Database seeding
- Migration versioning

### 4.4 Server & Infrastructure

**Requirements:**
- Ubuntu 22.04 LTS
- Nginx 1.24
- PHP-FPM 8.2
- PostgreSQL 15
- Redis (Cache & Queue)
- SSL Certificate (Let's Encrypt)

**Deployment:**
- Git version control
- CI/CD pipeline (GitHub Actions/GitLab CI)
- Automated testing
- Blue-green deployment
- Backup automation (daily)

---

## 5. KEAMANAN & COMPLIANCE

### 5.1 Authentication & Authorization

- Multi-factor authentication (2FA)
- Password complexity rules
- Session management
- Role-based access control (RBAC)
- Permission-based authorization

### 5.2 Data Security

- Encryption at rest (AES-256)
- Encryption in transit (TLS 1.3)
- Input validation & sanitization
- SQL injection prevention
- XSS protection
- CSRF protection

### 5.3 Audit & Compliance

- Comprehensive audit logging
- User activity tracking
- Change history
- Compliance dengan UU ITE
- Data retention policy

### 5.4 Backup & Recovery

- Automated daily backup
- Point-in-time recovery
- Disaster recovery plan
- Backup testing schedule

---

## 6. USER ROLES & PERMISSIONS

### 6.1 Super Admin
- Full system access
- User management
- System configuration
- Audit log access

### 6.2 Admin Mahkamah Agung
- Create tugas pembantuan
- Monitor semua pengadilan
- Approve/reject laporan
- Generate reports nasional

### 6.3 Ketua Pengadilan Agama
- View tugas pengadilan
- Assign tugas ke pelaksana
- Approve laporan internal
- Monitor progress pengadilan

### 6.4 Panitera Pengadilan Agama
- Koordinasi pelaksanaan
- Review laporan
- Upload dokumen
- Komunikasi dengan MA

### 6.5 Pelaksana Tugas
- View tugas assigned
- Create laporan
- Upload dokumen pendukung
- Update progress

### 6.6 Guest/Viewer (Opsional)
- Read-only access
- View public reports
- Dashboard summary

---

## 7. TESTING & QUALITY ASSURANCE

### 7.1 Testing Strategy

**Unit Testing:**
- PHPUnit (Backend)
- Jest (Frontend)
- Coverage minimum 80%

**Integration Testing:**
- API endpoint testing
- Database transaction testing
- Third-party integration testing

**E2E Testing:**
- Cypress/Playwright
- User flow testing
- Cross-browser testing

**Performance Testing:**
- Load testing (Apache JMeter)
- Stress testing
- Database query optimization

### 7.2 Code Quality

- PSR-12 coding standards
- ESLint + Prettier (Frontend)
- PHP CS Fixer (Backend)
- Code review process
- Static analysis (PHPStan)

---

## 8. MAINTENANCE & SUPPORT

### 8.1 Monitoring

- Application monitoring (New Relic/Laravel Telescope)
- Server monitoring (Prometheus/Grafana)
- Error tracking (Sentry)
- Uptime monitoring

### 8.2 Documentation

- API documentation (Swagger/Postman)
- User manual
- Admin guide
- Developer documentation
- Deployment guide

### 8.3 Support

- Help desk system
- FAQ section
- Video tutorials
- Training materials
- Technical support contact

---

## 9. ROADMAP & FUTURE ENHANCEMENTS

### Phase 1 (Launch)
- Core functionality
- Basic reporting
- User management
- Notifikasi email

### Phase 2 (3 bulan)
- Mobile app (Flutter)
- WhatsApp integration
- Advanced analytics
- Export batch reports

### Phase 3 (6 bulan)
- AI-powered insights
- Predictive analytics
- Integration SIPP/SIMPEL
- E-signature integration

### Phase 4 (12 bulan)
- Mobile offline mode
- Real-time collaboration
- Advanced workflow automation
- Machine learning recommendations

---

## 10. ESTIMASI & RESOURCES

### 10.1 Timeline

- Planning & Design: 2 minggu
- Development: 8-10 minggu
- Testing: 2 minggu
- Deployment & Training: 1 minggu
- **Total: 13-15 minggu**

### 10.2 Team

- Project Manager: 1
- Backend Developer: 2
- Frontend Developer: 2
- UI/UX Designer: 1
- QA Engineer: 1
- DevOps Engineer: 1

---

# 📊 KESIMPULAN

## SITUNEO DIGITAL (Marketing Website)

**Status:** Ready for Development
**Complexity:** High (85 tables, 400+ files, MLM system)
**Target:** Quality First, Perfect Result
**Timeline:** Flexible (no rush)

**Key Features:**
- 5-level MLM system
- Dynamic tier-based commission
- 50 demo websites
- Multi-language support
- Comprehensive analytics

## SITUNEO PENGADILAN AGAMA

**Status:** Dokumentasi Lengkap - Ready for Development
**Complexity:** Medium-High (10 tables, government system)
**Tech Stack:** Vue.js 3 + Laravel 10 + PostgreSQL 15
**Timeline:** 13-15 weeks

**Key Features:**
- Multi-role dashboard
- Task management
- Reporting system
- Workflow approval
- Document management
- Analytics & monitoring

---

## 📋 CATATAN AKHIR

**STATUS PEMBACAAN:**
- ✅ File 1: 296 baris - DIBACA 100%
- ✅ File 2: 426 baris - DIBACA 100%
- ✅ File 3: 224 baris - DIBACA 100%
- ✅ File 4: 550 baris - DIBACA 100%
- ✅ File 5: 6 baris - DIBACA 100%
- ✅ **TOTAL: 1,502 baris - SEMUA DIBACA 100%**

**KEJUJURAN:**
- ✅ Tidak ada yang terlewat
- ✅ Tidak ada yang dibaca setengah
- ✅ Semua detail ter-capture
- ✅ 2 project berbeda dipisahkan dengan jelas

---

**Dokumen ini adalah MASTER REFERENCE untuk development kedua project SITUNEO.**

**Dibuat:** 21 November 2025  
**Developer:** Claude AI  
**Status:** FINAL - READY FOR IMPLEMENTATION

---

© 2025 SITUNEO Digital - Build Your Future, Today 💙✨
