# Constructor

Ketika kita membuat sebuah objek, adakalanya karakteristik dari _blueprint_ yang kita buat harus sudah didefinisikan bersamaan dengan sebuah objek saat pertama kali diinisiasi. Constructor adalah sebuah method/function yang dijalankan pertama kali ketika object dibuat. Dari contoh kelas yang kita buat sebelumnya, kita akan membuat from sebagai sebuah value yang harus ditulis ketika sebuah objek di inisiasi. Maka dalam JavaScript ada dua cara, yaitu:

```javascript
// cara 1, jika kita menggunakan statement class
class YourClassName{
  constructor(params1, params2, ....) {
    // do something here
  };

// cara 2, jika kita menggunakan statemen function
function Mail(params1, params2, ....) {
    this.yourPropertyName = params1;
  // do something here
}
```

Contoh penerapannya sebagai berikut:

```javascript
// cara 1
class Mail{
  constructor(author) {
    this.from = 'pengirim@dicoding.com'
    console.log('is instantiated', author);
  };

// cara 2
function Mail(author) {
    this.from = author
  console.log('is instantiated', author);
}
```

Dari contoh constructor di atas, maka cara pemanggilannya menjadi seperti di bawah ini:

```javascript
const mail1 = new Mail("emailku@dicoding.com");
```

Karena JavaScript bukan bahasa dengan dukungan _static type_ maka sebenarnya kita dapat melakukan instansiasi dengan parameter sesuka kita:

```javascript
const mail1 = new Mail(085000111222); // misalkan untuk SMS
const mail2 = new Mail("emailku@dicoding.com"); // misalkan untuk Email
```

\`

