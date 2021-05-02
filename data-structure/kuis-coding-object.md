# Kuis Coding: Object

Untuk menguji kemampuan praktikal Anda dalam memahami materi object di JavaScript, silakan selesaikan kuis berikut.

Sebelum Anda mengerjakan kuis, ada beberapa hal yang perlu Anda perhatikan.

* Mohon untuk membaca secara seksama perintah, kriteria, atau soal pada komentar kode yang diberi tanda **TODO.**
* Lakukan pengujian pada kode yang Anda tulis contohnya dengan menggunakan console.log\(\) untuk memastikan hasil sesuai dengan yang Anda harapkan. Gunakan tombol **Jalankan**.

Bila sudah yakin dengan pekerjaan yang Anda lakukan, silakan submit kode dengan klik tombol **Submit kode**. Jika kode yang di-_submit_ benar, Anda bisa melanjutkan ke modul berikutnya. Jika tidak, Anda bisa memperbaiki kembali kode sebanyak yang Anda mau.

Batas waktu tunggu untuk mengirimkan kembali perbaikan kode adalah 1 menit. Jadi pastikan kode yang Anda tulis sudah memenuhi perintah, kriteria, atau soal pada kuis kali ini.

**Hasil Tugas**

```javascript
/**
 * TODO
 * 1. Buatlah variabel dengan nama restaurant yang object dengan ketentuan berikut:
 *    - Memiliki properti bernama "name"
 *       - Bertipe data string
 *       - Bernilai apa pun, asalkan tidak string kosong atau null.
 *    - Memiliki properti bernama "city"
 *       - Bertipe data string
 *       - Bernilai apa pun, asalkan tidak string kosong atau null.
 *    - Memiliki properti "favorite drink"
 *       - Bertipe data string
 *       - Bernilai apa pun, asalkan tidak string kosong atau null.
 *    - Memiliki properti "favorite food"
 *       - Bertipe data string
 *       - Bernilai apa pun, asalkan tidak string kosong atau null.
 *    - Memiliki properti "isVegan"
 *       - Bertipe data boolean
 *       - Bernilai boolean apa pun.
 *
 * 2. Buatlah variabel bernama name.
 *    Kemudian isi dengan nilai name dari properti object restaurant
 * 3. Buatlah variabel bernama favoriteDrink.
 *    Kemudian isi dengan nilai "favorite drink" dari properti object restaurant
 */


// TODO
const restaurant = {
  name: "hendra",
  city: "Malang",
  "favorite drink": "Kopi",
  "favorite food": "Nasi Goreng",
  isVegan: false
};

const favoriteDrink = restaurant["favorite drink"];
const name = restaurant.name;
console.log(`nama saya ${name}, minuman favorit saya ${favoriteDrink}`);


/**
 * Hiraukan kode di bawah ini
 */
module.exports = { restaurant, name, favoriteDrink };
```

