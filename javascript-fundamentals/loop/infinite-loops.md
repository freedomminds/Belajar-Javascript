# Infinite loops

Ketika menerapkan perulangan pada program, ada satu kondisi yang perlu kita hindari yaitu _infinite loop_. Infinite loop atau _endless loop_ adalah kondisi di mana program kita _stucked_ di dalam perulangan. Ia akan berjalan terus hingga menyebabkan _crash_ pada aplikasi dan komputer kecuali ada intervensi secara eksternal, seperti mematikan aplikasi.

Kode berikut ini adalah contoh di mana kondisi infinite loop dapat terjadi:

**While**

```javascript
    let i = 1;
     
    while (i <= 5) {
        console.log(i);
    }
```

**For**

```javascript
    for(let i = 1; i <= 5; i=1) {
        console.log(i);
    }
```

Dapatkah Anda menemukan apa yang salah dari kode di atas sehingga terjadi infinite loop?

Jawabannya adalah karena variabel i selalu bernilai 1. Alhasil, kondisi i &lt;= 5 akan selalu bernilai true yang mengakibatkan aplikasi akan terus mencetak 1 ke konsol sehingga mengalami _crash_.

