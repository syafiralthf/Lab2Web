# Lab2Web - Praktikum 2: CSS Dasar

## Langkah Praktikum

### 1. Membuat dokumen HTML

Pertama kita buat file baru `lab2_css_dasar.html`.
Di dalamnya ditulis struktur HTML dasar berisi header, nav, dan div intro.
Tujuannya agar ada konten yang nanti bisa kita beri style dengan CSS.

<img width="1013" height="699" alt="Cuplikan layar 2025-10-02 195723" src="https://github.com/user-attachments/assets/5ebd3df6-12d3-4c9f-b767-cf4893408284" />

Output:

<img width="955" height="471" alt="Cuplikan layar 2025-10-02 134803" src="https://github.com/user-attachments/assets/c5f12173-da5c-4ac0-8f8b-37125e5a9506" />

### 2. Mendeklarasikan CSS Internal

CSS internal ditulis di dalam tag `<style>` pada bagian `<head>`.
Misalnya mengatur font, warna teks, ukuran heading, dan style tambahan untuk judul.
Dengan internal CSS, semua elemen yang sesuai aturan akan langsung berubah tampilannya.

<img width="839" height="667" alt="image" src="https://github.com/user-attachments/assets/3d99280b-7b5a-4165-aea4-c3ee271a2582" />

Output:

<img width="956" height="554" alt="Cuplikan layar 2025-10-02 135221" src="https://github.com/user-attachments/assets/52dca64f-6913-4b29-a5d0-2944172a2030" />

### 3. Menambahkan inline CSS

Inline CSS ditulis langsung di dalam tag HTML menggunakan atribut `style`.
Contohnya di `<p style="text-align: center; color: #ccd8e4;"> ... </p>`.
Hasilnya hanya berlaku untuk elemen tersebut saja.
Inline CSS punya prioritas paling tinggi dibanding internal atau eksternal.

<img width="1006" height="98" alt="image" src="https://github.com/user-attachments/assets/99d8108f-1630-4e07-bb8a-bf01102de91f" />

Output:

<img width="957" height="534" alt="Cuplikan layar 2025-10-02 140613" src="https://github.com/user-attachments/assets/a0132b00-f6da-468c-bcd2-5be5e465828a" />

### 4. Membuat CSS eksternal

Buat file baru bernama `style_eksternal.css`.
Isi file ini dengan aturan CSS, misalnya untuk `nav`, `a`, dan tampilan tombol.
Lalu file CSS ini dipanggil ke HTML dengan tag `<link rel="stylesheet" href="style_eksternal.css">`.

<img width="818" height="404" alt="image" src="https://github.com/user-attachments/assets/fe2f4054-f7a3-43d8-9267-2698f5b99587" />

<img width="764" height="78" alt="image" src="https://github.com/user-attachments/assets/97066fd0-8157-49f8-9d79-10bdbf7c98c3" />

Output:

<img width="953" height="569" alt="Cuplikan layar 2025-10-02 141848" src="https://github.com/user-attachments/assets/42cadca8-89c9-4f70-99d6-2b0582ed8578" />

### 5. Menambahkan CSS selector

Selector dipakai untuk memilih elemen tertentu.
- ID Selector (`#id`) → hanya berlaku untuk satu elemen dengan id tertentu.
- Class Selector (`.class`) → bisa dipakai di banyak elemen.

<img width="579" height="572" alt="image" src="https://github.com/user-attachments/assets/d3efe5a3-3ba6-443e-a2d5-23c4a7039e69" />

Output:

<img width="955" height="638" alt="Cuplikan layar 2025-10-02 142436" src="https://github.com/user-attachments/assets/4b8176ac-9454-4148-9c4e-76d2d144bcf6" />

## Pertanyaan dan tugas
### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

Saya mencoba menambahkan beberapa properti CSS, contohnya:

<img width="942" height="790" alt="image" src="https://github.com/user-attachments/assets/0fb6d3cb-64b3-41a3-b165-8e333dbca466" />

Output:

<img width="947" height="378" alt="image" src="https://github.com/user-attachments/assets/295be731-9f19-4a9d-8838-20b00891a8d5" />

Penjelasan:

- Body: diberi background biru muda (`#f0f8ff`) dan font diganti dengan Arial supaya tampilan lebih modern.
- Heading (h1): diatur agar berwarna biru tua, posisinya rata tengah, hurufnya otomatis menjadi kapital semua, dan jarak antar huruf dibuat lebih lebar agar terlihat tegas.
- Paragraf (p) dibuat berwarna abu-abu gelap, rata tengah, huruf agak besar (18px), dan bergaya miring agar berbeda dengan teks judul.

Dengan pengaturan ini, teks “Halo, nama saya Fira” tampil lebih jelas dan menarik, serta memberikan contoh nyata bagaimana CSS dapat mengubah tampilan halaman web hanya dengan beberapa baris kode.

### 2.Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!

<img width="790" height="693" alt="image" src="https://github.com/user-attachments/assets/99cda24c-1fb2-4d99-a20e-accbb3f40415" />

Output:

<img width="952" height="452" alt="image" src="https://github.com/user-attachments/assets/b2e03c74-bc9b-4768-82ec-0b7b521c712b" />

Penjelasan:

Deklarasi `h1 {...}` adalah aturan CSS yang berlaku untuk semua elemen `<h1>` pada halaman web, tanpa memandang letaknya. Jadi jika ada lima buah heading `<h1>` di halaman, maka semuanya akan terkena style yang sama. Aturan ini bersifat global untuk elemen tertentu.

Sementara itu, deklarasi `#intro h1 {...}` jauh lebih spesifik. Aturan ini hanya berlaku untuk elemen `<h1>` yang berada di dalam elemen lain yang memiliki atribut `id="intro"`. Artinya, jika ada beberapa heading `<h1>` di halaman, hanya `<h1>` yang berada di dalam `<div id="intro">...</div>` saja yang akan menerima style tersebut, sedangkan `<h1>` lainnya tidak terpengaruh.

### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

<img width="828" height="668" alt="image" src="https://github.com/user-attachments/assets/4f156f88-9e61-469a-a83e-b8e6b75c2d64" />
<img width="405" height="164" alt="image" src="https://github.com/user-attachments/assets/ca614c0f-ee69-4bef-8949-98222cd5b780" />

Output:

<img width="956" height="318" alt="image" src="https://github.com/user-attachments/assets/0fb3821c-2729-4d10-a616-b648ceeceeed" />

Penjelasan:

Dalam CSS terdapat konsep yang disebut specificity (tingkat kekuatan aturan). Browser memiliki urutan prioritas dalam membaca style, yaitu:
- Eksternal CSS → ditulis dalam file terpisah (`.css`) dan dipanggil dengan `<link>`.
- Internal CSS → ditulis di dalam file HTML pada tag `<style>` dalam `<head>`.
- Inline CSS → ditulis langsung dalam atribut `style` pada elemen HTML.

Jika ketiga jenis CSS tersebut diterapkan pada elemen yang sama, maka browser akan menampilkan style dari inline CSS, karena memiliki prioritas tertinggi. Internal CSS akan menimpa eksternal, sedangkan inline akan menimpa keduanya.

### 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! `( <p id="paragraf-1" class="text-paragraf"> )`

<img width="869" height="805" alt="image" src="https://github.com/user-attachments/assets/53b31777-3816-416e-8f12-c542d785563d" />

Output:

<img width="951" height="402" alt="image" src="https://github.com/user-attachments/assets/4a9f9880-3f96-4be8-8b77-47778df8f7c1" />

Penjelasan Hasil:
- Paragraf pertama (`class="text-paragraf"`) → tampil merah.
- Paragraf kedua (`id="paragraf-1"`) → tampil biru.
- Paragraf ketiga (`id="paragraf-1" class="text-paragraf"`) → tetap biru, karena aturan ID selector lebih kuat daripada class selector.
