# Boolean

Boolean hanya memiliki dua nilai, yaitu **true** atau **false**. Tipe data ini menjadi kunci utama dalam penentuan logika. Kita akan banyak menggunakannya nanti dalam materi _if/else statement_. Untuk menetapkan nilai boolean pada variabel, gunakan keyword true atau false seperti di bawah ini.

```javascript
let x = true;
let y = false;

console.log(typeof(x))
console.log(typeof(y))

/* output: 
boolean
boolean
*/
```

Kita juga bisa menggunakan operator komparasi seperti lebih dari \(&gt;\) atau kurang dari \(&lt;\). Contohnya:

```javascript
const a = 10;
const b = 12;

let isGreater = a > b;
let isLess = a < b;

console.log(isGreater);
console.log(isLess);

/* output:
false
true
*/
```

