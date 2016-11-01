#JS di Halaman Web
Dalam sebuah halaman web, JS digunakan untuk menambahkan konten dinamis. Tanpa JS, halaman web yang tersusun dari file HTML dan CSS hanya bisa menampilkan halaman statis, di mana isinya tidak akan berubah-ubah sepanjang waktu, kecuali bila file tersebut diubah.

Sebagai contoh, halaman web berikut hanya menampilkan sebuah angka, 0.

```
<html>

<head>
</head>

<body>
  <div id="penghitung">0</div>
</body>

</html>
```

Apabila kita ingin agar angka tersebut berganti setiap detik, sehingga bisa menjadi semacam counter sederhana, maka kita bisa menambahkan script JS di dalam file HTML tersebut, sehingga bentuk akhirnya menjadi berikut

```
<html>

<head>
</head>

<body>
  <div id="penghitung">0</div>

  <!-- Script JS untuk membuat counter -->
  <script>
    var angka = 0;
    var intervalWaktu = window.setInterval(hitungWaktu, 1000);

    function hitungWaktu() {
      angka++;
      document.getElementById('penghitung').innerHTML = angka;
    }
  </script>
</body>

</html>
```

Dalam prakteknya, JS digunakan untuk menambahkan interaktivitas, terutama di tampilan antarmuka (UI) sebuah halaman website. Setiap tombol yang dibuat untuk melakukan suatu tugas, seperti login atau menambahkan belanjaan ke dalam keranjang belanja di sebuah situs *e-commerce*, pasti mengaplikasikan script yang secara spesifik menjalankan tugas yang berkaitan.

Contoh lain di mana JS digunakan untuk membuat konten dinamis adalah di halaman web Instagram, di mana foto-foto yang ditampilkan akan diambil terlebih dahulu dari server untuk kemudian dimunculkan secara berurutan, mengikuti algoritma tertentu. Di sisi peramban milik pengguna halaman web Instagram, ini dilakukan oleh JS. Sehingga, meskipun struktur file HTML-nya sama, ia akan menampilkan konten yang berbeda, saat diakses oleh pengguna.
