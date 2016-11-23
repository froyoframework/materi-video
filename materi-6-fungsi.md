Fungsi adalah sebuah cara untuk mengumpulkan beberapa pernyataan yang melakukan tugas tertentu, ke dalam satu entitas. Fungsi ini bisa dibayangkan sebagai sebuah modul kecil yang menyusun program yang lebih besar. Penggunaan fungsi akan membuat program lebih rapih dan modular, karena kita tidak lagi membuat satu program panjang, melainkan program yang terdiri dari blok-blok yang lebih kecil dan spesifik.

Sebagai contoh, dalam sebuah karakter di game, kita bisa membuat fungsi lompat, lari, tembak dan sebagainya. Dengan membagi program seperti ini, kode sumber akan lebih mudah dibaca dan diinterpretasi di masa depan.

## Membuat Fungsi

Format penulisan fungsi adalah sebagai berikut

```javascript
function namaFungsi() {
  //badan fungsi, kumpulan pernyataan yang akan dijalankan oleh fungsi
}
```

Sebagai contoh, fungsi berikut akan menampilkan suhu kota hari ini

```javascript
function tulisSuhu() {
  let suhu = 26;
  let kota = 'Jakarta';

  console.log("suhu di kota " + kota + " adalah " + suhu);
}
```

Di contoh tadi, fungsi baru dibuat saja, dan belum digunakan. Untuk menjalankan fungsi tersebut, kita perlu memanggil nama fungsinya saja.

```javascript
tulisSuhu();
```

Menjalankan fungsi ini kemudian dikenal dengan istilah memanggil fungsi.

## Memberikan Argumen

Fungsi `tulisSuhu()` tadi jika dipanggil, akan selalu menampilkan pesan yang sama. Jika kita ingin menampilkan pesan yang berbeda, maka kita perlu mengubah isi dari variabel `suhu` dan `kota`. Ini bisa dilakukan berbarengan dengan memanggil fungsi, apabila fungsi kita memiliki tempat untuk argumen. Penulisannya bisa sebagai berikut:

```javascript
function tulisSuhu(kota_, suhu_) {
  let suhu = suhu_;
  let kota = kota_;

  console.log("suhu di kota " + kota + " adalah " + suhu);
}
```

Kali ini, kita berikan tempat bagi argumen dan ia bisa langsung dipakai di dalam badan fungsi. Sehingga, sebagai contoh, fungsi bisa dipanggil sebagai berikut:

```javascript
tulisSuhu("Bandung", 24);
```

## Nilai Balik Fungsi

Setelah sebuah fungsi selesai berjalan, ia bisa menghasilkan sebuah nilai. Ini kemudian dikenal dengan istilah nilai balik (_return value_). Nilai balik ini kemudian bisa langsung digunakan sebagai nilai dari sebuah variabel. Keberadaan nilai balik ditandai oleh kata kunci `return`.

Fungsi berikut akan melakukan konversi suhu dari satuan Fahrenheit ke Celcius. Perlu diingat, rumusnya adalah

```
5/9 x (suhuFahrenheit - 32)
```

```javascript
function fahrenheitKeCelcius (suhuFahrenheit_) {
  let suhuFahrenheit = suhuFahrenheit_;
  let suhuCelcius;
  suhuCelcius = 5 / 9 * (suhuFahrenheit - 32);
  return suhuCelcius;
}
```

Kemudian fungsi ini bisa langsung dipanggil dan nilainya diberikan ke variabel yang akan menampungnya.

```javascript
let suhuKota;
suhuKota = fahrenheitKeCelcius(128);
```
