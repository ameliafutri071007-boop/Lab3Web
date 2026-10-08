# LAB3WEB - Praktikum 3 CSS Dasar

## Identitas Mahasiswa
- **Nama:** Amelia Futri
- **NIM:** 312510348
- **Mata Kuliah:** Pemrograman Web
- **Praktikum:** Lab2_css_dasar.html


## Deskripsi Praktikum
Praktikum 3 membahas dasar-dasar CSS (Cascading Style Sheet), mulai dari konsep CSS, struktur CSS, cara penulisan CSS internal, external, dan inline, sampai penggunaan selector elemen, ID, dan class.

## Tujuan Praktikum
1. Memahami konsep dasar CSS.
2. Memahami aturan penulisan pada CSS.
3. Memahami selector sebagai pengontrol CSS.
4. Membuat pengaturan CSS pada HTML.

## Struktur Repository
```text
Lab3Web/
├── index.html
├── lab2_css_eksternal.html
├── style_eksternal.css
└── README.md
```

## Langkah Praktikum

### 1. Membuat Dokumen HTML
Membuat dokumen HTML dasar dengan judul **CSS Dasar**, header, navigation, paragraf, dan tombol informasi. Dokumen ini menjadi dasar untuk menerapkan CSS.

**Hasil:** halaman HTML berhasil dibuat dan dapat dibuka melalui browser.
`![gambar1](images/01-html-dasar.png)`

### 2. Mendeklarasikan CSS Internal
CSS internal ditambahkan di dalam bagian `<head>` menggunakan tag `<style>`. Pengaturan diterapkan pada body, header, heading, dan teks italic.

**Hasil:** tampilan halaman berubah setelah CSS internal diterapkan.

**Screenshot:**  
`![CSS Internal](images/02-css-internal.png)`

### 3. Menambahkan Inline CSS
Inline CSS ditambahkan langsung pada elemen HTML. Pada praktikum, paragraf diberi pengaturan rata tengah dan warna teks.

**Hasil:** hanya elemen yang diberi inline CSS yang menerima pengaturan tersebut.

**Screenshot:**  
`![Inline CSS](images/03-inline-css.png)`

### 4. Membuat CSS Eksternal
Dibuat file `style_eksternal.css` yang terpisah dari file HTML. File tersebut kemudian dihubungkan menggunakan tag `<link>` pada bagian `<head>`.

**Hasil:** tampilan halaman dapat diatur melalui file CSS yang terpisah dari HTML.

**Screenshot:**  
`![CSS Eksternal](images/04-css-eksternal.png)`

### 5. Menambahkan CSS Selector
Pada file CSS eksternal digunakan ID Selector dan Class Selector.

ID Selector menggunakan tanda `#` dan diterapkan pada elemen dengan ID `intro`. Class Selector menggunakan tanda `.` dan diterapkan pada class `button` serta `btn-primary`.

**Hasil:** bagian `intro` dan tombol mendapatkan tampilan khusus sesuai aturan CSS.

**Screenshot:**  
`![ID dan Class Selector](images/05-selector.png)`

## Soal dan Jawaban

### Soal 1
**Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.**

**Jawaban:**
Eksperimen dilakukan dengan mengubah beberapa properti CSS seperti `font-size`, `color`, `background`, `padding`, `margin`, `text-align`, dan `border`. Perubahan properti tersebut memengaruhi tampilan halaman tanpa harus mengubah struktur HTML.

Contohnya, `background` dapat digunakan untuk mengubah warna latar, `font-size` untuk mengatur ukuran tulisan, `padding` untuk memberikan jarak bagian dalam elemen, dan `margin` untuk memberikan jarak antar elemen.

### Soal 2
**Apa perbedaan pendeklarasian CSS elemen `h1 {...}` dengan `#intro h1 {...}`? Berikan penjelasannya!**

**Jawaban:**
`h1 {...}` merupakan selector elemen yang berlaku untuk semua elemen `<h1>` pada halaman tersebut. Sedangkan `#intro h1 {...}` merupakan selector yang lebih spesifik karena hanya berlaku untuk elemen `<h1>` yang berada di dalam elemen yang memiliki ID `intro`.

Jadi, jika terdapat beberapa `<h1>`, aturan `h1` dapat memengaruhi semuanya, sedangkan `#intro h1` hanya memengaruhi `<h1>` yang berada di dalam `#intro`.

### Soal 3
**Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!**

**Jawaban:**
Jika selector memiliki tingkat spesifisitas yang sama, CSS inline pada elemen akan memiliki prioritas lebih tinggi dibandingkan CSS internal dan CSS eksternal. CSS internal dan eksternal kemudian mengikuti aturan cascade dan spesifisitas selector.

Contoh, jika sebuah paragraf memiliki CSS eksternal `p { color: blue; }`, CSS internal `p { color: green; }`, dan pada HTML terdapat `style="color: red;"`, maka warna teks yang ditampilkan adalah merah karena inline CSS memiliki prioritas lebih tinggi pada kondisi tersebut.

### Soal 4
**Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!**

**Jawaban:**
Jika satu elemen memiliki ID dan Class, selector ID memiliki tingkat spesifisitas lebih tinggi daripada selector Class. Oleh karena itu, jika kedua selector mengatur properti yang sama, deklarasi dari ID biasanya akan diprioritaskan.

Contoh:
`<p id="paragraf-1" class="text-paragraf">Teks paragraf</p>`

Jika terdapat:
`#paragraf-1 { color: red; }`

dan:
`.text-paragraf { color: blue; }`

maka warna teks yang ditampilkan adalah merah karena selector ID lebih spesifik daripada selector Class.

## Kesimpulan
Praktikum 3 memberikan pemahaman tentang penggunaan CSS untuk mengatur tampilan halaman web. Pada praktikum ini dipelajari CSS internal, inline, dan eksternal serta penggunaan selector elemen, ID, dan class. Dengan CSS, tampilan HTML menjadi lebih terstruktur, menarik, dan mudah diatur.

## Validasi CSS
Validasi CSS dapat dilakukan menggunakan CSS Validator dari W3C:
https://jigsaw.w3.org/css-validator/

## Dokumentasi
Sesuai instruksi praktikum, setiap perubahan sebaiknya didokumentasikan menggunakan screenshot dan dimasukkan ke repository. Tambahkan folder `images/` jika ingin menyimpan screenshot hasil praktikum.

Contoh:
```text
Lab3Web/
├── images/
│   ├── 01-html-dasar.png
│   ├── 02-css-internal.png
│   ├── 03-inline-css.png
│   ├── 04-css-eksternal.png
│   └── 05-selector.png
├── index.html
├── lab2_css_eksternal.html
├── style_eksternal.css
└── README.md
```

