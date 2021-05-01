# Logical Operator

Terdapat beberapa operator lain yang dapat kita gunakan untuk menetapkan logika yang lebih kompleks, yakni dengan _logical operators_. Dengan logical operator, kita dapat menggunakan kombinasi dari dua nilai boolean atau bahkan lebih dalam menetapkan logika.

Pada JavaScript terdapat tiga buah karakter khusus yang berfungsi sebagai logical operator. Berikut macam-macam logical operator dan fungsinya:

| Operator | Deskripsi |
| :--- | :--- |
| && | Operator dan \(and\). Logika akan menghasilkan nilai true apabila semua kondisi terpenuhi \(bernilai true\). |
| \|\| | Operator atau \(or\). Logika akan menghasilkan nilai true apabila ada salah satu kondisi terpenuhi \(bernilai true\). |
| ! | Operator tidak \(not\). Digunakan untuk membalikkan suatu kondisi. |

Berikut contoh penerapannya pada JavaScript:

```javascript
let a = 10;
let b = 12;

/* AND operator */
console.log(a < 15 && b > 10); // (true && true) -> true
console.log(a > 15 && b > 10); // (false && true) -> false

/* OR operator */
console.log(a < 15 || b > 10); // (true || true) -> true
console.log(a > 15 || b > 10); // (false || true) -> true

/* NOT operator */
console.log(!(a < 15)); // !(true) -> false
console.log(!(a < 15 && b > 10)); // !(true && true) -> !(true) -> false

/* output
true
false
true
true
false
false
*/
```

Mungkin sebagian dari kita bertanya, sebenarnya apa kegunaan dari nilai boolean selain hanya menampilkan nilai true dan false saja? Pada pembahasan tipe data sudah pernah disebutkan bahwa boolean merupakan salah satu kunci dari logika pemrograman, karena boolean dapat mengontrol bagaimana alur program kita akan berjalan.

Lantas bagaimana cara boolean mengontrol sebuah aliran program? Pada materi selanjutnya, kita akan membahas mengenai if/else statement yang dapat mengontrol _flow_ pada program, tentunya pada penggunaan _statement boolean_ ini sangat berguna.

