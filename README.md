# Vortex Arena — Champions Are Rising

Vortex Arena adalah rancangan halaman website untuk sebuah gaming arena yang menyediakan berbagai fasilitas gaming, mulai dari area gaming reguler, ruang VIP, studio streaming, hingga simulator racing.

Project saat ini masih berada pada tahap awal dan **baru menggunakan struktur HTML**. README ini menjelaskan struktur HTML yang sudah tersedia agar anggota tim lain dapat memahami fungsi setiap bagian sebelum project dikembangkan lebih lanjut.

---

## 1. Struktur Halaman

Struktur HTML saat ini secara umum terdiri dari:

```text
HTML
│
├── Head
│   ├── Meta Charset
│   ├── Meta Viewport
│   ├── Title
│   └── Google Fonts
│
└── Body
    ├── Navbar
    │   ├── Logo
    │   ├── Menu Navigasi
    │   ├── WhatsApp
    │   └── Tarif & Reservasi
    │
    ├── Hero / Banner Utama
    │   ├── Background
    │   ├── Label
    │   ├── Judul
    │   ├── Deskripsi
    │   └── Tombol
    │
    └── Zona Gaming
        ├── Judul
        ├── Deskripsi
        ├── Tab Zona
        └── Detail Zona
            ├── Kode
            ├── Nama
            ├── Harga
            ├── Gambar
            ├── Judul
            ├── Label
            └── Statistik
```

---

# 2. Informasi Dasar HTML

Dokumen dimulai dengan:

```html
<!DOCTYPE html>
<html lang="id">
```

`<!DOCTYPE html>` memberitahu browser bahwa dokumen menggunakan HTML5.

Sedangkan:

```html
<html lang="id">
```

menunjukkan bahwa bahasa utama halaman adalah Bahasa Indonesia.

---

# 3. Bagian `<head>`

Bagian `<head>` berisi informasi yang dibutuhkan oleh browser mengenai halaman website.

Struktur saat ini:

```html
<head>
    <meta charset="utf-8">

    <meta
        name="viewport"
        content="width=device-width, initial-scale=1, viewport-fit=cover"
    >

    <title>
        Vortex Arena — Champions Are Rising
    </title>

    <link
        href="..."
        rel="stylesheet"
    >

    <link rel="stylesheet" href="">
</head>
```

---

## 3.1 Character Encoding

```html
<meta charset="utf-8">
```

Digunakan untuk menentukan encoding karakter yang digunakan oleh halaman.

Dengan UTF-8, halaman dapat menampilkan berbagai karakter termasuk karakter Bahasa Indonesia seperti:

```text
é
à
ñ
```

dan karakter lainnya dengan benar.

---

## 3.2 Viewport

```html
<meta
    name="viewport"
    content="width=device-width, initial-scale=1, viewport-fit=cover"
>
```

Tag ini digunakan untuk mengatur bagaimana halaman ditampilkan pada perangkat dengan ukuran layar berbeda.

Bagian:

```text
width=device-width
```

berarti lebar halaman mengikuti lebar perangkat.

Sedangkan:

```text
initial-scale=1
```

menentukan skala awal halaman.

---

## 3.3 Title

```html
<title>Vortex Arena — Champions Are Rising</title>
```

Merupakan judul halaman yang biasanya ditampilkan pada:

* Tab browser
* Bookmark
* Beberapa hasil pencarian

---

## 3.4 Google Fonts

HTML juga sudah memanggil Google Fonts:

```html
<link
    href="https://fonts.googleapis.com/..."
    rel="stylesheet"
>
```

Font yang digunakan dalam rancangan ini adalah:

* Inter
* JetBrains Mono

Pemanggilan font tersebut sudah disiapkan pada HTML, tetapi pengaturan penggunaan font di halaman belum dibahas dalam project ini.

---

# 4. Bagian `<body>`

Semua konten yang akan terlihat oleh pengguna berada di dalam:

```html
<body>
    ...
</body>
```

Saat ini body memiliki dua bagian utama:

1. Navbar
2. Hero
3. Zona Gaming

---

# 5. Navbar

Navbar dibuat menggunakan elemen:

```html
<nav>
    ...
</nav>
```

Navbar merupakan bagian navigasi utama website.

Strukturnya:

```text
Navbar
│
├── Logo Vortex Arena
│
├── Menu
│   ├── Arena
│   ├── Zona Gaming
│   ├── Spek PC
│   ├── Tarif Paket
│   └── Daily Menu
│
└── Action
    ├── WhatsApp
    └── Tarif & Reservasi
```

---

# 6. Logo

Bagian logo:

```html
<a class="logo" href="#atas">
    <i class="bingkai-gambar" data-img="logo"></i>
    Vortex Arena
</a>
```

Logo menggunakan elemen `<a>` sehingga dapat diklik.

```html
href="#atas"
```

berarti ketika logo diklik, browser akan menuju elemen HTML yang memiliki:

```html
id="atas"
```

Elemen logo juga memiliki:

```html
<i class="bingkai-gambar" data-img="logo"></i>
```

`data-img="logo"` merupakan data attribute yang menandai bahwa elemen tersebut digunakan untuk gambar logo.

---

# 7. Menu Navigasi

Menu navigasi berada di:

```html
<div class="menu-pil" id="navigasiPil">
```

Di dalamnya terdapat beberapa link:

```html
<a href="#atas" class="aktif">Arena</a>

<a href="#bagian-zona">
    Zona Gaming
</a>

<a href="#bagian-spek">
    Spek PC
</a>

<a href="#bagian-tarif">
    Tarif Paket
</a>

<a href="#bagian-menu">
    Daily Menu
</a>
```

Menu tersebut menggunakan sistem anchor HTML.

Contohnya:

```html
<a href="#bagian-zona">Zona Gaming</a>
```

akan mengarah ke elemen yang memiliki:

```html
id="bagian-zona"
```

Pada HTML yang sekarang, bagian `bagian-zona` sudah tersedia.

Sementara:

```text
bagian-spek
bagian-tarif
bagian-menu
```

sudah digunakan sebagai tujuan navigasi, tetapi section tersebut belum terdapat pada kode HTML yang diberikan.

---

# 8. Tombol WhatsApp

Navbar memiliki tombol:

```html
<a
    class="tombol-wa"
    href="https://wa.me/"
    id="waAtas"
>
    WhatsApp
</a>
```

Tombol ini disiapkan untuk mengarahkan pengguna ke WhatsApp.

Saat ini URL masih:

```text
https://wa.me/
```

sehingga nomor WhatsApp sebenarnya belum dimasukkan.

---

# 9. Tombol Tarif & Reservasi

Terdapat tombol:

```html
<a
    class="tombol putih"
    href="#bagian-tarif"
>
    Tarif & Reservasi
</a>
```

Tombol ini dirancang untuk mengarahkan pengguna ke bagian tarif dan reservasi.

Namun section:

```html
id="bagian-tarif"
```

belum tersedia pada HTML saat ini.

---

# 10. Hero Section

Bagian utama halaman menggunakan:

```html
<header
    class="banner-utama"
    id="atas"
>
```

Hero merupakan bagian pertama yang dilihat pengguna ketika membuka website.

Struktur hero:

```text
Hero
│
├── Background
│
└── Isi
    ├── Label
    ├── Judul
    ├── Deskripsi
    └── Tombol
```

ID:

```html
id="atas"
```

digunakan sebagai tujuan link untuk kembali ke bagian atas halaman.

---

# 11. Background Hero

Background hero disiapkan menggunakan:

```html
<div
    class="latar bingkai-gambar"
    data-img="hero"
></div>
```

Bagian pentingnya adalah:

```html
data-img="hero"
```

Atribut tersebut memberikan informasi bahwa elemen ini diperuntukkan bagi gambar hero.

Saat ini HTML hanya mendefinisikan tempat atau elemen untuk gambar tersebut.

---

# 12. Isi Hero

Konten hero berada di:

```html
<div class="isi">
```

Di dalamnya terdapat beberapa elemen.

---

## 12.1 Label

```html
<span class="label-atas teks-mono">
    CASUAL GAMERS / PRO ESPORTS
</span>
```

Label ini menjelaskan target utama Vortex Arena.

Konsep target yang disebutkan adalah:

* Casual gamers
* Pro esports

---

## 12.2 Judul Utama

```html
<h1>
    Vortex Arena, Champions Are Rising.
</h1>
```

`<h1>` merupakan heading utama halaman.

Pada halaman ini, teks tersebut digunakan sebagai headline utama Vortex Arena.

---

## 12.3 Deskripsi

```html
<p>
    Tempat berkumpulnya semua gamer:
    pemain santai, live streamer,
    pemburu rank, lire turnamen,
    hingga komunitas esports.
    ...
</p>
```

Elemen `<p>` digunakan untuk memberikan deskripsi mengenai Vortex Arena.

Informasi yang diperkenalkan antara lain:

* Gamer casual
* Live streamer
* Pemain rank
* Pemain turnamen
* Komunitas esports
* PC gaming
* Monitor 240Hz
* Internet cepat
* Lingkungan gaming yang nyaman

---

# 13. Tombol Hero

Hero memiliki dua tombol utama.

### Tombol Tarif

```html
<a
    class="tombol putih"
    href="#bagian-tarif"
>
    Lihat Tarif & Reservasi
</a>
```

Tombol ini ditujukan untuk menuju bagian tarif dan reservasi.

---

### Tombol Zona Gaming

```html
<a
    class="tombol garis"
    href="#bagian-zona"
>
    Jelajahi Zona Gaming
</a>
```

Tombol ini menuju:

```html
<section id="bagian-zona">
```

yang memang sudah tersedia di HTML.

---

# 14. Section Zona Gaming

Bagian berikutnya adalah:

```html
<section id="bagian-zona">
```

Section ini digunakan untuk menampilkan pilihan zona gaming.

Struktur dasarnya:

```text
Zona Gaming
│
├── Judul
├── Subjudul
│
├── Tab Zona
│
└── Detail Zona
    ├── Bar informasi
    ├── Gambar
    ├── Keterangan
    └── Statistik
```

---

# 15. Container Zona

Di dalam section terdapat:

```html
<div class="pembungkus tengah">
```

Container ini digunakan sebagai pembungkus seluruh isi Zona Gaming.

Di dalamnya terdapat:

```html
<h2>Zona Gaming</h2>
```

`<h2>` digunakan sebagai heading untuk section tersebut.

---

# 16. Subjudul Zona

Di bawah heading terdapat:

```html
<p class="subjudul">
    Pilih arena reguler, ruang privat VIP,
    studio streaming, hingga simulator racing
    dengan spesifikasi turnamen tier-1.
</p>
```

Subjudul menjelaskan pilihan zona yang tersedia dalam konsep Vortex Arena.

Pilihan yang disebutkan:

* Arena reguler
* Ruang privat VIP
* Studio streaming
* Simulator racing

---

# 17. Tab Zona

Elemen:

```html
<div
    class="deretan-tab"
    id="tabZona"
></div>
```

disiapkan sebagai tempat untuk menampilkan pilihan/tab zona.

Saat ini elemen tersebut masih kosong:

```html
<div id="tabZona"></div>
```

Artinya struktur HTML baru menyediakan tempat untuk tab tersebut.

---

# 18. Detail Zona

Informasi zona berada di dalam:

```html
<div
    class="etalase"
    style="text-align: left;"
>
```

Bagian ini menjadi area utama untuk menampilkan detail dari zona yang dipilih.

---

# 19. Bar Informasi Zona

Bagian atas detail zona:

```html
<div class="bar-atas">
    <span
        class="teks-mono"
        id="zonaKode"
    ></span>

    <b id="zonaNama"></b>

    <span
        class="teks-mono"
        id="zonaHarga"
    ></span>
</div>
```

Terdapat tiga informasi utama.

### `zonaKode`

```html
<span id="zonaKode"></span>
```

Digunakan untuk kode zona.

Contoh data yang nantinya dapat ditampilkan:

```text
ZONE-01
```

---

### `zonaNama`

```html
<b id="zonaNama"></b>
```

Digunakan untuk nama zona.

Contoh:

```text
Gaming Regular
```

---

### `zonaHarga`

```html
<span id="zonaHarga"></span>
```

Digunakan untuk menampilkan harga zona.

Contoh:

```text
Rp15.000 / Jam
```

Saat ini ketiga elemen tersebut masih kosong.

---

# 20. Gambar Zona

Elemen gambar:

```html
<div
    class="gambar bingkai-gambar"
    data-img="zona"
    id="zonaGambar"
></div>
```

Elemen ini disiapkan untuk menampilkan gambar dari zona gaming.

Atribut:

```html
data-img="zona"
```

menandai bahwa elemen tersebut berkaitan dengan gambar zona.

Sedangkan:

```html
id="zonaGambar"
```

memberikan identitas khusus kepada elemen tersebut.

---

# 21. Keterangan Zona

Bagian keterangan:

```html
<div class="keterangan">
    <h3 id="zonaJudul"></h3>

    <div
        class="daftar-label teks-mono"
        id="zonaLabel"
    ></div>
</div>
```

Terdapat dua bagian.

### Judul Zona

```html
<h3 id="zonaJudul"></h3>
```

Digunakan untuk menampilkan judul atau nama detail zona.

---

### Label Zona

```html
<div
    class="daftar-label teks-mono"
    id="zonaLabel"
></div>
```

Disiapkan untuk menampilkan daftar informasi atau fasilitas zona.

Contoh informasi yang nantinya dapat dimasukkan:

```text
Monitor 240Hz
Gaming PC
Mechanical Keyboard
Gaming Mouse
Headset
```

---

# 22. Statistik Zona

Elemen terakhir pada zona:

```html
<div
    class="statistik"
    id="zonaStatistik"
></div>
```

Bagian ini disiapkan untuk menampilkan statistik atau spesifikasi singkat dari zona.

Contohnya dapat berupa:

```text
240Hz
1Gbps
RTX
32GB RAM
```

Namun pada HTML saat ini elemen tersebut masih kosong.

---

# 23. Daftar ID yang Digunakan

Berikut adalah ID yang sudah tersedia dalam HTML.

| ID              | Fungsi                             |
| --------------- | ---------------------------------- |
| `atas`          | Penanda bagian paling atas halaman |
| `navigasiPil`   | Container menu navigasi            |
| `waAtas`        | Tombol WhatsApp pada navbar        |
| `bagian-zona`   | Section Zona Gaming                |
| `bagian-spek`   | Tujuan navigasi Spek PC            |
| `bagian-tarif`  | Tujuan navigasi Tarif Paket        |
| `bagian-menu`   | Tujuan navigasi Daily Menu         |
| `tabZona`       | Container tab Zona Gaming          |
| `zonaKode`      | Tempat kode zona                   |
| `zonaNama`      | Tempat nama zona                   |
| `zonaHarga`     | Tempat harga zona                  |
| `zonaGambar`    | Tempat gambar zona                 |
| `zonaJudul`     | Tempat judul zona                  |
| `zonaLabel`     | Tempat informasi/label zona        |
| `zonaStatistik` | Tempat statistik zona              |

Perlu diperhatikan bahwa `bagian-spek`, `bagian-tarif`, dan `bagian-menu` **belum memiliki `<section>` pada HTML saat ini**. Ketiganya baru digunakan sebagai target pada link navigasi.

---

# 24. Daftar Class yang Digunakan

Beberapa class yang sudah didefinisikan di HTML:

| Class            | Digunakan Pada     | Fungsi Berdasarkan Struktur                       |
| ---------------- | ------------------ | ------------------------------------------------- |
| `logo`           | Logo               | Menandai bagian logo                              |
| `bingkai-gambar` | Elemen gambar      | Menandai elemen yang berkaitan dengan gambar      |
| `menu-pil`       | Menu navigasi      | Container menu                                    |
| `aktif`          | Menu Arena         | Menandai menu aktif                               |
| `baris`          | Beberapa container | Menandai kelompok elemen dalam satu baris         |
| `tombol-wa`      | WhatsApp           | Menandai tombol WhatsApp                          |
| `tombol`         | Link tombol        | Class umum tombol                                 |
| `putih`          | Tombol             | Variasi tombol                                    |
| `garis`          | Tombol             | Variasi tombol                                    |
| `banner-utama`   | Header             | Menandai hero/banner utama                        |
| `latar`          | Background hero    | Menandai area latar                               |
| `isi`            | Konten hero        | Menandai isi hero                                 |
| `label-atas`     | Label hero         | Menandai label bagian atas                        |
| `teks-mono`      | Beberapa teks      | Menandai teks dengan konsep monospace             |
| `pembungkus`     | Container          | Pembungkus section                                |
| `tengah`         | Container          | Menandai bagian yang berhubungan dengan alignment |
| `subjudul`       | Subtitle           | Menandai subjudul                                 |
| `deretan-tab`    | Tab zona           | Container tab                                     |
| `etalase`        | Detail zona        | Container informasi zona                          |
| `bar-atas`       | Informasi zona     | Bagian atas detail zona                           |
| `gambar`         | Gambar zona        | Container gambar                                  |
| `keterangan`     | Detail zona        | Container keterangan                              |
| `daftar-label`   | Informasi zona     | Container label                                   |
| `statistik`      | Statistik zona     | Container statistik                               |

Class tersebut baru merupakan **penamaan/struktur HTML**. Perilaku visual masing-masing class belum menjadi bagian dari dokumentasi ini.

---

# 25. Konsep Anchor pada HTML

Website menggunakan anchor untuk berpindah antarbagian.

Contoh:

```html
<a href="#bagian-zona">
    Zona Gaming
</a>
```

Targetnya:

```html
<section id="bagian-zona">
```

Hubungannya adalah:

```text
href="#bagian-zona"
        │
        ▼
id="bagian-zona"
```

Contoh lainnya:

```html
<a href="#atas">
    Vortex Arena
</a>
```

akan menuju:

```html
<header id="atas">
```

Dengan konsep ini, halaman dapat memiliki navigasi antar-section tanpa harus membuat halaman HTML baru.

---

# 26. Kondisi HTML Saat Ini

Pada tahap sekarang, HTML sudah memiliki:

* Struktur dokumen HTML5
* Navbar
* Logo
* Menu navigasi
* Tombol WhatsApp
* Tombol Tarif & Reservasi
* Hero section
* Judul utama
* Deskripsi
* Tombol CTA
* Section Zona Gaming
* Container tab zona
* Container informasi zona
* Container gambar zona
* Container keterangan
* Container statistik

Sedangkan beberapa bagian masih berupa struktur kosong atau belum tersedia:

* Detail Spek PC
* Detail Tarif Paket
* Detail Daily Menu
* Isi tab zona
* Data zona
* Isi informasi zona
* Gambar aktual

---

# 27. Catatan untuk Anggota Tim

Saat melanjutkan project ini, sebaiknya pahami terlebih dahulu struktur HTML sebelum melakukan perubahan.

Hal yang perlu diperhatikan:

1. Jangan mengubah `id` sembarangan karena ID digunakan sebagai tujuan navigasi.
2. Pastikan setiap `href="#..."` memiliki elemen dengan ID yang sesuai.
3. Gunakan struktur `<section>` untuk bagian utama halaman.
4. Gunakan heading secara berurutan seperti `<h1>`, `<h2>`, dan `<h3>`.
5. Gunakan `data-*` attribute hanya untuk informasi tambahan yang memang diperlukan.
6. Pertahankan penamaan class dan ID agar konsisten.
7. Jika menambahkan section baru, tambahkan juga link navigasinya jika section tersebut perlu diakses dari navbar.

---

# 28. Ringkasan

HTML Vortex Arena saat ini merupakan **kerangka dasar landing page gaming arena**.

Struktur yang sudah dibuat:

```text
Vortex Arena
│
├── Navbar
│   ├── Logo
│   ├── Arena
│   ├── Zona Gaming
│   ├── Spek PC
│   ├── Tarif Paket
│   ├── Daily Menu
│   ├── WhatsApp
│   └── Tarif & Reservasi
│
├── Hero
│   ├── Label
│   ├── Judul
│   ├── Deskripsi
│   └── CTA
│
└── Zona Gaming
    ├── Judul
    ├── Subjudul
    ├── Tab Zona
    └── Detail Zona
        ├── Kode
        ├── Nama
        ├── Harga
        ├── Gambar
        ├── Judul
        ├── Label
        └── Statistik
```

