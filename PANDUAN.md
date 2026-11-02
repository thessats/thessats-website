# Panduan memasang portofolio TSVISION

Isi folder ini:

- `index.html`: seluruh situs (tampilan, teks, dan isi proyek).
- `images/`: tempat semua foto dan gambar proyekmu.
- `PANDUAN.md`: file ini.

Kamu tidak perlu menginstal apa pun untuk mulai. Kamu hanya butuh editor teks. Disarankan **Visual Studio Code** (gratis, code.visualstudio.com).

---

## Langkah 1. Buka situs di komputermu

1. Buka folder `tsvision-site`.
2. Klik dua kali `index.html`. Situs terbuka di browser.
3. Setiap kali kamu mengubah file lalu menyimpannya, muat ulang browser (F5) untuk melihat hasilnya.

## Langkah 2. Memasukkan gambar

Situs mencari gambar di folder `images/` berdasarkan **nama file**. Kalau file tidak ada, tampilan placeholder tetap dipakai, jadi kamu boleh mengisi satu per satu.

1. Siapkan gambarmu dalam format **JPG** (huruf kecil, `.jpg`, bukan `.JPG` atau `.jpeg`).
2. Ganti namanya persis seperti daftar ini, lalu taruh di folder `images/`.

| Untuk | Nama file |
| --- | --- |
| Foto profil (kotak di halaman Home) | `foto-profil.jpg` |
| Anggaran Daerah | `anggaran-daerah.jpg` |
| BukaLowongan | `bukalowongan.jpg` |
| Dashboard BRI | `dashboard-bri.jpg` |
| BRI Menanam | `bri-menanam.jpg` |
| Rentric | `rentric.jpg` |
| Makna Mitra | `makna-mitra.jpg` |
| IPIN | `ipin.jpg` |
| New Year 2022 | `new-year-2022.jpg` |
| The Last Vanguard | `the-last-vanguard.jpg` |
| Moonlight Expedition | `moonlight-expedition.jpg` |
| Mother Nature's Embrace | `mother-natures-embrace.jpg` |
| Concrete Jungle Moonlight | `concrete-jungle-moonlight.jpg` |
| Sushi Minimalist 3D | `sushi-minimalist-3d.jpg` |
| Dancing in the Dusk | `dancing-in-the-dusk.jpg` |
| The Devil's Gaze | `the-devils-gaze.jpg` |
| The Digital Creator | `the-digital-creator.jpg` |
| Drink of Orange | `drink-of-orange.jpg` |

Aturan nama untuk proyek baru: judul dalam huruf kecil, spasi jadi tanda hubung `-`, apostrof dihapus.

Tips ukuran gambar:
- Foto profil: persegi, sekitar 800 x 800 px.
- Gambar proyek: landscape, sekitar 1200 x 900 px.
- Usahakan tiap file di bawah 300 KB supaya situs cepat. Kecilkan gratis di **squoosh.app**.

## Langkah 3. Mengubah teks

1. Buka `index.html` di VS Code (klik kanan file, Open with Code).
2. Tekan **Ctrl+F** dan ketik potongan kalimat yang mau diubah.
3. Ganti tulisannya, lalu **Ctrl+S** untuk menyimpan. Jangan hapus tanda `<` `>` di sekitar teks.

Teks yang paling sering diubah:

| Yang diubah | Cari |
| --- | --- |
| Judul dan paragraf pembuka | `Hi, I’m Theresia Sekar` |
| Angka 5+ dan 10+ | `UI/UX Projects` dan `All Design` |
| Daftar skill yang berjalan | `Design System` (tiap skill muncul dua kali, ubah keduanya) |
| Bio di bagian About | `I’m passionate about` |
| Tiga poin di About | `2 Years of Experiences` |
| Nama dan email di footer | `thereajeng@gmail.com` (ada dua tempat) |
| Teks halaman Contact | `Let’s talk today` |

### Mengubah daftar proyek

Cari `var cases = [` (daftar proyek UI/UX) dan `var works = [` (karya Illustration, Editing, Animation). Contoh satu proyek UI/UX:

```
['2023', 'Anggaran Daerah', 'Website', 'Built Anggaran Daerah, ...', 'web', 't1'],
```

Urutannya: tahun, judul, jenis, deskripsi, bentuk placeholder, warna placeholder. Untuk menambah proyek, salin satu baris lalu ubah isinya. Pastikan setiap baris diakhiri koma, dan tanda kutip tidak terhapus.

Untuk karya seni, contohnya `['Drink of Orange', 'animation']`. Kategori yang boleh dipakai: `illustration`, `editing`, `animation`.

## Langkah 4. Mengganti link

Cari tiga alamat ini lalu ganti:

| Cari | Ganti dengan |
| --- | --- |
| `https://www.linkedin.com/` | alamat profil LinkedIn-mu |
| `https://wa.me/` | `https://wa.me/62812xxxxxxx` (nomor tanpa 0 di depan, diawali 62) |
| `https://www.instagram.com/` | `https://www.instagram.com/usernamekamu` |

## Langkah 5. Memasang ke internet dengan Netlify

1. Buat akun di **netlify.com** (gratis) dan aktifkan verifikasi dua langkah.
2. Buka **app.netlify.com/drop**.
3. Seret **seluruh folder `tsvision-site`** (bukan hanya `index.html`) ke kotak yang tersedia.
4. Tunggu beberapa detik. Kamu mendapat alamat seperti `nama-acak.netlify.app`.
5. Klik **Site configuration → Change site name** dan ganti jadi nama yang kamu mau, misalnya `theresia-sekar`.
6. Untuk domain sendiri: **Domain management → Add a domain** lalu ikuti petunjuknya.

### Memperbarui situs nanti

Ubah file di komputermu, lalu di Netlify buka situsmu, tab **Deploys**, dan seret ulang folder `tsvision-site` ke kotak "Drag and drop" di sana.

## Kalau ada masalah

- **Gambar tidak muncul:** periksa nama file (huruf kecil semua, `.jpg`), lokasinya di dalam `images/`, lalu muat ulang dengan Ctrl+F5.
- **Halaman kosong setelah mengubah daftar proyek:** biasanya ada koma atau tanda kutip yang terhapus. Tekan Ctrl+Z di VS Code sampai tampilan normal lagi.
- **Foto terpotong:** foto profil dipotong menjadi kotak, jadi taruh wajahmu di tengah gambar.
- **Mau melihat mode gelap atau terang:** situs mengikuti tema Windows atau browser-mu.

---

# Jalur lengkap: GitHub + Netlify (update otomatis)

Dengan jalur ini, setiap kali kamu mengubah file di GitHub, Netlify memperbarui situsmu sendiri dalam sekitar 1 menit.

## A. Akun GitHub
1. Buka github.com/signup dan buat akun dengan emailmu.
2. Verifikasi email.
3. Aktifkan verifikasi dua langkah: foto profil kanan atas, Settings, Password and authentication.

## B. Buat repository
1. Klik tombol **+** kanan atas, pilih **New repository**.
2. Repository name: `tsvision-portfolio`.
3. Pilih **Public**. Jangan centang pilihan tambahan apa pun.
4. Klik **Create repository**.

## C. Unggah file situs
1. Di halaman repository yang kosong, klik link **uploading an existing file**.
2. Buka folder `tsvision-site` di komputermu. Pilih **isinya** (`index.html`, folder `images`, `PANDUAN.md`), lalu seret ke halaman GitHub. Jangan seret foldernya, karena `index.html` harus berada di paling atas repository.
3. Tunggu sampai semua file muncul di daftar.
4. Klik **Commit changes**.

## D. Hubungkan ke Netlify
1. Buka netlify.com, klik **Sign up**, lalu pilih **Sign up with GitHub**.
2. Setelah masuk, klik **Add new project**, lalu **Import an existing project**.
3. Pilih **GitHub**. Saat diminta izin, pilih **Only select repositories** dan pilih `tsvision-portfolio` saja.
4. Pada pengaturan build: **Build command** dan **Publish directory** dikosongkan.
5. Klik **Deploy**. Setelah selesai, kamu mendapat alamat `.netlify.app`.
6. Ubah nama situs: **Site configuration, Change site name**.

## E. Memperbarui situs
- **Mengubah teks:** di GitHub, buka `index.html`, klik ikon pensil, edit, lalu **Commit changes**.
- **Menambah gambar:** buka folder `images`, klik **Add file, Upload files**, seret gambarnya, lalu **Commit changes**.
- Netlify membuat versi baru otomatis. Lihat prosesnya di tab **Deploys**.

## F. Domain sendiri (opsional)
Di Netlify: **Domain management, Add a domain**. Ikuti petunjuk untuk mengarahkan domain dari tempatmu membelinya.
