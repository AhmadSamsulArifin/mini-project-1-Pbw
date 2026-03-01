Nama : Ahmad Samsul Arifin

Nim : 2409116113

Mini Project 1 Pemrograamn Berbasis Web


# Website Portfolio Ahmad Samsul Arifin


## Deskripsi Project
Website portfolio berbasis HTML & CSS dengan tampilan seperti website portfolio yang ada home,about,certificates,contact, dan lets talk. Website ini juga menggunakan Bootstrap 5 dan Vue JS sebagai nilai tambah.


## Tujuan Project
- Membuat halaman web dengan struktur HTML yang benar.
- Menerapkan styling CSS untuk warna, layout, dan tampilan yang modern.
- Menggunakan Bootstrap 5 untuk mempercepat pembuatan layout.
- Menggunakan Vue JS untuk menampilkan data statis dengan cara yang lebih rapi.


## Struktur Folder
- index.html
- style.css
- assets
  - foto saya.jpeg
  - sertifikat makrab.png
  - setifikat aplikasi.jpg
  - sertifikat ic.jpg
  - sertifikat Hrd.png
 
## Navbar

### Fitur yang ada :
  - Brand MyPortfolio
  - Menu navigasi: Home, About, Certificates, Contact
  - Tombol Let’s Talk

### Penjelasan Code:
a.  Navbar dibuat menggunakan komponen Bootstrap:
- nav class="navbar navbar-expand-lg navbar-dark navTop sticky-top">. saya hilangkan tanda nya < satu karena nanti terbaca oleh githubnya
- navbar-expand-lg : menu akan collapse pada layar kecil.
- sticky-top : navbar tetap terlihat saat halaman di-scroll.
- collapse navbar-collapse : berfungsi untuk menyembunyikan menu ketika ukuran layar mengecil.
- data-bs-toggle="collapse" : mengatur buka/tutup menu.
  
b. Brand yang ditampilkan menggunakan Vue: {{ brand }} nilai brand disimpan di dalam bagian data().

<img width="1338" height="48" alt="image" src="https://github.com/user-attachments/assets/bd56bad1-26b3-4e56-81da-e82b45815017" />


## Home 

### Fitur yang ada :
- Foto profil
- Nama lengkap
- Role / status
- Deskripsi singkat
- Tombol navigasi (About Me & Certificates)
- Icon Instagram

Penjelasan code : 
Section Home menggunakan:
 - header id="home">. saya hilangkan tanda nya < satu karena nanti terbaca oleh githubnya


a. Layoutnya menggunakan Bootstrap grid :
- container py-5 : untuk jarak atas bawah.
- row align-items-center : untuk konten sejajar vertikal.
- col-lg-6 : untuk membagi jadi 2 kolom teks dan foto.

b. Data yang ditampilkan menggunakan Vue terdiri dari :
- {{ profile.name }}
- {{ profile.role }}
- {{ profile.tagline }}

c. Foto dipanggil dari: 
- img src="assets/foto saya.jpeg" class="heroPhoto">/. saya hilangkan tanda nya < satu karena nanti terbaca oleh githubnya


<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/700b00da-296d-404d-a3e4-8cc22d89ad04" />

## Highlights Section

### Fitur yang ada :
- Main Style
- Game Favorit
- Aktivitas

Penjelasan code : 
a. Layout menggunakan: col-md-4 yang berarti pada ukuran layar sedang hingga besar akan tampil dalam 3 kolom.
Ketika ukuran layar lebih kecil atau mobile, setiap kolom akan tersusun vertikal ke bawah secara otomatis.

b. Card menggunakan class : .glassCard yang memberikan efek transparan dengan tambahan border dan bayangan.


<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/51347555-a7bb-4ce0-b0e7-b4a7c0d56256" />

## About me 

Ada lima bagian pada about me yaitu : 

Penjelasan code :

a. Pada quick info terdapat 3 fitur yaitu :
- Fokus
- Minat
- Tujuan
Data diambil dari Vue jadi kalau mau ganti tinggal di ubah di bagian datanya yang berisikan :
- {{ about.focus }}
- {{ about.interest }}
- {{ about.goal }}

b. Kemudian yang kedua terdapat favorites yang terdapat 4 fitur yaitu :
- pubg
- mobile legends
- main olahraga
- voice chat
pada bagian saya menggunakan class .favBadge yang dibuat agar terlihat seperti tag yang modern.

c. Yang ketiga terdapat about me yang berisi deskripsi. 
- Deskripsi diambil dari: {{ about.description }} yang ditampilkan dalam card .glassCard agar terlihat modern.

d. Yang keempat terdapat skills yang menampilkan skill dengan persentase.
- Data skill disimpan dalam array skills,
- Kemudian ditampilkan menggunakan: v-for="(s,i) in skills"
- Progress bar menggunakan binding : :style="{ width: s.level + '%' }" yangg berarti panjang dari bar mengikuti nilai presentase.

e. Dan yang terakhir terdapat Experience yang menampilkan pengalaman organisasi dan ditampilkan dalam bentuk timeline sederhana.
- Data diambil dari: v-for="(e,i) in experiences"
- Timeline dibuat menggunakan CSS:
- .timeLine {
  border-left: ...
}
Sehingga muncul garis vertikal seperti alur pengalaman.


<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/c8ccdfba-e78b-4803-b700-0c7885e68382" />

## Certificates

### Fitur yang ada :
- Menampilkan daftar sertifikat
- Layout grid 2 kolom
- Tombol lihat sertifikat
- Menampilkan jumlah total sertifikat

Penjelasan code :
a. Layout grid menggunakan: col-md-6 yang berarti pada ukuran layar sedang hingga besar akan tampil dalam 2 kolom. Ketika ukuran layar lebih kecil atau mobile,akan tampil dalam 1 kolom.

b. Kemudian menampilkan tahun menggunakan : {{ c.year }} 

c. dan yang terakhir tombol akan aktif jika link yang di isi pada bagian : v-if="c.link" jika tidak di isi maka tombol disabled otomatis.

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/2a3228f4-87ef-4bd4-9cd0-7e516e8e5928" />

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/4342f16b-3379-4393-85ac-a0e43dfb72cd" />

## Contact

### Fitur yang ada : 
- Menampilkan email
- Menampilkan lokasi

Penjelasan code :
a. Data berasal dari Vue:
{{ profile.email }}
{{ profile.location }}

Dan ditampilkan dalam bentuk badge dengan class .pill untuk membuat elemen terlihat berbentuk kapsul atau pil.

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/8cfdcb2e-d3b4-46a4-a44b-bd8820af0984" />

## Teknologi yang Digunakan
1. Html
   Digunakan untuk membangun struktur utama website:
   - Struktur dasar (<!DOCTYPE html>, html, head, body)
   - Section dengan id (#home, #about, #certificates, #contact)
   - Elemen utama (navbar, header, section, footer)
   - Gambar profil dan link sertifikat

2. Css
   Digunakan untuk mengatur tampilan dan tema :
   - Background utama (body, .heroWrap)
   - Efek glow hero (radial-gradient)
   - Card transparan / glass (.glassCard)
   - Panel gelap Quick Info (.darkCard)
   - Styling tombol (.btnMain, .btnOutline, .btnTalk)
   - Styling icon sosial (.socialBtn)
   - Badge / tag (.favBadge, .chipTag, .yearBadge)
   - Timeline pengalaman (.timeLine, .timeItem)
   - Progress bar custom (.progressDark, .barCyan)
   - Responsif tambahan (@media (max-width: 992px))
  
3. Bootstrap 5
   Digunakan untuk membantu layouting :
   - Navbar responsif (navbar, navbar-expand-lg, collapse)
   - Grid system (container, row, col-md-*, col-lg-*)
   - Progress bar (progress, progress-bar)
   - Button (btn)
   - Utilities spacing (py-*, mb-*, gap-*)
  
4. Vue JS
   Digunakan untuk menampilkan data tetap statis:
   - Penyimpanan data (data())
   - Interpolation ({{ }})
   - Perulangan data (v-for)
   - Binding atribut (:style, :href)
   - Mounting Vue (.mount('#app'))
   










