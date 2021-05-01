# Switch Case Statement

Sebelumnya kita telah mempelajari bagaimana percabangan logika menggunakan _if statement_. Selain if, JavaScript juga mendukung _switch statement_ untuk melakukan pengecekan banyak kondisi dengan lebih mudah dan ringkas.

```javascript
    switch (expression) {
      case value1:
        // do something
        break;
      case value2:
        // do something
        break;
      ...
      ...
      default:
        // do something else
    }
```

Tanda kurung setelah _keyword_ switch berisi variabel atau expression yang akan dievaluasi. Kemudian untuk setiap kondisi yang mungkin terjadi, kita masukkan _keyword_ case diikuti dengan nilai yang valid. Jika kondisi pada case sama dengan variabel pada switch, maka blok kode setelah titik dua \(:\) akan dijalankan. Keyword break digunakan untuk keluar dari proses switch. Terdapat satu case bernama default yang memiliki fungsi yang sama dengan keyword _else_ pada _control flow if-else_. Jika tidak ada nilai yang sama dengan variabel pada switch, maka blok kode ini akan dijalankan.

Berikut ini adalah contoh kode dari materi if-else yang dikonversi menjadi statement switch:

```javascript
let language = "French";
let greeting = null;

switch (language) {
    case "English":
        greeting = "Good Morning!";
        break;
    case "French":
        greeting = "Bonjour!";
        break;
    case "Japanese":
        greeting = "Ohayou Gozaimasu!";
        break;
    default:
        greeting = "Selamat Pagi!";
}

console.log(greeting);

/* output
Bonjour!
*/
```

