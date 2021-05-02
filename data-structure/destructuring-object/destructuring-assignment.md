# Destructuring Assignment

Pada contoh sebelumnya, kita telah melakukan destructuring object pada deklarasi variabel. Namun, pada kasus tertentu mungkin kita perlu melakukannya pada variabel yang sudah dideklarasikan.

```javascript
const profile = {
    firstName: "John",
    lastName: "Doe",
    age: 18
}
 
let firstName = "Dimas";
let age = 20;
 
// menginisialisasi nilai baru melalui object destruction
({firstName, age} = profile);
 
console.log(firstName);
console.log(age);
 
/* output:
John
18
*/
```

Saat melakukan destructuring assignment, kita perlu menuliskan destructuring object di dalam tanda kurung. Jika tidak menuliskan tanda kurung, tanda kurung kurawal akan membuat JavaScript mengira kita membuat _block_ statement, sementara _block_ statement tidak bisa berada pada sisi kiri _assignment_.

```javascript
// tidak bisa karena JavaScript mengira kita membuat block statement
// block statement tidak bisa berada pada sisi kiri assignment
{firstName, age} = profile;
```

Nah, inilah fungsinya tanda kurung. Ia akan memberi tahu JavaScript bahwa tanda kurawal di dalamnya bukan sebuah _block statement_ melainkan sebuah _expression_, sehingga _assignment_ dapat dilakukan.

```javascript
({firstName, age} = profile);
```

