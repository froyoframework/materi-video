Salah satu poin melakukan pemrograman adalah kita ingin melakukan hal-hal yang berulang secara otomatis. Misalnya, saya ingin menulis 10 bilangan ganjil pertama. Tentu saya bisa menuliskan ini secara manual, namun ini akan terasa membosankan dan tidak efisien. Kasus seperti ini adalah saat yang tepat untuk menggunakan konsep perulangan (loop).

Perulangan memungkinkan seorang programmer untuk mengotomasi melakukan menjalankan pernyataan yang sama berulang kali. Programmer cukup menuliskan parameter yang menggambarkan berapa kali perulangan ini akan terjadi. Pernyataan ini memiliki 2 bentuk di dalam JavaScript, `for` dan `while`.

## Perulangan `for`

Perulangan ini memiliki format sebagai berikut:

```javascript

for (titikAwal; titikAkhir; iterasi) {
  pernyataan;
}

```

Pada dasarnya, ketiga parameter di dalam `for()` menggambarkan index, sebuah nilai yang menunjukkan jumlah perulangan. Parameternya dijelaskan sebagai berikut:
- titikAwal adalah nilai awal index
- titikAkhir adalah nilai akhir index
- iterasi adalah nilai yang menunjukkan penambahan titikAwal hingga ia akan mencapai titikAkhir

Sebagai contoh, untuk menuliskan sebuah pernyataan di console sebanyak 10 kali, kita bisa menuliskan script berikut

```javascript
for (let i = 0; i < 10; i++) {
  console.log ("ini adalah pernyataan ke " + i);
}
```

Pada contoh tadi, perulangan terjadi sebanyak 10 kali, diawali dari titikAwal bernilai 0, hingga bernilai 9. Parameter `i++` artinya titikAwal akan bertambah 1, setiap 1 kali perulangan selesai. Perlu diingat juga, bahwa titikAwal bisa dimulai dari angka berapapun, tidak harus 0. Iterasi juga tidak perlu bertambah 1 dalam setiap langkah. Menuliskan `i += 2` juga valid sekali.

Kembali ke kasus awal, jika saya ingin menuliskan 10 bilangan ganjil pertama, saya bisa menggabungkan perulangan dengan kondisional, sebagaimana ditulis di script ini:

```javascript
// saya uji terhadap 20 bilangan pertama
for (let i=1; i < 20; i++) {
  //mengecek apakah bilangan ganjil atau tidak
  if (i % 2 != 0) {
    console.log (i);
  }
}
```

## Perulangan `while`

Format kedua yang bisa digunakan adalah `while`. Dalam format ini, sebuah perulangan akan berlangsung, selama kondisi yang ditulis di dalam `while` bernilai benar. Contoh, program sebelumnya apabila ditulis menggunakan `while` akan nampak sebagai berikut:

```javascript
//titikAwal indeks
let i = 0;
//titikAkhir indeks
while (i<10) {
  console.log ("ini adalah pernyataan ke " + i);
  //iterasi
  i++;
}
```

Kita bisa melihat bahwa, apa yang ditulis dalam 1 baris saat menuliskan `for`, kali ini ditulis dalam 3 baris terpisah.

## Latihan

1. Coba konversikan script yang menampilkan 10 bilangan ganjil pertama, dari format `for`, menjadi `while`
2. Buatlah sebuah deret berisi 100 angka, yang dimulai dari angka 5, dengan aturan sebagai berikut:
  - Jika angkanya ganjil, maka tampilkan angka tersebut
  - Jika angkanya genap, maka tampilkan kuadrat dari angka tersebut
Contoh: 5, 36, 7, 64, ...
