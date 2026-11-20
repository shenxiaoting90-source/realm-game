# REALM — Versi Web (HTML5) dari Prototipe Godot Chibi 3D

**Dibuat:** 19 November 2026. Gratis 100%, tanpa bayar.
**Isi:** desa Wilwatikta 3D chibi **v0.33** (di-export ulang 20 Nov 2026
dari ChibiVillage v0.33) — **baru: RUMAH & KEBUN NOVICE — karakter kini
punya rumah sendiri di selatan desa (Rumah Novice, di (-10, 14), lengkap
dengan label RUMAH NOVICE) + 2 petak kebun rumah yang tanam-panennya
sama seperti sawah (terpengaruh musim, hama, dan bonus pet); E di pintu
rumah = "Istirahat" — tidur sampai besok: hari game +1 (tugas harian
baru diganti), padi tumbuh 120 detik selama tidur, hama tenang; tidur di
ujung musim bisa membalik musim; spawn tetap di tempat semula** —
**baru juga: FESTIVAL DESA tiap 3 hari game (hari 3, 6, 9, …) — alun-alun
berhias lampion bambu prosedural (emas + ungu, tanpa aset baru), keempat
mentor berkumpul di alun-alun dengan dialog festival, tugas festival:
sapa 4 mentor di hari festival → +10 Gold (sekali per festival)** —
**baru juga: CERITA DESA "Kisah Wilwatikta" — alur berantai dari Pak
Sastro (dimulai saat bicara Sastro setelah lulus Trial Tani), 5 langkah
memakai aksi yang sudah ada: tanam 1 petak di kebun (+5 Gold), bicara
Nyai Kirana soal pasar festival (+5), 1 pukulan bagus di landasan (+5),
1 langkah jahit benar untuk panji festival (+10) — total +25 Gold;
langkah aktif tampil di pelacak quest dan seksi "Desa" baru (ke-7) di
Menu; semua state baru tersimpan di save (save lama tetap kebuka)** —
**perbaikan juga: LATIHAN BEBAS setelah lulus — landasan/tenun tidak
lagi diblokir sesudah magang selesai (dulu "Kamu sudah lulus…" menutup
aksi), jadi pemain yang sudah lulus tetap bisa tempa/jahit kapan saja;
panel tempa/jahit menutup sendiri saat pemain berjalan menjauh (>4 m)**
— **v0.32 tetap: LOOP HARIAN — tiap hari game
(120 detik main aktif) ada 3 tugas harian acak dari 6 macam (Tanam 2
petak, Panen 1 karung, Dagang 1x di lapak, Tempa 1 pukulan bagus,
Bicara dengan 1 NPC, Jahit 1 langkah motif benar), masing-masing
selesai memberi +5 Gold (maks +15 Gold/hari); tugas berganti tiap
hari baru dan yang belum selesai HANGUS (tidak menumpuk); sapaan
harian berubah mengikuti hari/musim/progres ("Hari ke-N, musim
Kemarau. Pak Sastro menunggumu di sawah."); NPC INGAT — Pak Sastro,
Empu Wira, Nyai Kirana, Nyai Sekar berkomentar berbeda sesudah trial
mereka lulus (judul dialog baru `again`, 2 baris per NPC); seksi
KOLEKSI baru di Menu (4 trial, 4 magang, 4 skill, pet + tier, musim
yang pernah dilewati, tugas harian yang pernah selesai — hanya yang
benar-benar ada di game); semua state harian tersimpan di save
(save lama tetap kebuka)** — **baru juga: HUD RESPONSIF HP — font
membesar di layar kecil (skala dari lebar viewport: desktop ≥1000 px
×1,0; 700–1000 px ×1,15; HP <700 px ×1,25 — di HP 390 px: judul fs28,
tugas harian fs19, prompt fs23, isi Menu fs18, AKSI fs33); bar atas
jadi tumpukan kolom di HP, baris Trial/Musim disembunyikan (isinya di
Menu), tombol AKSI 170×170 + Menu 120×48, panel Menu tidak mepet tepi
(margin ≥12 px), prompt/dialog/pilihan selalu di atas AKSI dan di
dalam layar; di desktop ≥1000 px tampilan SAMA PERSIS seperti v0.31;
warna/palet dan angle kamera TIDAK diubah** — **v0.31 tetap: PET
BERTINGKAT — Ayam Kampung
(prosedural, tanpa aset baru): didapat dari Pak Sastro setelah lulus
Trial Tani (bukan dibeli); mengikuti pemain di desa (jejak langkah,
cepat 6 m/dtk, tetap di dalam pagar, tidak menembus bangunan);
tier Biasa → Bagus → Langka → Super Rare — naik otomatis lewat
panen (Bagus 10 karung, Langka 20 karung); bonus NYATA: padi tumbuh
lebih cepat (Biasa 10%, Bagus 20%, Langka 30%, Super Rare 40% —
Kemarau 2,7 / 2,4 / 2,1 / 1,8 dtk per tahap) + Jual Pasti tambah Gold
(Bagus +2, Langka +5, Super Rare +10); Super Rare TIDAK naik
otomatis — hanya lewat GM / quest rahasia (fondasi kode saja di
prototipe single-player ini: belum ada NPC GM, quest rahasia baru
berupa petunjuk tersembunyi di Rumpun Bambu); pet berteduh di emper
rumah saat Hujan dan pemain jauh; pet + tier + petunjuk tersimpan di
save (save lama tetap kebuka); seksi Pet baru di Menu (nama, tier,
bonus, kemajuan, petunjuk)** — **baru juga: PERBAIKAN TUMPUKAN PANEL
MENU (cacat sejak v0.29 — judul seksi menempel/menutupi baris isi,
baris Musim ketutup kepala "Status Skill"): posisi semua baris kini
diukur dari tinggi render sebenarnya (isi fs14, kepala fs17, judul
fs20) dengan celah 4–6 px, baris panjang wrap DI DALAM panel (tidak
lagi meluber keluar), tombol di dalam panel; dicek headless di 4
keadaan (belum pet, Biasa, Langka + petunjuk, Super Rare)** —
**v0.30 tetap: MUSIM Kemarau/Hujan — berganti
otomatis tiap 360 detik bermain aktif (1 hari game 120 dtk, 1 musim 3
hari), berpengaruh NYATA ke sawah: Kemarau padi tumbuh lambat (3,0
dtk/tahap = 6 dtk total) + hama jarang (jeda 18 dtk, pertama 14 dtk),
Hujan padi tumbuh cepat (1,5 dtk/tahap = 3 dtk total) + hama sering
(jeda 7 dtk, pertama 6 dtk); visual: partikel hujan + langit/tanah
lebih gelap saat Hujan, langit terang + tanah kering saat Kemarau;
musim + perkiraan ganti musim tampil di HUD dan Menu > Status
Karakter; musim + sisa waktu tersimpan di save (save lama tetap
kebuka, default Kemarau); Trial Tani tetap 3 karung; modul baru
`season_system.gd` (178 baris), `signal_wiring.gd` tetap 25
`connect()` (tanpa sinyal baru)** — **v0.29 tetap: D-pad DIHAPUS, tombol Menu + panel
Status/Skill/Tas/Opsi, tulisan bar atas efek 3D, layar loading dengan
progres + tips** (gerakkan HP kini HANYA usap layar — tidak ada lagi
node D-pad / tombol arah / cara memunculkannya; modul HUD baru
`game_menu.gd` (199 baris): tombol Menu kiri bawah + panel tengah
Status Karakter (nama Novice, gelar Murid/Pemula per job, Gold,
Karung), Status Skill (4 skill mentor: Baca Tanda Musim, Pukul Tepat
Waktu, Baca Pasar, Desain Baju tahap 1 — terkunci/terbuka + syaratnya),
Tas Item (HANYA Gold + Karung padi yang benar-benar dimiliki + 4 slot
kosong), Opsi (Suara Nyala/Mati + Simpan manual — tombol Simpan/Suara
lama di HUD PINDAH ke dalam menu, fungsinya tidak hilang); gameplay
DIJEDA saat menu terbuka (tick + input + fisika pemain mati, seperti
menu save; buka/tutup: tombol Menu/Tutup atau keyboard M / Esc —
ditolak saat dialog / menu save / panel dagang / panel jahit terbuka);
tulisan bar atas (judul, instruksi, status, quest, Karung/Gold, status
trial, "Ujian Panen") memakai `make_3d_label` baru di `hud_widgets.gd`
— JUJUR efek timbul outline + bayangan jatuh di HUD 2D, BUKAN Label3D;
layar loading kustom `web_shell/realm_shell.html` (judul REALM, persen
+ MB terunduh, 6 tips bergilir) — unduhan pertama tetap ~46 MB (wasm
39,5 MB + pck 6,3 MB + js) sehingga loading awal tetap berat di
internet lambat, yang diperbaiki adalah loading yang TERLIHAT, bukan
ukuran unduhannya; `signal_wiring.gd` kini 25 `connect()` (+2 menu);
`village.gd` 221 baris (handler `_on_menu_requested`); perilaku game
lain SAMA PERSIS seperti v0.28) — **wiring sinyal v0.27 tetap** — wiring sinyal pindah dari village.gd
ke helper `signal_wiring.gd` (semua 23 `connect()` antar sistem —
nama sinyal, pengirim, penerima, urutan — SAMA PERSIS seperti v0.26;
`village.gd` 231 → 214 baris, hanya memanggil
`SignalWiring.wire(ctx, self)` sekali; handler desa tetap di
`village.gd`; perilaku game SAMA PERSIS seperti v0.26, tanpa fitur
baru dan tanpa perubahan tampilan) — **pangkas v0.26 tetap** — village.gd dipangkas (305 → 231
baris) + guard urutan rakit WorldContext (`check_registered` /
`check_trial_modules`; `_ready` dua fase — buat + daftarkan semua
sistem dulu, baru `setup(ctx)` berurutan; perilaku game SAMA PERSIS
seperti v0.25, tanpa fitur baru dan tanpa perubahan tampilan) — **refactor setup v0.25 tetap** — satu WorldContext
(`WorldContext` dirakit `village.gd` sekali, diberikan ke `setup(ctx)`
tiap sistem menggantikan deretan parameter `SaveSystem` 7 dan
`InteractionSystem` 9+9; komunikasi tetap lewat sinyal; perilaku game
SAMA PERSIS seperti v0.24, tanpa fitur baru dan tanpa perubahan
tampilan) — **pagar bambu v0.24 tetap** — pagar bambu prosedural di ±23,3 sepanjang 4 sisi tepi
(92 tiang + 8 bilah, tanpa gerbang — dunia di luar belum ada); saat
pemain mendorong ke tepi ~1 detik, status/HUD menampilkan "Ujung desa
— pagar bambu. Dunia di luar belum terbuka." (sekali per mentok,
hilang saat menjauh); BOUND tetap 23.0, dinding collision tetap di
±23.0; **desa diperbesar v0.23 tetap** — tanah desa 48×48 m (batas
gerak pemain BOUND 23.0, dinding tepi v0.9 dipindah ke tepi baru,
jaring pengaman y < −2 tetap), area timur baru (x > 17) berisi 3 petak
sawah tambahan (total 6 petak, trial Tani tetap butuh 3 karung),
rumpun bambu, sumur kecil kedua, jalan tanah ke alun-alun, dan label
lokasi 3D "SAWAH TIMUR" + "RUMPUN BAMBU" (total 6 label);
**trial Jahit diacak v0.22 tetap** — urutan motif
Parang Sekar kini diacak tiap percobaan
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
6,3 MB** (6.643.060 byte, NAIK hanya 1.200 byte dari 6.641.860 v0.22 — hanya kode + objek desa baru v0.23, tanpa audio/model baru; runtime Dialogue Manager kini ikut ter-export, karena
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
sentuh HP (tanpa D-pad sejak v0.29 — gerak hanya usap layar, tombol AKSI kanan bawah
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
| `index.pck` | Data game: scene ChibiVillage, script, aset KayKit + audio (6,3 MB; v0.30 6.660.260 byte, MD5 `b5445d17cf4f76b3164353aad9a80d6e`, berbeda dari v0.29, berisi `season_system.gd` baru (musim Kemarau/Hujan: siklus 360 dtk bermain aktif, tumbuh 3,0/1,5 dtk per tahap, jeda hama 18/7 dtk, partikel hujan + langit/tanah berubah, label musim HUD + Menu > Status Karakter, musim + `season_time` tersimpan di save, save lama default Kemarau) + `game_menu.gd` baru (modul HUD: tombol Menu + panel Status Karakter / Status Skill / Tas Item / Opsi; Simpan + Suara pindah ke dalam menu) + `touch_controls.gd` tanpa D-pad + `hud_widgets.gd` `make_3d_label` (outline + shadow) + shell loading kustom `web_shell/realm_shell.html` (judul + persen MB + 6 tips; file shell TIDAK ikut ke pck — `web_shell/*` di `exclude_filter`) + `village.gd` 221 baris (handler `_on_menu_requested` + jeda menu) + `signal_wiring.gd` 25 `connect()` (+2 menu) + desa 48×48 m + area timur (`builder_terrain`/`builder_farm`/`builder_buildings` v0.23 — tanah 48 m, BOUND 23.0, 6 petak, rumpun bambu, sumur timur, jalan timur, label SAWAH TIMUR/RUMPUN BAMBU; `save_manager.gd` PLOT_COUNT 6 + clamp posisi ±23; save lama 3 petak tetap bisa di-load) — dan yang lama tetap: urutan motif Jahit acak (`roll_sew_sequence` + `sew_sequence` di `game_state.gd`/`save_manager.gd`, label target di `trial_panels.gd`, 2 baris `sekar.dialogue` diubah) + 3 SFX Jahit (`sfx_sew_good`/`sfx_sew_miss`/`sfx_sew_done` di `audio_system.gd` + `trial_sew.gd`) — dan yang lama tetap: `boot.gd` meneruskan ke ChibiVillage + panel pilihan jawaban di `hud_main.gd` + `choose_response` di `dialogue_system.gd` + 12 balasan pilihan di 4 `.dialogue` + `prompt_system.gd` + `interaction_system.gd` (193 baris) + facade `hud_system.gd` (241 baris, tanpa ~35 referensi node lama) + `village.gd` (224 baris) + 6 modul refactor v0.19 (`interaction_system`, `world_primitives`, `builder_terrain`, `builder_buildings`, `builder_farm`, `builder_actors`) + facade `world_builder.gd` (75 baris) + koordinator `trial_system.gd` (116 baris) + 4 resource `.dialogue` (Sastro/Wira/Kirana/Sekar, sebagai `.godot/imported/*.tres`) + runtime Dialogue Manager 4.2.0 (`addons/dialogue_manager/`, 92 entri; filter export membuang semua addon KECUALI `dialogue_manager` — tanpanya semua dialog gagal di web) + 2 file sistem v0.17 (`save_system`, `dialogue_effects`) + 10 modul v0.16 (`hud_main`, `trial_panels`, `touch_controls`, `save_menu`, `hud_widgets`, `plot_system`, `trial_farming`, `trial_forge`, `trial_trade`, `trial_sew`) + `save_manager.gd` + `player_chibi.gd` v0.9 + `npc_sekar.gd` + 4 GLB yang dipakai — Rogue_chibi, Rogue_Hooded, Barbarian, Mage — + bangunan desa + musik ambient + 10 SFX + blip ketik (dibuat saat runtime, tanpa file baru); NAIK hanya 7.260 byte dari v0.29, hanya kode musim + label musim; tidak ada GLB baru; tidak ada addon lain yang ikut; file basi `index.pck-Z3j9Q8` (786 KB, sisa export lama, tidak dirujuk `index.html`/`index.js`) dihapus dari folder ini) |
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
dan WebAssembly. RAM disarankan 2 GB+. Di HP kini ada kontrol sentuh (usap layar + tombol
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
- **Di HP (layar sentuh, v0.6–v0.28 pakai D-pad, v0.29 D-pad dihapus):** gerak hanya **usap layar** mengikuti arah usapan (tanpa joystick/D-pad),
  tombol **AKSI** kanan bawah sebagai pengganti E (bicara, lanjut
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

- **Export ulang v0.33 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export. Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik, MD5 `3e4d566f15083838de224c1f26633215`). File `.pck` diperiksa: MD5 `025b179b931eb6f43323db998cb7fa00` (berbeda dari v0.32 `92c4942c9d8d42a104f10d3a1ef1f7e2`, 6.729.368 byte — NAIK 21.928 byte: modul baru `home_system.gd` + `festival_system.gd` + `story_system.gd`, Rumah Novice + 2 petak kebun, dekor festival prosedural, 8 dialog baru (`~ festival` + `~ story` di keempat mentor), seksi Menu "Desa" ke-7, tanpa aset/model/audio baru). PCK diverifikasi dengan memuatnya (`ProjectSettings.load_resource_pack`, checker `tools/check_pck_v33.gd`): Boot dari PCK meneruskan ke ChibiVillage, wiring 31 connect, dialog festival/cerita ada, home/festival/story di village/ctx/tick, 8 petak, Rumah Novice + label, FestivalDecor tersembunyi hari 1, `desa_text`, tidur +1 hari, festival hari 3 (dekor + Sastro berkumpul), save berisi story_step/nights_slept/festival_talked (**PCK_CHECK PASS, 93/93**). Uji otomatis **TEST V0.33 PASS 1164/1164** (runner `tools/test_v33.gd` — regresi v0.10–v0.32 + fitur baru + uji tepi; 2 run pertama gagal karena bug runner, bukan game: cache import Dialogue Manager basi — `.tres` di `.godot/imported/` belum berisi cue `festival`/`story`, diperbaiki dengan `--headless --import` sebelum test; lalu asumsi urutan cerita di test salah — cerita ternyata dimulai di dialog Sastro pertama setelah lulus Tani, bukan di seksi festival, test direstrukturisasi mengikuti alur nyata). Zip baru: `workspace/user/files/REALM_web_v0.33.zip` (16.648.346 byte, MD5 `c60cd93fcd289f7d9c5833e349d3cfb7`). **TIDAK dipublish** — publish dilakukan terpisah oleh tugas lain.
- **Export ulang v0.30 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export (9 SCRIPT ERROR yang ada semuanya dari plugin editor Cyclops/BetterTerrain saat export headless — bukan error game). Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik, MD5 `3e4d566f15083838de224c1f26633215`). File `.pck` diperiksa: MD5 `b5445d17cf4f76b3164353aad9a80d6e` (berbeda dari v0.29 `006c5c99255f14225a7fecb7616403f2`, 6.660.260 byte — NAIK hanya 7.260 byte: modul `season_system.gd` baru (178 baris) + angka musim di GameState/SaveManager + label musim HUD/Menu, tanpa audio/model baru). Shell HTML kustom `web_shell/realm_shell.html` terverifikasi di hasil export: placeholder `$GODOT_CONFIG`/`$GODOT_THREADS_ENABLED` diganti exporter (nol literal tersisa), `fileSizes` terhitung ulang (pck 6.660.260, wasm 39.514.754), judul "REALM — Desa Wilwatikta", elemen persen + 6 tips ada. PCK diverifikasi dengan memuatnya ke proyek Godot kosong (checker adaptasi v0.29 + 34 cek musim): Boot dari PCK meneruskan ke ChibiVillage, `season_system.gd` termuat dari PCK + punya `update`/`apply_visuals`/`season_label_text`/`season_effect_text`, musim awal Kemarau (label HUD, langit terang, tanah kering, tidak hujan), timer tanam Kemarau 3,0 vs Hujan 1,5 dtk, visual Hujan (hujan + langit gelap + tanah basah), musim berganti otomatis (359 dtk → Hujan + status), musim di Menu > Status Karakter, Trial Tani lulus di Kemarau + magang lulus di Hujan, 4 trial + magang, hama, save roundtrip musim + save lama → Kemarau, 25 sambungan sinyal hidup, menu game, tepi + jaring pengaman + kontrol + AKSI (**PCK_CHECK PASS, 174/174**). Server HTTP lokal sementara (`python3 -m http.server 8947`, lalu dimatikan): 5 file utama status **200** (index.html 9.175 byte berisi shell kustom). Uji otomatis **TEST V0.30 PASS 336/336** (runner sementara `tools/test_v30.gd` — 4 run; semua kegagalan run awal adalah bug runner, bukan game: pemanggilan helper async tanpa `await` tidak memblokir pemanggil (90 pemanggilan diperbaiki); hitung `connect(` mentah ikut komentar; teks "~6 dtk" baru muncul saat planted_count >= 3; `validate: season 5` dijepit ke 1; label HUD musim butuh frame setelah Lanjut; status "merusak" bisa ditimpa "padi menguning"; prompt "jauh dari hama" flaky karena hama memilih petak acak). Backup v0.29 dibuat di `/tmp/REALM_web_v29_backup/` (pck MD5 cocok v0.29). Zip baru: `workspace/user/files/REALM_web_v0.30.zip`.
- **Export ulang v0.29 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export (9 SCRIPT ERROR yang ada semuanya dari plugin editor Cyclops/BetterTerrain saat export headless — bukan error game). Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik, MD5 `3e4d566f15083838de224c1f26633215`). File `.pck` diperiksa: MD5 `006c5c99255f14225a7fecb7616403f2` (berbeda dari v0.28 `03266111544ac7ded97a5f5f204524fb`, 6.653.000 byte — NAIK hanya 5.092 byte: modul `game_menu.gd` baru + hapus D-pad + label 3D + shell loading kustom, tanpa audio/model baru). Shell HTML kustom `web_shell/realm_shell.html` terverifikasi di hasil export: placeholder `$GODOT_CONFIG`/`$GODOT_THREADS_ENABLED` diganti exporter (nol literal tersisa), `fileSizes` terhitung ulang (pck 6.653.000), judul "REALM — Desa Wilwatikta", elemen persen + 6 tips ada. PCK diverifikasi dengan memuatnya ke proyek Godot kosong (checker ditulis ulang dari pola v0.28): Boot dari PCK meneruskan ke ChibiVillage (`current_scene` = ChibiVillage), `game_menu.gd` termuat dari PCK + punya `show_menu`/`refresh`/`hide_menu`, `hud.game_menu` ada, tidak ada node DPad, tombol Menu ada, tidak ada lagi SaveButton/MuteButton HUD, judul + label Karung 3D (outline + shadow), ke-25 sambungan sinyal hidup via `is_connected` (+2 menu), menu game dari PCK (M membuka, kamera BEKU + fisika mati saat terbuka, isi Status/Skill/Tas benar, Esc menutup, simpan + bisu dari menu, tombol Tutup), menu diblokir saat dialog terbuka, dialog Sastro + pilihan jawaban + bunyi ketik, 4 trial lulus (Tani + magang Petani, Tempa + magang, Dagang + magang, Jahit acak + magang), hama muncul + prompt jauh/dekat + diusir, save roundtrip + bisu + tepi timur + pesan mentok + jaring pengaman + keyboard/usap/event usap sungguhan + tombol AKSI menanam petak timur (**PCK_CHECK PASS, 140/140**). Server HTTP lokal sementara (`python3 -m http.server 8946`, lalu dimatikan): 5 file utama status **200** (index.html 9.155 byte berisi shell kustom). Uji otomatis **TEST V0.29 PASS 179/179** (runner sementara sudah dihapus) — struktur v0.29 + menu lengkap (buka/tutup M/Esc/tombol, isi 4 bagian, jeda tick/input/fisika, blokir modal, tombol sentuh Dagang/Jahit tetap muncul) + usap 4 arah + event usap sungguhan + regresi v0.10–v0.28 (6 kegagalan pertama adalah bug runner, bukan game: menutup dialog dari baris pertama tanpa menjawab pilihan tidak bisa — uji blokir dipindah ke dalam alur dialog; tombol AKSI memakai sinyal `button_down` bukan `pressed`; magang Tempa/Dagang/Jahit belum dijalankan sehingga gelar Pemula belum ada — magang ditambahkan ke runner; cari tombol Tutup/Simpan lewat `find_child` di node GameMenu padahal panelnya anak CanvasLayer — tombol kini disimpan sebagai var modul). Backup v0.28 dibuat di `/tmp/REALM_web_v28_backup/` (pck MD5 cocok v0.28). Zip baru: `workspace/user/files/REALM_web_v0.29.zip`. **Jujur:** tidak ada Chromium/Firefox di VM ini, jadi halaman HTML/JS di browser grafis sungguhan belum bisa diverifikasi di sini — verifikasi browser dilakukan terpisah saat publish. **TIDAK dipublish** — publish dilakukan terpisah oleh tugas lain.
- **Export ulang v0.28 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export (9 SCRIPT ERROR yang ada semuanya dari plugin editor Cyclops/BetterTerrain saat export headless — bukan error game). Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik, MD5 `3e4d566f15083838de224c1f26633215`). File `.pck` diperiksa: MD5 `03266111544ac7ded97a5f5f204524fb` (berbeda dari v0.27 `03c979a88b14a32f64e63a1a1a73d210`, 6.647.908 byte — NAIK hanya 1.496 byte: helper `village_tick.gd` baru, tanpa audio/model baru). PCK diverifikasi dengan memuatnya ke proyek Godot kosong (checker ditulis ulang dari pola yang terdokumentasi karena `/tmp` terhapus restart runtime): Boot dari PCK meneruskan ke ChibiVillage (`current_scene` = ChibiVillage), `village_tick.gd` termuat dari PCK + punya `tick`/`setup`, `village.tick` hidup + mengisi quest, `ctx` lolos `check_registered`/`check_trial_modules`, ke-23 sambungan sinyal hidup via `is_connected`, 6 petak, BOUND 23.0, pagar bambu + label timur, dialog Sastro + pilihan jawaban + bunyi ketik, 4 trial lulus (Tani + magang Petani, Tempa, Dagang, Jahit acak), hama muncul + prompt jauh/dekat + diusir, save roundtrip + bisu + tepi timur + pesan mentok + jaring pengaman + keyboard/usap (**PCK_CHECK PASS, 105/105**). Catatan jujur: script di PCK terkompilasi (`.gdc` + `.remap`), bukan sumber `.gd` — cek isi sumber tidak bisa dilakukan dari PCK, yang diuji adalah perilaku dari PCK. Server HTTP lokal sementara (`python3 -m http.server 8945`, lalu dimatikan): 5 file utama status **200**. Uji otomatis **TEST V0.28 PASS 240/240** (runner sementara sudah dihapus) — struktur VillageTick + regresi v0.10–v0.27 (3 kegagalan pertama adalah bug runner, bukan game: pemanggilan helper async tanpa `await` sehingga jalan di latar; desa harus jadi `current_scene` supaya `_process` jalan di headless; prompt jauh hama dicek saat pemain masih berdiri di petak yang diserang). Backup v0.27 dibuat di `/tmp/REALM_web_v27_backup/` (pck MD5 cocok v0.27). Zip baru: `workspace/user/files/REALM_web_v0.28.zip`. **Jujur:** tidak ada Chromium/Firefox di VM ini, jadi halaman HTML/JS di browser grafis sungguhan belum bisa diverifikasi di sini — verifikasi browser dilakukan terpisah saat publish. **TIDAK dipublish** — publish dilakukan terpisah oleh tugas lain.
- **Export ulang v0.23 (20 Nov 2026):** exit 0, tanpa SCRIPT ERROR game di log export (8 SCRIPT ERROR yang ada semuanya dari plugin editor Cyclops/BetterTerrain saat export headless — bukan error game). Main scene tetap Boot (TIDAK diganti sementara — sejak v0.21 Boot meneruskan ke ChibiVillage). `run/main_scene` tetap Boot, 3 autoload dev sudah dikembalikan (`project.godot` dipulihkan identik). File `.pck` diperiksa: MD5 `9f6bf8625f522585fb7e13695d20c535` (berbeda dari v0.22 `877d809fc0681766f14aa21470a0898b`, 6.643.060 byte — NAIK hanya 1.200 byte: desa 48×48 m + area timur, tanpa audio/model baru). PCK diverifikasi dengan memuatnya ke proyek Godot kosong: Boot dari PCK meneruskan ke ChibiVillage (`current_scene` = ChibiVillage), SaveSystem + DialogueEffects ada, 4 modul HUD + 5 modul trial ada, InteractionSystem ada (tanpa `compute_prompt`) + PromptSystem ada, fasad hud tidak lagi mengekspos `title_label`, bangunan builder (Plaza/Well/TailorHouse/Irrigation) + 6 label lokasi ada (baru: SAWAH TIMUR + RUMPUN BAMBU), BambooGrove + WellEast ada, 6 petak, BOUND 23.0, panel trial tersembunyi, NPC Sekar di (12,5, 6,8), autoload DialogueManager + `sastro.dialogue` termuat, efek ketik + bunyi ketik jalan, dialog Sastro → `met_sastro`, tanam petak 1 → file save ada + quest (1/3), usap timur menggerakkan pemain, tahan jalan timur 300 frame berhenti di tepi baru (22,597, y ≈ 0), tanam petak timur → planted_count 2, tombol bisu → bus di-mute + save muted true, dialog Sekar → `sew_ready` + 3 SFX Jahit ada di AudioSystem, motif acak (bukan `[1,2,3,1]` lama) → panel menampilkan urutan itu → langkah benar → `sew_good` → lulus Jahit → save berisi urutan itu, dialog Wira → `forge_ready` + 3 pukulan bagus → lulus Tempa, dialog Kirana → `trade_ready` + Jual Pasti +10 → gold 20 + lulus Dagang (**PCK_CHECK PASS, 53/53**). Server HTTP lokal sementara (`python3 -m http.server 8941`, lalu dimatikan): 5 file utama status **200**. Uji otomatis **TEST V0.23 PASS 158/158** (runner sementara sudah dihapus) — batas desa baru 4 arah + usap diagonal + jaring pengaman, petak timur tanam/panen, label baru, + regresi v0.10–v0.22 (2 kegagalan pertama adalah bug runner, bukan game: cek matang petak timur tanpa jeda frame; pencarian tombol D-pad dari node TouchControls, bukan `touch_root`). Backup v0.22 dibuat di `/tmp/REALM_web_v22_backup/` (45 MB, MD5 pck cocok v0.22). Zip baru: `workspace/user/files/REALM_web_v0.23.zip` (16.566.380 byte, MD5 `1fd57fcb7aa5c4c2c73c5529efd1343a`). **Jujur:** tidak ada Chromium/Firefox di VM ini, jadi halaman HTML/JS di browser grafis sungguhan belum bisa diverifikasi di sini — verifikasi browser dilakukan terpisah saat publish. **TIDAK dipublish** — publish dilakukan terpisah oleh tugas lain.
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

- **v0.23 ini hanya perluasan desa — tampilan TIDAK diperbaiki.** Keluhan
  sehnxi soal palet "tidak hidup", detailing karakter, baju ganti, dan
  "3D tapi kayak 1D" masih berlaku; perbaikan visual v1.0 dihentikan
  dan tidak dilanjutkan. Yang baru di v0.23: tanah 48×48 m (BOUND 23),
  3 petak sawah tambahan (total 6, trial Tani tetap 3 karung), rumpun
  bambu, sumur timur kedua, jalan timur, label SAWAH TIMUR + RUMPUN
  BAMBU. Yang masih kurang: desa 48×48 m masih SANGAT jauh dari skala
  1 juta orang (2.304 m², masih single-player, tanpa server/sharding);
  dinding tepi baru tetap tidak terlihat; bambu tidak beranimasi; sumur
  timur hanya dekorasi; kamera tidak diubah sehingga ujung timur sudah
  di tepi pandangan dari spawn. Desa baru + petak timur baru diuji
  headless — **belum dicek di HP sungguhan sehnxi**. Nama "Nyai Sekar"
  masih belum dikonfirmasi sehnxi. **Start web di browser sungguhan
  belum terverifikasi di VM ini** (tanpa Chromium/Firefox) — yang
  terbukti: pck ter-export start normal + PCK check; verifikasi di
  browser grafis dilakukan saat publish.
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
  di HP sungguhan sehnxi**: jalan ke 4 tepi desa dengan usap,
  pastikan karakter berhenti di tepi dan tidak jatuh. Tombol AKSI
  150 px dalam viewport 1280×720 yang diskalakan
  ke layar HP juga belum dinilai di HP sungguhan.
  (D-pad sudah dihapus di v0.29 — gerak HP kini hanya usap layar.)
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
