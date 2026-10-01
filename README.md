# Vortex Arena: Catatan soal `div`, `class`, dan `id`
Catatan sedikit Tolong di Baca.

---

## 1. `div`, `class`, `id` itu apa sih?

| Istilah | Gampangnya | Contoh |
|---|---|---|
| `div` | Kotak kosong buat bungkus elemen lain biar rapi | `<div>...</div>` |
| `class` | Label buat dipasangi tampilan nanti (warna, ukuran, posisi) | `class="tombol putih"` |
| `id` | Nama khusus satu elemen, nggak boleh kembar | `id="bagian-zona"` |

Bayangin `class` itu seragam sekolah: banyak orang boleh pakai yang sama. `id` itu nama kamu sendiri, dan di satu halaman cuma boleh ada satu yang namanya begitu.

Satu elemen juga boleh punya beberapa class, tinggal dipisah spasi:

```html
<a class="tombol putih">  <!-- dapat class "tombol" dan "putih" sekaligus -->
```

---

## 2. Susunan `div` di halaman

Yang menjorok ke dalam berarti ada di dalam elemen di atasnya.

```
body
├── nav
│   ├── a.logo
│   ├── div.menu-pil #navigasiPil
│   └── div.baris
│
├── header.banner-utama #atas
│   ├── div.latar.bingkai-gambar
│   └── div.isi
│       └── div.baris
│
└── section #bagian-zona
    └── div.pembungkus.tengah
        ├── div.deretan-tab #tabZona
        └── div.etalase
            ├── div.bar-atas
            ├── div.gambar.bingkai-gambar #zonaGambar
            ├── div.keterangan
            │   └── div.daftar-label #zonaLabel
            └── div.statistik #zonaStatistik
```

---

## 3. Daftar `id`

### Id yang jadi tujuan link

Kalau kamu klik menu di navbar, halaman loncat ke elemen yang id-nya sama dengan `href`-nya.

```html
<a href="#bagian-zona">Zona Gaming</a>   <!-- yang diklik -->
<section id="bagian-zona">...</section>  <!-- tempat landing -->
```

| ID | Ada di | Dipanggil dari | Status |
|---|---|---|---|
| `atas` | `<header>` | Logo, menu Arena | Ada |
| `bagian-zona` | `<section>` | Menu Zona Gaming, tombol Jelajahi Zona | Ada |
| `bagian-spek` | - | Menu Spek PC | **Belum dibuat** |
| `bagian-tarif` | - | Menu Tarif Paket, dua tombol Tarif & Reservasi | **Belum dibuat** |
| `bagian-menu` | - | Menu Daily Menu | **Belum dibuat** |

Tiga yang belum dibuat itu bikin linknya nggak ngapa-ngapain kalau diklik.

### Id yang masih kosong, nanti diisi data

| ID | Elemen | Bakal berisi |
|---|---|---|
| `tabZona` | `div` | Tombol pilihan zona |
| `zonaKode` | `span` | Kode zona, misalnya `ZONE-01` |
| `zonaNama` | `b` | Nama zona |
| `zonaHarga` | `span` | Harga per jam |
| `zonaGambar` | `div` | Foto zona |
| `zonaJudul` | `h3` | Judul detail zona |
| `zonaLabel` | `div` | Daftar fasilitas |
| `zonaStatistik` | `div` | Angka spesifikasi singkat |

### Sisanya

| ID | Fungsi |
|---|---|
| `navigasiPil` | Pembungkus menu navbar |
| `waAtas` | Tombol WhatsApp di navbar (nomornya belum diisi, masih `wa.me/` doang) |

---

## 4. Daftar `class`

### Navbar

| Class | Dipasang di | Fungsi |
|---|---|---|
| `logo` | `a` | Logo Vortex Arena |
| `menu-pil` | `div` | Pembungkus menu |
| `aktif` | `a` | Penanda menu yang lagi dibuka |
| `baris` | `div` | Biar isinya berjajar ke samping |
| `tombol-wa` | `a` | Tombol WhatsApp |

### Tombol

| Class | Fungsi |
|---|---|
| `tombol` | Dasar semua tombol |
| `putih` | Tombol yang warnanya putih |
| `garis` | Tombol yang cuma bergaris pinggir |

### Hero (bagian paling atas halaman)

| Class | Dipasang di | Fungsi |
|---|---|---|
| `banner-utama` | `header` | Pembungkus seluruh hero |
| `latar` | `div` | Tempat gambar background |
| `isi` | `div` | Pembungkus teks dan tombol hero |
| `label-atas` | `span` | Tulisan kecil di atas judul |

### Zona Gaming

| Class | Dipasang di | Fungsi |
|---|---|---|
| `pembungkus` | `div` | Pembungkus isi section |
| `tengah` | `div` | Bikin isinya rata tengah |
| `subjudul` | `p` | Kalimat di bawah judul section |
| `deretan-tab` | `div` | Tempat tab zona |
| `etalase` | `div` | Kotak besar detail zona |
| `bar-atas` | `div` | Baris atas yang isinya kode, nama, harga |
| `gambar` | `div` | Tempat foto zona |
| `keterangan` | `div` | Judul dan label zona |
| `daftar-label` | `div` | Deretan label fasilitas |
| `statistik` | `div` | Deretan angka spek |

### Dipakai di banyak tempat

| Class | Fungsi |
|---|---|
| `bingkai-gambar` | Penanda elemen yang bakal diisi gambar (logo, hero, zona) |
| `teks-mono` | Penanda teks yang pakai font JetBrains Mono |

---

## 5. Pesan buat tim

- Jangan asal ganti `id`. Link navbar dan JavaScript nyari elemen lewat nama itu, jadi sekali diganti langsung putus.
- Tiap `href="#..."` harus ada pasangan `id`-nya.
- Bikin dulu `section` untuk `bagian-spek`, `bagian-tarif`, dan `bagian-menu`.
- Semua elemen berawalan `zona` masih kosong karena JavaScript-nya belum ditulis (`<script src="">` masih kosong).
- Class belum kelihatan efeknya sama sekali, soalnya file CSS-nya (`<link rel="stylesheet" href="">`) juga belum ada.
- Kalau nambah class atau id baru, ikuti gaya penamaan yang sudah ada.
