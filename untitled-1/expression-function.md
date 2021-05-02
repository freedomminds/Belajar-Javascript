# Expression Function

Cara lain untuk membuat sebuah fungsi pada JavaScript adalah _expression function_. Ingat kembali bahwa _expression_ adalah kode atau instruksi yang mengembalikan nilai, sehingga expression function bisa disimpan dalam sebuah variabel.

Pada expression function umumnya kita tidak perlu menuliskan nama fungsinya. Fungsi yang tidak bernama juga dikenal dengan _anonymous function_. Berikut ini merupakan contoh penulisan expression function:

```javascript
const greeting = function(name, language) {
    if(language === "English") {
        return "Good Morning " + name + "!";
    } else if (language === "French") {
        return "Bonjour " + name + "!";
    } else {
        return "Selamat Pagi " + name + "!";
    }
}

console.log(greeting('Ron', 'English'));

/* output
Good Morning Ron!
 */
```

