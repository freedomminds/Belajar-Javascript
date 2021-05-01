# Strings

Tipe data selanjutnya adalah _string_ yang merupakan sebuah teks. Untuk menetapkan nilai sebagai string pada variabel gunakan tanda petik satu \(‘\) atau petik dua \(“\) di antara teksnya. Contohnya:

```javascript
let greet = "Hello";
console.log(typeof(greet))

/* output: string */
```

Tidak ada perbedaan antara menggunakan petik satu atau petik dua. Anda dapat menggunakan tanda petik secara bergantian, khususnya jika Anda memiliki teks yang mengandung tanda petik.

```javascript
const question = '"What do you think of JavaScript?" I asked';

console.log(question)

/* output: "What do you think of JavaScript?" he asked */
```

Lalu bagaimana jika teks memiliki kedua tanda petik seperti ini?

```javascript
const answer = '"I think it's awesome!" he answered confidently';

console.log(answer);
```

Tentunya kode di atas akan menghasilkan eror. Solusinya, gunakan _backslash_\(\\) untuk mengurangi ambiguitas dalam tanda petik. Mekanisme ini juga dikenal dengan nama _escape string_. Sehingga kode di atas akan menjadi seperti berikut:

```javascript
const answer = '"I think it\'s awesome!" he answered confidently';
```

Backslash sebelum tanda petik akan memberitahukan _interpreter_ bahwa itu hanyalah tanda petik dan tidak boleh ditafsirkan sebagai pembatas string. Selain tanda petik, backslash juga berguna untuk mengabaikan simbol lain yang menimbulkan ambigu di dalam string, contohnya seperti backslash itu sendiri.

```javascript
console.log("Windows path: C:\\Program Files\\MyProject");
```

Pada String, kita juga dapat menggunakan operator plus \(+\). Operator tersebut berfungsi untuk menggabungkan dua teks yang terpisah menjadi satu buah teks. Contohnya seperti ini:

```javascript
let greet = "Hello";
let moreGreet = greet + greet;
console.log(moreGreet);

/* output: HelloHello */
```

Ingat, _string concatenation_ seperti di atas akan menggabungkan string apa adanya, sehingga jika Anda ingin menggabungkan dua kata atau lebih perlu menambahkan spasi sendiri.

Selain _concatenation_, string pada JavaScript juga mendukung _string interpolation_. Sederhananya, kita bisa memasukkan variabel ke dalam sebuah _string template_. Contohnya adalah seperti berikut:

```javascript
const myName = "Luke";
console.log(`Hello, my name is ${myName}.`);

/* output: Hello, my name is Luke. */
```

Perhatikan bahwa untuk mendefinisikan _string template,_ Anda perlu menggunakan backticks \(\`\), biasanya terletak di _keyboard_ di sebelah kiri tombol 1\). Di dalam string letakkan variabel yang ingin dimasukkan ke dalam _placeholder_ ${myName}.

