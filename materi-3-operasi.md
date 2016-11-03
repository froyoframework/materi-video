# Operasi

Video ini membahas seputar operasi, sebuah cara untuk memanipulasi variabel. Konsepnya sama dengan dasar matematika, di mana sebuah bilangan bisa diubah-ubah nilainya dengan mengunakan simbol tertentu.

# Operasi Matematika

Operasi matematika, adalah sebuah operasi yang dilakukan untuk mengubah nilai sebuah bilangan. Bilangan ini bisa berupa variabel konstan, ataupun sebuah variabel yang mengandung tipe data numerik (integer atau float). Hasil dari operasinya juga berupa bilangan baru.

Sebagai contoh, apabila kita memiliki 2 variabel, `a = 12` dan `b = 4` maka, beberapa operasi metematika dasar yang bisa dilakukan adalah:

- Penambahan

```
a + b;
```

- Pengurangan

```
a - b;
```

- Perkalian

```
a * b;
```

- Pembagian

```
a / b;
```

- Modulo (sisa pembagian)

```
a % b; // hasilnya 0
```

Tentu saja hasil dari operasi ini bisa langsung diberikan ke variabel yang akan menampung nilainya. Sebagai contoh:

```
let z;
z = a * b; // z = 48
```

Selain itu, ada pula notasi yang melakukan operasi dan pemberian nilai langsung dalam 1 operasi. Sebagai contoh, untuk menambahkan 7 ke dalam variabel `a`, kita bisa mempersingkat penulisan:

```
a = a + 7;
```

menjadi

```
a += 7;
```

Penulisan ini valid juga untuk operasi lain, (perkalian, pengurangan dan pembagian). Khusus untuk penambahan dan pengurangan 1, kita bisa menggunakan notasi lain, yaitu:

```
a++;
```

Penulisan ini sama dengan menuliskan

```
a += 1;
```

## Operasi Perbandingan

Operasi perbandingan dilakukan dengan membandingkan besaran 2 bilangan numerik. Hasilnya kemudian berupa nilai boolean true atau false (benar atau salah). Operasi perbandingan yang bisa dilakukan adalah:

- Lebih kecil

```
a < b;
```

- Lebih kecil atau sama dengan

```
a <= b;
```

- Lebih besar

```
a > b;
```

- Lebih besar atau sama dengan

```
a >= b;
```

- Sama besar

```
a == b;
```

- Sama besar dan tipe datanya sama

```
a === b;
```

- Tidak sama besar

```
a != b
```

- Tidak sama besar atau tidak sama tipe datanya

```
a !== b;
```

# Operasi Logika

Operasi logika dilakukan kepada variabel yang memiliki tipe data boolean, dan hanya menghasilkan nilai boolean true atau false (benar atau salah). Operasi logika yang tersedia adalah:


- Negasi (kebalikan nilai logika)

```
let x = true;
!x; //menghasilkan false
```

- AND (bernilai benar jika kedua operand benar)

```
let x = true;
let y = true;
x && y; //menghasilkan true
```

- OR (bernilai benar jika salah satu operand benar)

```
let x = true;
let y = false;
x || y; //menghasilkan true
```
