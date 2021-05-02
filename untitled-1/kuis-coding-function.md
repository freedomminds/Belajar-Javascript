# Kuis Coding: Function

Untuk menguji kemampuan praktikal Anda dalam memahami materi Function di JavaScript, silakan selesaikan kuis berikut.

Sebelum Anda mengerjakan kuis, ada beberapa hal yang perlu Anda perhatikan.

* Mohon untuk membaca secara seksama perintah, kriteria, atau soal pada komentar kode yang diberi tanda **TODO.**
* Lakukan pengujian pada kode yang Anda tulis contohnya dengan menggunakan console.log\(\) untuk memastikan hasil sesuai dengan yang Anda harapkan. Gunakan tombol **Jalankan**.

Bila sudah yakin dengan pekerjaan yang Anda lakukan, silakan submit kode dengan klik tombol **Submit kode**. Jika kode yang di-_submit_ benar, Anda bisa melanjutkan ke modul berikutnya. Jika tidak, Anda bisa memperbaiki kembali kode sebanyak yang Anda mau.

Batas waktu tunggu untuk mengirimkan kembali perbaikan kode adalah 1 menit. Jadi pastikan kode yang Anda tulis sudah memenuhi perintah, kriteria, atau soal pada kuis kali ini.

```javascript
/**
 * TODO:
 * 1. Buatlah fungsi bernama minimal dengan ketentuan berikut:
 *    - Menerima dua buah argumen number, a dan b.
 *    - Mengembalikan nilai terkecil antara a atau b.
 *    - Bila nilai keduanya sama, maka kembalikan dengan nilai a
 *
 *    contoh:
 *    minimal(1, 4) // 1
 *    minimal(3, 2) // 2
 *    minimal(3, 3) // 3
 *
 * 2. Buatlah fungsi bernama power dengan ketentuan berikut:
 *    - Menerima dua buah argumen number, a dan b.
 *    - Mengembalikan nilai dari hasil perkalian a * a sebanyak b (fungsi kuadrat).
 *
 *    contoh:
 *    power(7, 3) // 343
 *    power(3, 3) // 27
 *    power(4, 0.5) // 2
 */


// TODO
function minimal(a, b){
  return Math.min(a, b);
}
console.log(minimal(1, 4));
console.log(minimal(3, 2));
console.log(minimal(3, 3));

function power(a, b){
  let c = a ** b
  return c;
}
console.log(power(7, 3));
console.log(power(3, 3));
console.log(power(4, 0.5));



/**
 * Hiraukan kode di bawah ini
 */

module.exports = { minimal, power };
```

