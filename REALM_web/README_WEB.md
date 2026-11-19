# REALM — Versi Web (HTML5) dari Prototipe Godot Chibi 3D

**Dibuat:** 19 November 2026. Gratis 100%, tanpa bayar.
**Isi:** desa Wilwatikta 3D chibi **v0.8** (di-export ulang 19 Nov 2026
dari ChibiVillage v0.8) — gerak **usap jari di HP**: usap di mana saja di
area game, karakter jalan mengikuti arah usapan (makin jauh makin cepat,
lepas jari = berhenti), TANPA joystick visual sama sekali; plus kontrol
sentuh HP v0.6 (D-pad kiri bawah untuk jalan, tombol AKSI kanan bawah
pengganti E, tombol Dagang 1/2 saat panel dagang terbuka) dan keyboard
WASD/panah + E yang tetap jalan; plus bug interaksi sejak v0.2 yang
diperbaiki (di tengah petak 1 kini menanam, di sisi barat landasan kini
menempa — interaksi dipilih dari yang terdekat); plus semua isi v0.7:
Novice model chibi Blender (`Rogue_chibi.glb`: kepala dilebarkan/
dibulatkan, tunik/jubah ungu, logam emas, 76 animasi utuh); plus semua
isi v0.5: langit prosedural hangat, palet ungu-emas konsisten di semua
panel HUD, label lokasi (BENGKEL / PASAR / SAWAH WILWATIKTA / RUMAH
PENJAHIT), kamera wide shot lebih tinggi/mundur, tanaman 3 tahap dengan
batang yang ikut tumbuh, tanah dan sawah lebih kontras, bunga di alun-alun;
sawah 3 tahap tumbuh, HUD strip atas ungu-emas + bar progres panen, panel
Tempa dengan bar zona hijau, panel Dagang 1/2, alun-alun + sumur di
tengah, rumah penjahit; karakter rigged KayKit
Adventurers CC0 dengan animasi jalan, desa KayKit Medieval Hexagon,
trial **Tani** (Pak Sastro), **Tempa** (Empu Wira), **Dagang**
(Nyai Kirana), plus **hama sawah**.
Sama seperti `scenes/chibi3d/ChibiVillage.tscn` di proyek Godot.
Detail gameplay: `~/workspace/REALM_godot/docs/CHIBI3D_v0.1.md`.

## File di folder ini

| File | Isi |
|---|---|
| `index.html` | Halaman utama — buka ini lewat server (lihat bawah) |
| `index.js` | Loader/engine Godot untuk web (274 KB) |
| `index.wasm` | Engine Godot WebAssembly, build **no-threads** (38 MB) |
| `index.pck` | Data game: scene ChibiVillage, script, aset KayKit (14,9 MB; v0.8 14.951.276 byte, MD5 `336e66fc20ff4e4164bb1b6a1307947f`, berbeda dari v0.7, berisi `village.gd` v0.8 + `Rogue_chibi.glb`; membesar karena 5 plugin pengembangan — Cyclops, Better Terrain, Inventory Manager, Juicee, gd-YAFSM — ikut ter-export oleh `export_filter="all_resources"`, padahal belum dipakai kode game) |
| `index.audio.worklet.js`, `index.audio.position.worklet.js` | Audio web |
| `index.png`, `index.icon.png`, `index.apple-touch-icon.png` | Ikon |

## Cara buka (penting)

**Jangan double-click `index.html` langsung.** File `.wasm` dan `.pck`
harus disajikan lewat HTTP, kalau dibuka sebagai `file://` game tidak jalan.

### Cara 1 — server lokal (paling mudah, di komputer sendiri)
```bash
cd ~/workspace/user/files/REALM_web
python3 -m http.server 8931
```
Lalu buka di browser: `http://127.0.0.1:8931/index.html`
(atau `http://localhost:8931/`). Untuk berhenti, tekan `Ctrl+C` di terminal.

### Cara 2 — hosting / upload
Upload **seluruh isi folder ini** ke hosting statis apa pun
(GitHub Pages, Netlify, itch.io, dsb). Build ini memakai template
**no-threads** (`variant/thread_support=false`), jadi **tidak butuh
header COOP/COEP khusus** — server HTTP biasa sudah cukup.
(PWA dimatikan di preset export.)

### Kebutuhan browser
Browser modern (Chrome / Edge / Firefox / Safari terbaru), WebGL2,
dan WebAssembly. RAM disarankan 2 GB+. Di HP kini ada kontrol sentuh (D-pad + tombol
AKSI + tombol Dagang 1/2, lihat "Kontrol" di bawah); di laptop/PC
pakai keyboard seperti biasa.

## Kontrol

- **WASD / panah** — jalan (kamera sudut tetap, atas = menjauhi kamera)
- **E / Enter / Spasi** — bicara dengan NPC, lanjut dialog, tanam,
  panen, mulai menempa, memukul saat mini-game tempa berjalan, usir hama
- **1 / 2** — saat pilihan dagang terbuka: 1 = Jual Pasti (+10 gold),
  2 = Kirim Jauh (hasil bervariasi, dijelaskan alasannya)
- **Di HP (layar sentuh, v0.6):** D-pad kiri bawah (▲ ▼ ◀ ▶) untuk
  jalan, tombol **AKSI** kanan bawah sebagai pengganti E (bicara, lanjut
  dialog, tanam, panen, tempa, usir hama), tombol **1 — Jual Pasti /
  2 — Kirim Jauh** muncul di atas tombol AKSI saat panel dagang terbuka.
  Tombol sentuh hanya muncul di layar sentuh; di laptop/PC tetap
  tersembunyi.

## Alur main (2–5 menit)

1. **Tani:** ke Pak Sastro (baju hijau, dekat rumah), E, baca dialog.
   Tanam 3 petak (E), tunggu ~4 detik sampai padi menguning, panen (E)
   sampai 3 karung → gelar "Murid Pak Sastro". Awas hama (bola gelap
   di petak): dekati dan tekan E sebelum ~10 detik, kalau tidak petak
   itu rusak — karung yang sudah dipanen tetap aman.
2. **Tempa:** ke Empu Wira (baju abu, timur, dekat tungku), E, baca
   dialog. Ke landasan, E untuk mulai, tekan E saat penanda merah di
   zona hijau — 3 pukulan bagus = lulus → "Murid Empu Wira".
3. **Dagang:** ke Nyai Kirana (baju ungu, barat, di lapak), E, baca
   dialog. Ke lapak, E, lalu 1 (Jual Pasti) atau 2 (Kirim Jauh).
   Satu transaksi selesai = lulus → "Murid Nyai Kirana".

## Cara export ini dibuat (supaya bisa diulang)

- Template export resmi Godot 4.7.2 diunduh dari rilis GitHub
  `godotengine/godot` 4.7.2-stable (`Godot_v4.7.2-stable_export_templates.tpz`,
  SHA512 terverifikasi cocok dengan `SHA512-SUMS.txt` resmi),
  diinstal di `~/.local/share/godot/export_templates/4.7.2.stable/`.
- Preset: `~/workspace/REALM_godot/export_presets.cfg` (preset "Web",
  thread support OFF).
- Saat export, `run/main_scene` di `project.godot` **sementara** diganti
  ke `res://scenes/chibi3d/ChibiVillage.tscn`, lalu **dikembalikan** ke
  `res://scenes/boot/Boot.tscn` — main scene proyek tidak berubah permanen.
- Perintah export (headless):
  `Godot_v4.7.2-stable_linux.x86_64 --headless --path . --export-release "Web" /home/hatch/workspace/user/files/REALM_web/index.html`

## Verifikasi (19 Nov 2026, VM headless)

- **Export ulang v0.7 (19 Nov 2026):** exit 0, tanpa SCRIPT ERROR
  (hanya pesan leak shutdown generik saat proses headless keluar).
  `run/main_scene` sudah dikembalikan ke Boot. File `.pck` diperiksa:
  MD5 `9b0ff2a30d9ddda5f68bdf7068ba3e00` (berbeda dari v0.6
  `e298fb4d1b4314152bd83f65656376ae`), berisi `Rogue_chibi.glb`
  + tekstur ungu-emasnya (dicek lewat `strings` di `.pck`).
  PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene
  termuat dan mencetak v0.7, skala chibi 0.8, 76 animasi, Idle jalan,
  D-pad menggerakkan pemain, tombol AKSI membuka dialog Sastro
  (**PCK_CHECK PASS**). Server HTTP lokal sementara
  (`python3 -m http.server 8936`, lalu dimatikan): semua file utama
  status **200** — `index.html`, `index.js`, `index.wasm` (38 MB),
  `index.pck` (10,9 MB), `index.audio.worklet.js`, `index.icon.png`.
  Headless run scene mencetak `REALM — Chibi 3D v0.7… Novice chibi
  Blender.`, tanpa SCRIPT ERROR. Uji regresi otomatis v0.7:
  **96/96 lolos** (runner sementara sudah dihapus). Backup v0.6 ada di
  `/tmp/REALM_web_v06_backup/`.
  Zip baru: `workspace/user/files/REALM_web_v0.7.zip` (21 MB).
- **Export ulang v0.6 (19 Nov 2026):** exit 0, tanpa SCRIPT ERROR
  (hanya pesan leak shutdown generik saat proses headless keluar).
  `run/main_scene` sudah dikembalikan ke Boot. File `.pck` diperiksa:
  MD5 `e298fb4d1b4314152bd83f65656376ae` (berbeda dari v0.5
  `16681ca68a40f3044f1ebf7107afb754`), berisi `village.gdc` v0.6.
  PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene
  termuat dan mencetak v0.6, TouchUI ada/tersembunyi/tampil, D-pad
  menggerakkan pemain, tombol AKSI membuka dialog (**PCK_CHECK PASS**).
  Server HTTP lokal sementara (`python3 -m http.server 8935`, lalu
  dimatikan): semua file utama status **200** — `index.html`,
  `index.js`, `index.wasm` (38 MB), `index.pck` (10,9 MB),
  `index.audio.worklet.js`, `index.icon.png`. Headless run scene
  mencetak `REALM — Chibi 3D v0.6… Kontrol sentuh HP aktif bila layar
  sentuh tersedia.`, tanpa SCRIPT ERROR. Uji regresi otomatis v0.6:
  **75/75 lolos**. Backup v0.5 ada di `/tmp/REALM_web_v05_backup/`.
  Zip baru: `workspace/user/files/REALM_web_v0.6.zip` (21 MB).
- **Export ulang v0.5 (19 Nov 2026, 19:48 WIB):** exit 0, tanpa SCRIPT
  ERROR (hanya pesan leak shutdown generik saat proses headless keluar).
  `run/main_scene` sudah dikembalikan ke Boot. File `.pck` diperiksa:
  MD5 `16681ca68a40f3044f1ebf7107afb754` (berbeda dari v0.4
  `418198372cb105cb918a2b1178b54960`), berisi `ProceduralSkyMaterial_chibi`
  dari scene v0.5. Server HTTP lokal sementara
  (`python3 -m http.server 8934`, lalu dimatikan): semua file utama
  status **200** — `index.html`, `index.js`, `index.wasm` (38 MB),
  `index.pck` (8,9 MB), `index.audio.worklet.js`, `index.icon.png`.
  Headless run scene mencetak `REALM — Chibi 3D v0.5… Palet ungu-emas,
  model KayKit CC0.`, tanpa SCRIPT ERROR. Uji regresi otomatis
  v0.5: **80/80 lolos**. Backup v0.4 ada di `/tmp/REALM_web_v04_backup/`.
- **Export ulang v0.4 (19 Nov 2026, 15:28 WIB):** exit 0, tanpa SCRIPT
  ERROR. `run/main_scene` sudah dikembalikan ke Boot. File `.pck`
  diperiksa: MD5 berbeda dari v0.3, berisi scene ChibiVillage dan
  `village.gd` v0.4 (terkompilasi). Server HTTP lokal sementara
  (`python3 -m http.server 8933`, lalu dimatikan): semua file utama
  status **200** — `index.html`, `index.js`, `index.wasm` (38 MB),
  `index.pck` (8,9 MB), `index.audio.worklet.js`, `index.icon.png`.
  Headless run scene mencetak `REALM — Chibi 3D v0.4… Desain mockup
  v0.2, model KayKit CC0.`, tanpa SCRIPT ERROR. Uji regresi otomatis
  v0.4: **75/75 lolos**. Backup v0.3 ada di `/tmp/REALM_web_v03_backup/`.
- **Export ulang v0.3 (19 Nov 2026, 14:26 WIB):** exit 0, tanpa SCRIPT
  ERROR (hanya pesan leak shutdown generik saat proses headless keluar,
  sama seperti sebelumnya — bukan error game). `run/main_scene` sudah
  dikembalikan ke Boot. File `.pck` diperiksa: berisi scene
  ChibiVillage, `village.gd`, `player_chibi`, dan aset KayKit
  (8,9 MB, dulu 2,3 MB). Server HTTP lokal sementara
  (`python3 -m http.server 8932`): semua file utama status **200** —
  `index.html`, `index.js`, `index.wasm` (38 MB), `index.pck` (8,9 MB),
  `index.audio.worklet.js`, `index.icon.png`. Headless run scene
  mencetak `REALM — Chibi 3D v0.3… Model KayKit CC0.`, tanpa SCRIPT ERROR.
- Export v0.2 sebelumnya: exit 0, tanpa SCRIPT ERROR; `.pck` berisi
  scene ChibiVillage dan `village.gd`; server lokal: semua file utama
  status **200**.

## Keterbatasan (jujur)

- **Belum diuji di browser grafis sungguhan, apalagi di HP sungguhan**
  — VM ini headless, jadi game belum benar-benar dimainkan lewat
  browser di sini. File-file lengkap dan tersaji dengan benar, tapi
  tampilan, performa, kontrol keyboard, dan terutama kontrol sentuh
  (ukuran D-pad 84 px / tombol AKSI 150 px dalam viewport 1280×720
  yang diskalakan ke layar HP) harus dicek di HP sungguhan sehnxi.
  D-pad-nya digital 4 arah, bukan joystick analog.
- Karakter Novice kini model chibi Blender (kepala dilebarkan/
  dibulatkan, tunik/jubah ungu, logam emas — lihat
  `docs/CHIBI_NOVICE_v0.1.md`), tapi 3 mentor masih model KayKit asli,
  kepala Novice masih rasio 0,456 bukan 1/3 seperti Dewi Larasmaya,
  atap masih Eropa bukan limasan, belum ada tekstur batik. Desain v0.5
  menambah langit prosedural hangat, label lokasi, kamera wide shot,
  dan tanaman berbatang, tapi atap limasan + batik Parang Sekar masih
  belum bisa tanpa pemodelan lebih lanjut di Blender. Belum ada suara/musik di versi Godot ini,
  belum ada save/load, multiplayer, atau build Android.
- Loading pertama agak lama karena `index.wasm` 38 MB — itu normal
  untuk export web Godot; setelah itu game jalan lokal.
- Prototipe browser v0.1 (`~/workspace/user/files/REALM_prototype/index.html`)
  tidak diganggu — itu file terpisah, tetap ada seperti sebelumnya.
