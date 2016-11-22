# Conditional Statement

Sejauh ini, kita telah membuat script sederhana dengan alur linear dan hanya memiliki 1 kemungkinan keluaran.

```javascript
let gaji = 3500000;
console.log("gaji kamu sebesar " + gaji);
```

Berapa kalipun script tadi dijalankan, ia akan tetap mencetak pernyataan yang sama di console.

Saat kita menulis sebuah program, akan ada kondisi di mana program kita membutuhkan beberapa kemungkinan hasil. Pada saat itu lah kita akan membutuhkan _conditional statement_ (pernyataan kondisional). Penggunaan pernyataan ini akan memungkinkan program untuk mengeluarkan hasil yang berbeda, tergantung dari masukan yang diterimanya.

Untuk membuat kondisi pada JavaScript kita menggunakan format berikut.

```javascript
if(value1 comparison_operator value2) {
    // blok kode untuk program jika kondisi true
} else {
    // blok kode untuk program jika kondisi false
}
```

Contoh penggunaannya seperti berikut ini.

```javascript
let gaji = 5500000;

if(gaji < 6000000) {
    console.log("Kamu pasti masih junior.");
} else {
    console.log("Levelmu sudah senior.");
}
```

Jika percabangan program kita lebih dari 1 kondisi, kita bisa menuliskan dengan cara seperti ini.

```javascript
let ongkos = 4500;

if(ongkos < 2000) {
    console.log("Tarif pelajar"); // true
} else if(ongkos > 2000 && ongkos < 5000) {
    console.log("Tarif normal"); // true
} else {
    console.log("Jangan lupa minta kembalian"); // false
}
```

`if ... else ...` juga bisa dibuat berlapis, pernyataan `if ... else ...` di dalam pernyataan `if ... else ...` yang lain.

```javascript
let username = 'asepbagja';
let password = '123456';

if(username === 'asepbagja') {
    console.log('Username ditemukan'); // true

    if(password === '123456') {
        console.log('Login berhasil'); // true
    } else {
        console.log('Login gagal'); // false
    }
} else {
    console.log('Login gagal'); // false
}
```

Apabila program yang dibuat memiliki banyak sekali kemungkinan keluaran, maka kita bisa juga menggunakan bentuk pernyataan kondisional lain, yakni `switch`. Pernyataan ini mirip dengan membuat pernyataan `if ... else if` dengan banyak sekali kemungkinan keluaran.

Contoh penulisan pernyataan ini adalah sebagai berikut:

```javascript
let posisi = 'manajer';
let gaji;

switch (posisi) {
  case 'manajer' :
    gaji = 20000000;
    break;
  case 'lead' :
    gaji = 10000000;
    break;
  case 'junior' :
    gaji = 5000000;
    break;
}

console.log(posisi + " dibayar sebesar " + gaji);
```

Perlu dicatat bahwa kondisi yang diperiksa haruslah berupa variabel dan bukan operasi. Dengan kata lain,
`switch (x)` bisa dilakukan, namun `switch (x+y)` tidak bisa dijalankan.

## Pro Tips

Sebaiknya tidak membuat `if ... else ...` yang berlapis terlalu dalam, karena akan membuat alur program menjadi sulit dibaca.
