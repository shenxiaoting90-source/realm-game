# REALM — Versi Web (HTML5) dari Prototipe Godot Chibi 3D

**Dibuat:** 19 November 2026. Gratis 100%, tanpa bayar.
**Isi:** desa Wilwatikta 3D chibi **v0.22** (di-export ulang 20 Nov 2026
dari ChibiVillage v0.22) — **baru: trial Jahit diacak + 3 SFX Jahit
sendiri** — urutan motif Parang Sekar kini diacak tiap percobaan
(panel menampilkan urutan yang berlaku, tersimpan di save) dan
langkah benar/salah/selesai punya suara jahit sendiri (bukan lagi
SFX Tempa); **pilihan jawaban dialog v0.21 tetap** — dialog
perkenalan 4 NPC (Pak Sastro, Empu Wira, Nyai Kirana, Nyai Sekar) kini
punya 3 pilihan jawaban (`responses` Dialogue Manager, dipilih klik /
keyboard 1/2/3 / tombol sentuh; muncul setelah ketikan pertanyaan
selesai; semua cabang berakhir sama, tidak ada trial yang terkunci) —
**dan perbaikan bug start v0.20** — Boot kini langsung meneruskan ke
desa, jadi game web tidak lagi macet di layar judul "REALM — Novice di
Wilwatikta" (penyebab v0.20: export main scene-nya Boot dan Boot dulu
tidak pernah pindah scene; terbukti lewat `--main-pack` pck v0.20 yang
hanya mencetak baris Boot); **refactor v0.20 tetap** — prompt konteks
(`compute_prompt`) dipisah dari `interaction_system.gd` (267 → 193 baris)
ke `prompt_system.gd` baru (satu pemilik prompt; jarak tetap dari
`nearest_interaction` yang sama, tidak diduplikasi), dan fasad
`hud_system.gd` dirapikan (304 → 241 baris: ~35 referensi node lama
dihapus, pemanggil memakai `hud.main` / `hud.panels` / `hud.touch` /
`hud.menu` langsung); perilaku game sama persis seperti v0.19, tanpa fitur baru dan tanpa
perubahan tampilan; **refactor v0.19 tetap** — `world_builder.gd`
(423 baris) dipecah per bangunan/area (`world_primitives` + `builder_terrain`
+ `builder_buildings` + `builder_farm` + `builder_actors`) dan logika
interaksi/prompt (`nearest_interaction` + `do_interact` + `compute_prompt`)
pindah dari `trial_system.gd` (329 → 116 baris) ke `interaction_system.gd`; **dialog v0.18 tetap** — dialog NPC di Dialogue Manager
+ efek ketik; **refactor v0.17 tetap** — save + dunia real-time di `save_system.gd`
dan akibat dialog di `dialogue_effects.gd`; village.gd 200 baris dan
hanya orkestrator; perilaku game sama persis seperti v0.16, tanpa fitur
baru dan tanpa perubahan tampilan; **Penjahit v0.14 tetap** — NPC Nyai Sekar di Rumah
Penjahit (nama "Nyai Sekar" dari build Spaces, BELUM dikonfirmasi sehnxi),
trial Jahit urutan motif Parang Sekar 4 langkah (pilih 1/2/3, salah langkah
= coba lagi langkah itu; **v0.22: urutan diacak tiap percobaan** — panel
menampilkan urutan yang berlaku dan urutan itu tersimpan di save),
magang Penjahit (ulangi motif 3x lagi → "Penjahit Pemula"), masuk
pelacak quest (tujuan ke-4) + save JSON; **suara
+ musik v0.13 tetap** — musik ambient desa loop pelan (sintesis bebas
lisensi, 32 detik) + 10 efek suara sintesis (tanam, panen, tempa
bagus/meleset, koin dagang, usir hama, lulus trial/magang, **v0.22: 3
SFX Jahit sendiri — langkah benar, salah langkah, motif selesai**)
+ tombol bisu
"Suara: Nyala/Mati" di HUD yang tersimpan di save; **save + dunia
real-time v0.12 tetap** — progres tersimpan (JSON `user://`, auto-save
tiap progres + tombol "Simpan" di HUD) dan padi terus tumbuh walau game
ditutup (dihitung dari timestamp save saat kembali; hama TIDAK menyerang
saat offline); saat buka game ada pilihan **Lanjut / Mulai Baru** (Mulai
Baru minta konfirmasi hapus);
**performa v0.11 tetap (dengan satu pengecualian wajib): `index.pck`
6,3 MB** (6.641.860 byte, NAIK 15.396 byte dari 6.626.464 v0.21 — hanya 3
SFX Jahit baru + kode urutan acak; runtime Dialogue Manager kini ikut ter-export, karena
`exclude_filter` lama membuang seluruh `addons/*` sehingga script autoload
Dialogue Manager tidak ada di pck dan semua dialog akan gagal di web;
filter kini membuang semua addon KECUALI `dialogue_manager`; tidak ada
GLB/audio baru; resource tak terpakai tetap tidak ikut ter-export; total
folder web 46 MB); **gameplay 3 menit pertama v0.10 tetap:
pelacak quest yang selalu terlihat** ("★ Tujuan: …" di bawah strip status — temui Pak
Sastro → tanam 3 petak → panen 3 karung → magang → Tempa → Dagang → Jahit),
**Pak Sastro menyapa** saat pemain baru mendekat ("Nak, kemari!"),
**feedback tiap aksi** (status menghitung petak/karung/pukulan, prompt
menampilkan sisa detik tumbuh), **hama adil 14 detik** (dulu 10 detik,
dengan hitung mundur di status + prompt, dan timer berhenti selama
dialog terbuka), dan **magang jelas setelah lulus trial** (panen 3
karung lagi → Petani Pemula; 3 pukulan bagus lagi → Pandai Besi Pemula;
3 transaksi lagi → Saudagar Pemula; ulangi motif Parang Sekar 3x lagi →
Penjahit Pemula); plus batas desa v0.9: karakter
tidak bisa lagi keluar desa lalu jatuh (clamp posisi ke [-16,16] + 4
dinding tak terlihat di tepi tanah + jaring pengaman kembali ke spawn);
plus gerak **usap jari di HP** v0.8: usap di mana saja di
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
(Nyai Kirana), **Jahit** (Nyai Sekar), plus **hama sawah**.
Sama seperti `scenes/chibi3d/ChibiVillage.tscn` di proyek Godot.
Detail gameplay: `~/workspace/REALM_godot/docs/CHIBI3D_v0.1.md`.

## File di folder ini

| File | Isi |
|---|---|
| `index.html` | Halaman utama — buka ini lewat server (lihat bawah) |
| `index.js` | Loader/engine Godot untuk web (274 KB) |
| `index.wasm` | Engine Godot WebAssembly, build **no-threads** (38 MB) |
| `index.pck` | Data game: scene ChibiVillage, script, aset KayKit + audio (6,3 MB; v0.22 6.641.860 byte, MD5 `877d809fc0681766f14aa21470a0898b`, berbeda dari v0.21, berisi 252 entri — baru: urutan motif Jahit acak (`roll_sew_sequence` + `sew_sequence` di `game_state.gd`/`save_manager.gd`, label target di `trial_panels.gd`, 2 baris `sekar.dialogue` diubah) + 3 SFX Jahit (`sfx_sew_good`/`sfx_sew_miss`/`sfx_sew_done` di `audio_system.gd` + `trial_sew.gd`) — dan yang lama tetap: `boot.gd` meneruskan ke ChibiVillage + panel pilihan jawaban di `hud_main.gd` + `choose_response` di `dialogue_system.gd` + 12 balasan pilihan di 4 `.dialogue` + `prompt_system.gd` + `interaction_system.gd` (193 baris) + facade `hud_system.gd` (241 baris, tanpa ~35 referensi node lama) + `village.gd` (224 baris) + 6 modul refactor v0.19 (`interaction_system`, `world_primitives`, `builder_terrain`, `builder_buildings`, `builder_farm`, `builder_actors`) + facade `world_builder.gd` (75 baris) + koordinator `trial_system.gd` (116 baris) + 4 resource `.dialogue` (Sastro/Wira/Kirana/Sekar, sebagai `.godot/imported/*.tres`) + runtime Dialogue Manager 4.2.0 (`addons/dialogue_manager/`, 92 entri; filter export membuang semua addon KECUALI `dialogue_manager` — tanpanya semua dialog gagal di web) + 2 file sistem v0.17 (`save_system`, `dialogue_effects`) + 10 modul v0.16 (`hud_main`, `trial_panels`, `touch_controls`, `save_menu`, `hud_widgets`, `plot_system`, `trial_farming`, `trial_forge`, `trial_trade`, `trial_sew`) + `save_manager.gd` + `player_chibi.gd` v0.9 + `npc_sekar.gd` + 4 GLB yang dipakai — Rogue_chibi, Rogue_Hooded, Barbarian, Mage — + bangunan desa + musik ambient + 10 SFX + blip ketik (dibuat saat runtime, tanpa file baru); NAIK 15.396 byte dari v0.21, hanya 3 SFX Jahit + kode urutan acak; tidak ada GLB baru; tidak ada addon lain yang ikut; file basi `index.pck-Z3j9Q8` (786 KB, sisa export lama, tidak dirujuk `index.html`/`index.js`) dihapus dari folder ini) |
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
- **1 / 2 / 3** — saat panel jahit terbuka: pilih motif Parang Sekar
  (1 = Parang, 2 = Mega Mendung, 3 = Kawung) sesuai urutan di panel;
  salah langkah = coba lagi langkah itu, kain tidak rusak
- **1 / 2 / 3** — saat pilihan jawaban dialog terbuka (v0.21, di dialog
  perkenalan 4 NPC): pilih jawaban; pilihan muncul setelah ketikan
  pertanyaan selesai (tekan E dulu untuk menyelesaikan ketikan);
  E saat pilihan terbuka tidak memajukan dialog
- **Di HP (layar sentuh, v0.6):** D-pad kiri bawah (▲ ▼ ◀ ▶) untuk
  jalan, tombol **AKSI** kanan bawah sebagai pengganti E (bicara, lanjut
  dialog, tanam, panen, tempa, usir hama), tombol **1 — Jual Pasti /
  2 — Kirim Jauh** muncul di atas tombol AKSI saat panel dagang terbuka,
  tombol **1 — Parang / 2 — Mega / 3 — Kawung** muncul di atas tombol
  AKSI saat panel jahit terbuka, dan **3 tombol pilihan jawaban** muncul
  di atas panel dialog saat pilihan jawaban terbuka (v0.21).
  Tombol sentuh hanya muncul di layar sentuh; di laptop/PC tetap
  tersembunyi.

## Alur main (2–5 menit)

Pelacak quest di bawah strip status selalu menunjukkan tujuan berikutnya —
ikuti saja. Pak Sastro menyapa saat kamu mendekat; dekati dan tekan E.

1. **Tani:** ke Pak Sastro (baju hijau, dekat rumah), E, baca dialog.
   Tanam 3 petak (E), tunggu ~4 detik sampai padi menguning, panen (E)
   sampai 3 karung → gelar "Murid Pak Sastro". Awas hama (bola gelap
   di petak): dekati dan tekan E sebelum **14 detik**, kalau tidak petak
   itu rusak — karung yang sudah dipanen tetap aman. Hama tidak
   menyerang selama kamu sedang bicara (timer berhenti saat dialog
   terbuka). Setelah lulus, Sastro menawarkan **magang**: panen 3 karung
   lagi → gelar "Petani Pemula".
2. **Tempa:** ke Empu Wira (baju abu, timur, dekat tungku), E, baca
   dialog. Ke landasan, E untuk mulai, tekan E saat penanda merah di
   zona hijau — 3 pukulan bagus = lulus → "Murid Empu Wira". Magang:
   tempa lagi 3 pukulan bagus → "Pandai Besi Pemula".
3. **Dagang:** ke Nyai Kirana (baju ungu, barat, di lapak), E, baca
   dialog. Ke lapak, E, lalu 1 (Jual Pasti) atau 2 (Kirim Jauh).
   Satu transaksi selesai = lulus → "Murid Nyai Kirana". Magang:
   3 transaksi lagi → "Saudagar Pemula".
4. **Jahit:** ke Nyai Sekar (di Rumah Penjahit, timur-selatan), E, baca
   dialog. Ke meja jahit di depan rumahnya, E, lalu pilih motif sesuai
   urutan yang ditampilkan di panel (diacak tiap percobaan — misal
   Mega → Parang → Kawung → Mega) dengan tombol 1, 2, atau 3.
   Salah langkah = coba lagi langkah itu. Empat langkah benar = lulus
   → "Murid Nyai Sekar". Magang: ulangi motif 3x lagi → "Penjahit
   Pemula".

## Cara export ini dibuat (supaya bisa diulang)

- Template export resmi Godot 4.7.2 diunduh dari rilis GitHub
  `godotengine/godot` 4.7.2-stable (`Godot_v4.7.2-stable_export_templates.tpz`,
  SHA512 terverifikasi cocok dengan `SHA512-SUMS.txt` resmi),
  diinstal di `~/.local/share/godot/export_templates/4.7.2.stable/`.
- Preset: `~/workspace/REALM_godot/export_presets.cfg` (preset "Web",
  thread support OFF).
- Saat export, `run/main_scene` di `project.godot` **tidak lagi**
  diganti sementara ke `res://scenes/chibi3d/ChibiVillage.tscn` —
  sejak v0.21 Boot langsung meneruskan ke ChibiVillage
  (`scripts/core/boot.gd`), jadi export jalan dengan main scene tetap
  `res://scenes/boot/Boot.tscn`. (Dulu, sebelum v0.21, export
  mengganti main scene sementara lalu mengembalikannya — langkah itu
  pernah terlewat di v0.20 dan membuat game web macet di layar judul;
  sekarang kelas bug itu sudah tidak bisa terulang.)
- Sejak v0.11, saat export 3 autoload dev (`Juicee`, `BetterTerrain`,
  `CyclopsAutoload`) juga **sementara** dihapus dari `project.godot` lalu
  **dikembalikan** — plugin tetap terinstal dan aktif di editor, hanya
  tidak ikut ter-export (tidak dipakai kode game sama sekali). Bersama
  `exclude_filter` di preset ("addons/*, tools/*, docs/*, assets/audio/*,
  GLB Knight/Rogue + teksturnya, .godot/exported/*,
  .godot/global_script_class_cache.cfg"), ini yang memangkas `.pck`.
- Perintah export (headless):
  `Godot_v4.7.2-stable_linux.x86_64 --headless --path . --export-release "Web" /home/hatch/workspace/user/files/REALM_web/index.html`

## Verifikasi (20 Nov 2026, VM headless)

- **Export ulang v0.22 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export (14 SCRIPT ERROR yang ada semuanya dari plugin editor Cyclops/BetterTerrain saat export — bukan error game). Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik). File `.pck` diperiksa: MD5 `877d809fc0681766f14aa21470a0898b` (berbeda dari v0.21 `4438c59bd3adb886aa7b76dd854ea3ee`, berisi 3 SFX Jahit baru — `sfx_sew_good`/`sfx_sew_miss`/`sfx_sew_done` sebagai `.sample` + `.import` — + runtime Dialogue Manager 4.2.0 (92 entri) + 4 `.dialogue` sebagai `.tres` + 10 modul v0.16 + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (252 entri, 6.616.900 byte isi, nol entri addon lain/`tools/`/`docs/`, nol `Knight.glb`, nol runner uji). **Bukti start:** `index.pck` v0.22 dijalankan mandiri (`--main-pack`) mencetak `REALM — Boot…` LALU `REALM — Chibi 3D v0.22…` — transisi start bekerja di artefak export itu sendiri. PCK diverifikasi dengan memuatnya ke proyek Godot kosong: Boot dari PCK meneruskan ke ChibiVillage (`current_scene` = ChibiVillage), SaveSystem + DialogueEffects ada, 4 modul HUD + 5 modul trial ada, InteractionSystem ada (tanpa `compute_prompt`) + PromptSystem ada, fasad hud tidak lagi mengekspos `title_label`, bangunan builder (Plaza/Well/TailorHouse/Irrigation) + 4 label lokasi ada, panel trial tersembunyi, NPC Sekar di (12,5, 6,8), autoload DialogueManager + `sastro.dialogue` termuat, efek ketik + bunyi ketik jalan, dialog Sastro → `met_sastro`, tanam petak 1 → file save ada + quest (1/3), usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (15,597, y ≈ 0), tombol bisu → bus di-mute + save muted true, dialog Sekar → `sew_ready` + 3 SFX Jahit ada di AudioSystem, motif acak (bukan `[1,2,3,1]` lama) → panel menampilkan urutan itu → langkah benar → `sew_good` → lulus Jahit → save berisi urutan itu, dialog Wira → `forge_ready` + 3 pukulan bagus → lulus Tempa, dialog Kirana → `trade_ready` + Jual Pasti +10 → gold 20 + lulus Dagang (**PCK_CHECK PASS, 47/47**). Server HTTP lokal sementara (`python3 -m http.server 8953`, lalu dimatikan): 8 file utama status **200**. Uji otomatis **TEST V0.22 PASS 174/174** (runner sementara sudah dihapus) — urutan motif diacak (30x roll, semua beda dari sebelumnya, ≥5 varian) + panel menampilkan urutan berlaku + save/load urutan + SFX Jahit baru (benar/salah/selesai) + regresi v0.10–v0.21 (4 kegagalan pertama adalah bug runner, bukan game: helper tunggu petak, titik awal usap diagonal, panel Jahit uji bisu tidak ditutup). Backup v0.21 dibuat di `/tmp/REALM_web_v21_backup/` lalu hilang saat runtime restart di tengah PCK check (seluruh `/tmp` terhapus; checker v0.21 ikut hilang dan ditulis ulang dari pola yang terdokumentasi — PCK check lolos 47/47 pada percobaan pertama checker baru; zip v0.21 tetap ada). Zip baru: `workspace/user/files/REALM_web_v0.22.zip` (16.573.959 byte, MD5 `7ccd9d157deab7186bff6c05c8faa95f`). **Jujur:** tidak ada Chromium/Firefox di VM ini, jadi halaman HTML/JS di browser grafis sungguhan belum bisa diverifikasi di sini — verifikasi browser dilakukan terpisah saat publish. **TIDAK dipublish** — publish dilakukan terpisah oleh tugas lain.
- **Export ulang v0.21 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export (SCRIPT ERROR yang ada semuanya dari plugin editor Cyclops/BetterTerrain saat `_enter_tree`). Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik). File `.pck` diperiksa: MD5 `4438c59bd3adb886aa7b76dd854ea3ee` (berbeda dari v0.20 `316f8e630084d00c04f2d89469679f4c`), berisi `boot.gd` baru (meneruskan ke ChibiVillage) + panel pilihan jawaban + `choose_response` + 12 balasan pilihan di 4 `.dialogue` + runtime Dialogue Manager 4.2.0 (92 entri) + 10 modul v0.16 + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (246 entri, 6.602.091 byte isi, nol entri addon lain/`tools/`/`docs/`, nol `Knight.glb`, nol runner uji). **Bukti perbaikan bug start v0.20:** `index.pck` v0.21 dijalankan mandiri (`--main-pack`) mencetak `REALM — Boot…` LALU `REALM — Chibi 3D v0.21…` — transisi start bekerja di artefak export itu sendiri (pck v0.20 yang sama hanya mencetak baris Boot dan tidak pernah sampai desa). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: Boot dari PCK meneruskan ke ChibiVillage (`current_scene` = ChibiVillage), SaveSystem + DialogueEffects ada, 4 modul HUD + 5 modul trial ada, InteractionSystem ada (tanpa `compute_prompt`) + PromptSystem ada, fasad hud tidak lagi mengekspos `title_label`, bangunan builder (Plaza/Well/TailorHouse/Irrigation) + 4 label lokasi ada, panel trial tersembunyi, NPC Sekar di (12,5, 6,8), autoload DialogueManager + `sastro.dialogue` termuat, efek ketik + bunyi ketik jalan, dialog Sastro → `met_sastro`, tanam petak 1 → file save ada + quest (1/3), usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (15,597, y ≈ 0), tombol bisu → bus di-mute + save muted true, dialog Sekar → `sew_ready` + urutan 1,2,3,1 → lulus Jahit, dialog Wira → `forge_ready` + 3 pukulan bagus → lulus Tempa, dialog Kirana → `trade_ready` + Jual Pasti +10 → gold 20 + lulus Dagang (**PCK_CHECK PASS, 40/40**). Server HTTP lokal sementara (`python3 -m http.server 8951`, lalu dimatikan): 8 file utama status **200**. Uji otomatis **TEST V0.21 PASS 178/178** (runner sementara sudah dihapus) — pilihan jawaban 4 NPC (tampil setelah ketik selesai, klik + keyboard 1/2/3 + tombol sentuh, E tidak maju saat pilihan terbuka, pilihan tidak valid diabaikan, tiap pilihan ke balasan yang benar, akibat dialog sama) + regresi v0.10–v0.20. Backup v0.20 ada di `/tmp/REALM_web_v20_backup/` (backup v18 + v19 masih di `/tmp`, zip-nya tetap ada). Zip baru: `workspace/user/files/REALM_web_v0.21.zip` (16.551.067 byte, MD5 `0eec19ca5e44f7e3810d440ccf561822`). **Jujur:** tidak ada Chromium/Firefox di VM ini, jadi halaman HTML/JS di browser grafis sungguhan belum bisa diverifikasi di sini — verifikasi browser dilakukan terpisah saat publish. **TIDAK dipublish** — publish dilakukan terpisah oleh tugas lain.
- **Export ulang v0.20 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR di log export. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `316f8e630084d00c04f2d89469679f4c` (berbeda dari v0.19 `a7ad84af6e15c74301dce47fc9fb0f36`), berisi `prompt_system.gd` (baru) + `interaction_system.gd` 193 baris + facade `hud_system.gd` 241 baris + `village.gd` 224 baris + 6 modul v0.19 + 4 resource `.dialogue` + runtime Dialogue Manager 4.2.0 (92 entri) + 10 modul v0.16 + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (246 entri, 6.593.159 byte isi, nol entri addon lain/`tools/`/`docs/`, nol `Knight.glb`, nol runner uji). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.20, PromptSystem ada di PCK (interaction tidak lagi punya compute_prompt), fasad hud di PCK tidak lagi mengekspos `title_label`, bangunan builder (Plaza/Well/TailorHouse/Irrigation) + 4 label lokasi ada, prompt tengah petak 1 = "Tanam padi", dialog Sastro → `met_sastro`, tanam petak 1 → file save ada, quest "Tanam padi di 3 petak sawah (1/3)", usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (15,597, y ≈ 0), tombol AKSI membuka dialog Sastro, tombol bisu → bus di-mute + save muted true, dialog Sekar → `sew_ready` + urutan 1,2,3,1 → lulus Jahit, dialog Wira → `forge_ready` + 3 pukulan bagus → lulus Tempa, dialog Kirana → `trade_ready` + Jual Pasti +10 → gold 20 + lulus Dagang (**PCK_CHECK PASS, 38/38**). Server HTTP lokal sementara (`python3 -m http.server 8949`, lalu dimatikan lewat PID): 8 file utama status **200**. Uji otomatis **TEST V0.20 PASS 195/195** (runner sementara sudah dihapus) — struktur baru + regresi v0.10–v0.19 (quest, sapaan, dialog DM + efek ketik + bunyi ketik, 4 trial + 4 magang, hama 14 detik + beku saat dialog + prompt hama jauh/dekat, save/load + save lama v0.13 + offline growth + laporan kembali, suara/mute, interaksi terdekat + prompt petak 1/landasan/meja jahit, batas desa 4 arah + jaring pengaman, keyboard/D-pad/usap/AKSI/tombol sentuh Dagang/Jahit). Backup v0.19 ada di `/tmp/REALM_web_v19_backup/` (backup v17 dihapus dari `/tmp` supaya muat, zip-nya tetap ada). Zip baru: `workspace/user/files/REALM_web_v0.20.zip` (16.556.131 byte, MD5 `1c75c9e91584deeede3bcfd50d9a0613`). Catatan jujur: total baris kode TURUN sedikit untuk pertama kalinya (4.299 → 4.272, -27) karena facade HUD kehilangan 63 baris dan interaction_system 74 baris, sementara prompt_system baru 99 baris; log export kali ini nol SCRIPT ERROR (versi sebelumnya 4 dari plugin editor Cyclops). Tiga kegagalan pertama uji adalah bug runner, bukan game (sapaan dicek terlalu cepat — `_process` headless tertinggal ~30 frame; tombol AKSI memakai sinyal `button_down` bukan `pressed`; tombol sentuh Jahit dicek sebelum `sync_touch_buttons` jalan). **CATATAN BUG START v0.20 (ditemukan saat publish, diperbaiki di v0.21):** export v0.20 main scene-nya Boot dan Boot dulu tidak pernah pindah scene, sehingga game web macet di layar judul "REALM — Novice di Wilwatikta" — rollback ke v0.19 dilakukan di link publik.
- **Export ulang v0.19 (20 Nov 2026):** exit 0. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `a7ad84af6e15c74301dce47fc9fb0f36` (berbeda dari v0.18 `b2c411dbe69ce942e5e94223343ce667`), berisi 6 modul baru v0.19 (`interaction_system`, `world_primitives`, `builder_terrain`, `builder_buildings`, `builder_farm`, `builder_actors`) + facade `world_builder.gd` 75 baris + `trial_system.gd` 116 baris + `village.gd` 213 baris + 4 resource `.dialogue` + runtime Dialogue Manager 4.2.0 (92 entri) + 10 modul v0.16 + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (244 entri, 6.593.838 byte isi, nol entri addon lain/`tools/`/`docs/`, nol `Knight.glb`, nol runner uji). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.19, InteractionSystem ada (trial tidak lagi punya do_interact/compute_prompt), bangunan builder (Plaza/Well/TailorHouse/Irrigation) + 4 label lokasi ada, prompt tengah petak 1 = "Tanam padi", dialog Sastro → `met_sastro`, tanam petak 1 → file save ada, quest "Tanam padi di 3 petak sawah (1/3)", usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (15,597, y ≈ 0), tombol AKSI membuka dialog Sastro, tombol bisu → bus di-mute + save muted true, dialog Sekar → `sew_ready` + urutan 1,2,3,1 → lulus Jahit, dialog Wira → `forge_ready` + 3 pukulan bagus → lulus Tempa, dialog Kirana → `trade_ready` + Jual Pasti +10 → gold 20 + lulus Dagang (**PCK_CHECK PASS, 36/36**). Server HTTP lokal sementara (`python3 -m http.server 8948`, lalu dimatikan): 8 file utama status **200**. Uji otomatis **TEST V0.19 PASS 188/188** (runner sementara sudah dihapus) — struktur baru + regresi v0.10–v0.18 (quest, sapaan, dialog DM + efek ketik + bunyi ketik, 4 trial + 4 magang, hama 14 detik + beku saat dialog, save/load + save lama v0.13 + offline growth + laporan kembali, suara/mute, interaksi terdekat + prompt petak 1/landasan/meja jahit, batas desa 4 arah + jaring pengaman, keyboard/D-pad/usap/AKSI/tombol sentuh Dagang/Jahit). Backup v0.18 ada di `/tmp/REALM_web_v18_backup/` (backup v16 dihapus dari `/tmp` supaya muat, zip-nya tetap ada). Zip baru: `workspace/user/files/REALM_web_v0.19.zip` (16.564.744 byte, MD5 `8d57cc5ce78cff9c01e96e2747fb634a`). Catatan jujur: total baris kode naik lagi karena pemisahan (9 file terkait world/trial/village 952 → 1.160 baris); yang berkurang adalah tanggung jawab per file, bukan jumlah baris; `interaction_system.gd` sendiri 267 baris (aksi + prompt masih menempel, berbagi `nearest_interaction`); 4 SCRIPT ERROR di log export semuanya dari plugin editor Cyclops — bukan error game. Dua kegagalan pertama uji adalah bug runner, bukan game (teks quest lengkap "Tanam padi di 3 petak sawah (0/3)"; petak yang selamat dicek state == 1 padahal padi sudah tumbuh ke tahap 2 selama uji).
- **Export ulang v0.17 (20 Nov 2026):** exit 0. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `dd03546f0f1a486a72a6a5e371bdcf8c` (berbeda dari v0.16 `bc63e7089c992cd4aca50bbc1a7a6817`), berisi 2 file sistem baru v0.17 (`save_system.gd`, `dialogue_effects.gd`) + `village.gd` (200 baris) + 10 modul v0.16 + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (121 entri, 6.308.302 byte isi, nol entri `addons/`/`tools/`/`docs/`, nol `Knight.glb`, nol runner uji). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.17, SaveSystem + DialogueEffects ada, 4 modul HUD + 5 modul trial ada, panel trial tersembunyi, NPC Sekar di (12,5, 6,8), dialog Sastro → `met_sastro`, tanam petak 1 → file save ada, quest "Tanam padi di 3 petak sawah (1/3)", usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (15,597, y ≈ 0), tombol AKSI membuka dialog Sastro, tombol bisu → bus di-mute + save muted true, urutan Jahit 1,2,3,1 → lulus, 3 pukulan bagus → lulus Tempa, Jual Pasti +10 → lulus Dagang (**PCK_CHECK PASS, 26/26**). Server HTTP lokal sementara (`python3 -m http.server 8946`, lalu dimatikan): 8 file utama status **200**. Uji otomatis **TEST V0.17 PASS 178/178** (runner sementara sudah dihapus) — struktur baru + regresi v0.10–v0.16 (quest, sapaan, 4 trial + 4 magang, hama 14 detik + beku saat dialog, save/load + save lama v0.13 + offline growth + laporan kembali, suara/mute, interaksi terdekat, batas desa 4 arah + jaring pengaman, keyboard/D-pad/usap/AKSI). Backup v0.16 ada di `/tmp/REALM_web_v16_backup/`. Zip baru: `workspace/user/files/REALM_web_v0.17.zip` (16.349.558 byte, MD5 `b94b9c479f9fb83eb4cca1ccd5f8312d`). Catatan jujur: total baris kode naik (3.941 → 4.013) karena pemisahan; yang berkurang adalah tanggung jawab per file, bukan jumlah baris; 15 SCRIPT ERROR di log export semuanya dari plugin editor (Cyclops/BetterTerrain) — bukan error game. Satu kekurangan nyata yang ditemukan uji dan sudah diperbaiki: judul HUD sempat masih "v0.16".
- **Export ulang v0.16 (20 Nov 2026):** exit 0. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `bc63e7089c992cd4aca50bbc1a7a6817` (berbeda dari v0.15 `4c9199374dc2861a65facf5ccfbfa7a5`), berisi 10 file modul baru v0.16 (`hud_main`, `trial_panels`, `touch_controls`, `save_menu`, `hud_widgets`, `plot_system`, `trial_farming`, `trial_forge`, `trial_trade`, `trial_sew`) + facade/koordinator `hud_system.gd` (291 baris) + `trial_system.gd` (329 baris) + `village.gd` (367 baris) + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (116 entri, 6.305.154 byte isi, nol entri `addons/`/`tools/`/`docs/`). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.16, 4 modul HUD + 5 modul trial ada, dialog Sastro → `met_sastro`, tanam petak 1 → file save ada, usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (x = 15,597, y ≈ 0), tombol AKSI membuka dialog Sastro, tombol bisu → bus di-mute + save muted true, urutan Jahit 1,2,3,1 → lulus, 3 pukulan bagus → lulus Tempa, Jual Pasti → lulus Dagang (**PCK_CHECK PASS, 36/36**). Server HTTP lokal sementara (`python3 -m http.server 8945`, lalu dimatikan): 8 file utama status **200**. Uji otomatis **TEST V0.16 PASS 238/238** (runner sementara sudah dihapus) — struktur baru + regresi v0.10–v0.15. Backup v0.15 ada di `/tmp/REALM_web_v15_backup/`. Zip baru: `workspace/user/files/REALM_web_v0.16.zip` (16.362.786 byte, MD5 `859b889ee37b8a9666b9e95031c7ee86`). Catatan jujur: total baris kode naik (2.816 → 3.359) karena pemisahan; yang berkurang adalah tanggung jawab per file, bukan jumlah baris; 14 SCRIPT ERROR di log export semuanya dari plugin editor (Cyclops/BetterTerrain) — bukan error game.
- **Export ulang v0.14 (19 Nov 2026):** exit 0. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `48850072738e8120fbbe65ae457f690a` (berbeda dari v0.13 `1c11ba5f2ab031b7334c34f58e1c52ee`), berisi `village.gd` v0.14 + `npc_sekar.gd` (baru) + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (76 entri, 6.273.482 byte isi, nol entri `addons/`/`tools/`). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.14, panel Jahit ada (tersembunyi), NPC Sekar ada di (12,5, 6,8), dialog Sekar → `sew_ready`, trial Jahit (salah langkah lalu urutan 1,2,3,1) → lulus + file save ada (`sew_passed` true), usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (x = 15,597, y ≈ 0), tombol AKSI membuka dialog Sastro, pelacak quest menunjukkan "★ Tujuan: Tanam padi di 3 petak sawah (0/3)" (**PCK_CHECK PASS, 17/17**). Server HTTP lokal sementara (`python3 -m http.server 8943`, lalu dimatikan): 8 file utama status **200**. Uji otomatis **TEST V0.14 PASS 130/130** (runner sementara sudah dihapus) — dialog Sekar, trial Jahit (salah = coba lagi, tidak reset), magang Penjahit 3x, quest Jahit, save/load Penjahit, save lama v0.13 tetap bisa di-load, + regresi v0.10–v0.13. Backup v0.13 ada di `/tmp/REALM_web_v13_backup/`. Zip baru: `workspace/user/files/REALM_web_v0.14.zip` (16.332.387 byte, MD5 `4c09649bb39b633ee523ed8e84ad1507`). Catatan jujur: nama "Nyai Sekar" belum dikonfirmasi sehnxi (dari build Spaces); urutan motif tetap sama setiap kali; "desain baju tahap pertama" baru berupa gelar/teks, belum ada lemari/baju yang bisa diganti; SFX Jahit memakai ulang SFX Tempa; 4 SCRIPT ERROR di log export semuanya dari plugin editor (Cyclops/BetterTerrain) — bukan error game.
- **Export ulang v0.13 (19 Nov 2026):** exit 0. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `1c11ba5f2ab031b7334c34f58e1c52ee` (berbeda dari v0.12 `02f833cc29652158567abb2d79c5db5b`), berisi `village.gd` v0.13 + `save_manager.gd` + `player_chibi.gd` v0.9 + 4 GLB yang dipakai + bangunan desa + musik ambient + 7 SFX (74 entri, nol entri `addons/`). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.13, tombol Simpan ada, menu save tersembunyi (tanpa save), tanam petak 1 → file save ADA dan load dari PCK (karung 0, planted 1), usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi (x = 15,597, y ≈ 0), AKSI membuka dialog Sastro, pelacak quest "Tanam padi di 3 petak sawah (1/3)" (**PCK_CHECK PASS**). Uji otomatis **TEST V0.13 PASS 142/142**. Server HTTP lokal sementara (`python3 -m http.server 8942`, lalu dimatikan): 8 file utama status **200**. Zip: `REALM_web_v0.13.zip` (16.325.431 byte).
- **Export ulang v0.12 (19 Nov 2026):** exit 0. `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah dikembalikan. File `.pck` diperiksa: MD5 `02f833cc29652158567abb2d79c5db5b` (berbeda dari v0.11 `8ccafc661e33ab3a6564370a0292334b`), berisi `village.gd` v0.12 + `save_manager.gd` (baru) + `player_chibi.gd` v0.9 + 4 GLB yang dipakai (58 entri, 5.659.739 byte isi, nol entri `addons/`). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene termuat dan mencetak v0.12, tombol Simpan ada, menu save tersembunyi (tanpa save), tanam petak 1 → file save ADA dan load dari PCK (karung 0, planted 1), usap timur menggerakkan pemain (-5 → 0 setelah 60 frame), tahan jalan timur 300 frame berhenti di tepi (x = 15,597, y ≈ 0, tidak jatuh), tombol AKSI membuka dialog Sastro, pelacak quest menunjukkan "★ Tujuan: Tanam padi di 3 petak sawah (1/3) — tekan E di petak kosong" (**PCK_CHECK PASS**). Uji otomatis **TEST V0.12 PASS 129/129**. Server HTTP lokal sementara (`python3 -m http.server 8941`, lalu dimatikan): 8 file utama status **200**. Zip: `REALM_web_v0.12.zip` (15.858.820 byte). Catatan jujur: save web tersimpan di IndexedDB browser per situs (hapus data situs / ganti browser = save hilang, tidak tersinkron antar perangkat); 9 SCRIPT ERROR di log export semuanya dari plugin editor (BetterTerrain/Cyclops, karena autoload dev dilepas sementara saat export) — bukan error game.
- **Export ulang v0.11 (19 Nov 2026):** exit 0, tanpa SCRIPT ERROR
  (hanya pesan leak shutdown generik + satu SCRIPT ERROR dari plugin
  editor Cyclops saat editor headless keluar — bukan error game).
  `run/main_scene` sudah dikembalikan ke Boot, 3 autoload dev sudah
  dikembalikan. File `.pck` diperiksa: MD5
  `8ccafc661e33ab3a6564370a0292334b` (berbeda dari v0.10
  `c641f515d1d948b8916b2a1d8606345c`), berisi `village.gd` v0.11 +
  `player_chibi.gd` v0.9 + 4 GLB yang dipakai (56 entri, 5.655.900 byte
  isi). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene
  termuat dan mencetak v0.11, usap timur menggerakkan pemain (x = 5,0
  setelah 60 frame), tahan jalan timur 300 frame berhenti di tepi
  (x = 15,597, y ≈ 0, tidak jatuh), tombol AKSI membuka dialog Sastro,
  pelacak quest menunjukkan "★ Tujuan: Tanam padi di 3 petak sawah
  (0/3) — tekan E di petak kosong" (**PCK_CHECK PASS**). Uji otomatis
  **TEST V0.11 PASS 88/88**. Server HTTP lokal sementara
  (`python3 -m http.server 8940`, lalu dimatikan): 8 file utama status
  **200**. Zip: `REALM_web_v0.11.zip` (15.866.683 byte).
- **Export ulang v0.10 (19 Nov 2026):** exit 0, tanpa SCRIPT ERROR
  (hanya pesan leak shutdown generik saat proses headless keluar).
  `run/main_scene` sudah dikembalikan ke Boot. File `.pck` diperiksa:
  MD5 `c641f515d1d948b8916b2a1d8606345c` (berbeda dari v0.9
  `9151e0caecb54d656f55498b5a366458`), berisi `village.gd` v0.10 +
  `player_chibi.gd` v0.9 + `Rogue_chibi.glb`.
  PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene
  termuat dan mencetak v0.10, usap timur menggerakkan pemain (x = 5,0
  setelah 60 frame), tahan jalan timur 300 frame berhenti di tepi
  (x = 15,6, y ≈ 0, tidak jatuh), tombol AKSI membuka dialog Sastro,
  pelacak quest menunjukkan "★ Tujuan: Tanam padi di 3 petak sawah
  (0/3) — tekan E di petak kosong" (**PCK_CHECK PASS**). Server HTTP
  lokal sementara (`python3 -m http.server 8939`, lalu dimatikan):
  8 file utama status **200** — `index.html`, `index.js`,
  `index.wasm` (38 MB), `index.pck` (15,0 MB),
  `index.audio.worklet.js`, `index.audio.position.worklet.js`,
  `index.png`, `index.icon.png`.
  Headless run scene mencetak `REALM — Chibi 3D v0.10… Gameplay:
  pelacak quest, sapaan Pak Sastro, magang setelah lulus trial, hama
  adil 14 detik.`, tanpa SCRIPT ERROR. Uji gameplay otomatis v0.10:
  **98/98 lolos** (runner sementara sudah dihapus) — quest, sapaan,
  3 magang, hama 14 detik + jeda dialog, regresi batas desa v0.9 dan
  kontrol. Backup v0.9 ada di `/tmp/REALM_web_v09_backup/`.
  Zip baru: `workspace/user/files/REALM_web_v0.10.zip` (24 MB).
- **Export ulang v0.9 (19 Nov 2026):** exit 0, tanpa SCRIPT ERROR
  (hanya pesan leak shutdown generik saat proses headless keluar).
  `run/main_scene` sudah dikembalikan ke Boot. File `.pck` diperiksa:
  MD5 `9151e0caecb54d656f55498b5a366458` (berbeda dari v0.8
  `336e66fc20ff4e4164bb1b6a1307947f`), berisi `village.gd` v0.9 +
  `player_chibi.gd` v0.9 + `Rogue_chibi.glb`.
  PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene
  termuat dan mencetak v0.9, usap timur menggerakkan pemain (x = 5,0
  setelah 60 frame), tahan jalan timur 300 frame berhenti di tepi
  (x = 15,6, y ≈ 0, tidak jatuh), tombol AKSI membuka dialog Sastro
  (**PCK_CHECK PASS**). Server HTTP lokal sementara
  (`python3 -m http.server 8938`, lalu dimatikan): semua file utama
  status **200** — `index.html`, `index.js`, `index.wasm` (38 MB),
  `index.pck` (15,0 MB), `index.audio.worklet.js`, `index.icon.png`.
  Headless run scene mencetak `REALM — Chibi 3D v0.9… Batas desa:
  tidak bisa keluar lalu jatuh.`, tanpa SCRIPT ERROR. Uji regresi
  otomatis v0.9: **65/65 lolos** (runner sementara sudah dihapus).
  Backup v0.8 ada di `/tmp/REALM_web_v08_backup/`.
  Zip baru: `workspace/user/files/REALM_web_v0.9.zip` (24 MB).
- **Export ulang v0.8 (19 Nov 2026):** exit 0, tanpa SCRIPT ERROR
  (hanya pesan leak shutdown generik saat proses headless keluar).
  `run/main_scene` sudah dikembalikan ke Boot. File `.pck` diperiksa:
  MD5 `336e66fc20ff4e4164bb1b6a1307947f` (berbeda dari v0.7
  `9b0ff2a30d9ddda5f68bdf7068ba3e00`), berisi `village.gd` v0.8.
  PCK diverifikasi dengan memuatnya ke proyek Godot kosong: scene
  termuat dan mencetak v0.8, usap menggerakkan pemain, D-pad
  menggerakkan pemain, tombol AKSI membuka dialog Sastro
  (**PCK_CHECK PASS**). Server HTTP lokal sementara
  (`python3 -m http.server 8937`, lalu dimatikan): semua file utama
  status **200** — `index.html`, `index.js`, `index.wasm` (38 MB),
  `index.pck` (14,9 MB), `index.audio.worklet.js`, `index.icon.png`.
  Headless run scene mencetak `REALM — Chibi 3D v0.8… Gerak usap HP
  (tanpa joystick visual) + D-pad + keyboard.`, tanpa SCRIPT ERROR.
  Uji regresi otomatis v0.8: **91/91 lolos**. Backup v0.7 ada di
  `/tmp/REALM_web_v07_backup/`.
  Zip baru: `workspace/user/files/REALM_web_v0.8.zip` (24 MB).
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

- **v0.22 ini hanya gameplay Jahit + SFX Jahit — tampilan TIDAK diperbaiki.** Keluhan
  sehnxi soal palet "tidak hidup", detailing karakter, baju ganti, dan
  "3D tapi kayak 1D" masih berlaku; perbaikan visual v1.0 dihentikan
  dan tidak dilanjutkan. Yang baru di v0.22: urutan motif Jahit diacak
  tiap percobaan (panel menampilkan urutan yang berlaku, tersimpan di
  save) + 3 SFX Jahit sendiri (bukan lagi SFX Tempa). Yang masih kurang
  di Jahit: motif masih 3 jenis yang sama (Parang/Mega/Kawung — hanya
  urutannya yang diacak, belum ada motif baru); SFX jahit masih
  sintesis sederhana (bukan rekaman jarum/gunting sungguhan); trial
  Jahit acak + SFX baru baru diuji headless — **belum dicek di HP
  sungguhan sehnxi**. Nama "Nyai Sekar" masih belum dikonfirmasi
  sehnxi. **Start web di browser sungguhan belum terverifikasi di VM
  ini** (tanpa Chromium/Firefox) — yang terbukti: pck ter-export start
  normal lewat `--main-pack` + PCK check; verifikasi di browser
  grafis dilakukan saat publish.
- **v0.21 ini hanya dialog interaktif + perbaikan bug start — tampilan TIDAK diperbaiki.** Keluhan
  sehnxi soal palet "tidak hidup", detailing karakter, baju ganti, dan
  "3D tapi kayak 1D" masih berlaku; perbaikan visual v1.0 dihentikan
  dan tidak dilanjutkan. Yang baru di v0.21: pilihan jawaban di dialog
  intro 4 NPC (3 pilihan per NPC, klik / keyboard 1/2/3 / tombol
  sentuh; semua cabang berakhir sama — sengaja, tidak ada trial yang
  terkunci) dan Boot yang kini meneruskan ke desa (bug start v0.20
  diperbaiki). Yang masih kurang di dialog: pilihan hanya di intro,
  belum ada potret chibi, kecepatan ketik tetap 50 huruf/detik.
  **Start web di browser sungguhan belum terverifikasi di VM ini**
  (tanpa Chromium/Firefox) — yang terbukti: pck ter-export start
  normal lewat `--main-pack` + PCK check; verifikasi di browser
  grafis dilakukan saat publish. `SaveSystem.setup()` masih menerima
  7 referensi sekaligus; `interaction_system.gd` (193 baris) masih
  memegang `setup` 9 parameter + `set_world` 9 parameter.
- **v0.14 ini hanya konten Penjahit — tampilan TIDAK diperbaiki.** Keluhan
  sehnxi soal palet "tidak hidup", detailing karakter, baju ganti, dan
  "3D tapi kayak 1D" masih berlaku; perbaikan visual v1.0 dihentikan
  dan tidak dilanjutkan. Yang baru di v0.14 (Nyai Sekar, trial Jahit,
  magang Penjahit, 3 tombol sentuh Jahit) baru diuji headless + emulasi
  sentuh — **belum dicek di HP sungguhan sehnxi**. Nama "Nyai Sekar"
  belum dikonfirmasi sehnxi (dari build Spaces); urutan motif Parang
  Sekar tetap sama setiap kali; "desain baju tahap pertama" baru berupa
  gelar/teks, belum ada lemari/baju yang bisa diganti di game Godot;
  SFX Jahit memakai ulang SFX Tempa.
- **Sudah dimainkan sehnxi di HP (link v0.8)** — dan dari situlah bug
  v0.9 ketemu: karakter bisa keluar desa lalu jatuh. v0.9 memperbaikinya
  (batas desa + dinding tak terlihat + jaring pengaman), tapi perbaikan
  itu baru diuji headless + emulasi sentuh — **masih harus dicek ulang
  di HP sungguhan sehnxi**: jalan ke 4 tepi desa dengan usap dan D-pad,
  pastikan karakter berhenti di tepi dan tidak jatuh. Ukuran D-pad
  84 px / tombol AKSI 150 px dalam viewport 1280×720 yang diskalakan
  ke layar HP juga belum dinilai di HP sungguhan.
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
