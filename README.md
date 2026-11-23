# أسماء الزائرين للمشاريع تحت المجلس الإشرافي ١٤٤٨ هـ

Situs statis (tema biru) di GitHub Pages. Data tersimpan di Google Sheet, pengedit memakai **PIN**.

## Isi folder
- `index.html` : aplikasi
- `config.js` : tempat URL Apps Script
- `logo.png` : logo Al-Majlis Al-Isyrafy
- `Code.gs` : backend (ditempel di Apps Script, TIDAK diunggah ke GitHub)
- `.nojekyll`

## Langkah 1: Backend (Google Sheet BARU, terpisah dari aplikasi proyek)
1. Buat Google Sheet baru, mis. "Database Zuwar 1448". Buka **Ekstensi > Apps Script**.
2. Hapus isi default, tempel seluruh isi `Code.gs`, ganti `const PIN = '...'` dengan PIN rahasia, lalu simpan.
3. **Deploy > Deployment baru > Aplikasi web**: Jalankan sebagai **Saya**, akses **Siapa saja**. Setujui izin, lalu salin URL berakhiran `/exec`.

## Langkah 2: Repo GitHub BARU
1. Buat repo baru, misalnya `zuwar-1448` (Public). Unggah isi folder ini (`index.html`, `config.js`, `logo.png`, `.nojekyll`).
2. Isi `config.js`: `SCRIPT_URL: "https://script.google.com/macros/s/XXXX/exec"` lalu commit.
3. **Settings > Pages > Deploy from a branch > main / (root)**.
4. Situs: `https://kafalah-duat.github.io/zuwar-1448/`.

## Langkah 3: Pakai
Klik **تسجيل الدخول للتحرير**, masukkan PIN. Di halaman tiap proyek: klik lingkaran untuk memilih foto, isi nama, alamat, dan tujuan kunjungan.

## Catatan
- Foto otomatis dikecilkan (160 px) lalu disimpan di Google Sheet, jadi tidak perlu hosting gambar.
- Ganti PIN / ubah Code.gs: **Deploy > Kelola deployment > Edit > Versi baru > Deploy** (URL tetap).
- Siapa pun yang tahu URL bisa **membaca** data (termasuk foto); hanya yang tahu PIN yang bisa **mengubah**.
- Jangan ubah nama tab `DEPTS` dan `DB`, dan jangan menyisipkan baris kosong di tengah data.
