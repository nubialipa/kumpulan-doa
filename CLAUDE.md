# Proyek: Kumpulan Doa Pagi & Sore

## Tujuan
Situs statis berisi kumpulan doa pagi dan sore, di-deploy ke GitHub Pages
secara otomatis via GitHub Actions.

## Sumber konten
- Tidak memakai PDF. Teks zikir dan doa ditulis langsung di `site/index.html`
  (array `DATA` dan konstanta bacaan di dalam `<script>`).
- Situs statis ada di `site/` (index.html). Hanya folder ini yang di-deploy.

## Aturan teknis
- Situs harus berupa HTML/CSS/JS statis murni. Tidak ada framework build.
- Semua gaya dan skrip inline di `site/index.html`. Satu-satunya dependensi eksternal adalah font Amiri dari Google Fonts.
- Jangan menambahkan dependensi npm atau proses build.
- Konten doa: teks Arab (RTL), latin, dan terjemahan Indonesia.
- Tampilan bergaya Symbian S60 dengan warna ungu: status bar, title bar, grid menu, daftar, dan softkey di bawah.

## Konvensi konten
- Setiap bacaan memiliki `arab`, `latin`, `arti`, dan `ulang` (jumlah target hitungan).
- Sebelum publish, cocokkan lafal dan jumlah bacaan dengan rujukan zikir yang sahih.

## Perintah
- Preview lokal: `python3 -m http.server 8000 --directory site`
- Deploy: push ke `main` (GitHub Actions otomatis men-deploy folder `site/`).

## Konvensi
- Setiap doa adalah section dengan heading level 2.
- Nama file Markdown: `[pagi|sore]-[slug-doa].md`.
- Jangan mengubah teks doa; hanya format presentasi yang boleh disesuaikan.
