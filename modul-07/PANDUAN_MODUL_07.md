# MODUL 7 — Pengenalan Framework CSS (Bootstrap)

(Di cover PDF tertulis Modul 7, di halaman isi tertulis Modul 9. Pakai nomor di cover: Modul 7.)

## Pembagian kerja

| Bagian | Siapa | Keterangan |
|---|---|---|
| Struktur folder, `index.html`, `style.css` (praktikum bagian 1-9) | Sudah dikerjakan | Folder `modul-07-bootstrap/` |
| Gambar | Sebagian | Gambar di folder itu hanya pengganti. Ganti dengan aset asli (langkah B) |
| Halaman personal (Tugas no. 2) | Template sudah ada | Kamu isi data dirimu (langkah E) |
| Install VS Code, jalankan di browser, screenshot | **Kamu** | Langkah A, C, D |
| Online-kan website | **Kamu** | Langkah F |
| Laporan PDF dan zip | **Kamu** | Langkah G, H |

---

## Langkah A — Install dan buka VS Code (kamu)
1. Download di https://code.visualstudio.com/download lalu install.
2. Ekstrak `paw-praktikum.zip`.
3. Di VS Code: **File → Open Folder** → pilih `modul-07-bootstrap`.
4. Install extension **Live Server** (ikon Extensions di kiri, cari "Live Server", klik Install).
5. 📸 Screenshot: VS Code terbuka dengan struktur folder di panel kiri.

## Langkah B — Ganti aset gambar dengan yang asli (kamu)
1. Buka link aset dari modul: https://shorturl.at/mtCKZ
2. Download lima file: `bs-icons.png`, `bs-themes.png`, `logo-black.svg`, `logo-white.svg`, `main.svg`.
3. Timpa file dengan nama yang sama di `modul-07-bootstrap/assets/images/`.
4. Kalau link tidak bisa dibuka, biarkan gambar pengganti. Halaman tetap jalan, hanya gambarnya beda.

## Langkah C — Jalankan di browser (kamu)
1. Buka `index.html` di VS Code → klik kanan → **Open with Live Server**.
2. Browser terbuka di `http://127.0.0.1:5500`.
3. Uji responsif: tekan **F12** → ikon HP/tablet (Toggle device toolbar). Menu harus jadi tombol hamburger, lalu panel offcanvas muncul saat diklik.
4. Klik dropdown "v5.3" dan "Toggle theme" untuk memastikan menu terbuka.

## Langkah D — Screenshot untuk laporan (kamu)
- Struktur folder di VS Code
- Kode tiap section (navbar, main, icons, themes, footer, css)
- Hasil browser tampilan desktop (seluruh halaman)
- Hasil browser tampilan HP (navbar tertutup dan offcanvas terbuka)

## Penjelasan kode (untuk bagian "penjelasan" di laporan)

| Bagian | Class penting | Fungsi |
|---|---|---|
| `<head>` | link CDN bootstrap, bootstrap-icons, `style.css` | Memuat CSS Bootstrap dari internet. `style.css` dimuat terakhir supaya bisa menimpa gaya Bootstrap |
| Navbar | `navbar fixed-top navbar-expand-lg` | Navbar menempel di atas, terbuka penuh di layar `lg` ke atas, jadi hamburger di layar kecil |
| Offcanvas | `offcanvas offcanvas-end`, `data-bs-toggle="offcanvas"` | Menu geser dari kanan di layar kecil. Dikontrol JS Bootstrap lewat atribut `data-bs-*` |
| Menu | `col-6 col-md-auto` | 2 kolom per baris di HP, lebar otomatis di layar `md` ke atas |
| Dropdown | `dropdown`, `dropdown-menu-end` | Menu turun, rata ke kanan |
| Main | `container`, `row`, `col-md-5 order-md-2` | Grid 12 kolom. `order-md-2` memindahkan gambar ke kanan di layar `md` ke atas |
| Tombol | `btn btn-lg`, `d-flex flex-column flex-md-row` | Tombol tersusun vertikal di HP, horizontal di layar `md` ke atas |
| Icons | `bi bi-subtract`, `fs-2`, `rounded-3` | Ikon dari Bootstrap Icons, ukuran font 2, sudut membulat |
| Gambar | `img-fluid` | Gambar menyesuaikan lebar kolom |
| Footer | `col-lg-3`, `offset-lg-1`, `list-unstyled` | 5 kolom di layar `lg`; daftar tanpa bullet |
| `style.css` | `.bg-purple` + `!important` | Warna ungu kustom. `!important` agar menang atas class Bootstrap |
| `style.css` | `#main a`, `#footer a:hover` | Gaya link berbeda tiap section memakai selector id |

Catatan: pada `index.html` di folder saya ada tambahan CSS `.icon-link` di bagian bawah `style.css`, karena class itu belum lengkap di Bootstrap 5.3.0-alpha2. Tulis di laporan bahwa bagian itu tambahan.

---

## Langkah E — Tugas no. 2: halaman personal (kamu isi)
Folder: `modul-07-tugas-halaman-personal/`
1. Buka folder itu di VS Code.
2. Tekan **Ctrl+Shift+H** (Find & Replace di semua file). Cari `[NAMA KAMU]`, ganti dengan namamu.
3. Di `index.html`, ganti:
   - inisial `NK` di `.avatar` (atau pakai foto, petunjuknya ada di komentar)
   - paragraf "Tentang saya", email, dan kota
   - persentase keahlian
   - tiga kartu proyek
4. Warna tema ada di `assets/css/style.css`, bagian `:root`.
5. Jalankan dengan Live Server, lalu uji tampilan HP.
6. 📸 Screenshot kode dan hasil browser (desktop + HP).

## Langkah F — Online-kan website (kamu)
**Opsi termudah: Netlify Drop (tanpa Git)**
1. Buka https://app.netlify.com/drop dan login (bisa pakai akun Google/GitHub).
2. Drag folder `modul-07-tugas-halaman-personal` ke halaman itu.
3. Kamu dapat URL `https://xxxx.netlify.app`. Salin ke laporan dan screenshot halaman dengan URL tersebut.

**Opsi lain: GitHub Pages**
1. Buat repository publik di GitHub, upload isi folder (index.html langsung di root).
2. Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.
3. Tunggu 1-2 menit, URL: `https://username.github.io/nama-repo/`.

## Langkah G — Laporan Praktikum PDF (kamu)
Buat di Word atau Google Docs, lalu **Export / Save as PDF**. Kerangka:
1. Halaman judul (Modul 7, nama, NIM, kelas)
2. Bagian A — Praktikum (clone Bootstrap): screenshot kode, hasil browser, dan penjelasan per section (pakai tabel di atas, dengan kata-katamu sendiri)
3. Bagian B — Tugas no. 2: deskripsi website, screenshot kode, hasil browser, penjelasan, **URL website online**
4. Kesimpulan, 3-4 kalimat

## Langkah H — Kumpulkan (kamu)
Buat satu file `.zip` berisi:
- Laporan PDF
- Folder `modul-07-bootstrap` (HTML praktikum)
- Folder `modul-07-tugas-halaman-personal` (HTML tugas no. 2)

Upload ke LMS sebelum jadwal praktikum minggu depan.
