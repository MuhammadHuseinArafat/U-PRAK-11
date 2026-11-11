# Ujian Praktik Informatika (ANBK-Style Exam Platform)

![HTML5](https://img.shields.io/badge/HTML5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

> Platform Ujian Praktik berbasis web modern dengan antarmuka menyerupai **ANBK** (Asesmen Nasional Berbasis Komputer), dilengkapi sistem keamanan ketat (anti-cheat), navigasi soal interaktif, dan manajemen waktu otomatis. Didesain khusus untuk mata pelajaran Informatika dengan skema warna **Hijau Tosca** dan **Cokelat Muda**.

---

## 🚀 Fitur Utama

### 1. 🖥️ Antarmuka Gaya ANBK
* **Halaman Login Modern:** Desain dua kolom dengan ilustrasi komputer interaktif, input dengan ikon, dan corak batik halus di latar belakang.
* **Layout Ujian Terstruktur:** Panel informasi siswa dan sisa waktu di bagian atas, area soal di sebelah kiri, serta kotak navigasi nomor soal di sebelah kanan.
* **Indikator Status:** Warna nomor soal berubah menjadi Hijau (selesai dikerjakan) atau Abu-abu (belum dikerjakan).

### 2. 🛡️ Sistem Keamanan Ketat (Anti-Cheat)
* **Deteksi Pelanggaran Lapis Tiga:** Mendeteksi peserta yang berpindah tab (*visibilitychange*), keluar dari mode layar penuh (*fullscreenchange*), atau kehilangan fokus jendela (*window blur*).
* **Sistem 3 Strikes:** Peserta diberikan peringatan pada pelanggaran ke-1 dan ke-2. Pada pelanggaran ke-3, layar ujian akan terkunci total (*Lockdown*).
* **Buka Kunci Pengawas:** Layar terkunci hanya dapat dibuka kembali dengan memasukkan password khusus guru (`MSRF04`).
* **Proteksi Tambahan:** Pencegahan klik kanan, *Inspect Element*, dan kombinasi tombol pintasan *Developer Tools* (F12 / Ctrl+Shift+I).

### 3. ✨ Aksesibilitas & Interaktivitas
* **Toggle Password (Ikon Mata):** Memungkinkan siswa melihat token ujian atau password pengawas yang sedang mereka ketik.
* **Tombol 3D Interaktif:** Seluruh tombol dilengkapi efek timbul (*shadow depth*), animasi *hover* mengambang, dan efek tekan saat diklik.
* **Validasi Penyelesaian:** Tombol "Hentikan Ujian" mewajibkan siswa untuk mencentang *checkbox* tanda selesai pada seluruh soal terlebih dahulu.

### 4. ⏱️ Manajemen Waktu & Sesi
* **Timer Mundur 80 Menit:** Waktu berjalan otomatis dengan perubahan warna menjadi merah menyala saat waktu menipis (sisa < 5 menit).
* **Reset & Rotasi Token:** Token ujian otomatis berganti dinamis dari `U-INF-11` (sesi awal) menjadi `INF-11` setelah peserta mengakhiri ujian dan kembali ke halaman login.

---

## 🛠️ Teknologi yang Digunakan
* **HTML5:** Struktur semantik modular.
* **CSS3:** Custom Properties, Flexbox/Grid layout, Responsive design, SVG inline background.
* **JavaScript (Vanilla ES6+):** DOM Manipulation, State Management, Fullscreen API, Timer intervals.

---

## 📁 Struktur Berkas
Menggunakan pendekatan *Single-File Architecture*, seluruh aplikasi (tampilan, gaya, dan kumpulan soal) diringkas ke dalam satu file agar sangat mudah dijalankan tanpa konfigurasi server tambahan:

```text
📁 ujian-praktik-informatika/
│
├── index.html       # Berkas utama (HTML + CSS + JavaScript terintegrasi)
└── README.md        # Dokumentasi resmi repositori
```

---

## ⚙️ Cara Menjalankan Aplikasi

1. **Clone repositori ini** atau unduh file `index.html`:
   ```bash
   git clone https://github.com/username/ujian-praktik-informatika.git
   ```
2. Pastikan file tersimpan dengan nama `index.html`.
3. Buka file tersebut menggunakan **browser modern** (Google Chrome, Microsoft Edge, Mozilla Firefox, atau Safari). 
4. *Catatan:* Aplikasi ini murni berjalan di sisi klien (*client-side*), sehingga tidak memerlukan instalasi Node.js, PHP, ataupun database lokal.

---
---

## 📝 Daftar Soal Ujian (Informatika Bab 3)

Secara *default*, platform ini memuat 7 studi kasus Ujian Praktik berdasarkan materi Bab 3:

1. **Analisis Kelemahan Greedy & Penerapan Memoisasi** (Skor: 20)
2. **Logika Struktur Data Matriks / Array 2D** (Skor: 20)
3. **Analisis Manipulasi String** (Skor: 10)
4. **Manipulasi Larik / Array 1D** (Skor: 10)
5. **Analisis Pohon Rekursi** (Skor: 10)
6. **Studi Kasus OSN: Labirin Koin Emas (Maximum Path Sum)** (Skor: 10)
7. **Studi Kasus OSN: Pak Dengklek & Panen Durian (0/1 Knapsack)** (Skor: 10)

*Tips: Anda dapat mengubah teks soal, menambah, atau mengurangi butir soal dengan mengedit variabel array `soalData` di dalam tag `<script>` pada berkas `index.html`.*

---

## 👤 Pembuat

© 2026 **Muhammad Husein Arafat**. All Rights Reserved.
