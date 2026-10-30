# Website Ulang Tahun untuk Ade cipa

Kejutan ulang tahun personal untuk **Syifa Sukma Hayati (ade cipa)**, dibuat oleh **Noval (amas)**. Website ini dibungkus seperti scrapbook digital: kertas krem, polaroid, tulisan tangan, dan kue baby blue.

Semua ada dalam satu file `index.html`. Tidak ada build step, backend, atau package yang perlu di-install.

## Fitur

- **Layar pembuka** dengan countdown ke 13 Maret 2027 dan tombol "Buka kejutan". Fokus keyboard dikunci di layar ini sampai kejutan dibuka.
- **Hero** dengan ucapan ulang tahun, hati melayang, balon, dan confetti.
- **Timeline empat bab** kenangan, ditutup dengan momen resmi jadi tunangan amas.
- **Galeri polaroid** dengan empat foto yang bisa dibuka dalam lightbox, plus satu kartu kutipan.
- **Surat** dengan efek ketik dan paragraf yang muncul saat discroll.
- **Kue interaktif** dengan rakitan tingkat kue yang mengikuti scroll, tombol tiup lilin, dan kartu doa.
- **Musik** kotak musik original yang dibuat dengan Web Audio API, mulai setelah kejutan dibuka, dan bisa dimatikan lewat tombol di kanan bawah.
- **Progress scroll** dan parallax ringan.
- **Fallback** untuk reduced motion, JavaScript mati, dan foto yang belum tersedia.

## Teknologi

| Bagian | Dipakai |
| --- | --- |
| Layout | Bootstrap 5.3.3 via CDN |
| Ikon | Bootstrap Icons 1.11.3 via CDN |
| Font | Fredoka, Nunito, dan Caveat dari Google Fonts |
| Animasi | CSS transition, IntersectionObserver, requestAnimationFrame |
| Musik | Web Audio API, melodi original tanpa file audio |
| Confetti | Canvas 2D |

Tidak ada dependency lokal dan tidak perlu `npm install`.

## Cara menjalankan

Buka `index.html` langsung di browser. Koneksi internet tetap diperlukan untuk Bootstrap, ikon, dan font dari CDN.

Kalau mau lewat local server:

```bash
python -m http.server 8000
```

Lalu buka `http://localhost:8000`.

Alternatif lain:

```bash
npx serve .
```

## Struktur folder

```text
website-ultah/
├── index.html    # seluruh website: markup, CSS, JavaScript
├── foto1.jpg     # foto hero
├── foto2.jpg     # galeri
├── foto3.jpg     # galeri
├── foto4.jpg     # galeri
├── foto5.jpg     # galeri
├── prompt.md     # brief awal project
└── README.md
```

## Yang bisa diganti

### Foto

Foto yang ada sekarang adalah placeholder berlabel. Ganti dengan foto asli, tetap dengan nama file yang sama:

- `foto1.jpg` untuk foto besar di hero, rasio 4:5.
- `foto2.jpg` sampai `foto5.jpg` untuk galeri.

Foto dipotong otomatis dengan `object-fit: cover`. Kalau mau memakai nama file lain, ubah `src`, `alt`, `data-file`, dan `data-caption` di bagian galeri.

### Nama, tanggal, dan umur

Semua teks ada langsung di `index.html`. Cari bagian yang relevan:

- Countdown: `const BIRTHDAY = new Date(2027, 2, 13, 0, 0, 0);` di bagian script. Angka `2` berarti Maret karena bulan dimulai dari `0`.
- Angka umur di kue: cari `<text ...>24</text>` di SVG kue.
- Nama dan panggilan: cari `ade cipa`, `Syifa Sukma Hayati`, dan `amas`.
- Meta description dan judul halaman ada di `<head>`.

### Teks dan cerita

Setiap section punya komentar `GANTI:` di dekat bagian yang perlu diedit, misalnya timeline, surat, caption foto, dan pesan penutup. Gaya bahasanya sengaja santai, jadi kalau mengubah teks, pertahankan nada amas ke ade.

### Warna dan font

Warna diatur lewat CSS variable di `:root`, termasuk `--blue-300`, `--rose`, `--paper`, dan `--ink`. Font dimuat dari Google Fonts di `<head>` dan dipakai di beberapa aturan CSS. Kalau mengganti font, sesuaikan nama family di CSS.

### Musik

Musik default adalah melodi kotak musik original yang dibuat dengan Web Audio API, jadi tidak ada file audio. Kalau mau memakai lagu sendiri, ikuti komentar di bagian `Musik kotak musik` pada `index.html`.

### Animasi kue

Urutan dan timing rakitan kue ada di `cakeAssemblyParts`:

```js
{ el: ..., start: 0.02, end: 0.34, lift: -46 }
```

`start` dan `end` adalah posisi progress scroll (0 sampai 1). Naikkan nilainya kalau ingin bagian kue muncul lebih lambat.

## Aksesibilitas

- Bisa dipakai dengan keyboard: Tab, Shift+Tab, Enter, dan Escape.
- Fokus keyboard terkunci di layar pembuka dan lightbox.
- Fokus kembali ke tombol asal setelah lightbox ditutup.
- Ada skip link ke konten utama.
- `prefers-reduced-motion` mematikan animasi dan langsung menampilkan kue utuh.
- Tanpa JavaScript, layar pembuka disembunyikan dan seluruh konten tetap bisa dibaca.
- Target sentuh minimal 44 px di semua breakpoint.

## Sudah dites

- Layout 320, 360, 390, 768, 1024, 1280, dan 1440 px tanpa horizontal overflow.
- Tidak ada error di console.
- Kontras teks lolos WCAG AA.
- Lightbox, musik, tombol tiup lilin, dan anchor link berfungsi.
- Reduced motion dan no-JS menampilkan konten dengan benar.

## Kredit

- Bootstrap 5 dan Bootstrap Icons.
- Font Fredoka, Nunito, dan Caveat dari Google Fonts.
- Melodi musik dibuat khusus untuk project ini, bukan lagu berhak cipta.
- Foto saat ini adalah placeholder, ganti dengan foto pribadi sebelum dibagikan.
