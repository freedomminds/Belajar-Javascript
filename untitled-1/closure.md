# Closure

Setelah mempelajari tentang scope pada materi selanjutnya, kali ini kita akan membahas seputar _closure_. Sebelumnya kita telah tahu bahwa fungsi dapat didefinisikan dalam lingkup global atau di dalam fungsi lain. Suatu fungsi yang dapat mengakses variabel di dalam _lexical scope_-nya disebut dengan closure. _Lexical scope_ berarti pada sebuah fungsi bersarang, fungsi yang berada di dalam memiliki akses ke variabel di lingkup induknya.

```javascript
function init() {
    var name = 'Obi Wan';   // Variabel lokal di dalam scope fungsi init
    
    function greet() {      // Inner function, merupakan contoh closure
        console.log(`Halo, ${name}`);   // Memanggil variabel yang dideklarasikan di parent function
    }

    greet();
}

init();

/* output
Halo, Obi Wan
 */
```

Fungsi init\(\) memiliki variabel lokal name dan fungsi greet\(\). Fungsi greet\(\) adalah _inner function_ yang didefinisikan di dalam init\(\) dan hanya bisa diakses dari dalam fungsi init\(\). Perhatikan bahwa fungsi greet\(\) tidak memiliki variabel lokal. Namun, karena _inner function_ memiliki akses ke variabel di _parent function_-nya, sehingga greet\(\) dapat mengakses variabel name. Itulah yang dimaksud dengan _lexical scope_.

Sekarang perhatikan contoh kode berikut:

```javascript
function init() {
    var name = 'Obi Wan';

    function greet() {
        console.log(`Halo, ${name}`);
    }

    return greet;
}

let myFunction = init();
myFunction();

/* output
Halo, Obi Wan
 */
```

Kode di atas akan menghasilkan output yang sama. Perbedaannya adalah fungsi greet\(\) dikembalikan \(_return_\) dari _outer function_-nya sebelum dieksekusi. Karena variabel name berada dalam scope init\(\), maka umumnya variabel tersebut akan hilang atau dihapus ketika fungsinya selesai dijalankan. Namun, pada kasus di atas fungsi greet\(\) yang diakses melalui fungsi MyFunction\(\) masih memiliki referensi atau akses ke variabel name. Variabel pada mekanisme di atas telah tertutup \(_close covered_\), yang berarti variabel tersebut berada di dalam _closure_.

Memang di awal cukup sulit untuk memahami closure. Jadi, mari kita lihat langsung untuk apa closure ini digunakan pada suatu program yang nyata.

JavaScript tidak memiliki cara untuk mendeklarasikan suatu fungsi atau variabel menjadi _private_ seperti bahasa Java. Sehingga sebuah fungsi atau variabel bisa diakses dari mana pun. Kenapa kita membutuhkan _private method_? Salah satunya adalah untuk membatasi akses ke fungsi atau variabel. Perhatikan contoh berikut:

```javascript
let counter = 0;

let add = () => {
    return ++counter;
}

console.log(add());
console.log(add());
counter = 23;
console.log(add());

/* output
1
2
24
 */
```

Nilai counter akan bertambah ketika kita memanggil fungsi add\(\). Namun, kita juga bisa mengubah nilai counter secara langsung dengan _assignment operator_. Pada contoh program yang lebih kompleks, sebaiknya hal ini dihindari karena perubahan langsung pada nilai counter bisa saja memunculkan _bug_.

Closure memungkinkan kita membuat fungsi dan variabel seolah menjadi _private_. Seperti inilah contoh program counter yang dibuat dengan closure:

```javascript
let add = () => {
    let counter = 0;
    return () => {
        return ++counter;
    };
}

let addCounter = add();

console.log(addCounter());
console.log(addCounter());
console.log(addCounter());

/* output
1
2
3
 */
```

