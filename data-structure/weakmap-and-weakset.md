# WeakMap and WeakSet

WeakMap merupakan varian dari Map yang mendukung _garbage collection_. Garbage collection adalah proses di mana interpreter JavaScript mengambil kembali memori yang tidak lagi “dapat dijangkau” dan tidak dapat digunakan oleh program\[[3](https://learning.oreilly.com/library/view/javascript-the-definitive/9781491952016/ch11.html)\]. Garbage collection di JavaScript dilakukan secara otomatis dan bukan menjadi urusan dari developer.

Yang dimaksud _weak_ dalam WeakMap adalah referensi terhadap nilai yang disimpan. Apabila suatu nilai yang disimpan di WeakMap sudah tidak terjangkau atau tidak bisa lagi diakses, maka referensi ke memorinya akan dihapus.

Berikut ini adalah beberapa hal yang membedakan antara Map dan WeakMap:

* Key dari WeakMap harus berupa object atau array. Nilai primitif tidak bisa digunakan sebagai key karena tidak mendukung garbage collection.
* WeakMap memiliki _method_get\(\), set\(\), has\(\), dan delete\(\). Namun, WeakMap tidak termasuk kategori iterable sehingga tidak memiliki method keys\(\), values\(\), atau forEach\(\).
* WeakMap juga tidak memiliki property size. Ini karena ukuran WeakMap dapat berubah karena proses garbage collection.

Masih bingung? Mari kita lihat contoh kode dan perbedaan antara Map dan WeakMap.

```javascript
let visitsCountMap = new Map(); // Menyimpan daftar user
 
function countUser(user) {
    let count = visitsCountMap.get(user) || 0;
    visitsCountMap.set(user, count + 1);
}
 
let jonas = { name: "Jonas" };
countUser(jonas);                // Menambahkan user "Jonas"
 
jonas = null;                    // Data object "Jonasdihapus
 
console.log(visitsCountMap);
 
/* output
Map(1) { { name: 'Jonas' } => 1 }
*/
```

Ketika _reference_ objek jonas dihapus dengan mengubahnya menjadi null, seharusnya map tidak lagi menyimpan data user \(_garbage collected_\). Namun, kenyataannya data jonas masih tersedia di dalam Map. Artinya, data jonas masih tersimpan di dalam memori sampai kita benar-benar menghapusnya.

Berbeda jika kita menggunakan WeakMap seperti inI:

```javascript
let visitsCountMap = new WeakMap();
```

Ketika nilai jonas sudah tidak bisa dijangkau, object jonas akan dihapus dari memori termasuk informasi yang disimpan di dalam WeakMap.

```javascript
let visitsCountMap = new WeakMap(); // Menyimpan daftar user

function countUser(user) {
    let count = visitsCountMap.get(user) || 0;
    visitsCountMap.set(user, count + 1);
}

let jonas = { name: "Jonas" };
countUser(jonas);                // Menambahkan user "Jonas"

jonas = null;                    // Data object "Jonas" dihapus

console.log(visitsCountMap);

/* output
WeakMap { <items unknown> }
*/
```

Seperti halnya WeakMap, WeakSet adalah versi _weak_ reference dari Set. Perbedaan antara WeakSet dan Set antara lain:

* WeakSet tidak bisa menyimpan nilai primitif.
* WeakSet bukan iterable dan hanya memiliki method add\(\), has\(\), dan delete\(\).
* WeakSet tidak memiliki properti size.

