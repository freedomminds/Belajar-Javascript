# Contoh Penggunaan Date

Berikut ini adalah kode misalkan kita ingin menghitung berapa umur kita dengan memanfaatkan object date.

```javascript
// parameter birthday dapat berupa miliseconds ataupun date string
const myAge = birthday => {
  const birtday = new Date(birthday);
  const today = Date.now(); // today menghasilkan nilai miliseconds saat ini

  const diff_ms = today - birtday.getTime(); // menghitung selisih nilai miliseconds hari ini dan tanggal lahir
  const diffDate = new Date(diff_ms);

  return diffDate.getFullYear() - 1970; // 1970 adalah representasi 0 dari miliseconds
};

myAge('2000-01-22'); // 21 tahun
```

Selain Date, kita juga dapat menggunakan built-in class javascript yang lainnya.

```javascript
const listOfContent = [1,2,”President”, {}];
console.log(Array.isArray(listOfContent)); 
// result is tru
const splitText = "12:20:00".split(':');
// result is [ '12', '20', '00' ]
```

