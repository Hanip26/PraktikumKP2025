# 🎬 Responsi 2 – Simulasi Netflix 

Halo, tim pejuang C! 💻
Buat program simulasi layanan streaming ala Netflix berbasis C. Pengguna bisa menambahkan video, membuat watchlist, memutar & menghentikan (simulasi) video, dan mengelola daftar tontonan.

---

## 📘 Informasi Umum

<br>**Jenis Penugasan:** Tugas Projek </br>
**Pengerjaan:** Kelompok
<br>**Durasi:** 2 Minggu</br>

## 🧩 Spesifikasi Teknis

**1) Struktur Data**
Buat minimal 2 struktur:
- Video: judul, kategori, durasiMenit, rating (0–10)
- Watchlist: namaDaftar, koleksi Video[] + penghitung elemen
<br>Contoh deklarasi (boleh dimodifikasi):</br>
```
#define MAX_VID  300
#define MAX_WL   50
#define TITLE_SZ 64
#define CAT_SZ   24

typedef struct {
    char  title[TITLE_SZ];
    char  category[CAT_SZ];
    int   duration;     // menit
    float rating;       // 0.0 - 10.0
} Video;

typedef struct {
    char   name[32];
    int    count;
    int    videoIdx[MAX_VID]; // indeks ke daftar video global
} Watchlist;
```

**2) Fitur Wajib**
- Tambah video baru ke koleksi.
- Buat watchlist baru dan tambahkan video ke dalamnya.
- Tampilkan semua video: judul, kategori, durasi, rating.
- Pilih video dari watchlist lalu putar (simulasi) dan tampilkan info yang sedang ditonton.
- Hentikan simulasi pemutaran.
- Kelola watchlist: ubah nama, hapus video dari watchlist, hapus watchlist.

**3) Bonus (opsional)**
- Riwayat tontonan (history) pengguna.
- Pencarian video (berdasarkan judul/kategori).
- Beri rating setelah menonton (memperbarui rating rata-rata).
Gunakan materi wajib praktikum: pemilihan (if/else atau switch), perulangan (for/while/do…while), fungsi buatan sendiri (di luar main), dan array non-string (mis. array Video, array indeks).

---

## 🖥️ Antarmuka & Alur (contoh sederhana)

Menu utama (contoh):
```
1. Tambah Video
2. Buat Watchlist
3. Tambah Video ke Watchlist
4. Lihat Semua Video
5. Lihat & Putar dari Watchlist
6. Hentikan Pemutaran
7. Kelola Watchlist (edit/hapus)
8. Pencarian (Bonus)
9. Riwayat (Bonus)
0. Keluar
```
---

## 🧪 Build & Run

Kompilasi (contoh GNU GCC):
```
gcc -O2 -Wall -Wextra -o netflix main.c
./netflix
```

Struktur proyek yang disarankan:
```
📦 Responsi2_Kelompok1
 ┣ 📜 main.c
 ┣ 📜 video.h / watchlist.h (opsional)
 ┣ 📜 utils.c (opsional)
 ┣ 📄 Dokumentasi_Responsi2.pdf
 ┗ 📜 README.md
```

---

## 🧮 Bobot Penilaian

| **Aspek**	| **Bobot** |
| --------- | --------- |
| Pengumpulan tugas	| 10% |
| Bebas dari error	| 20% |
| Relevansi dengan instruksi tugas	| 40% |
| Kreativitas & kelengkapan fitur	| 30% |

---

## 📄 Dokumentasi (PDF)

Sertakan:
1. Judul & Deskripsi program
2. Daftar fitur (tandai mana yang wajib/bonus, sertakan screenshot terminal bila ada)
3. Petunjuk penggunaan (cara build & run, contoh alur menu)
4. Kode program (rapi, diberi komentar singkat)
5. Tantangan & solusi (bug, desain array, validasi input, dsb.)

---

## 📦 Format Pengumpulan

- Isi .zip:
1. Source code C (*.c, plus header jika ada)
2. Dokumentasi PDF (*.pdf)
- Nama file zip: Responsi2_KelompokX.zip
  Contoh: Responsi2_Kelompok1.zip

---

## 🌟 Tips Singkat Supaya Sukses

- Rancang menu & alur data dulu, baru koding.
- Pecah logika ke fungsi-fungsi kecil agar rapi.
- Validasi input (batas indeks, kapasitas array).
- Uji semua fitur minimal 1× sebelum submit.
- Tambahkan komentar pendek di fungsi penting.

## 💬 Kontak

Pertanyaan? Silakan hubungi **asprak** atau diskusi di **grup kelas**.  
Semangat coding! 🚀
