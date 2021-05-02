# Kuis Coding: Array

Untuk menguji kemampuan praktikal Anda dalam memahami materi Array di JavaScript, silakan selesaikan kuis berikut.

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
 * Buatlah sebuah variabel dengan nama evenNumber yang merupakan sebuah array dengan ketentuan:
 *   - Array tersebut menampung bilangan genap dari 1 hingga 100
 *
 * Catatan:
 *   - Agar lebih mudah, gunakanlah for loop dan logika if untuk mengisi bilangan genap pada array.
 */

// TODO
const evenNumber = []
for(let i = 1; i <= 100; i++){
	if((i % 2) == 0){
      evenNumber.push(i)
    }
}

console.log(evenNumber);

/**
 * Hiraukan kode di bawah ini
 */

module.exports = evenNumber;
```

