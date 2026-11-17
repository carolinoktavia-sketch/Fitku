# FitKu — Aplikasi Gym, Kalori & Pengingat (gratis)

Aplikasi web (PWA) yang dibangun dari desain Google Stitch FitKu.
Bisa dipasang di **iPhone & iPad** seperti aplikasi biasa, jalan offline, tanpa akun, tanpa biaya.

## Pasang GRATIS lewat GitHub Pages (± 10 menit, cukup sekali)

1. Buat akun gratis di https://github.com (kalau belum punya).
2. Klik **+ → New repository** → nama: `fitku` → pilih **Public** → **Create repository**.
3. Di halaman repo, klik **uploading an existing file**.
4. Ekstrak `FitKu-website.zip` di laptop. Isinya ±66 file **tanpa folder**.
   Di GitHub klik **choose your files** → buka folder hasil ekstrak → tekan **Ctrl+A** (pilih semua) → **Open**.
   Tunggu sampai semua file selesai terunggah → klik **Commit changes**.
5. Buka **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** / **(root)** → **Save**.
6. Tunggu 1–2 menit. Alamat aplikasi: `https://NAMA-AKUN-GITHUB.github.io/fitku/`

## Pasang di iPhone & iPad

1. Buka alamat di atas dengan **Safari**.
2. Ketuk **Bagikan** (kotak dengan panah ke atas) → **Tambah ke Layar Utama** → **Tambah**.
3. Buka FitKu dari ikon petir oranye. Lakukan hal yang sama di iPad.

## Penting diketahui

- **Data tersimpan di perangkat masing-masing** (tanpa server = tanpa biaya). Untuk memindahkan data
  iPhone ⇄ iPad: menu *Lainnya → Cadangkan data* (AirDrop / iCloud Drive) lalu *Pulihkan data* di perangkat lain.
- **Pengingat saat aplikasi ditutup:** menu *Pengingat → Pasang di Kalender iPhone* (file .ics). Ini cara gratis
  yang paling andal di iPhone. Saat FitKu terbuka, pengingat juga muncul sebagai banner + bunyi.
- **Pindai barcode** memakai database gratis Open Food Facts (butuh internet). Produk yang belum ada bisa diisi manual.
- Gambar gerakan dari *free-exercise-db* (domain publik), file `ex-*.webp` (2 frame per file) sehingga tetap tampil offline.
- Angka kalori/protein/air adalah perkiraan (rumus Mifflin-St Jeor), bukan pengganti saran dokter/ahli gizi.

## Untuk mengubah kode (opsional, misalnya di Antigravity)

Butuh Node.js 18+:

```
npm install
npm run dev      # coba di laptop
npm run build    # hasil siap upload ada di folder dist/
```

Struktur: `src/data` (gerakan, makanan, program 12 minggu), `src/lib` (rumus target, progresi beban, streak, pengingat),
`src/screens` (semua layar), `tailwind.config.js` (warna & tipografi dari DESIGN.md Stitch).
Setelah menambah ikon baru, ikon Material Symbols perlu di-subset ulang atau ganti `src/assets/symbols.woff2`
dengan file lengkap dari paket `material-symbols`.
