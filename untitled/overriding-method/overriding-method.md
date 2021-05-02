# Overriding Method

Hampir sama dengan _overriding constructor_, namun yang di-_override_ di sini adalah _method-method_ yang ada pada parent class. Pada dasarnya semua method yang ada pada kelas parent dapat diakses langsung di _child_ kelasnya \(_as is_\).

```javascript
super.methodName();
```

Kadang kita tidak menggunakan sebuah method seutuhnya sama seperti parent kelasnya. namun dapat menambahkan perintah tertentu ataupun menguranginya. Berikut merupakan contoh override pada method sendMessage

```javascript
class WhatsApp extends Mail{
  constructor(username, isBussinessAccount, phone) {
    super(phone);
    this.username = username;
    this.isBussinessAccount = true;
  
  // Overriding method => Melakukan Override Total
  sendMessage = function(msg, to) {
    console.log('Send by WA');
  }
}
```

Dari contoh tersebut, ketika kita memanggil method sendMessage hanya akan mengeksekusi kode yang ada pada child class.

```javascript
const wa1 = new WhatsApp('di', true, 089000999888);
wa1.sendMessage('halo', 089000999888)
/**
Output:
Send by WA
**/
```

Untuk tetap melakukan eksekusi kode pada parent class maka perlu menggunakan operator `super.methodName()`.

```javascript
sendMessage = function(msg, to) {
    super.sendMessage(msg, to);
    console.log('Send by WA');
}
```

Catatan: `super(...)` digunakan untuk memanggil constructor parent, dan hanya dapat digunakan di constructor.

`super.methodName(...)` digunakan untuk memanggil parent method.

