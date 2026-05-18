# 🎤 Caraoke

Tampilkan lirik lagu tersinkron di layar Android Auto — tanpa ganti app musik kamu.
<img width="791" height="477" alt="Screenshot 2026-05-19 at 02 34 37" src="https://github.com/user-attachments/assets/1d5af066-9fff-4958-b620-4806ae9715e6" />


Putar lagu seperti biasa di Spotify atau YouTube Music. Caraoke baca lagunya, 
ambil lirik tersinkron, lalu tampilkan di head unit mobil kamu. 
Tinggal nyanyi.

---

## Download

Cek [Releases](https://github.com/dev-flihh/caraoke/releases) 
untuk download APK versi terbaru.

> Caraoke masih dalam tahap awal. Feedback sangat welcome.

---

## Cara Kerja

1. Setel lagu di Spotify / YouTube Music seperti biasa
2. Caraoke baca lagu yang sedang diputar dari media notification HP
3. Lirik tersinkron muncul di layar Android Auto, mengikuti posisi lagu

Audio tetap dari app musik kamu. Caraoke hanya mengurus liriknya.

---

## Prasyarat

- Android phone
- Android Auto (terpasang di HP)
- Head unit mobil yang support Android Auto
- Aplikasi musik yang menyediakan media notification Android 
  (Spotify, YouTube Music, dll)
- Koneksi internet (untuk ambil lirik dari LRCLIB)

---

## Setup Awal (Satu Kali)

**1. Install APK**
Download dari halaman Releases, aktifkan "Install from unknown sources" 
di HP kamu, lalu install.

**2. Buka Caraoke, izinkan Notification Access**
Caraoke butuh akses ini untuk membaca lagu yang sedang diputar — 
bukan untuk membaca chat atau notifikasi pribadi.

**3. Aktifkan Android Auto Developer Mode**
Buka Android Auto → tap "Version" beberapa kali sampai 
developer settings aktif → aktifkan "Unknown sources".

**4. Hubungkan ke Mobil**
Sambungkan HP ke head unit, buka launcher Android Auto, 
pilih Caraoke. Putar lagu — lirik akan muncul.

---

## Keterbatasan Saat Ini

- Hanya support Android Auto (bukan Apple CarPlay)
- Ketersediaan lirik bergantung pada database [LRCLIB](https://lrclib.net)
- Jika lagu tidak ditemukan di LRCLIB, akan muncul "Lyrics not found"
- Belum tersedia di Google Play Store

---

## Lirik dari LRCLIB

Caraoke mengambil lirik dari [LRCLIB](https://lrclib.net) — 
layanan lirik tersinkron open source. Terima kasih buat komunitas 
yang sudah berkontribusi ke database-nya.

---

## Feedback & Bug Report

Buka [Issues](https://github.com/[username]/caraoke/issues) 
kalau menemukan bug atau punya saran.
