# Overriding Constructor

Sebelumnya kita telah mempelajari tentang constructor dan juga pewarisan. Pada contoh kasus di inheritance atau pewarisan, kita menemukan kasus seperti di bawah ini.

```javascript
class WhatsApp extends Mail{
  username = 'dicoding';
    isBussinessAccount = true;
    ....

//pemanggilan
const wa1 = new WhatsApp(080111000222);
```

Sekarang bagaimana jika kita menambahkan **username** dan **isBussinessAccount** ke dalam constructor? Jika kita membuat constructor baru kodenya akan seperti ini:

```javascript
class WhatsApp extends Mail{
    constructor(username, isBussinessAccount, phone) {
        this.from=phone;
    this.username = username;
    this.isBussinessAccount = true;
    }

const wa1 = new WhatsApp('dicoding', true, 089989090898);
/** 
Error:
Must call super constructor in derived class beforaccessing 'this' or returning from derived constructor
**/
```

Akan terjadi error tersebut dikarenakan constructor pada kelas parent gagal dieksekusi, meskipun kita telah menggunakan operator this.nameOfProperty. Solusinya kita menggunakan operator super\(\) untuk mengeksekusi _method parent_-nya. Sehingga constructor pada kelas WhatsApp menjadi seperti ini.

```javascript
constructor(username, isBussinessAccount, phone) {
  super(phone);
  this.username = username;
  this.isBussinessAccount = true;
}
```

