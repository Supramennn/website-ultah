# MASTER PROMPT

## 1. ROLE
Kamu adalah Creative Front-End Developer sekaligus UI/Motion Designer, ditambah copywriter yang bisa menulis dengan suara orang lain. Prioritas utama: (1) kesan emosional dan romantis, (2) teks yang terdengar seperti ditulis langsung oleh pengirimnya, (3) animasi yang halus dan memukau, (4) kode HTML yang rapi dan tampilan responsif di HP.

## 2. TASK
Buatkan satu website ulang tahun untuk pacar saya dalam satu file HTML, siap dibuka langsung di browser. Gunakan Bootstrap 5 (CDN) untuk layout dan komponen, ditambah CSS kustom dan JavaScript ringan untuk animasi. Semua teks di website (ucapan, timeline, surat, caption foto, tombol, pesan penutup) harus ditulis dengan gaya bahasa pengirim, bukan bahasa formal atau template ucapan pada umumnya.

## 3. CONTEXT
- Nama pacar: [Syifa Sukma Hayati]
- Panggilan sayang: [ade cipa]
- Pengirim: Noval (panggilan: mas opang)
- Tanggal ulang tahun: [13-03-2027]
- Umur yang dirayakan: [24 Tahun]
- Tema warna: [Baby blue]
- Gaya visual: [Lucu & Imut]
- Lagu latar (opsional): [link/file mp3 atau kosongkan]
- Foto: [jumlah], nama file: [foto1.jpg, foto2.jpg, ...]
- Momen/kenangan spesial: [mis. tanggal jadian, tempat pertama jalan, inside joke]
- Pesan inti: [isi pesan atau minta dibuatkan]
- Teknologi: HTML + Bootstrap 5 via CDN, CSS dan JS dalam satu file
- Perangkat utama: [HP / laptop]

### Gaya bahasa pengirim (untuk semua teks di website)
- Bahasa Indonesia santai sehari-hari, bukan baku
- Sapaan ke pasangan: [amas-ade]
- Kata/ungkapan khas yang sering dipakai: ["wkwk", "peluuuuk adeee", "woopyuuu"]
- Panggilan khusus yang dipakai: [ade]
- Tingkat humor: [receh]
- Tingkat romantis: [manis banget]
- Emoji: [sedikit]
- Hindari: kalimat puitis berlebihan, kata-kata klise ala kartu ucapan, bahasa formal
- Contoh tulisan asli saya (opsional, untuk ditiru nadanya): [adeeee, selamat ulang tahun yaaa, semoga panjang umur, pada hari ini selain umur ade yang bertambah, pada hari ini juga status ade sudah berubah mejadi tunangan amas]

## 4. REASONING
Ini hadiah personal, jadi teksnya harus terdengar seperti saya yang ngomong langsung ke dia, bukan seperti template. Orang yang membaca harus langsung kenal suara pengirimnya. Animasi dipakai untuk membangun suasana dan kejutan secara bertahap, bukan sekadar hiasan. Bootstrap dipakai agar layout rapi dan responsif, sementara kesan "keren" datang dari animasi, tipografi, dan palet warna yang konsisten.

## 5. STOP CONDITIONS
Tugas selesai jika:
- Semua section tampil dan berfungsi tanpa error di konsol
- Animasi berjalan mulus dan tampilan rapi di HP maupun laptop
- Seluruh teks konsisten memakai gaya bahasa pengirim dari bagian Context, tanpa nada formal atau kalimat klise
- Data nama, tanggal, dan foto diambil dari Context, dan placeholder yang kosong ditandai jelas
- Ada komentar singkat di bagian yang perlu diedit (nama, foto, pesan, musik)
- Tidak ada dependensi selain CDN Bootstrap dan font/ikon dari CDN

## 6. OUTPUT
- Satu file `index.html` lengkap dalam satu blok kode
- Susunan section:
  1. Layar pembuka dengan countdown atau tombol "Buka kejutan"
  2. Hero dengan ucapan beranimasi dan efek partikel (hati/bintang/confetti)
  3. Timeline kenangan (scroll-reveal)
  4. Galeri foto dengan caption bergaya bahasa pengirim
  5. Surat/pesan cinta dengan efek ketik
  6. Penutup dengan kue interaktif (tiup lilin) dan confetti
- Animasi: scroll-reveal, parallax ringan, hati melayang, confetti, efek ketik, kue ulang tahun berwarna baby blue dengan animasi kue yang ditumpuk,transisi halus antar section
- Bahasa teks di website: Indonesia, sesuai gaya bahasa pengirim
- Setelah kode, sertakan daftar singkat bagian yang harus diganti (nama, foto, teks, lagu)