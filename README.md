# Japanese Hangout — Roblox Map

Source code untuk experience Roblox **[Beta] JAPANESE HANGOUT** (experience ID `10151770531`).

## Struktur

| Folder | Masuk ke (di Studio) | Isi |
| --- | --- | --- |
| `src/server` | `ServerScriptService.Server` | Script server |
| `src/client` | `StarterPlayer.StarterPlayerScripts.Client` | LocalScript |
| `src/shared` | `ReplicatedStorage.Shared` | ModuleScript yang dipakai server & client |

Map (bangunan, terrain, model) tetap disimpan di place Roblox. Repo ini hanya menyimpan script
supaya punya riwayat versi dan bisa di-review.

## Cara sinkron dengan Roblox Studio

1. Pasang [Rokit](https://github.com/rojo-rbx/rokit), lalu di folder ini jalankan `rokit install`.
2. Pasang plugin Rojo di Studio (`rojo plugin install`).
3. Jalankan `rojo serve`, buka JAPANESE HANGOUT di Studio, klik **Connect** di plugin Rojo.
4. Script di `src/` sekarang tersinkron ke Studio. Tekan **Play** untuk mencoba, lalu **Publish**.

Cek kode: `selene src`.
