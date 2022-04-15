# Selamat Datang di DogglersApp!
==================================

Aplikasi ini merupakan proyek mandiri kedua yang diberikan dalam [Android Basics in Kotlin](https://developer.android.com/courses/android-basics-kotlin/course).


# Apa yang ada di DogglersApp?
------------
DogglersApp menggunakan RecyclerView dalam tampilan vertikal, horizontal, dan grid untuk menampilkan sekelompok tampilan dalam bentuk CardViews yang terdiri atas gambar, nama, umur, dan hobi.


## Bagaimana Cara Mengerjakan Tugas DogglersApp?
--------------
Tugas Mandiri Proyek Dogglers app sudah dibekali dengan kode, yang harus dilakukan kemudian adalah melengkapi bagian kode serta desain tampilan dengan panduan pada daftar TODO. Langkah-langkah yang dilakukan dapat diuraikan sebagai berikut:

## Bagian Desain Tampilan

Pada bagian desain, kita perlu membuat desain xml untuk tampilan horizontal atau vertikal serta tampilan grid. Untuk RecyclerView horizontal/vertikal, kita bisa menggunakan MaterialCardView dengan ConstraintLayout di dalamnya untuk memberikan informasi tentang si anjing, yaitu nama, umur, dan hobinya. Demikian pula halnya dengan tata letak grid.

### Bagian Koding

Pada bagian koding, kita harus menerapkan adapter untuk menampilkan gambar, nama, umur, dan hobi anjing pada desain frontend yang telah kita buat pada bagian sebelumnya.

Pertama, kita deklarasikan sebuah variabel yang memuat daftar (list) informasi tentang anjing.

![Imgur](https://i.imgur.com/8eELkFr.png)

Lalu, kita buat kelas DogCardViewHolder yang merupakan extend dari RecyclerView.ViewHolder.

Pada kelas itu kita definisikan tampilan yang berbeda untuk item yang kita perlu modifikasi, yaitu: gambar anjing serta teks dari nama, umur dan hobi.

![Imgur](https://i.imgur.com/dCYBl9r.png)

Kemudian, kita terapkan method onCreateViewHolder dari kelas DogCardViewHolder yang inherit dari parent class RecyclerView.ViewHolder.

Untuk yang mengalami kendala dengan skenario ini, misalnya, tata letak (layout) mana yang harus di inflate (Vertikal/Horizontal atau Grid) ? Kita bisa menggunakan ekspresi when yang memeriksa apakah variabel layout dari DogCardAdapter bernilai "Layout.Grid" atau bernilai lain seperti "Layout.Vertical" atau "Layout.Horizontal".

![Imgur](https://i.imgur.com/CiKmmgp.png)

Selanjutnya, kita bisa implementasikan metode getItemCount().

![Imgur](https://i.imgur.com/mkyYD5Z.png)

Langkah terakhir, kita terapkan metode onBindViewHolder() yang mengatur nilai yang berbeda sesuai dengan antarmuka yang ada pada ViewHolder.

Ambil posisi terkini tampilan si anjing yang ada dalam variabel dogData, lalu atur gambar,  nama, umur, dan hobinya. Perlu diingat untuk selalu menggunakan ".?" (safe call operator untuk null-safety).

![Imgur](https://i.imgur.com/nG7HR4X.png)


## Tampilan Akhir Project

- Tampilan Halaman Peluncuran (Launcher app):

![Imgur](https://i.imgur.com/b2apNk9.png)

- Tampilan Vertikal:

![Imgur](https://i.imgur.com/Ol31Ty4.png)

- Tampilan Horizontal:

![Imgur](https://i.imgur.com/o4w6PII.png)

- Tampilan Grid:

![Imgur](https://i.imgur.com/wbsM0xm.png)

