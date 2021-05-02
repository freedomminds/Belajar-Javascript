# Kuis Coding: Map

Untuk menguji kemampuan praktikal Anda dalam memahami materi Map di JavaScript, silakan selesaikan kuis berikut.

Sebelum Anda mengerjakan kuis, ada beberapa hal yang perlu Anda perhatikan.

* Mohon untuk membaca secara seksama perintah, kriteria, atau soal pada komentar kode yang diberi tanda **TODO.**
* Lakukan pengujian pada kode yang Anda tulis contohnya dengan menggunakan console.log\(\) untuk memastikan hasil sesuai dengan yang Anda harapkan. Gunakan tombol **Jalankan**.

Bila sudah yakin dengan pekerjaan yang Anda lakukan, silakan submit kode dengan klik tombol **Submit kode**. Jika kode yang di-_submit_ benar, Anda bisa melanjutkan ke modul berikutnya. Jika tidak, Anda bisa memperbaiki kembali kode sebanyak yang Anda mau.

Batas waktu tunggu untuk mengirimkan kembali perbaikan kode adalah 1 menit. Jadi pastikan kode yang Anda tulis sudah memenuhi perintah, kriteria, atau soal pada kuis kali ini.

_Good luck!_

**Hasil Tugas**

```javascript
/**
 * TODO:
 * 1. Buatlah variabel currency yang merupakan Map dengan kriteria:
 *   - key "USD", value 14000
 *   - key "JPY", value 131
 *   - key "SGD", value 11000
 *   - key "MYR", value 3500
 * 2. Buatlah variabel priceInIDR yang bernilai dari hasil perkalian:
 *     - priceInJPY dengan nilai currency JPY
 */

const priceInJPY = 5000;

// TODO
const currency = new Map([
  ["USD", 14000],
  ["JPY", 131],
  ["SGD", 11000],
  ["MYR", 3500]
]);
const priceInIDR = priceInJPY * currency.get("JPY")
console.log(priceInIDR)

/**
 * Hiraukan kode di bawah ini
 */
module.exports = { currency, priceInJPY, priceInIDR };
```

