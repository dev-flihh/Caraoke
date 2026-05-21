# 🎤 Caraoke
# Caraoke di Head Unit Mobil: Lirik Tersinkron, Langsung di Layar Dashboard

> Caraoke menghadirkan karaoke serius ke dalam pengalaman berkendara — menampilkan lirik real-time di Android Auto tanpa menggantikan aplikasi musik yang sudah kamu pakai.

<img 
  width="320" 
  alt="Screenshot Caraoke di Android Auto head unit - halaman awal" 
  src="https://github.com/user-attachments/assets/8430cdc6-acfe-40b1-a701-f515e3517b6f" 
/>

<img 
  width="320" 
  alt="Screenshot Caraoke di Android Auto head unit - lirik tersinkron" 
  src="https://github.com/user-attachments/assets/9ff42fae-d591-450d-8fbb-3d49720179d4" 
/>

**Platform:** Android 8.0+ · Android Auto  
**Versi panduan ini:** Caraoke v0.1.7  
**Sumber APK resmi:** [github.com/dev-flihh/caraoke/releases](https://github.com/dev-flihh/caraoke/releases)

---

## Daftar Isi

- [Cara Kerja Caraoke](#cara-kerja-caraoke)
- [Kenapa Instalasi Manual?](#kenapa-instalasi-manual)
- [1 · Download APK](#1--download-apk)
- [2 · Install APK di HP](#2--install-apk-di-hp)
- [3 · Konfigurasi Izin di HP](#3--konfigurasi-izin-di-hp)
- [4 · Aktifkan di Android Auto](#4--aktifkan-di-android-auto)
- [5 · Buka Caraoke di Head Unit](#5--buka-caraoke-di-head-unit)
- [Batasan yang Perlu Diketahui](#batasan-yang-perlu-diketahui)
- [Checklist Sebelum ke Mobil](#checklist-sebelum-ke-mobil)
- [Troubleshooting](#troubleshooting)
- [Kenapa Tidak Bisa di iPhone?](#kenapa-tidak-bisa-di-iphone)

---

## Cara Kerja Caraoke

Caraoke **bukan** pemutar musik. Musik tetap berjalan dari aplikasi yang biasa dipakai — YouTube Music, Spotify, atau lainnya. Caraoke hanya membaca info lagu dari sistem Android, mencari lirik tersinkron, lalu menampilkannya di layar head unit.

```
App musik putar lagu
       ↓
Notifikasi musik muncul di HP
       ↓
Caraoke baca info lagu (judul, artist)
       ↓
Caraoke cari lirik di LRCLIB (online)
       ↓
Lirik tampil tersinkron di Android Auto
```

---

## Kenapa Instalasi Manual?

Caraoke belum tersedia di Google Play Store dan didistribusikan sebagai APK dari GitHub Releases. Karena itu:

- Android akan meminta izin tambahan untuk install dari sumber tidak dikenal
- Android Auto perlu diaktifkan mode developernya agar bisa menampilkan app yang diinstall manual
- Prosesnya sedikit lebih panjang dari install Play Store biasa, tapi semuanya normal dan aman selama APK diambil dari repo resmi

> ⚠️ **Penting:** Hanya download APK dari `github.com/dev-flihh/caraoke/releases`. Jangan install dari sumber lain meskipun tampilannya mirip.

---

## 1 · Download APK

1. Buka halaman release resmi:  
   👉 [https://github.com/dev-flihh/caraoke/releases](https://github.com/dev-flihh/caraoke/releases)
2. Pilih release terbaru yang tersedia
3. Di bagian **Assets**, cari dan tap file dengan akhiran `.apk` — misalnya `caraoke-v0.1.7.apk`
4. Jika browser memperingatkan bahwa file APK berpotensi berbahaya, itu perilaku normal sistem Android. Selama URL berasal dari repo resmi `dev-flihh/caraoke`, lanjutkan download

---

## 2 · Install APK di HP

1. Buka notifikasi download, app **Files**, atau folder **Download**
2. Tap file `caraoke-...apk`
3. Tap **Install** jika tombolnya muncul langsung
4. Tunggu proses instalasi selesai
5. Tap **Open** untuk membuka Caraoke

### Jika Android menolak karena sumber tidak dikenal

Android akan menampilkan pesan seperti:  
*"For your security, your phone is not allowed to install unknown apps from this source"*

Langkah mengatasinya:

1. Tap **Settings** atau **Setelan** pada pesan tersebut
2. Aktifkan **Allow from this source** untuk app yang dipakai membuka APK (Chrome, Files, Drive, dll.)
3. Kembali ke file APK
4. Tap **Install** lagi

> 💡 **Setelah berhasil install**, matikan kembali izin **Allow from this source**. Izin ini hanya diperlukan saat proses instalasi, bukan untuk pemakaian harian.

### Penyebab umum gagal install

| Penyebab | Solusi |
|----------|--------|
| APK rusak / download tidak selesai | Download ulang, pastikan file selesai terdownload |
| Android terlalu lama | Caraoke membutuhkan minimal Android 8.0 |
| Ada versi Caraoke lain dengan tanda tangan berbeda | Uninstall versi lama dulu, lalu install versi baru |
| Ruang penyimpanan penuh | Bebaskan storage lalu coba lagi |
| HP memakai profil kerja / mode anak | Izin install APK manual mungkin diblokir admin |

---

## 3 · Konfigurasi Izin di HP

Setelah Caraoke terinstall, ada empat pengaturan yang harus dilakukan sebelum app bisa bekerja di mobil.

### Langkah 1 — Buka Caraoke

Buka app **Caraoke** dari launcher HP. Saat pertama dibuka, app akan menampilkan langkah setup awal. Caraoke perlu dibuka minimal sekali agar service-nya siap berjalan di belakang layar.

<img 
  width="280" 
  alt="Screenshot buka Caraoke app pertama kali di HP" 
  src="https://github.com/user-attachments/assets/950c5447-0417-47f1-9b16-373fe86c7fef" 
/>

### Langkah 2 — Izinkan Notifikasi

Di Android 13 ke atas, sistem akan meminta izin notifikasi. Pilih **Allow / Izinkan**.

<img 
  width="280" 
  alt="Screenshot Caraoke notification access setup" 
  src="https://github.com/user-attachments/assets/b55fccb2-38aa-47f8-a6c2-c812d337b5ff" 
/>

Caraoke memakai notifikasi kecil untuk menjaga service-nya tetap aktif. Tanpa ini, Android bisa mematikan prosesnya saat layar HP mati atau saat app tidak dibuka.

### Langkah 3 — Aktifkan Notification Access

1. Di layar Caraoke, tap **Open notification settings**
2. Cari **Caraoke** di daftar
3. Aktifkan akses untuk Caraoke
4. Jika muncul peringatan, pilih **Allow / Izinkan**
5. Kembali ke Caraoke

<img 
  width="300" 
  alt="Screenshot Notification Access settings di Android" 
  src="https://github.com/user-attachments/assets/3b514a72-b8b4-4213-81b5-ec3aae4ce2eb" 
/>

**Mengapa ini penting?**  
Caraoke membaca notifikasi musik (berisi judul lagu, artist, dan status pemutaran) untuk mengetahui lagu apa yang sedang berjalan. Tanpa akses ini, Caraoke tidak tahu lirik apa yang harus dicari.

### Langkah 4 — Putar Musik dari App Favorit

1. Buka YouTube Music, Spotify, atau aplikasi musik lain
2. Putar sebuah lagu

<img 
  width="280" 
  alt="Screenshot aplikasi musik dijalankan di HP" 
  src="https://github.com/user-attachments/assets/ff856ed0-4be9-4e9f-bfb2-9d6049fed33f" 
/>

3. Pastikan notifikasi musik muncul di HP

<img 
  width="320" 
  alt="Screenshot notifikasi musik di status bar HP" 
  src="https://github.com/user-attachments/assets/34100ad0-5045-4cfd-bbad-b50dc54c6807" 
/>

4. Kembali ke Caraoke

Caraoke mengikuti aplikasi musik lain — bukan memutar sendiri — jadi musik harus aktif agar ada data lagu yang bisa diproses.

---

## 4 · Aktifkan di Android Auto

### Langkah 1 — Aktifkan Developer Mode

**Opsi A:** Buka aplikasi Caraoke dan klik **Open Android Auto**

<img 
  width="280" 
  alt="Screenshot shortcut Open Android Auto di Caraoke app" 
  src="https://github.com/user-attachments/assets/75721971-83e4-456f-a5c3-230e9e334239" 
/>

**Opsi B:** Atau buka melalui Settings HP:

1. Buka **Settings** di HP
2. Cari dan buka **Android Auto**

<img 
  width="280" 
  alt="Screenshot membuka pengaturan Android Auto" 
  src="https://github.com/user-attachments/assets/1d85e602-bec1-4b70-a388-6af1ad343628" 
/>

3. Scroll ke bagian **Version**

<img 
  width="280" 
  alt="Screenshot menu version di Android Auto settings" 
  src="https://github.com/user-attachments/assets/a7cf5acc-cf08-4ef6-91c6-a8bb2f20ac49" 
/>

4. Tap **Version** sekitar 10 kali hingga muncul pesan bahwa Developer Settings aktif. Tap **Ok**

<img 
  width="280" 
  alt="Screenshot pesan Developer Settings berhasil diaktifkan" 
  src="https://github.com/user-attachments/assets/1a643b1b-dd75-4ec2-9527-1f700ffeb729" 
/>

5. Tap menu **titik tiga** di kanan atas
6. Buka **Developer settings**

<img 
  width="280" 
  alt="Screenshot menu Developer settings di Android Auto" 
  src="https://github.com/user-attachments/assets/b13665a8-3535-44d3-ae60-86d8f1c1969e" 
/>

7. Aktifkan **Unknown sources**

<img 
  width="320" 
  alt="Screenshot Unknown sources toggle di Developer Settings" 
  src="https://github.com/user-attachments/assets/37e21c7e-002f-4779-b66d-51a6e4ccc729" 
/>

Android Auto tidak otomatis menampilkan semua aplikasi yang diinstall manual. `Unknown sources` memberi izin ke Android Auto untuk menampilkan app seperti Caraoke.

### Langkah 2 — Tambahkan Caraoke ke Launcher

1. Masih di pengaturan Android Auto, buka **Customize launcher**

<img 
  width="320" 
  alt="Screenshot membuka Customize launcher di Android Auto" 
  src="https://github.com/user-attachments/assets/da986342-1992-4fea-bf88-675a04ad07a2" 
/>

2. Cari **Caraoke**
3. Centang atau aktifkan Caraoke

<img 
  width="320" 
  alt="Screenshot mengaktifkan Caraoke di Customize launcher" 
  src="https://github.com/user-attachments/assets/4e25b0c4-9e58-45d3-95bc-3426b8131684" 
/>

4. Jika belum muncul, cabut lalu sambungkan ulang Android Auto, atau restart HP

---

## 5 · Buka Caraoke di Head Unit

1. Pastikan semua setup di HP sudah selesai
2. Sambungkan HP ke mobil via kabel USB atau Android Auto wireless
3. Tunggu Android Auto muncul di head unit
4. Putar lagu dari app musik di HP
5. Buka app launcher di Android Auto
6. Pilih **Caraoke**

<img 
  width="320" 
  alt="Screenshot memilih Caraoke di Android Auto launcher" 
  src="https://github.com/user-attachments/assets/5121c48b-e955-4d18-b5b7-888b6b1ded46" 
/>

7. Lirik akan tampil mengikuti lagu yang sedang diputar

<img 
  width="320" 
  alt="Screenshot Caraoke menampilkan lirik di head unit" 
  src="https://github.com/user-attachments/assets/8430cdc6-acfe-40b1-a701-f515e3517b6f" 
/>

---

## Batasan yang Perlu Diketahui

- **Bukan untuk iPhone / CarPlay.** Caraoke dibuat khusus untuk Android. APK tidak bisa diinstall atau dijalankan di iPhone.
- **Butuh koneksi internet.** Lirik diambil secara online dari LRCLIB. Tanpa koneksi, lirik tidak akan muncul.
- **Tidak semua lagu punya lirik.** Hanya lagu dengan lirik tersinkron yang tersedia di LRCLIB yang bisa ditampilkan.
- **Head unit standalone.** Head unit Android standalone tanpa Android Auto mungkin menampilkan Caraoke sebagai app Android biasa, bukan tampilan Android Auto.
- **Android minimum 8.0.** Versi Android di bawahnya tidak didukung.
- **Kebijakan sideload ke depan.** Mulai September 2026, beberapa wilayah akan mulai mewajibkan verifikasi developer tambahan untuk install APK manual di perangkat Android tersertifikasi.

---

## Checklist Sebelum ke Mobil

Pastikan semua poin di bawah sudah selesai sebelum mencoba Caraoke di head unit:

- [ ] APK didownload dari GitHub Releases resmi
- [ ] APK berhasil diinstall di HP
- [ ] Caraoke sudah dibuka minimal sekali
- [ ] Izin notifikasi sudah diizinkan
- [ ] Notification Access untuk Caraoke sudah aktif
- [ ] Lagu sedang diputar dan notifikasi musik muncul
- [ ] Developer Mode Android Auto sudah aktif
- [ ] Unknown sources di Android Auto sudah aktif
- [ ] Caraoke dicentang di Customize launcher
- [ ] HP tersambung ke head unit via Android Auto

---

## Troubleshooting

### Caraoke tidak muncul di Android Auto

- Pastikan **Unknown sources** di Developer settings Android Auto sudah aktif
- Cek **Customize launcher** — pastikan Caraoke dicentang
- Tutup Android Auto dan sambungkan ulang
- Restart HP jika Android Auto belum refresh daftar app
- Pastikan Caraoke sudah dibuka minimal sekali di HP

### Lirik tidak muncul

- Pastikan koneksi internet aktif — Caraoke mengambil lirik dari LRCLIB secara online
- Coba lagu lain; tidak semua lagu punya lirik tersinkron
- Pastikan notifikasi musik muncul di HP saat lagu diputar
- Tunggu beberapa detik setelah lagu berganti

---

## Kenapa Tidak Bisa di iPhone?

Singkatnya: Caraoke dibangun di atas fondasi teknis Android yang tidak ada padanannya di iOS.

### 1. APK tidak bisa diinstall di iPhone

File APK adalah format paket aplikasi milik Android. iPhone menggunakan format `.ipa` dan hanya bisa menginstall aplikasi dari App Store (atau melalui TestFlight untuk beta). Tidak ada cara untuk menjalankan APK di iPhone — ini bukan soal izin atau pengaturan, tapi memang dua sistem yang berbeda sepenuhnya.

### 2. Notification Access tidak ada di iOS

Caraoke mengandalkan **Notification Listener** — fitur Android yang memungkinkan satu app membaca notifikasi dari app lain. Dari situlah Caraoke tahu lagu apa yang sedang diputar: ia membaca notifikasi musik yang berisi judul, artist, dan status pemutaran.

iOS tidak punya sistem seperti ini. Apple tidak mengizinkan satu app membaca notifikasi dari app lain demi alasan privasi. Tanpa akses ini, Caraoke tidak punya cara untuk mengetahui lagu yang sedang berjalan.

### 3. Foreground Service bekerja berbeda di iOS

Di Android, Caraoke berjalan sebagai **foreground service** — proses yang tetap aktif di belakang layar selama HP terhubung ke mobil. iOS punya batasan ketat soal background process: app yang tidak aktif di layar akan ditangguhkan sistemnya dalam hitungan menit. Caraoke tidak bisa terus memantau lagu yang berjalan jika prosesnya bisa dihentikan kapan saja oleh iOS.

### 4. Android Auto dan CarPlay adalah dua ekosistem berbeda

Android Auto adalah platform Google yang hanya berjalan di Android. CarPlay adalah platform Apple yang hanya berjalan di iPhone. Keduanya tidak saling kompatibel — app yang dibuat untuk Android Auto tidak bisa langsung dipakai di CarPlay dan sebaliknya.

Membuat versi CarPlay dari Caraoke bukan sekadar "port" sederhana. Ia membutuhkan pengembangan ulang dari awal menggunakan framework iOS, API CarPlay dari Apple, dan mekanisme berbeda untuk mendeteksi lagu yang sedang diputar — karena semua fondasi teknisnya berbeda.

### Ringkasan

| Fitur yang dibutuhkan Caraoke | Android | iPhone |
|-------------------------------|---------|--------|
| Install APK | ✅ | ❌ |
| Notification Listener (baca notif app lain) | ✅ | ❌ |
| Foreground Service yang stabil | ✅ | ❌ Dibatasi |
| Android Auto | ✅ | ❌ |
| Apple CarPlay | ❌ | ✅ (tapi perlu app berbeda) |

Jika ada permintaan versi CarPlay, itu perlu disampaikan langsung ke developer di repo GitHub sebagai feature request.

---

## Referensi

- [GitHub Releases Caraoke](https://github.com/dev-flihh/caraoke/releases)
- [Android Developer Verification](https://developer.android.com/developer-verification)
- [LRCLIB — Sumber Lirik](https://lrclib.net)
