# Comparison Operator

Sekarang kita sudah mengetahui bagaimana cara menyimpan nilai pada sebuah variabel. Nah, selanjutnya kita akan belajar mengenai operator komparasi sebagai logika dasar dalam membandingkan nilai pada JavaScript.

Terdapat serangkaian karakter khusus yang disebut dengan operator pembanding/komparasi yang dapat mengevaluasi dan membandingkan dua nilai. Berikut daftar operator dan fungsinya:

| Operator | Fungsi |
| :--- | :--- |
| == | Membandingkan kedua nilai apakah sama. \(tidak identik\). |
| != | Membandingkan kedua nilai apakah tidak sama. \(tidak identik\). |
| === | Membandingkan kedua nilai apakah identik. |
| !== | Membandingkan kedua nilai apakah tidak identik. |
| &gt; | Membandingkan dua nilai apakah nilai pertama lebih dari nilai kedua. |
| &gt;= | Membandingkan dua nilai apakah nilai pertama lebih atau sama dengan nilai kedua. |
| &lt; | Membandingkan dua nilai apakah nilai pertama kurang dari nilai kedua. |
| &lt;= | Membandingkan dua nilai apakah nilai pertama kurang atau sama dengan nilai kedua. |

Ketika kita melakukan perbandingan antara dua nilai, JavaScript akan mengevaluasi kedua nilai tersebut dan mengembalikan boolean dengan nilai hasil perbandingan tersebut, baik false atau true. Berikut contohnya:

```text
let a = 10;
let b = 12;

console.log(a < b);
console.log(a > b);

/* output
true
false
*/
```

