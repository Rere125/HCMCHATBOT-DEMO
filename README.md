# HRD Chat Bot — Demo (Portfolio)

Folder ini adalah **hasil build statis** dari project `Hcmchatbot-main`,
khusus untuk dipajang di portfolio. Semua info pribadi/perusahaan asli
sudah disamarkan untuk versi demo ini:

- Nama bot diganti jadi **"HRD Chat Bot"** (generic, bukan nama
  perusahaan asli).
- Logo/foto perusahaan diganti jadi **avatar ikon generic** (SVG),
  bukan file gambar asli.
- Semua pertanyaan & jawaban FAQ diganti dengan **data sampling/dummy**
  seputar topik HR umum (cuti, kontrak, klaim medis, slip gaji) — supaya
  pengunjung portfolio tetap bisa coba chat interaktif tanpa melihat
  data perusahaan asli.
- Demo ini **tidak terhubung ke Supabase/database apa pun** — semua data
  FAQ murni statis di frontend, dan halaman admin sengaja tidak
  disertakan di build ini.

Kode JavaScript-nya juga sudah di-*minify* dan di-*obfuscate*, jadi
orang yang buka DevTools cuma lihat kode acak yang susah dibaca/ditiru
— bukan source code asli (JSX/React) yang ada di folder `Hcmchatbot-main`.

## Isi folder

```
Hcmchatbot-demo/
├── netlify.toml     # config deploy Netlify (static hosting, no build step)
├── index.html
└── assets/
    ├── index-*.css
    └── index-*.js   # sudah di-obfuscate
```

## Cara deploy ke Netlify

1. Push folder ini (atau seluruh repo) ke GitHub.
2. Di Netlify → "Add new site" → "Import an existing project" → pilih
   repo, lalu set **Base directory** ke `Hcmchatbot-demo` (kalau di-push
   satu repo bareng project lain).
3. Build command dikosongkan (biarin default), publish directory `.`
   (sudah otomatis kebaca dari `netlify.toml`).
4. Deploy. Demo langsung online tanpa expose source code maupun data
   perusahaan asli.

## Catatan

- Demo ini murni statis (tanpa Supabase), jadi tombol "Edit/Hapus FAQ"
  di admin tidak disertakan sama sekali — fokus demo cuma di sisi chat
  publik yang interaktif.
- Kalau source code (`src/`) di `Hcmchatbot-main` berubah, folder demo
  ini perlu di-generate ulang (build + samarkan data + obfuscate)
  supaya sinkron.
- Tidak ada perubahan **logika/alur** chat dari project asli (bubble
  chat, tombol pilihan, typing indicator, akhiri/mulai chat baru semua
  identik) — yang diganti cuma nama, avatar, dan isi pertanyaan/jawaban.

