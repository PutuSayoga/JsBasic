JavaScript (js)

1. Introduction
   - js dikenalkan oleh NetScape (NetScape LiveWire)
   - Berjalan dalam sebuah js engine dalam browser (v8, spider monkey, Trident, SquirrelFish, dll)
   - JavaScript tidak ada hubungannya dengan Java
   - Dibuat untuk membuat web menjadi interaktif
   - Multiparadigm = OOP, Fungsional, Procedural
2. Hello World
   - js berjalan di browser jd buat file .html
   - Buat html sederhana (atau pakai snippet di vs code)
   - Script js diletakkan didalam tag <script> ... </script>
   - Untuk melihat keluarannya, jalankan file .html tersebut, dan buka console pd browser (developer tools)
3. Variabel
   - js memiliki 2 type variable: mutable & immutable
   - Muttable bisa dibuat dgn kata kunci 'var' & 'let'
   - Immutable bisa dibuat dgn kata kunci 'const'
   - penulisan:
   [dataType] [namaVariabel] = [data];
   - Hoisting: perilaku js yang memindahkan deklarasi variabel ke atas
4. Variabel 'var'
   - Scope var dapat pindah dari lokal scope menjadi scope yg lbh tinggi
   - Dapat diubah dan dideklarasi ulang
   - Dapat diinstansiasi dan diinisasi pada posisi dimana saja. Namun akan bernilai 'undefined' / 'NaN'
   - Sudah tidak disarankan untuk menggunakan 'var'
5. Variabel 'let'
   - Hanya bisa diakses discope dia dideklarasikan
   - Dapat diubah tapi tidak dapat dideklarasi ulang (jika ada variabel yang sama program tidak akan berjalan)
   - Disarankan instansiasi diawal Untuk mencegah terjadinya error 'ReferenceError'
   - Sangat disarankan untuk menggunakan 'let' agar mengurangi kemungkinan terjadinya error
6. Variabel 'const'
   - Hanya bisa diakses discope dia dideklarasikan
   - Nilainya tidak dapat diubah dan tidak dapat dideklarasi ulang (jika ada variabel yang sama program tidak akan berjalan)
   - Harus langsung diassign
   - Harus diinstansiasi diawal, jika tidak akan terjadi error (program tidak berjalan)
7. Tipe Data
   - Ada beberapa tipe data pada javascript
8. Tipe Data Number
   - Pada javascript hanya hanya number yang merupakan tipe data untuk bekerja dengan angka (int, float, double, dll)
   - contoh: 10 (int), 19.8 (float), 0733 (okta), 0o644, 0x12, 0b1101, NaN (not a number), infinty
   - deklarasi => let one = 1;
                  let hundred = new Number(100);
9. Tipe Data Boolean
   - benar/salah.
   - deklarasi => let isDead = false;
                  let isLife = new Boolean(true);
10. Tipe Data String
    - Tidak ada tipe data char, langsung jadi string
    - deklarasi => let firstWord = "alex";
                   let secondWord = 'bernard';
                   let thirdWord = `charlie`;
                   let forthWord = new String("daniel");
    - Pakek "" (petik dua) untuk string
    - Manipulasi string:
      > concatenate => + (tambah)
      > format => `` (backtag) dan $ (dolar) => `${firstWord} ${secondWord}`
      > upperCase => .toUpperCase()
      > lowerCase => .toLowerCase()
      > trim => .trim() | .trimStart() | .trimEnd()
      > repeat => .repeat(number)
11. Tipe Data Undefined
    - Merupakan representasi dari value yang tidak ada isinya
    - Value bawaan ketika mendeklarasikan variable tanpa ada isinya
    - deklarasi => let emptyVar;
12. Tipe Data Null
    - Sama seperti undefined, yang merupakan representasi dari tipe data kosong
    - Dipakai jika kita MEMANG ingin mendeklarasi tipe data dengan nilai kosong
    - deklarasi => let nullVariable = null;
13. Tipe Data Array
    - Berisi kumpulan data
    - Akses dengan index base (dimulai dari 0)
    - Isi array merupakan kumpuan data bertipe sama
    - deklarasi => let numbers = [1, 2, 3, 4, 5, 6, 7, 8];
                   let fruits = new Array("apple", "banana", "citrus", "dragon fruit");
13a. Akses Data Array
     - Gunakan index base
     - numbers[0];
13b. Mengubah Data Array
     - Gunakan index;
     - numbers[0] = 10;
13c. Menghapus Data Array
     - Bisa gunakan pop() (hapus dr blkg, mengembalikan nilai), shift() (hapus dari depan, mengembalikan nilai)
     - numbers.pop(); | numbers.shift();
13d. Menambah Data ke Dalam Array
     - Bisa gunakan push() (tambah dr blkg), unshift() (tambah dari depan)
     - numbers.push(value); | numbers.unshift(value);
13e. Merubah String ke Array
     - Merubah string ke char array
     - Banyak caranya, salah satunya dengan Array.from(string)
     - let charArray = Array.from("banana");
13f. Mencari Data Dalam Array
     - Menentukan suatu elemen ada pada array
     - fruits.includes("banana"); => case sensitive
13g. Mengurutkan Data Dalam Array
     - Diurut berdasarkan alphabet
     - fruits.sort();
     - Untuk kasus Number => [1, 3, 13, 4, 2, 35, 110], jika menggunakan sort() akan [1, 110, 13, 2, 3, 35, 4]. Untuk mengatasi itu tambahkan callback =>  [1, 3, 13, 4, 2, 35, 110].sort((a,b) => a-b)
13h. Array Slice
     - Memperoleh nilai dalam array
     - fruits.slice(1, 3); => mengembalikan nilai dari index [parameter awal] sampai [parameter akhir-1]
     - fruits.slice(1);    => mengembalikan nilai dari index [parameter awal] sampai akhir array
13i. Array Reverse
     - Membalikkan urutan array
     - fruits.reverse();
14. Tipe Data Object
    - Berisi kumpulan key dan value
    - Akses dengan key base
    - Isi objek bisa apa saja
    - deklarasi => let person = {
                        name: "jane",
                        age: 37,
                        hobbies: ["photograpy", "genealogy"]
                     };
14a. Akses Data Object
     - Akses data dalam object bisa melalui 2 cara
       > menggunakan dot (.) => person.name;
       > menggunakan array (['']) => person['name'];
     - Akses data object dengan array memiliki kelebihan, yaitu kita bisa mengassign string variabel key ke sebuah variabel lain
14b. Merubah Data Dalam Object
     - Assign dengan mengakses keynya
     - person.age = 40; | person['age'] = 40;
15. Operasi Matematika
    - Tambah (+), kurang (-), kali (*), bagi(/), sisa bagi/modulus (%)
16. Operasi Perbandingan
    - Lebih kecil dari (<), lebih kecil/sama dengan (<=), lebih besar (>), lebih besar/sama dengan (>=), sama dengan (==) tidak mengecek tipe data, sama dengan (===) cek tipe datanya juga, tidak sama dengan (!=) tidak mengecek tipe data, tidak sama dengan (!==) cek tipe datanya juga
    lebih lanjut:
      (0 ==  '0') // true
      (0 === '0') // false

      ('' ==  0 ) // true, the string will implicitly be converted to an integer
      ('' === 0 ) // false, no implicit cast is being made
17. Operasi Penugasan
    - Sama dengan (=), tambah sama dengan(+=), kurang sama dengan (-=), kali sama dengan (*=), bagi sama dengan (/=), hasil bagi sama dengan (%=)
18. Operasi Logika
    - dan (&&), atau (||), negasi (!), bitwise dan (&) jarang dipakai, bitwise atau (|) jarang dipakai

