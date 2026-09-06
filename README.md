# HCM FAQ Bot — Demo (Portfolio)

Folder ini adalah **hasil build statis** dari project `Hcmchatbot-main`,
khusus untuk dipajang di portfolio. Kode JavaScript-nya sudah di-*minify*
dan di-*obfuscate*, jadi orang yang buka DevTools cuma lihat kode acak
yang susah dibaca/ditiru — bukan source code asli (JSX/React) yang ada
di folder `Hcmchatbot-main`.

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
4. Deploy. Demo langsung online tanpa expose source code asli.

## Catatan

- Demo ini pakai kredensial Supabase **placeholder/demo**, bukan
  kredensial project asli. Kalau mau demo yang benar-benar fungsional,
  build ulang dari `Hcmchatbot-main` pakai Supabase project demo kamu
  sendiri, baru obfuscate hasil build-nya.
- Kalau source code (`src/`) di `Hcmchatbot-main` berubah, folder demo
  ini perlu di-generate ulang (build + obfuscate) supaya sinkron.
- Tidak ada perubahan fitur/fungsi apa pun dari project asli — folder
  ini murni hasil build + obfuscate untuk keperluan showcase.
