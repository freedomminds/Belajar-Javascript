# Built-in Class

Dalam JavaScript sendiri terdapat built-in Object bawaan, misalkan Date, Object, Array, Math, dan String yang dapat digunakan untuk memanipulasi data-data terkait dengan array, perintah matematik, manipulasi karakter, dan manipulasi objek.

Date merupakan core object bawaan dari bahasa pemrograman JavaScript yang digunakan untuk utilitas terkait tanggal dan waktu. Ini sangat membantu kita ketika dalam program yang kita buat terdapat penggunaaan dan manipulasi tanggal dan waktu.

Untuk menggunakannya kita dapat me-instansiasi Date object tersebut dengan 4 cara:

```javascript
// #1 tanpa parameter, yang berarti `myDate` akan beristanggal dan waktu saat ini
const myDate = new Date();
// #2 parameter tanggal dalam bentuk string, misal"January 01, 2021" 
const myDate = new Date(dateString);
// #3 parameter dalam bentuk number, misal 87400000
const myDate = new Date(miliseconds);
// #4 parameter tanggal dalam bentuk number (7 parameter)[hour,minute,second,millisecond] bersifat opsional
const myDate = new Date(year,month,date,hour,minute,seconmillisecond);
```

Dalam object Date terdapat beberapa method yang dapat kita gunakan. Berikut adalah daftar method yang umum digunakan.

| Methods | Penjelasan | Contoh penggunaan |
| :--- | :--- | :--- |
| getMonth\(\) | Nilai kembaliannya adalah bulan dalam bentuk angka \(0 sampai 11\), 0 berarti Januari. | myDate.getMonth\(\) |
| getFullYear\(\) | Nilai kembaliannya adalah tahun, misalkan 2021. | myDate.getFullYear\(\) |
| getDate\(\) | Nilai kembaliannya adalah tanggal dari 1 sampai 31. | myDate.getDate\(\) |
| getHours\(\) | Nilai kembaliannya adalah jam dari 0 sampai 23 | myDate.getHours\(\) |
| getMinutes\(\) | Nilai kembaliannya adalah menit dari 0 sampai 59 Nilai kembaliannya | myDate.getMinutes\(\) |
| getSeconds\(\) | Nilai kembaliannya adalah detik dari 0 sampai 59 | myDate.getSeconds\(\) |
| getMilliseconds\(\) | Nilai kembaliannya adalah mili-detik dari 0 to 999 | myDate.getMilliseconds\(\) |
| getTime\(\) | Nilai kembaliannya adalah waktu dalam bentuk epoch mili-detik \(dimulai dari 1 January, 1970 yang berarti 0\) | myDate.getTime\(\) |
| getDay\(\) | Nilai kembaliannya adalah hari dalam seminggu dari 0 sampai 6. 0 berarti minggu | myDate.getDay\(\) |

Selain itu, juga terdapat static method yang dapat digunakan tanpa perlu melakukan instansiasi, yaitu:

| Method | Penjelasan | Contoh Penggunaan |
| :--- | :--- | :--- |
| parse\(datestring\) | digunakan untuk merubah tanggal dalam format string, menjadi epoch miliseconds | Date.parse\("2021-01-01"\) |
| UTC\(year, \[..params\]\) | digunakan untuk merubah tanggal dalam format string, menjadi epoch miliseconds | Date.UTC\(2021, 01, 01\) |

