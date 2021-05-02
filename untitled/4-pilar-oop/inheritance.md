# Inheritance

Beberapa objek bisa memiliki beberapa karakteristik atau perilaku yang sama, tetapi mereka bukanlah objek yang sama. Di sinilah inheritance atau pewarisan berperan. SMS dan jenis pesan lainnya memiliki karakteristik umum yang dimiliki juga oleh jenis pesan lainnya, seperti memiliki konten pesan, alamat/nomor pengirim, alamat/nomor penerima, dsb. Maka dari itu Email sebagai objek turunan \(subclass\) mewarisi semua sifat dan perilaku dari objek induknya \(superclass\) Mail. Begitu juga dengan objek Whatsapp juga mewarisi sifat dan perilaku yang sama, namun whatsapp bisa membuat grup, mengirim broadcast message sedangkan Email tidak \(\*misalkan\).

![](../../.gitbook/assets/1%20%286%29.png)

Dari contoh di atas, misalkan kita ingin membuat 2 \(dua\) child class yaitu WhatsApp dan Email. Maka dalam JavaScript cara menuliskan pewarisan terdapat 2 cara, yaitu sebagai berikut:

```javascript
// cara 1: menggunakan keyword `extends` jika menggunakastatement `class`
class ChildClassName extends ParentClassName{
// cara 2: menggunakan `prototype` jika menggunakastatement `function` / `class`
ChildClassName.prototype = new ParentClassName()
```

Misalkan kita akan membuat sebuah child class bernama WhatsApp yang mewarisi kelas Mail. Maka contoh kodenya adalah sebagai berikut:

```javascript
class Mail{
  _contacts = [];
         constructor(author) {
                     this.from = author;
           };
    sendMessage = function(msg, to) {
        console.log('you send:', msg, 'to', to, 'from', this.from);
                     this._contacts.push(to);
    };
    showAllContacts() {
    return this._contacts;
  }
}

class WhatsApp extends Mail{
           username = 'dicoding';
    isBussinessAccount = true;

    myProfile = function() {
                   return `my name ${this.username}, is ${this.isBussinessAccount? 'Business': 'Personal'}`;
            };
}

const wa1 = new WhatsApp(080111000222);
console.log(wa1.myProfile());
// my name dicoding, is Business
```

Kita juga dapat mengakses attribute maupun method dari parent class yang Accessible. Misalkan:

```javascript
wa1.sendMessage('halo', 089000999888);
```

