# Portfolio Website + Creative CV — Bill Gates

Praktikum Modul 1 · Pemrograman Web (A) 2026 · **Kelompok A14 Asisten IRL**

Website portofolio dua halaman yang dibangun **native from scratch** menggunakan HTML dan CSS
saja, tanpa framework, tanpa library, dan tanpa JavaScript. Tokoh yang ditampilkan adalah
**Bill Gates**, sesuai ketentuan soal yang memperbolehkan penggunaan data tokoh terkenal.

---

## Anggota Kelompok

| Nama | NRP |
|---|---|
| Sultan Ahmad Maulana | 5027251070 |
| Sulthan Daffa Al Hasyimi | 5027251091 |
| Senna Bagus Harimurti | 5027251106 |

---

## Halaman

| Berkas | Halaman | Isi |
|---|---|---|
| `index.html` | Landing Page | Hero, statistik, profil singkat, biodata, linimasa perjalanan, galeri fokus, tabel karya tulis, penghargaan, form kontak |
| `cv.html` | Creative CV | Data diri, keahlian, bahasa & teknologi, bidang minat, kutipan, profil, pengalaman, penghargaan, pendidikan |

Tombol **call to action** pada hero halaman utama mengarah ke `cv.html`, dan kedua halaman
saling terhubung lewat navbar dan footer.

---

## Fitur

- **Navbar sticky** yang tetap terlihat saat halaman digulung
- **Responsive** pada tiga ukuran layar: desktop, tablet, dan HP
- **Linimasa perjalanan** mendatar di desktop, berubah menurun di layar kecil
- **Galeri grid** dengan satu kartu unggulan yang melebar dua kolom dan dua baris
- **Tabel karya tulis** dengan baris selang-seling; kolom paling sempit disembunyikan di HP
- **Form kontak** lengkap dengan berbagai tipe input, dropdown, radio button, dan textarea
- **Responsive image** dengan `srcset` dan `sizes`, sehingga HP mengunduh berkas yang lebih kecil
- **Layout CV** berbasis `grid-template-areas` yang urutannya disusun ulang di layar HP

---

## Teknologi

| Bagian | Keterangan |
|---|---|
| Struktur | HTML5 |
| Tampilan | CSS3, ditulis sebagai **external stylesheet** |
| Font | Poppins (Google Fonts) |
| Framework | **Tidak ada** |
| JavaScript | **Tidak ada** |

---

## Struktur Folder

```
.
├── index.html          Halaman utama (portfolio)
├── cv.html             Halaman CV kreatif
├── css/
│   ├── base.css        Gaya bersama kedua halaman
│   ├── landing.css     Khusus index.html
│   └── cv.css          Khusus cv.html
├── images/             11 foto pendukung
└── README.md
```

CSS dipecah menjadi tiga berkas dengan pertimbangan:

- `base.css` dipakai **kedua** halaman, sehingga perubahan pada navbar, tombol, palet warna,
  atau footer cukup ditulis sekali.
- `landing.css` dan `cv.css` hanya dimuat oleh halaman yang membutuhkannya, sehingga tiap
  halaman tidak ikut memuat aturan yang tidak dipakainya.

---

## Cara Menjalankan

buka berkas HTML-nya di browser:

```bash
git clone https://github.com/DaffHaxxim/pweb-html_css-p01-2026.git
cd pweb-html_css-p01-2026
xdg-open index.html
```

Atau klik dua kali `index.html` lewat file manager.

### Menguji tampilan responsive

Tekan **F12** untuk membuka Developer Tools, aktifkan **device toolbar**
(<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>M</kbd>), lalu coba lebar layar berikut:

| Lebar | Yang berubah |
|---|---|
| **> 768px** | Tampilan penuh: galeri 3 kolom, linimasa mendatar, CV 2 kolom |
| **≤ 768px** | Galeri 2 kolom, linimasa berubah menurun, CV jadi 1 kolom |
| **≤ 480px** | Galeri 1 kolom, label navbar dipendekkan, kolom tabel paling sempit disembunyikan |

Breakpoint yang dipakai adalah **768px** dan **480px**

---

## Catatan

Seluruh konten disusun untuk keperluan **Praktikum Modul 1
Pemrograman Web 2026** 
