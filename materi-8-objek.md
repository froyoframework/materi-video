# Objek

Dalam JavaScript, objek adalah sebuah entitas yang memiliki properti tertentu. Properti ini juga memiliki pasangan nilai, sehingga objek akan nampak sebagai sekumpulan pasangan properti-nilai dalam _field_-nya. 

Objek bisa dibayangkan sebagai sebuah makhluk yang memiliki properti tertentu yang akan mendeskripiskan makhluk tersebut.

Objek di JavaScript ditulis sebagai berikut:

```javascript
var hewan = {
	spesies: "kuda",
	kaki: 4,
	makanan: "rumput",
	lari: function() {
		console.log("saya sedang lari");
	}
};
```

# Properti dan Method Objek

Sebuah objek bisa memiliki properti dan method. Properti ditandai oleh nilai, sementara method adalah fungsi milik objek tersebut. Baik properti dan method bisa diakses dengan sintaks berikut:

```javascript
objek.properti;
objek.method();
```	

Sehingga untuk objek hewan tadi, kita bisa memanggil properti dan methodnya sebagai berikut:

```javascript
hewan.spesies;
hewan.lari();
```	

Cara lain untuk mengakses properti adalah

```javascript
hewan["spesies']
```

Properti sebuah objek juga bisa berupa array. Sebaliknya, array juga bisa berisi objek. Ini adalah dasar dari format penyimpanan data JSON (JavaScript Object Notation).

```javascript
var ternak = [
{spesies:"kuda", kelamin:"jantan"},{spesies:"sapi", kelamin:"betina"},{spesies:"ayam", kelamin:"betina"}
]
```

Setiap elemen kemudian bisa diakses seperti ini:

```javascript
console.log(ternak[0].spesies);
```

Contoh tadi menampilkan properti spesies milik objek pertama dalam array ternak.

