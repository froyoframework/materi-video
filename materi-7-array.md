# Array

Array adalah sebuah tipe data yang memungkinkan programmer untuk mengumpulkan beberapa data dengan tipe data yang sama. Atau dengan kata lain, Array bisa kita anggap sebagai himpunan. Berbeda dengan variabel yang hanya memiliki 1 nilai saja, array memiliki beberapa nilai yang ditampung oleh 1 variabel. Semua anggota dalam array, dikenal dengan nama elemen array.

Contoh berikut akan membuat array berukuran 10 (memiliki 10 nilai)

```javascript
let himp = [10];
himp = [10, 8, 9, 4, 5, 6, 7, 10, 23, 9];
```

Sebagai alternatif, kita bisa juga membuat array tanpa menentukan ukurannya di awal

```javascript
// tetap membuat array berukuran 10
let himp = [10, 8, 9, 4, 5, 6, 7, 10, 23, 9];
```

Tentu saja, kita pun bisa membuat sebuah array berisi string. Peraturan dasarnya hanya semua elemen dalam array harus memiliki tipe data yang sama.

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso"];
```

## Mengakses Elemen Array

Setiap elemen dalam array memiliki indeks yang menandakan posisinya di dalam array. Indeks dimulai dari angka 0, sehingga elemen pertama memiliki indeks 0, elemen kedua 1, dan seterusnya. Masing-masing elemen ini kemudian bisa diakses dengan menggunakan sintaks berikut:

```javascript
namaArray[indeks];
```

Dalam prakteknya, ia bisa ditulis sebagai berikut:

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
//mengakses dan menampilkan elemen pertama dalam makanan, yakni nasi goreng
console.log(makanan[0]);
``` 

Setelah diakses, maka ia bisa digunakan sebagaimana variabel lain, seperti misalnya, diganti nilainya.

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
console.log(makanan);
makanan[2] = "martabak";
console.log(makanan);
```

Untuk mengakses keseluruhan array seperti contoh di atas, kita cukup memanggil nama array tersebut.

Tentu saja, kita juga bisa mengakses elemen array dengan menggunakan perulangan `for`

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
for (let i = 0; i < makanan.length; i++) {
	console.log(makanan[i]);
}
```

## Method dan Properti Array

Array memiliki beberapa method dan properti bawaan yang bisa kita gunakan untuk memudahkan melakukan pekerjaan dengannya. Selanjutnya beberapa properti dan method yang akan sering digunakan akan dibahas.

### Properti `length`

Properti ini akan menampilkan ukuran array


```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
console.log(makanan.length); //4
```

### Menambahkan dan Mengurangi Elemen Array

Properti `push()` bisa digunakan untuk menambahkan elemen baru di akhir array.

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
makanan.push("lemper");
console.log(makanan);
```

Sebaliknya, untuk menghilangkan elemen terakhir array, kita gunakan `pop()`.

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
makanan.pop();
console.log(makanan);
```

Untuk menambahkan atau mengurangi secara spesifik elemen di posisi tertentu, maka bisa kita gunakan method `splice()`.

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
makanan.splice(2, 0, "lemper");
console.log(makanan);
```

Kode tadi akan menambahkan lemper pada elemen berindeks ke-2 (2 pada parameter pertama `splice()`) dan tidak ada elemen yang dihilangkan (0 pada parameter kedua `splice()`)

Sebaliknya, untuk menghilangkan elemen spesifik, kita gunakan `splice()` sebagai berikut:

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
makanan.splice(2, 1);
console.log(makanan);
```

Kode tadi akan menghilangkan sebanyak 1 elemen (1 pada parameter kedua `splice()`) mulai dari elemen dengan indeks ke-2 (2 pada parameter pertama `splice()`).

### Menggabungkan dan Memisahkan Array

Kita bisa menggabungkan 2 buah array dengan menggunakan method `concat()`

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
let minuman = ["es teh", "soda gembira"];
let menuSaya = makanan.concat(minuman);
console.log(menuSaya);
```

Dengan kode tadi, maka elemen-elemen dalam array minuman akan ditambahkan ke dalam array makanan dan menjadi elemen paling belakang. Operasi ini tidak mengubah array makanan, karena hasil penggabungan kedua array akan menjadi nilai dari array baru, yakni menuSaya.

Untuk memisahkan elemen-elemen pada array dan menjadikannya array baru, kita bisa menggunakan method `slice()`

```javascript
let makanan = ["nasi goreng", "mi rebus", "bakso", "bolu"];
let menuDiskon = makanan.slice(1,3);
```

Dengan kode tadi, maka elemen ke-1 dan ke-2 dari array makanan akan dipisahkan dan dijadikan array baru bernama menuDiskon. Perhatikan bahwa elemen ke-3 tidak termasuk dalam elemen yang dipindahkan. Seperti `concat()`, operasi ini juga tidak mengubah array makanan.
