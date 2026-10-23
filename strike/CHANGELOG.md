# Changelog — Strike Zone

Semua perubahan penting pada game Strike Zone dicatat di sini.
Game: https://zenaki.github.io/Doodle-Shooter/strike/

## v1.14 — 24 Okt 2026
### Diubah
- Semua senjata lama diganti 16 senjata toon (CC0, Quaternius Toon Shooter Game Kit) agar gayanya seragam dengan karakter bot.
### Ditambahkan
- **Pistol (slot 2):** Pistol (bawaan), Revolver Mini, Revolver.
- **Senjata utama (slot 1):** SMG, Shotgun (9 peluru sebar, pompa), Rifle AK, Sniper Ringan (semi-otomatis), Sniper Berat (bolt-action), Short Cannon (sebaran lebar, 2 peluru), Grenade Launcher (meledak saat kena), Rocket Launcher (roket lurus, ledakan besar).
- **Jarak dekat (slot 3):** Pisau (bawaan), Pisau Komando, Sekop. Tusukan dari belakang langsung membunuh; kill jarak dekat memberi $1500.
- **Granat:** Granat Ledak (maks 2) dan Granat Api (maks 1, membakar area ±7 detik). Tombol GRANAT di HP, G di PC.
- Granat memantul di lantai/dinding; ledakan dengan bola api, asap, cahaya, guncangan layar, dan damage berdasarkan jarak (terhalang dinding = aman).
- Bot Penjaga bisa melempar granat ledak/api; peluangnya naik sesuai tingkat kesulitan. Ada peringatan "⚠ GRANAT!" bila granat musuh mendarat dekat.
- Menu Beli dikelompokkan: Pistol, Senjata utama, Jarak dekat, Perlengkapan.
- Tombol 3 / Q / scroll untuk berganti antar tiga slot; GANTI di HP memutar slot.
### Catatan
- Ledakan milik sendiri juga melukai pemain (60%).

## v1.13 — 23 Okt 2026
### Ditambahkan
- Bot Penjaga memakai karakter tentara 3D beranimasi (CC0, Quaternius Toon Shooter Game Kit) menggantikan bot kotak-kotak.
- Animasi bot: diam, membidik di tempat, berjalan sambil menembak, lari membawa senjata, terkena tembakan (hit react), dan jatuh saat mati.
### Catatan
- Hitbox (kepala/badan/kaki) tetap sama, jadi headshot tetap di bagian kepala.
- Bila model gagal dimuat, bot kotak-kotak lama dipakai sebagai cadangan.

## v1.12 — 23 Okt 2026
### Ditambahkan
- Tekstur asli (CC0, Poly Haven): pasir untuk lantai, batu pasir untuk dinding, plester untuk dinding tengah, papan kayu untuk peti, beton untuk area zona bom A.
- Tekstur dikecilkan ke 512px (total ±50 KB) agar ringan di HP; tekstur prosedural lama tetap jadi cadangan.

## v1.11 — 23 Okt 2026
### Ditambahkan
- Model 3D senjata asli (CC0, Quaternius Ultimate Gun Pack): pistol, SMG, rifle gaya AK, sniper dengan scope.
- Suara tembakan rekaman asli (CC0, Free Firearm Sound Library) untuk tiap senjata dan tembakan musuh.
- `assets/CREDITS.md` berisi sumber dan lisensi aset.
### Catatan
- Model prosedural lama tetap dipakai sebagai cadangan bila model gagal dimuat.

## v1.10 — 23 Okt 2026
### Ditambahkan
- Pilihan tingkat kesulitan: **Mudah, Normal, Sulit, Ahli**. Memengaruhi akurasi, waktu reaksi, damage, nyawa, kecepatan, laju tembak, dan jarak pandang bot.
- Label tingkat kesulitan di papan skor atas.
### Diubah
- Menu awal di HP (landscape) disusun dua kolom (Gyro | Kesulitan & Jumlah musuh) agar semua pengaturan dan tombol MULAI muat di satu layar.
- "Reset pengaturan" juga mengembalikan kesulitan ke Normal.

## v1.9 — 23 Okt 2026
### Ditambahkan
- Zoom / bidik (ADS) untuk **semua senjata**: senjata bergeser ke tengah, pandangan diperbesar, akurasi naik, sensitivitas turun. Sniper tetap memakai teropong.
- Pengaturan **jumlah musuh** (1–10, atau Otomatis), tersimpan di browser.
- Tombol **⟲ RESET** saat bermain untuk mengulang pertandingan (dengan konfirmasi).
- Tombol **↺ Reset pengaturan** di menu awal.
- Titik muncul musuh ditambah agar banyak bot tidak menumpuk.
### Diperbaiki
- Tombol ZOOM tidak berefek saat memegang selain sniper.

## v1.8 — 23 Okt 2026
### Diperbaiki
- Gyro aim salah arah di mode landscape. Sekarang memakai pose lengkap perangkat (3D), benar di semua orientasi layar.

## v1.7 — 23 Okt 2026
### Ditambahkan
- Label versi di pojok kiri atas.
- Cek update otomatis tiap menit; muncul tombol "🔄 Update tersedia" untuk memuat ulang tanpa cache.

## v1.6 — 23 Okt 2026
### Ditambahkan
- Lencana versi dan tanggal build di menu awal.

## v1.5 — 23 Okt 2026
### Diperbaiki
- Gyro tidak bekerja di iPhone: izin sensor kini diminta saat jari diangkat (syarat iOS), tetap mendengarkan sensor walau izin dilaporkan ditolak, dan ada cadangan memakai data orientasi.
- Pesan diagnosis status sensor di menu.

## v1.4 — 23 Okt 2026
### Diperbaiki
- Menu tidak bisa digulir di HP sehingga tombol MULAI tidak bisa ditekan.
- Tombol MULAI dibuat menempel di bawah dan merespons sentuhan langsung.

## v1.3 — 23 Okt 2026
### Diperbaiki
- Teks menu terpotong / terlalu besar di HP landscape (auto text-size iOS dimatikan, ukuran ringkas untuk layar pendek).
- Petunjuk kontrol PC disembunyikan di HP dan sebaliknya.

## v1.2 — 23 Okt 2026
### Diperbaiki
- Game macet setelah tekan MULAI (error saat membuat senjata bot).
### Diubah
- Model senjata di HP diperkecil agar tidak menutupi layar.

## v1.1 — 23 Okt 2026
### Ditambahkan
- **Gyro aim** dari sensor perangkat, dengan sensitivitas dan opsi balik arah.
- Model 3D per senjata (pistol, SMG, rifle, sniper) dengan tangan.
- Animasi reload (magazen dicabut/dipasang, kokang; sniper bolt-action), ganti senjata, recoil, muzzle flash, selongsong peluru, ayunan senjata, hit marker, animasi bot jatuh.
- Zoom teropong sniper.
- Suara prosedural: tembakan per senjata, reload, langkah kaki (dengan arah kiri/kanan), hit/headshot, bom, ledakan, menang/kalah.
- Tombol HP: GANTI, ZOOM.

## v1.0 — 23 Okt 2026
### Rilis awal
- FPS 3D bergaya tactical shooter: tim Penyerang vs bot Penjaga, pasang bom di zona A, menang 8 ronde.
- Ekonomi & menu beli (SMG, Rifle, Sniper, rompi), headshot, recoil dasar.
- Kontrol PC (WASD + mouse) dan HP (joystick + tombol sentuh).
