# LAPORAN PRAKTIKUM — PEMROGRAMAN WEB
## Pratikum: HTML Semantik dan CSS

<img width="300" height="300" alt="image1" src="https://github.com/user-attachments/assets/f09b0081-6868-496c-9ff2-cb633d17851e" />

**Oleh:**  
I Made Dedy Wanditya (42430042)

**PROGRAM STUDI TEKNOLOGI INFORMASI**  
**FAKULTAS TEKNIK DAN INFORMATIKA**  
**UNIVERSITAS PENDIDIKAN NASIONAL**  
**2025**

---

## PENDAHULUAN

HTML (HyperText Markup Language) merupakan fondasi dalam membangun sebuah halaman web. Dengan adanya pengembangan ke HTML5, muncul konsep _semantic HTML_ yang memberikan makna lebih jelas terhadap struktur konten. Penggunaan tag semantik seperti `<header>`, `<footer>`, `<article>`, `<section>`, dan `<nav>` membantu developer mendeskripsikan fungsi setiap bagian halaman dengan lebih spesifik. Hal ini tidak hanya meningkatkan aksesibilitas bagi pengguna, termasuk yang menggunakan _assistive technologies_, tetapi juga memperkuat optimasi mesin pencari (SEO).

Di sisi lain, CSS (_Cascading Style Sheets_) berperan penting dalam mengatur presentasi dan tampilan dari elemen HTML. Dengan CSS, pengembang dapat mengontrol tata letak, warna, ukuran teks, hingga efek interaktif yang memberikan pengalaman lebih menarik bagi pengguna. CSS memungkinkan pemisahan antara struktur (HTML) dan desain (CSS), sehingga pengembangan website menjadi lebih teratur, fleksibel, dan mudah dikelola. Laporan ini akan membahas penerapan HTML semantik dan CSS dalam pembuatan website, mulai dari struktur dasar, penggunaan tag-tag semantik, hingga penerapan berbagai selektor CSS untuk memperindah tampilan. Dengan demikian, diharapkan pembaca dapat memahami pentingnya penggunaan semantic HTML dan CSS dalam menghasilkan website yang tidak hanya fungsional, tetapi juga estetis dan ramah pengguna.

---

## PEMBAHASAN

### 1) Membuat File `cv.html` dan Struktur Dasar HTML
<img width="653" height="244" alt="image2" src="https://github.com/user-attachments/assets/789aff45-fef5-4131-bda2-21b731c22659" />

Pada potongan kode ini menunjukkan pembuatan file HTML baru dengan struktur dasar (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`).  
**Fungsi:** Menyediakan kerangka utama halaman web yang menjadi tempat menulis konten dan menghubungkan CSS.

---

### 2) Menambahkan Struktur Semantic HTML ke dalam `<body>`

```html
<header>
  <h1>Dedy Wanditya</h1>
  <p>Web Developer | Graphic Designer</p>
</header>

<nav>
  <ul>
    <li><a href="#biodata">Biodata</a></li>
    <li><a href="#pendidikan">Pendidikan</a></li>
    <li><a href="#skills">Skills</a></li>
  </ul>
</nav>

<section id="biodata">
  <h2>Biodata Diri</h2>
  <p>Nama: Dedy Wanditya</p>
  <p>Email: <a href="mailto:imadededywanditya@gmail.com">imadededywanditya@gmail.com</a></p>
  <p>Telepon: 081337771929</p>
  <p>Domisili: Badung</p>
</section>

<section id="pendidikan">
  <h2>Pendidikan</h2>
  <ul>
    <li>SD Negeri 1 Pecatu</li>
    <li>SMP Negeri 2 Kuta Selatan</li>
    <li>SMK TI Bali Global Jimbaran</li>
  </ul>
</section>

<section id="skills">
  <h2>Skills</h2>
  <p>HTML, CSS, JavaScript, PHP, C++, React</p>
</section>

<footer>
  <p>Ikuti saya di social media: <a href="https://www.instagram.com/dedywndy/">Instagram</a>, <a href="https://www.tiktok.com/@dedipakey?is_from_webapp=1&sender_device=pc">Tiktok</a></p>
</footer>
```
**Fungsi:** Memberikan makna yang jelas pada setiap bagian halaman web (`<header>` untuk bagian atas, `<nav>` untuk menu, `<section>` untuk konten, `<footer>` untuk informasi bawah).

---

### 3) Menambahkan CSS di Tag `<style>` pada `<head>`

```html
<style>
  body {
    font-family: Arial, sans-serif;
  }
  header {
    background-color: #f0f0f0;
    padding: 20px;
    text-align: center;
  }
  nav ul {
    list-style-type: none;
    padding: 0;
    text-align: center;
  }
  nav ul li {
    display: inline;
    margin-right: 20px;
  }
  nav ul li a {
    text-decoration: none;
    color: blue;
  }
  a:hover {
    text-decoration: underline;
  }
  section {
    margin: 20px 0;
  }
  footer {
    background-color: #f0f0f0;
    padding: 10px;
    text-align: center;
  }
</style>
```
**Fungsi:** Memberi tampilan (warna, jarak, teks) langsung pada halaman tanpa file CSS terpisah.

---

### 4) Menggunakan Berbagai Jenis Selektor CSS
- **Selektor Kelas (`.navbar, .nav-list, .nav-item, .nav-link`)** – Menyasar elemen dengan class tertentu untuk styling seragam.  
<img width="624" height="126" alt="image3" src="https://github.com/user-attachments/assets/74b08371-41be-4c33-afcd-bb5f868cd24f" />

```css
.navbar {
  margin: 14 0;
  text-align: center;
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: inline-block;
}

.nav-item {
  display: inline-block;
  margin: 0 10;
}

.nav-link {
  text-decoration: none;
  color: #3f51b5;
}
```


- **Selektor Atribut (`[href*="instagram.com"], [href*="tiktok.com"]`)** – Memberi style berdasarkan atribut.  
```html
<footer>
  <p style="color: yellow">Ikuti saya di social media: <a href="https://www.instagram.com/dedywndy/">Instagram</a>, <a href="https://www.tiktok.com/@dedipakey?is_from_webapp=1&sender_device=pc">Tiktok</a></p>
</footer>
```

<img width="314" height="274" alt="image4" src="https://github.com/user-attachments/assets/d1966915-d0b5-4068-8203-c28d362de3b9" />

- **Selektor ID (`#email`)** – Menyasar elemen spesifik yang unik.
<img width="747" height="22" alt="image5" src="https://github.com/user-attachments/assets/2834ea3e-6410-463c-8efe-e535ec257a28" />

```css
#email {
  font-weight: 700;
  color: #3f51b5;
}
#email a {
  text-decoration: none;
}
```
- **Pseudo-class (`.nav-link:hover`)** – Menentukan tampilan saat kondisi tertentu (misal saat diarahkan kursor). 
<img width="597" height="57" alt="image7" src="https://github.com/user-attachments/assets/9a9e7a79-819e-47fe-b120-d7e5097e4b4b" />
<br>
<img width="237" height="91" alt="image6" src="https://github.com/user-attachments/assets/0534daf1-b887-4cc9-9d8d-dac1178002b0" />

- **Pseudo-element (`h1::first-line, p::first-line `)** – Memformat bagian tertentu dari elemen (misal baris pertama).
<img width="494" height="76" alt="image11" src="https://github.com/user-attachments/assets/e56f6439-50e1-403c-bd2b-850b7b788cb4" />

<br>

<img width="354" height="146" alt="image8" src="https://github.com/user-attachments/assets/b6c47c3b-b77d-46a6-b02e-4823d27300ba" />

**Fungsi umum selektor:** Mengatur tampilan elemen HTML secara fleksibel sesuai kebutuhan.

---

### 5) Mengenal **Box Model** pada CSS
<img width="482" height="244" alt="image" src="https://github.com/user-attachments/assets/540e325c-3c3e-4763-9c15-94012fc7eaca" />
<br>
<img width="225" height="102" alt="image" src="https://github.com/user-attachments/assets/842c6dca-b526-4c70-bb79-ea1d9d51ab5d" />

Potongan Kode ini menampilkan elemen dengan pengaturan `margin`, `padding`, `border`, dan `content`.  
**Fungsi:** Memahami bagaimana ukuran dan ruang di sekitar elemen web diatur agar layout rapi dan konsisten.

---

### 6) Membuat File CSS Eksternal dan Menghubungkannya (`style.css`)

<img width="116" height="108" alt="image" src="https://github.com/user-attachments/assets/09c25658-e42e-48a9-b410-ca5cb5424279" />

Hubungkan file CSS eksternal di dalam `<head>`:

```html
<link rel="stylesheet" href="style.css" />
```

Masukan style yang berada pada CV.html masukan ke file `style.css`:

```css
body {
  font-family: Arial, sans-serif;
}

header {
  background-color: #6b8e4e;
  padding: 20px;
  text-align: center;
}

header h1::first-line {
  font-size: 140%;
  font-weight: 800;
}

header p::first-line {
  font-variant: small-caps;
}

.navbar {
  margin: 14 0;
  text-align: center;
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: inline-block;
}

.nav-item {
  display: inline-block;
  margin: 0 10;
}

.nav-link {
  text-decoration: none;
  color: #3f51b5;
}

.nav-link:hover {
  background: #3f51b5;
  color: #fff;
  text-decoration: underline;
}

section {
  border: 1px solid #ddd;
  padding: 15px;
  margin: 20px 0;
  box-shadow: 0 0 5px #aaa;
}

#email {
  font-weight: 700;
  color: #3f51b5;
}

#email a {
  text-decoration: none;
}

footer {
  background-color: #6b8e4e;
  padding: 10px;
  text-align: center;
}

a[href*="instagram.com"]::after,
a[href*="tiktok.com"]::after {
  content: " ↗";
  display: inline-block;
  color: #fff;
  font-size: 10px;
  vertical-align: text-top;
}
```
Fungsi dibuatkan file style.css untuk memisahkan desain dari struktur agar kode lebih rapi, mudah dikelola, dan digunakan ulang.

---

### 7) Contoh **Inline CSS**

```html
<header>
  <h1 style="color: aliceblue">Dedy Wanditya</h1>
  <p style="color: yellow">Web Developer | Graphic Designer</p>
</header>

<footer>
  <p style="color: yellow">Ikuti saya di social media: <a href="https://www.instagram.com/dedywndy/">Instagram</a>, <a href="https://www.tiktok.com/@dedipakey?is_from_webapp=1&sender_device=pc">Tiktok</a></p>
</footer>
```
Fungsi menggunakan Inline CSS untuk memberi style cepat untuk elemen tertentu tanpa memengaruhi elemen lain.

---
### 8) Pengembangan html semantik dan CSS
## Struktur Halaman (HTML Semantik)
- **Header**
  
  <img width="699" height="166" alt="Tangkapan Layar 2025-09-26 pukul 21 01 47" src="https://github.com/user-attachments/assets/730b45be-25b3-4a2b-b4e5-1ba5cb75d732" />
  
```css
  header {
    position: relative;
    isolation: isolate;
    background: radial-gradient(1200px 400px at 0% 0%, rgba(122, 162, 255, 0.25), transparent 60%), linear-gradient(135deg, #7aa2ff -10%, #9ef0ff 40%, transparent 40%), #12162a;
    padding: 2.5rem 1.5rem 1.5rem;
    box-shadow: 0 8px 30px rgba(0, 0, 0, 0.25);
    border-bottom: 1px solid rgba(255, 255, 255, 0.06);
  }
  header .container {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 1.5rem;
    align-items: center;
  }
  .avatar {
    width: 108px;
    height: 108px;
    border-radius: 999px;
    object-fit: cover;
    border: 3px solid rgba(255, 255, 255, 0.6);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);
    background: #ddd;
  }
  header h1 {
    margin: 0 0 0.25rem;
    font-size: clamp(1.6rem, 2.8vw, 2.25rem);
    letter-spacing: 0.2px;
    color: #ffffff;
  }
  header p {
    margin: 0;
    color: #ffd166;
    font-weight: 600;
    opacity: 0.95;
  }
```
  Berisi avatar (`<img class="avatar">`), nama (`<h1>`), dan peran (`<p>`).

- **Navigasi** (`<nav class="navbar">`)
  <img width="884" height="177" alt="Tangkapan Layar 2025-09-26 pukul 21 05 39" src="https://github.com/user-attachments/assets/3fb2a9fc-6933-488b-982b-7da3ce0e6bbb" />
```css
.navbar {
  position: sticky;
  top: 0;
  z-index: 50;
  backdrop-filter: blur(6px);
  background: rgba(18, 22, 42, 0.85);
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}
.navbar .container {
  display: flex;
  justify-content: center;
}
.nav-list {
  list-style: none;
  margin: 0;
  padding: 0.75rem;
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
}
.nav-item {
  margin: 0;
}
.nav-link {
  display: inline-block;
  padding: 0.55rem 0.9rem;
  border-radius: 999px;
  background: rgba(18, 22, 42, 0.95);
  border: 1px solid rgba(255, 255, 255, 0.08);
  transition: transform 0.16s ease, background 0.2s ease, color 0.2s ease, box-shadow 0.2s ease;
}
.nav-link {
  color: #ffffff;
  text-decoration: none;
}
.nav-link:hover {
  transform: translateY(-1px);
  background: linear-gradient(180deg, #7aa2ff, #1fb6ff);
  color: #ffffff;
  text-decoration: none;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.25);
}
```
  Tautan anchor ke: **Biodata**, **Pendidikan**, **Skills**.

- **Section**  
  1. `<section id="biodata">` – kartu profil: foto kecil, nama, role, daftar info (email/telepon/domisili).
       <img width="1073" height="354" alt="Tangkapan Layar 2025-09-26 pukul 21 09 25" src="https://github.com/user-attachments/assets/f5cdf0bd-9052-444b-8547-d82fe3d7e5f4" />
       ```css
       #biodata {
          background: linear-gradient(180deg, #eef4ff, #ffffff 55%);
        }
        #pendidikan {
          background: linear-gradient(180deg, #f2f6ff, #ffffff 55%);
        }
        #skills {
          background: linear-gradient(180deg, #f7f9ff, #ffffff 55%);
        }
        
        #biodata,
        #pendidikan,
        #skills {
          border-top: 1px solid #e5e7eb;
          border-bottom: 1px solid #e5e7eb;
        }
        
        #biodata p {
          margin: 0.35rem 0;
        }
        #email {
          font-weight: 700;
          color: #2b6bff;
        }
        #email a {
          text-decoration: underline;
        }
       ```

  2. `<section id="pendidikan">` (riwayat pendidikan).
     <img width="596" height="498" alt="Tangkapan Layar 2025-09-26 pukul 21 10 55" src="https://github.com/user-attachments/assets/6972472b-06cd-4bd1-a9ae-fa59fde967a5" />
     ```css
        #pendidikan ul {
          margin: 0.25rem 0 0;
          padding-left: 1.15rem;
        }
        #pendidikan li {
          margin: 0.25rem 0;
        }
        #pendidikan li::marker {
          color: #2b6bff;
        }
     ```

  3. `<section id="skills">`
     <img width="789" height="211" alt="Tangkapan Layar 2025-09-26 pukul 21 13 31" src="https://github.com/user-attachments/assets/44d2631a-eb9b-475e-bddb-46f8f83d8308" />

     ```css
      #skills p {
        margin: 0;
        padding: 0.7rem 0.9rem;
        background: #ffffff;
        border: 1px solid #e5e7eb;
        border-radius: 12px;
        box-shadow: 0 6px 18px rgba(17, 24, 39, 0.06);
      }
     ```
---


## KESIMPULAN

Penggunaan HTML semantik (mis. `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`) memberikan struktur dan makna yang jelas pada konten web, meningkatkan aksesibilitas bagi pengguna termasuk pemakai _assistive technologies_ serta membantu optimasi mesin pencari (SEO). Sementara itu, CSS berperan dalam mengatur tampilan dan presentasi, memisahkan desain dari struktur sehingga pengelolaan dan pengembangan situs menjadi lebih rapi, fleksibel, dan konsisten. Kombinasi HTML semantik dan CSS menghasilkan website yang tidak hanya fungsional tetapi juga estetis, mudah diakses, dan lebih mudah dipelihara.

---

## LAMPIRAN
**Tampilan CV DEDY** (Tampilan style belum dikembangkan)
<img width="1426" height="788" alt="Tangkapan Layar 2025-09-26 pukul 19 44 43" src="https://github.com/user-attachments/assets/7a5fec0d-bc6a-4e5c-a341-68ab8eabfdd7" />
<br>
<br>
**Tampilan CV DEDY** (Tampilan style sudah dikembangkan)
<img width="1440" height="900" alt="Tangkapan Layar 2025-09-26 pukul 21 33 13" src="https://github.com/user-attachments/assets/05df07f2-ba65-4229-9396-c4fd026f2d23" />







