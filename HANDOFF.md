# Handover: lanjutkan JAPANESE HANGOUT lewat Roblox Studio MCP

Kamu berjalan di PC pengguna (Windows), di folder repo `E:\MY PROJECT\Japanese Hangout`
(GitHub: `andytuandi/japanese-hangout-roblox-map`). Roblox Studio terbuka dengan place
**[Beta] JAPANESE HANGOUT** (experience ID `10151770531`, game hangout/roleplay/santai bertema Jepang).

## Tentang pengguna
- Menulis dalam bahasa Indonesia; balas dalam bahasa Indonesia yang sederhana (pengguna masih pemula).
- Ingin pekerjaan dikerjakan otomatis; jangan banyak bertanya kecuali benar-benar perlu keputusannya.

## Aturan penting
- **Map sudah jadi dan dibangun manual.** Jangan memindah, menghapus, atau membangun ulang bangunan/model/terrain
  kecuali diminta. Tugasmu menambahkan logika (script), bukan mengubah desain.
- **Repo hanya untuk backup script.** Roblox Studio adalah sumber utama. Jangan jalankan `rojo serve`
  (bisa menimpa script di Studio).
- Jangan **Publish** ke Roblox tanpa izin pengguna.

## Tugas
1. Pastikan MCP Roblox Studio tersambung (`/mcp`). Jika tidak, bantu pengguna menyambungkannya dulu.
2. Pelajari isi place lewat MCP: struktur Workspace, ServerScriptService, ReplicatedStorage, StarterGui,
   StarterPlayer, script yang sudah ada, dan objek yang terlihat dimaksudkan untuk interaksi/event
   (ProximityPrompt, ClickDetector, Seat, pintu, NPC, panggung, area musik, kios/toko, festival, part bernama
   "Event"/"Trigger"/sejenisnya, RemoteEvent yang belum dipakai).
3. Buat daftar event yang ada/terlihat direncanakan di map, beserta usulan perilakunya. Tunjukkan daftar
   singkat ke pengguna, lalu langsung kerjakan kecuali pengguna menolak.
4. Implementasikan event-eventnya:
   - Logika penting di server (Script di ServerScriptService); UI/efek di client (LocalScript).
   - Komunikasi client-server lewat RemoteEvent di ReplicatedStorage, dengan validasi di server.
   - Gunakan tag CollectionService/attribute agar mudah ditambah di Studio tanpa mengubah kode.
   - Tangani error dengan aman (pcall untuk DataStore/HTTP), jangan sampai satu error mematikan script lain.
5. Uji di Studio (Play / Play Solo lewat MCP jika bisa), periksa Output untuk error, lalu perbaiki.
6. Backup: salin source semua script yang kamu buat/ubah ke repo sesuai `default.project.json`
   (`src/server` → ServerScriptService.Server, `src/client` → StarterPlayerScripts.Client,
   `src/shared` → ReplicatedStorage.Shared; gunakan `.server.luau`, `.client.luau`, `.luau`).
   Script yang berada di tempat lain (mis. di dalam model di Workspace) simpan di `src/workspace/<path>/`
   dan catat lokasi aslinya di README. Commit dengan pesan jelas lalu `git push`.
7. Akhiri dengan ringkasan untuk pengguna: event apa saja yang sudah jalan, cara mencobanya di Studio,
   dan apa yang belum/perlu keputusan mereka.
