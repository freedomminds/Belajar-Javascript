# If/Else Statement

Setiap hari kita melakukan perhitungan dan perbandingan guna membuat keputusan, apa pun itu. Contohnya, apakah perlu mencuci kendaraan ketika cuaca sedang cerah? Apa saja transportasi _online_ yang bisa dipesan ketika hujan untuk sampai di tempat tujuan?

Ketika mengembangkan sebuah program, kita akan bertemu dengan alur bercabang tergantung pada kondisi yang terjadi. Untuk mengakomodasi dan mengecek sebuah kondisi dalam JavaScript, kita menggunakan kata kunci **if**.

Statement if akan menguji suatu kondisi. Jika kondisi bernilai _true_, maka blok kode di dalamnya akan dijalankan. Sebaliknya, jika bernilai _false_, maka proses yang ditentukan akan dilewatkan.

![](../../.gitbook/assets/1%20%283%29.png)

_Flowchart_ di atas jika diterjemahkan menjadi kode, akan menjadi seperti berikut:

```javascript
const isRaining = true;

console.log("Persiapan sebelum berangkat kegiatan.");
if (isRaining) {
    console.log("Hari ini hujan. Bawa payung.");
}
console.log("Berangkat kegiatan.");

/* output:
Persiapan sebelum berangkat kegiatan.
Hari ini hujan. Bawa payung.
Berangkat kegiatan.
 */
```

Jika Anda mengubah nilai isRaining menjadi false, maka kode di dalam blok kode if akan dilewatkan. Sehingga program Anda tidak akan mengingatkan untuk membawa payung.

Lalu bagaimana jika Anda ingin melakukan operasi lain ketika kondisi bernilai false? Jawabannya adalah _statement_ else. Pada contoh kode berikut kita akan melakukan pengecekan kondisi menggunakan operator perbandingan.

```javascript
let x = 50;

if(x > 70) {
    console.log(x);
} else {
    console.log("Nilai kurang dari 70");
}

/* output
Nilai kurang dari 70
*/
```

Terdapat variabel x dengan nilai 50, kemudian kita bertanya, “Hai JavaScript! Apakah x lebih dari 70?” Jika kondisi tersebut benar, maka kita dapat memerintahkan JavaScript untuk menampilkan nilainya. Jika salah, kita perintahkan JavaScript untuk menampilkan teks “Nilai kurang dari 70”.

Kita juga bisa mengecek beberapa kondisi sekaligus dengan menggabungkan else dan if. Contohnya adalah seperti program berikut:

```javascript
let language = "French";
let greeting = "Selamat Pagi"

if(language === "English") {
    greeting = "Good Morning!";
} else if(language === "French") {
    greeting = "Bonjour!"
} else if(language === "Japanese") {
    greeting = "Ohayou Gozaimasu!"
}

console.log(greeting);

/* output
Bonjour!
*/
```

Pengecekan kondisi akan dilakukan dari statement if paling awal. Sehingga, ketika nilai language adalah “French”, maka pengecekan untuk language === “Japanese” tidak akan dilakukan.

Selain if statement di atas, JavaScript juga mendukung _ternary operator_ atau _conditional expressions_. Dengan ini, kita bisa menuliskan _if-else statement_ hanya dalam satu baris.

```javascript
// condition ? true expression : false expression

const isMember = false;
const discount = isMember ? 0.1 : 0;
console.log(`Anda mendapatkan diskon sebesar ${discount * 100}%`)

/* output
Anda mendapatkan diskon sebesar 0%
 */
```

Ternary operator membutuhkan tiga _operand_. Sebelum tanda tanya \(?\) berisi kondisi yang ingin kita evaluasi. Kemudian diikuti dengan _expression_ apabila nilai kondisinya benar sebelum tanda titik dua. Terakhir adalah _expression_ yang dieksekusi ketika kondisinya salah. Karena merupakan _conditional expression_, maka operand kedua dan ketiga harus mengembalikan nilai.

