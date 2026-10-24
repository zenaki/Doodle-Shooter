# Kredit Aset — Strike Zone

Semua aset pihak ketiga di folder ini berlisensi **CC0 1.0 (Public Domain)**. Atribusi tidak diwajibkan, dicantumkan sebagai apresiasi.

## Model senjata & granat (`models/`)
- **Toon Shooter Game Kit** (Des 2022) oleh **Quaternius** — https://quaternius.com/packs/toonshootergamekit.html (CC0)
  - pistol ← Pistol, revsmall ← Revolver_Small, revolver ← Revolver, smg ← SMG, shotgun ← Shotgun, rifle ← AK, sniper ← Sniper, sniper2 ← Sniper_2, cannon ← ShortCannon, launcher ← GrenadeLauncher, rocket ← RocketLauncher, knife ← Knife_1, knife2 ← Knife_2, shovel ← Shovel, nade_he ← Grenade, nade_fire ← FireGrenade
  - Dikonversi dari glTF ke GLB dan dikompres.

## Karakter (`models/soldier.glb`, `enemy.glb`, `hazmat.glb`)
- **Toon Shooter Game Kit** (Des 2022) oleh **Quaternius** — https://quaternius.com/packs/toonshootergamekit.html (CC0)
  - Character_Soldier, Character_Enemy, Character_Hazmat; animasi yang dipakai: Idle, Idle_Shoot, Walk, Walk_Shoot, Run, Run_Gun, Run_Shoot, HitReact, Death. Senjata lain dan animasi tak terpakai dihapus, lalu dikompres.

## Properti peta (`models/`)
- **Toon Shooter Game Kit** oleh **Quaternius** (CC0): Crate, Container_Long, Container_Small, SackTrench, SackTrench_Small, WaterTank_Floor, Barrier_Single, Barrier_Large, Debris_BrokenCar, Debris_Tires, Tank, Tree_1, Tree_3, StreetLight, TrafficCone, Pallet, CardboardBoxes_1, ExplodingBarrel, ExplodingBarrel_Spilled, Health, Landmine, BearTrap_Open, BearTrap_Closed.

## Suara tembakan (`sounds/`)
- **The Free Firearm Sound Library** oleh Ben Jaszczak, Brian Nelson, Kevin Heras, Matthew Nanney — https://opengameart.org/content/the-free-firearm-sound-library
  - `pistol.mp3` ← Walther PPQ (X_39P), `smg.mp3` ← PPSh (P_30P), `rifle.mp3` ← AK-47 (C_28P), `sniper.mp3` ← Tikka T3 (W_29P), `enemy.mp3` ← AR-15 jarak menengah (D_24P)
  - Dipotong ke satu tembakan, mono 44.1 kHz, dinormalisasi, MP3 96 kbps.

## Tekstur (`textures/`)
- **Poly Haven** — https://polyhaven.com (CC0)
  - `sand.jpg` ← Aerial Beach 01, `wall.jpg` ← Sandstone Blocks 08, `dark.jpg` ← Beige Wall 001, `crate.jpg` ← Wood Planks, `concrete.jpg` ← Concrete Floor Worn 001
  - Hanya peta diffuse, diperkecil ke 512×512.

## Kode pihak ketiga (`../lib/`)
- `GLTFLoader.js` dan `SkeletonUtils.js` dari three.js r128 — MIT License, © three.js authors.

## Library
- **PeerJS 1.5.4** (`lib/peerjs.min.js`) — MIT License, © Michelle Bu & Eric Zhang. Koneksi WebRTC peer-to-peer & server signaling gratis peerjs.com.
