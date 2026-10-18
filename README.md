# 🌙 Jelajah Tadabbur Alam Juz 30

Game penjelajahan **3D** bergaya kotak-kotak untuk mata pelajaran **Tadabbur Alam dalam Juz 30**
di **Kuttab Raudhah Nabawiyah**. Isinya disusun dari 8 Modul Ajar PAI (RPP KD2).

Santri berjalan mengelilingi sebuah pulau, menemukan **32 Lentera Ayat**, membaca ayat beserta terjemahnya,
merenungkan tadabbur, kisah, dan adabnya, lalu menjawab satu pertanyaan untuk mendapat bintang ⭐.

## Enam wilayah (sesuai urutan modul)

| Wilayah | Modul | Contoh isi |
|---|---|---|
| 🌱 Kebun Tumbuhan | Tumbuhan | Biji tumbuh, anggur, kurma, tin & zaitun, daun dimakan ulat |
| 🐪 Padang Hewan | Hewan | Hewan ternak, unta, unta Nabi Shalih, pasukan bergajah, burung Ababil |
| ⛰️ Pegunungan | Daratan | Gunung sebagai pasak, Gunung Thur, gunung saat kiamat |
| 🌊 Sungai & Laut | Perairan | Laut dipanaskan & meluap, sungai-sungai di surga |
| 🌍 Lembah Bumi | Bumi (2 modul) | Pemilik langit & bumi, bumi dihamparkan, 7 lapis bumi, gempa kiamat |
| 🌙 Bukit Langit | Bulan & Bintang, Langit | Bulan purnama, Lailatul Qadar, gugusan bintang, tujuh langit |

Saat mendaki Bukit Langit, siang berubah menjadi **malam berbintang**.

## Fitur

- Teks ayat **Rasm Utsmani** dan **terjemah Kemenag**, dengan font Amiri Quran yang sudah tertanam (tetap benar walau font internet gagal dimuat).
- Tombol **🔊 Dengarkan murottal** (Syaikh Mishary Alafasy, dari everyayah.com; butuh internet).
- **Buku Tadabbur** untuk membaca ulang lentera yang sudah ditemukan (murajaah hafalan).
- **Peta pulau** dan **panah kuning** yang menunjuk lentera berikutnya sesuai urutan modul.
- Avatar **Ikhwan (peci)** atau **Akhwat (kerudung)** dengan pilihan warna baju.
- Jawaban salah tidak dihukum, santri diminta membaca lagi lalu mencoba kembali.
- Progres tersimpan otomatis di perangkat. **Sertifikat** muncul setelah 32 lentera ditemukan.

## Cara upload ke GitHub Pages

1. Buka [github.com](https://github.com) → **New repository** → beri nama, misalnya `tadabbur-alam` → **Public** → **Create repository**.
2. Klik **uploading an existing file**, seret `index.html` dan `README.md`, lalu **Commit changes**.
3. Buka **Settings → Pages** → *Source*: **Deploy from a branch** → branch **main**, folder **/ (root)** → **Save**.
4. Setelah 1–2 menit, game bisa dibuka di `https://NAMA-AKUN.github.io/tadabbur-alam/`.

Game membutuhkan internet saat pertama dibuka (untuk memuat mesin 3D three.js).

## Kontrol

| Aksi | Laptop | HP / Tablet |
|---|---|---|
| Berjalan | W A S D / panah | Geser jempol di sisi kiri layar |
| Memutar kamera | Seret mouse, scroll untuk zoom | Geser di sisi kanan layar |
| Melompat | Spasi | Tombol ⤒ |
| Membaca lentera | E | Tombol "Baca Lentera" |
| Buku / Peta | B / M | Tombol 📖 / 🗺️ |

Disarankan memegang HP dalam posisi mendatar.

## Mengubah isi materi

Semua materi ada di bagian `const STATIONS=[` di dalam `index.html`. Contoh satu lentera:

```js
{z:'tumbuhan', t:'Zaitun dan Kurma', p:[63,-42], m:'palm', ay:['80:29'],
 tad:'Teks tadabbur…',
 kisah:'Teks kisah (opsional)…',
 adab:'Teks adab (opsional)…',
 q:['Pertanyaan?', 'Jawaban benar', ['Pengecoh 1','Pengecoh 2']]},
```

Teks ayat dan terjemah untuk setiap rujukan di `ay` diambil dari data `AYAT` di file yang sama.
Untuk menambah ayat baru di luar 61 ayat yang sudah ada, teks Arab dan terjemahnya perlu ditambahkan ke `AYAT`.

## Kredit

- Teks Al-Qur'an & terjemah: data Tanzil / Kemenag RI (melalui paket `quran-json`).
- Font: Amiri Quran (SIL Open Font License), Fredoka.
- Mesin 3D: three.js. Audio murottal: everyayah.com.
- Game bergaya kotak-kotak buatan sendiri, tidak berafiliasi dengan Roblox.
