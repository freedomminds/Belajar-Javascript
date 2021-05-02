# Class Method

#### Class Method

Class Method adalah function atau method yang ada di dalam sebuah object. Untuk menggunakannya, sebuah class harus di-_instantiate_ terlebih dahulu menjadi object baru bisa dijalankan. Contoh class mail di atas, kita akan menggunakan method sendMessage maka kita harus meng-_instantiate_ Mail terlebih dahulu.

```javascript
const mail1 = new Mail();
mail1.sendMessage('hallo', 'penerima@dicoding.com');
/**
output-nya berhasil:
you send: hallo to penerima@dicoding.com fropengirim@dicoding.com
**/
```

Kita tidak dapat langsung mengakses sendMessage tanpa melakukan instansiasi terlebih dahulu, misalkan:

```javascript
Mail.sendMessage('hallo', 'penerima@dicoding.com');
/**
output-nya error:
TypeError: Mail.sendMessage is not a function
**/
```

