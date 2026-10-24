# Changelog — Strike Zone

Semua perubahan penting pada game Strike Zone dicatat di sini.
Game: https://zenaki.github.io/Doodle-Shooter/strike/

## v1.25 — 24 Okt 2026
### Diubah
- **Semua map 4× lebih luas** (160×160 m, sebelumnya 80×80 m). Jarak antar-bangunan, dinding, dan zona dilipatgandakan; ukuran peti, kontainer, mobil, dan karakter tetap.
- Setiap map ditambah ±30 objek perlindungan sesuai temanya (peti, karung pasir, batu, mobil rusak, kontainer, mesin, pohon, pagar tanaman) agar area baru tidak kosong. Penempatannya sama di semua HP saat multiplayer.
- Zona bom sedikit diperbesar, jarak pandang (kabut) diperpanjang, peta (M), pratinjau map, pencarian jalan bot, dan kamera replay menyesuaikan ukuran baru.

## v1.24 — 24 Okt 2026
### Diubah
- Menu awal diseimbangkan: kolom kiri berisi **Gyro Aim + Map** (dengan pratinjau denah), kolom kanan berisi **Karakter, Kesulitan, Jumlah musuh, Tembok hancur** dan tombol Reset. Tinggi kedua kolom kini hampir sama.

## v1.23 — 24 Okt 2026
### Ditambahkan
- **Pilihan map** di menu awal (dengan pratinjau denah, dan latar menu langsung berganti ke map yang dipilih):
  - 🏜️ **Gurun Klasik** — map lama.
  - 🏙️ **Kota Kecil** — jalan bersilang di antara blok gedung tinggi, gang sempit, mobil rusak, lampu jalan, cone; zona bom di plaza utara.
  - 📦 **Pelabuhan Kontainer** — labirin kontainer (sebagian ditumpuk 2 tingkat) dengan **dua zona bom, A dan B**; tepi dermaga di utara.
  - 🏜️ **Gurun Terbuka** — area lapang untuk sniper/roket: batu besar, tank, mobil rusak, karung pasir, reruntuhan pos di zona A; jarak pandang jauh.
  - 🏭 **Pabrik** — 9 ruangan beton dengan pintu, pilar, mesin, banyak tong meledak, pencahayaan redup; jarak dekat.
  - 🌲 **Taman** — rumput, pagar tanaman sebagai perlindungan, banyak pohon, sungai yang hanya bisa diseberangi lewat dua jembatan (peluru tetap bisa melintas), gazebo di zona A.
  - 🎲 **Acak tiap ronde** — map berganti otomatis setiap ronde.
- Peta (M), titik muncul, jalur patroli & pencarian jalan bot menyesuaikan setiap map. Opsi tembok hancur berlaku di semua map.
- Di Co-op/PvP, map mengikuti pilihan host dan otomatis dimuat di HP semua pemain.

## v1.22 — 24 Okt 2026
### Diperbaiki
- Pesan "Gyro: sensor tidak mengirim data" muncul di mode solo (regresi v1.21). Izin sensor kini hanya diminta sekali walau beberapa sentuhan terjadi bersamaan; sebelumnya permintaan ganda membuat iPhone menolak izin.

## v1.21 — 24 Okt 2026
### Ditambahkan
- **Pengaturan "🧱 Tembok/objek hancur"** di menu awal: Mati, 5×, 10×, 20×, atau 40× tembakan. Bila aktif, dinding bagian dalam peta, peti, kontainer, karung pasir, mobil, dan properti lain retak (makin gelap) lalu hancur dengan debu setelah jumlah tembakan itu. Pagar luar arena tidak bisa dihancurkan.
  - Peluru shotgun/cannon dihitung ±1/3 tembakan per butir; ledakan granat/roket/tong dihitung 3 tembakan untuk objek di dekatnya.
  - Bot langsung memakai jalan baru yang terbuka. Semua objek pulih setiap ronde.
  - Di multiplayer, pengaturan mengikuti host dan objek hancur tersinkron ke semua pemain.
### Diperbaiki
- **Suara dan gyro aim hilang bagi pemain yang bergabung (Co-op/PvP).** Game pemain tamu dimulai oleh sinyal dari host, bukan oleh sentuhan, sehingga browser (terutama iPhone) tidak menyalakan suara dan tidak memberi izin sensor. Sekarang suara dan izin gyro dinyalakan saat menekan Gabung/Buat Room dan pada sentuhan pertama mana pun di layar.

## v1.20 — 24 Okt 2026
### Ditambahkan
- **Multiplayer online (peer-to-peer):** pilih mode **🤝 Co-op** atau **⚔️ PvP** di menu awal. Satu pemain menekan **Buat Room** dan membagikan kode 5 huruf, pemain lain memasukkan kode lalu **Gabung**. Tidak perlu server: HP saling terhubung langsung (WebRTC via PeerJS), dengan relay otomatis bila jaringan memblokir koneksi langsung.
  - **Co-op:** semua pemain menjadi Penyerang melawan bot Penjaga. Jumlah bot bertambah sesuai jumlah pemain. Ronde kalah bila semua pemain tewas.
  - **PvP:** pemain dibagi otomatis ke tim Penyerang dan Penjaga. Penjaga bisa **menjinakkan bom** (tahan E / tombol BOM di dekat bom selama 5 detik). Tembakan, pisau, granat, roket, dan api melukai lawan; teman setim tidak bisa saling melukai.
  - Host menjadi penentu: bot, ronde, waktu, bom, dan skor dijalankan di HP host lalu disinkronkan ke pemain lain.
  - Pemain lain tampil sebagai karakter 3D beranimasi pilihan mereka, lengkap dengan nama di atas kepala (teman setim) dan di peta.
  - Tembakan, tracer, granat, ledakan, tong, kotak P3K, ranjau, dan jebakan tersinkron ke semua pemain. Kill feed menampilkan siapa membunuh siapa.
  - Saat tewas, kamera mengikuti teman setim yang masih hidup (tap/klik untuk berganti) sampai ronde berikutnya.
  - Pemain bisa bergabung di tengah pertandingan dan ikut bermain mulai ronde berikutnya.
### Catatan
- Disarankan 2–4 pemain. Bila host keluar, pertandingan berakhir untuk semua pemain.
- Tombol RESET dan pengaturan musuh/kesulitan hanya bisa diubah oleh host.

## v1.19 — 24 Okt 2026
### Ditambahkan
- **Replay kini merekam tembakan dan ledakan**: setiap tembakan digambar sebagai garis tebal dari penembak ke titik kena (hijau = tembakanmu, merah = musuh) dengan kilat laras dan titik dampak, plus peluru melesat. Ledakan granat/roket/tong, area api, dan granat/roket yang sedang terbang juga diputar ulang, lengkap dengan suara ledakan.
### Diubah
- **Indikator arah tembakan lebih jelas** saat bermain: busur merah lebih tebal dan besar, ada panah penunjuk arah, rona merah di tepi layar sisi datangnya serangan, dan tampil lebih lama (±1.6 detik).

## v1.18 — 24 Okt 2026
### Ditambahkan
- **Layar setelah tewas** dengan tombol **▶ MAIN LAGI** (langsung ronde berikutnya) dan **🎬 TONTON REPLAY**. Ronde tidak lagi lanjut otomatis bila kamu tewas.
- **Replay ronde**: seluruh ronde direkam (posisi, arah, animasi kamu dan semua musuh, serta bom) lalu bisa diputar ulang.
  - **Kamera bebas (free roam)**: terbang ke mana saja — PC: WASD + mouse, Spasi naik, C turun, Shift lebih cepat; HP: joystick kiri + geser layar kanan, tombol NAIK/TURUN.
  - **Garis ke langit** di setiap karakter (hijau = kamu, merah = musuh, redup bila sudah tewas) plus lingkaran di tanah agar terlihat dari atas.
  - Kontrol: putar/jeda, kecepatan 0.5× / 1× / 2×, geser timeline, KELUAR (kembali ke layar tewas).

## v1.17 — 24 Okt 2026
### Diperbaiki
- **Bot tidak lagi tersangkut.** Bot sekarang memakai pencarian jalur (A* di grid peta 80×80) yang memutari dinding dan properti, ditambah deteksi macet yang menghitung ulang jalur atau memilih titik patroli lain. Dalam simulasi 3 menit dengan 10 bot, waktu tersangkut turun dari 89% menjadi ±1%.
- Bot menghadap arah jalannya saat berpatroli (tidak lagi berjalan menyamping).
### Ditambahkan
- **Tombol PETA** (HP) / **M** (PC): peta seluruh arena yang menampilkan posisi & arah hadap kamu (panah + kerucut pandang), semua musuh (merah; × untuk yang tewas), zona bom A, lokasi bom yang dipasang (berkedip), kotak P3K, dan tong meledak.

## v1.16 — 24 Okt 2026
### Ditambahkan
- **Dekorasi peta** dari Toon Shooter Game Kit (CC0): semua peti diganti model peti kayu asli; tambahan kontainer panjang & kecil, karung pasir di zona A, tangki air, barrier, pagar, mobil rusak + ban, tank, pohon, lampu jalan, cone, palet & kardus. Semua yang besar punya collider (bisa dipakai berlindung, menahan peluru & granat).
- **Tong meledak:** 6 tong merah di peta. Tembak (atau kena ledakan) → meledak, melukai bot dan pemain di sekitar, dan bisa memicu tong lain (reaksi berantai). Tong pulih setiap ronde.
- **Health pickup:** 3 kotak P3K berputar di peta; ambil untuk +50 nyawa (muncul lagi setelah 30 detik).
- **Ranjau ($400, maks 2) & Jebakan beruang ($250, maks 2)** di menu Beli → Perlengkapan. Pasang dengan tombol RANJAU di HP atau F di PC. Ranjau aktif setelah 1 detik dan meledak bila bot menginjaknya; jebakan menjepit bot 4 detik + 35 damage.

## v1.15 — 24 Okt 2026
### Ditambahkan
- **Pilih karakter** di menu awal: Tentara, Penyerbu, atau Hazmat, dengan pratinjau 3D berputar. Warna sarung tangan di tangan mengikuti karakter; musuh memakai dua karakter lainnya.
- **Peluru melesat (tracer):** jejak peluru terlihat terbang dari senjata ke sasaran, untuk pemain maupun bot. Peluru bot yang meleset di dekatmu berdesing.
- **Indikator arah tembakan:** busur merah di sekitar bidikan menunjukkan dari arah mana kamu terkena (tembakan, ledakan, api).
- **Indikator granat:** ikon 💣/🔥/🚀 di sekitar bidikan menunjuk ke granat/roket yang bisa melukaimu. Ikon hanya muncul bila kamu berada dalam radius ledakan dan tidak terlindung dinding; makin dekat makin besar dan berkedip merah.
### Diubah
- Peringatan teks "⚠ GRANAT!" diganti indikator arah + bunyi bip.

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
