# Learning Activity — GitHub-ready

Versi ini sudah dibersihkan dari ketergantungan Replit yang tidak perlu untuk deployment frontend.

## Yang sudah diubah
- `vite.config.ts` tidak lagi mewajibkan environment Replit (`PORT`, `BASE_PATH`, plugin Replit).
- `package.json` sudah diubah menjadi standalone sehingga bisa di-install tanpa monorepo Replit.
- `src/hooks/use-learning-data.ts` mendukung `VITE_APPS_SCRIPT_URL`.
- `vercel.json` ditambahkan agar route SPA seperti `/dashboard` tidak 404 di Vercel.
- `public/_redirects` ditambahkan agar route SPA bekerja di Cloudflare Pages / Netlify-style hosts.

## Cara jalan lokal
```bash
npm install
npm run dev
```

## Build
```bash
npm run build
```

## Deploy yang direkomendasikan
### Opsi A — Cloudflare Pages
- Framework preset: Vite
- Build command: `npm run build`
- Build output directory: `dist`

### Opsi B — Vercel
- Framework: Vite
- Build command: `npm run build`
- Output directory: `dist`

## Environment variable opsional
Jika URL Google Apps Script berubah, set:
- `VITE_APPS_SCRIPT_URL`

Kalau tidak diisi, app tetap memakai URL Apps Script yang ada saat ini.
