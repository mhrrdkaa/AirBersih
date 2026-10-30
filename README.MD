# Air Bersih untuk Semua
### Website Edukasi Air Bersih dan Sanitasi Layak
Mendukung Sustainable Development Goal (SDG) 6 — Air Bersih dan Sanitasi Layak

## Anggota Kelompok
1. I Gusti Lanang Darma Yasa — 2515091007
Berperan aktif dalam pengembangan halaman Beranda, penyusunan struktur HTML dan CSS, integrasi navigasi, pengelolaan repository GitHub, serta proses revisi dan penyempurnaan website.
2. I Putu Mahardika — 2515091015
Berperan aktif dalam pengembangan halaman Edukasi, penyusunan materi informatif, pengaturan tampilan website, pengelolaan gambar, serta membantu proses revisi, publikasi, dan penyelesaian proyek.
3. I Ketut Yudistira Saputra — 2515091129
Tercatat sebagai anggota kelompok, dengan keterlibatan partisipasi mengirim foto, yang masih terbatas dalam proses pengembangan dan penyelesaian website.
4. Citra Hermanda Br Sembiring — 2515091145
Tercatat sebagai anggota kelompok, dengan keterlibatan partisipasi mengirim foto, yang masih terbatas dalam proses pengembangan dan penyelesaian website.

## Deskripsi Website
Air Bersih untuk Semua merupakan website edukasi yang bertujuan meningkatkan kesadaran masyarakat mengenai pentingnya air bersih, sanitasi layak, dan perlindungan sumber air. Website ini dibuat sebagai bagian dari proyek UTS mata kuliah Pemrograman Web.

Website ini memberikan informasi yang mudah dipahami mengenai manfaat air bersih, penyebab pencemaran, serta langkah sederhana untuk menghemat air dan menjaga kebersihan lingkungan.

**Tujuan:**
- Memberikan edukasi tentang pentingnya air bersih dan sanitasi.
- Meningkatkan kepedulian terhadap pencemaran sumber air.
- Mengajak masyarakat menerapkan kebiasaan hemat air.

**Manfaat:**
- Menambah pengetahuan tentang air bersih dan sanitasi.
- Memberikan panduan sederhana untuk menjaga sumber air.
- Mendorong partisipasi masyarakat dalam melindungi lingkungan.

**Sasaran pengguna:**
Masyarakat umum, pelajar, keluarga, dan siapa saja yang ingin mempelajari cara menjaga air bersih serta lingkungan.

## Halaman Website
Website ini terdiri dari lima halaman HTML yang saling terhubung melalui navigasi.

1. **Beranda (`index.html`)** — Menampilkan pengenalan website, pesan utama, dan ringkasan manfaat air bersih.
2. **Edukasi (`edukasi.html`)** — Menjelaskan pengertian air bersih, pentingnya sanitasi, permasalahan air bersih, dan hubungannya dengan SDG 6.
3. **Panduan (`panduan.html`)** — Memberikan tips menghemat air, menjaga kebersihan, dan melindungi lingkungan.
4. **Artikel (`artikel.html`)** — Membahas tanggung jawab bersama dalam menjaga sumber air dan mencegah pencemaran.
5. **Tentang (`tentang.html`)** — Menjelaskan tujuan website, sasaran pengguna, teknologi, identitas anggota kelompok, dan referensi.

## Teknologi
Teknologi yang digunakan dalam pengembangan website ini meliputi:

- **HTML5** — Membuat struktur dan konten halaman website.
- **CSS3** — Mengatur warna, tipografi, jarak, dan tampilan elemen.
- **CSS Grid** — Mengatur tata letak, seperti kartu informasi dan bagian utama halaman.
- **Flexbox** — Menyusun elemen navigasi dan komponen agar lebih fleksibel.
- **CSS Media Queries** — Menyesuaikan tampilan website pada layar desktop, tablet, dan ponsel.
- **GitHub Pages** — Digunakan untuk memublikasikan website secara online.

## Penjelasan Implementasi

### 1. Navigasi
Setiap halaman memiliki header yang berisi logo dan menu navigasi menuju Beranda, Edukasi, Panduan, Artikel, dan Tentang. Navigasi dibuat menggunakan elemen HTML `<nav>` dan tautan `<a>` agar pengguna dapat berpindah halaman dengan mudah.

Contoh kode:

```html
<nav>
  <a href="index.html">Beranda</a>
  <a href="edukasi.html">Edukasi</a>
  <a href="panduan.html">Panduan</a>
  <a href="artikel.html">Artikel</a>
  <a href="tentang.html">Tentang</a>
</nav>
```

Fungsi kode tersebut adalah menyediakan tautan antarhalaman sehingga pengunjung dapat mengakses informasi yang dibutuhkan.

### 2. Layout Website
Tata letak website menggunakan CSS Grid dan Flexbox untuk menyusun konten agar rapi. Bagian Beranda memiliki area utama (*hero section*) yang berisi judul, deskripsi, tombol, dan gambar. Sementara itu, informasi pendukung disusun menggunakan kartu (*cards*).

Contoh kode CSS:

```css
.cards {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
}
```

Kode tersebut membagi area kartu menjadi tiga kolom dengan jarak antarkartu sebesar 24 piksel.

### 3. Responsive Design
Website dirancang agar dapat menyesuaikan ukuran layar perangkat. CSS Media Queries digunakan untuk mengubah susunan konten ketika lebar layar semakin kecil.

Contoh kode CSS:

```css
@media (max-width: 768px) {
    .cards {
        grid-template-columns: 1fr;
    }

    .hero {
        grid-template-columns: 1fr;
    }
}
```

Kode tersebut membuat kartu dan bagian utama website berubah menjadi satu kolom ketika lebar layar maksimal 768 piksel. Dengan demikian, konten lebih mudah dibaca pada perangkat seluler.

### 4. Penggunaan Gambar
Gambar disimpan di dalam folder `images` dan dipanggil melalui atribut `src` pada elemen `<img>`.

Contoh kode HTML:

```html
<div class="hero-art">
  <img
    src="images/hero.jpg"
    alt="Pemandangan sumber air bersih"
  >
</div>
```

Atribut `src` menunjukkan lokasi gambar, sedangkan `alt` memberikan deskripsi gambar untuk membantu aksesibilitas dan ketika gambar gagal dimuat.

Contoh pengaturan gambar menggunakan CSS:

```css
.hero-art img {
    width: 100%;
    height: 320px;
    object-fit: cover;
    border-radius: 20px;
}
```

Kode tersebut membuat gambar memenuhi lebar wadah, memiliki tinggi yang konsisten, dan mempunyai sudut membulat.

### 5. Penggunaan CSS Eksternal
Seluruh halaman menggunakan file CSS eksternal yang disimpan pada `css/style.css`. File CSS dipanggil melalui elemen berikut pada bagian `<head>` HTML:

```html
<link rel="stylesheet" href="css/style.css">
```

Penggunaan CSS eksternal membantu menjaga konsistensi desain dan memudahkan perubahan tampilan tanpa harus menulis ulang kode CSS di setiap halaman.

## Struktur Folder

Struktur folder proyek website adalah sebagai berikut:


## Struktur Proyek

```text
ProjectPemWeb_Kelompok8/
├── index.html
├── edukasi.html
├── panduan.html
├── artikel.html
├── tentang.html
├── style.css
├── artikel.jpg
├── edukasi.jpg
├── foto.CitraHermandaBrSembiring.jpeg
├── foto.IGustiLanangDarmaYasa.jpeg
├── foto.IKetutYudistiraSaputra.jpeg
├── foto.PutuMahardika.jpeg
└── README.md
```


Keterangan:
- File HTML digunakan untuk menyusun lima halaman website.
- Folder `css` menyimpan file desain eksternal.
- Folder `images` menyimpan gambar yang digunakan pada halaman website.
- File `README.md` berisi dokumentasi proyek, teknologi, struktur folder, dan referensi.

## Website dan Repository

- **URL GitHub Pages:** https://mhrrdkaa.github.io/AirBersih/
- **URL Repository GitHub:** https://mhrrdkaa.github.io/AirBersih/

Catatan: URL GitHub Pages perlu disesuaikan dengan alamat yang muncul pada pengaturan GitHub Pages setelah website berhasil dipublikasikan.

## Referensi

1. United Nations. *Goal 6: Ensure Availability and Sustainable Management of Water and Sanitation for All.* https://sdgs.un.org/goals/goal6
2. World Health Organization (WHO). *Drinking-water.* https://www.who.int/news-room/fact-sheets/detail/drinking-water
3. UNICEF. *Water, Sanitation and Hygiene (WASH).* https://www.unicef.org/wash
4. GitHub Docs. *GitHub Pages.* https://docs.github.com/en/pages
5. Sumber gambar: isi dengan nama situs dan URL sumber asli dari setiap gambar yang digunakan.

---

**Mata Kuliah:** Pemrograman Web  
**Proyek:** Ujian Tengah Semester (UTS)  
**Topik:** Website Edukasi Air Bersih dan Sanitasi Layak — SDG 6
