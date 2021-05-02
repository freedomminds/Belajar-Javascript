# Property

Property adalah atribut dari sebuah objek, property sendiri dapat berupa tipe data primitive--seperti yang sebelumnya dibahas-- bahkan bisa juga berbentuk object dan fungsi. Misalkan isi pesan, list penerima, data pengirim, perintah kirim, dll. Sebagai contoh:

```javascript
// cara 1
class Mail{
  from = 'pengirim@dicoding.com';
    contacts = [];
    sendMessage = function(msg, to) {
        console.log('you send:', msg, 'to', to, 'from'this.from);
    this.contacts.push(to); // menyimpan kontak baru
    };

// cara 2
function Mail() {
    this.from = 'pengirim@dicoding.com';
    this.contacts = [];
    this.sendMessage = function(msg, to) {
        console.log('you send:', msg, 'to', to, 'from'this.from);
    this.contacts.push(to); // menyimpan kontak baru
    };
};
```

Contoh class di atas memiliki 3 \(tiga\) property dan method. Yang perlu diingat adalah, this merupakan representasi bahwasanya _field_ yang ditunjuk adalah field global dan dapat diakses dari method ataupun property di dalam kelas tersebut dengan menambahkan this di depannya. Sebagai gambaran, kita akan coba ubah kode di atas menjadi seperti berikut ini:

```javascript
class Mail{
  from = 'pengirim@dicoding.com';
    contacts = [];
    sendMessage = function(msg, to, from) {
        console.log('you send:', msg, 'to', to, 'from', from); // from di sini merujuk ke `from` parameter, bukan ke `from` dari global value yaitu pengirim@dicoding.com
    this.contacts.push(to);
    };
}

const mail1 = new Mail();
mail1.sendMessage('hallo', 'penerima@dicoding.com', 'aku@gmail.com');

/**
you send: hallo to penerima@dicoding.com from aku@gmail.com
**/
```

Contoh di atas menunjukan bahwa ketika kita ingin menginisialisasi ataupun mengakses sebuah attribute global dari sebuah kelas, maka harus menggunakan this.attributeName.

Dalam OOP sendiri, properti dibagi menjadi 2:

* _Internal interface_ : method dan property yang dapat diakses oleh method lain namun tidak bisa diambil/dijalankan di luar kelas tersebut.
* _External interface_ : method dan property yang dapat diakses di luar kelas itu sendiri.

Sedangkan di dalam JavaScript sendiri terdapat 2 jenis akses identifier untuk sebuah field:

* _Public_ : dapat diakses dari mana pun.
* _Private_ : hanya dapat diakses dari dalam kelas itu sendiri.

Secara _default_, semua atribut yang didefinisikan adalah public. Sehingga semua attribute tersebut dapat diakses oleh objek yang telah meng-instansiasi kelas tersebut. Sebagai contoh:

```javascript
const mail1 = new Mail();
mail1.from; // 'pengirim@dicoding.com'
mail1.contacts; // ['penerima@dicoding.com']
mail1.sendMessage('hallo', 'penerima@dicoding.com'); /method mengirim pesan
```

Dari contoh tersebut, bagaimana jika kita ingin mengubah attribute contacts yang tidak dapat diakses langsung oleh objek yang telah meng-instansiasi. Kita perlu mengubah sedikit pada kode class Mail yang kita miliki:

```javascript
/** 
cara 1, menggunakan var (hanya dapat digunakan padpenulisan kelas menggunakan statement `function`)
**/
var contacts = [];
// contoh
function Mail(){
  this.from = 'pengirim@dicoding.com';
    var contacts = [];
    sendMessage = function(msg, to) {
        console.log('you send:', msg, 'to', to, 'from'this.from);
                      contacts.push(to);
    };

/**
cara 2, cara ini dapat digunakan pada penulisan kelamenggunakan statement `function` dan `class`
**/
_contacts = []
// contoh
class Mail{
  from = 'pengirim@dicoding.com';
    _contacts = [];
    sendMessage = function(msg, to) {
        console.log('you send:', msg, 'to', to, 'from'this.from);
    this._contacts.push(to);
    };

/** 
cara 3, menambahkan prefix # , cara ini dapat digunakapada penulisan kelas menggunakan statement `class` saja 
  **/
#contacts = [];
// contoh
class Mail{
  from = 'pengirim@dicoding.com';
    #contacts = [];
    sendMessage = function(msg, to) {
        console.log('you send:', msg, 'to', to, 'from'this.from);
    this.#contacts.push(to);
    };
}
```

Dari contoh di atas, ketika kita ingin mengakses attribute contacts secara langsung melalui objek yang menginisiasi maka return-nya adalah undefined. Ketiga cara tersebut juga dapat digunakan pada sebuah method atau function.

```javascript
const mail = new Mail();

mail.contacts; // undefined
```

Catatan: Ketahuilah bahwa cara ke-2 bukanlah cara murni yang diusung JavaScript dalam menetapkan atribut private. Namun, cara tersebut merupakan standarisasi penulisan yang biasanya digunakan oleh pengembang software \(dengan JS\) untuk membedakan variable-variable yang merupakan private variable.

Sedangkan untuk cara 3, belum sepenuhnya didukung oleh JavaScript engine versi lama. ini merupakan proposal pengembangan JavaScript terkait dengan identifier pada js \([https://github.com/tc39/proposal-private-methods](https://github.com/tc39/proposal-private-methods)\).

