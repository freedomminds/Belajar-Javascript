# Static Method

Static method adalah function atau method yang sama seperti class method, akan tetapi untuk mengaksesnya tidak perlu meng-_instantiate_ class, kita cukup menuliskan nama kelas dan nama _method_-nya secara langsung \(NamaClass.namaMehod\(\)\).

Sebagai contoh, kita menambahkan sebuah method untuk memeriksa apakah sebuah input adalah nomor handphone:

```javascript
class Mail{
  static isValidPhone(phone) {
    return typeof phone === 'number';
  }
}
```

Dari contoh di atas, kita dapat memanggil fungsi tersebut tanpa membuat instance kelas Mail terlebih dahulu.

```javascript
Mail.isValidPhone(089000000000) //true
```

