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
7. Tipe Data Number
   - Pada javascript hanya hanya number yang merupakan tipe data untuk bekerja dengan angka (int, float, double, dll)
   - contoh: 10 (int), 19.8 (float), 0733 (okta), 0o644, 0x12, 0b1101, NaN (not a number), infinty
   - deklarasi -> let one = 1;
                  let hundred = new Number(100);
8. Tipe Data Boolean
   - benar/salah.
   - deklarasi -> let isDead = false;
                  let isLife = new Boolean(true);
9. Tipe Data String
    - Tidak ada tipe data char, langsung jadi string
    - deklarasi -> let firstWord = "alex";
                   let secondWord = 'bernard';
                   let thirdWord = `charlie`;
                   let forthWord = new String("daniel");
    - Pakek "" (petik dua) untuk string
    - Manipulasi string:
      > concatenate -> + (tambah)
      > format -> `` (backtag) dan $ (dolar) -> `${firstWord} ${secondWord}`
      > upperCase -> .toUpperCase()
      > lowerCase -> .toLowerCase()
      > trim -> .trim() | .trimStart() | .trimEnd()
      > repeat -> .repeat(number)
10. Tipe Data Undefined
    - Merupakan representasi dari value yang tidak ada isinya
    - Value bawaan ketika mendeklarasikan variable tanpa ada isinya
    - deklarasi -> let emptyVar;
11. Tipe Data Null
    - Sama seperti undefined, yang merupakan representasi dari tipe data kosong
    - Dipakai jika kita MEMANG ingin mendeklarasi tipe data dengan nilai kosong
    - deklarasi -> let nullVariable = null;
12. Tipe Data Array
    - Berisi kumpulan data
    - Akses dengan index base (dimulai dari 0)
    - Isi array merupakan kumpulan data bertipe sama (idealnya, namun pada JS bisa digabung sesuka hati)
    - deklarasi -> let numbers = [1, 2, 3, 4, 5, 6, 7, 8];
                   let fruits = new Array("apple", "banana", "citrus", "dragon fruit");
12a. Akses Data Array
     - Gunakan index base
     - numbers[0];
12b. Mengubah Data Array
     - Gunakan index;
     - numbers[0] = 10;
12c. Menghapus Data Array
     - Bisa gunakan pop() (hapus dr blkg, mengembalikan nilai), shift() (hapus dari depan, mengembalikan nilai)
     - numbers.pop(); | numbers.shift();
12d. Menambah Data ke Dalam Array
     - Bisa gunakan push() (tambah dr blkg), unshift() (tambah dari depan)
     - numbers.push(value); | numbers.unshift(value);
12e. Merubah String ke Array
     - Merubah string ke char array
     - Banyak caranya, salah satunya dengan Array.from(string)
     - let charArray = Array.from("banana");
12f. Mencari Data Dalam Array
     - Menentukan suatu elemen ada pada array
     - fruits.includes("banana"); -> case sensitive
12g. Mengurutkan Data Dalam Array
     - Diurut berdasarkan alphabet
     - fruits.sort();
     - Untuk kasus Number -> [1, 3, 13, 4, 2, 35, 110], jika menggunakan sort() akan [1, 110, 13, 2, 3, 35, 4]. Untuk mengatasi itu tambahkan callback ->  [1, 3, 13, 4, 2, 35, 110].sort((a,b) => a-b)
12h. Array Slice
     - Memperoleh nilai dalam array
     - fruits.slice(1, 3); -> mengembalikan nilai dari index [parameter awal] sampai [parameter akhir-1]
     - fruits.slice(1);    -> mengembalikan nilai dari index [parameter awal] sampai akhir array
12i. Array Reverse
     - Membalikkan urutan array
     - fruits.reverse();
13. Tipe Data Object
    - Berisi kumpulan key dan value
    - Akses dengan key base
    - Isi objek bisa apa saja
    - deklarasi -> let person = {
                        name: "jane",
                        age: 37,
                        hobbies: ["photograpy", "genealogy"]
                     };
13a. Akses Data Object
     - Akses data dalam object bisa melalui 2 cara
       > menggunakan dot (.) -> person.name;
       > menggunakan array (['']) -> person['name'];
     - Akses data object dengan array memiliki kelebihan, yaitu kita bisa mengassign string variabel key ke sebuah variabel lain
13b. Merubah Data Dalam Object
     - Assign dengan mengakses keynya
     - person.age = 40; | person['age'] = 40;
14. Operasi Matematika
    - Tambah (+), kurang (-), kali (*), bagi(/), sisa bagi/modulus (%)
15. Operasi Perbandingan
    - Lebih kecil dari (<), lebih kecil/sama dengan (<=), lebih besar (>), lebih besar/sama dengan (>=), sama dengan (==) tidak mengecek tipe data, sama dengan (===) cek tipe datanya juga, tidak sama dengan (!=) tidak mengecek tipe data, tidak sama dengan (!==) cek tipe datanya juga
    lebih lanjut:
      (0 ==  '0') // true
      (0 === '0') // false

      ('' ==  0 ) // true, the string will implicitly be converted to an integer
      ('' === 0 ) // false, no implicit cast is being made
16. Operasi Penugasan
    - Sama dengan (=), tambah sama dengan(+=), kurang sama dengan (-=), kali sama dengan (*=), bagi sama dengan (/=), hasil bagi sama dengan (%=)
17. Operasi Logika
    - dan (&&), atau (||), negasi (!), bitwise dan (&) jarang dipakai, bitwise atau (|) jarang dipakai
18. Operasi Unary
    - typeof, mengetahui tipe data sebuah variabel
    - delete, menghapus object atau isi dari array
      > jika digunakan pada array, akan menyisakan empty pada nilai yg dihapus
      > jika digunakan pada object, akan menghapus keynya juga
19. If Else Expression
    - Melakukan percabangan kondisi
    - deklarasi -> if(kondisi){
                     doSomethingForThisKondisi();
                   }
                   else if(kondisi2){
                      doSomethingForKondisi2();
                   }
                   else{
                      doSomething();
                   }
20. Ternary Operator
    - kondisi? nilai jika true : nilai jika false
    - bisa di tumpuk/stack
    - deklarasi -> let isGenap = 19%2 === 0? true : false;
21. Thrutiness
    - Pada javascript sebuah nilai bisa dianggap true maupun false
    - Nilai yang dianggap true = true, {}, [], 42, -42, 3.14, 12n (number yang isi), "0", "false" (string yang isi), new Date() (mengeluarkan hasil), Infinity, -Infinity
    - nilai yang dianggap false = false, null, undefined, 0, -0, 0n (number 0), NaN, "" (string kosong)
22. Switch Statement
    - sama seperti percabangan if else, namun terdapat perbedaan pada switch kondisi yang di cek adalah nilai yang sesuai (=) dan tidak bisa memakai (>) / (<)
    - switch, case, default
    - menggunakan keyword break untuk mengakhiri suatu kondisi, jika tidak di break eksekusi akan lanjut pada case berikutnya
    - deklarasi -> switch(5){
                     case 0:
                        console.log(0);
                        break;
                     case 1:
                     case 2:
                     case 3:
                     case 5:
                        console.log("your number maybe between 1, 2, 3, 5");
                        break;
                     default:
                        console.log("your number neither 0, 1, 2, 3, 5");
                        break;
                   }
23. Perulangan For
    - Perulangan yang digunakan jika sudah jelas kita ingin mengulang berapa kali
    - deklarasi -> for(inisialisasi (optional); kondisi; increament/decreament) ->  
    for(let i = 0; i < 5; i++){
      doSomething();
    }
24. Perulangan While
    - Perulangan yang digunakan jika saat suatu kondisi masih terpenuhi
    - deklarasi -> inisialisasi;
                   while(kondisi){
                      doSomething();
                      increament/perubahan nilai;
                   }
                -> let repeat = "no";
                   while(repeat === "yes"){
                      doSomething();
                      repeat = "no";
                   }
25. Perulangan Do While
    - Hampir sama dengan while, namun kondisi ditaruh diakhir
    - Do while memastikan bahwa perulangan akan dieksekusi minimaln sekali
    - deklarasi -> inisialisasi; 
                   do {
                      doSomething();
                      increament/perubahan nilai;
                   } while(kondisi);
                -> let repeat = "no";
                   do {
                      doSomething();
                      repeat = "no";
                   } while(repeat === "yes");
Note: hati-hati saat menggunakan perulangan karena bisa menyebabkan infinit loop!!
26. Kata Kunci Break
    - Digunakan untuk sepenuhnya berhenti melakukan perulangan/ mengakhiri statement pada percabangan switch
27. Kata Kunci Continue
    - Digunakan untuk melanjutkan sebuah perulangan/ statement
28. Array Foreach
    - Sering digunakan untuk melakukan perulangan pada array atau sebuah koleksi
    - Merupakan sebuah function dalam Array
    - Menampung hasil data dalam callback function
    - deklarasi -> cities.forEach((city) => {
                     console.log(city);
                   });
29. Array Map
    - Digunakan untuk membuat array baru dari array sebelumnya
    - Merupakan sebuah function dalam Array
    - Menampung hasil data dalam callback function
    - deklarasi -> let citiesToUpperCase = cities.map((city) => city.toUpperCase());
30. Array Filter
    - Mengembalikan array baru berisi nilai dengan kondisi tertentu
    - Merupakan sebuah function dalam Array
    - Menampung hasil data dalam callback function
    - Hanya nilai yang memenuhi syarat yang akan dieksekusi
    - deklarasi -> let citiesInJawa = cities.filter((city) => city !== "Bali");
31. Array Reduce
    - Mengembalikan nilai tunggal dari sebuah array dengan melakukan suatu operasi
    - Mengeksekusi array dari kiri ke kanan
    - Kembalian dari reduce disimpan pada sebuah akumulator (biasanya diberi nama result)
    - Nilai awal akumulator bisa di setting dengan default undefined
    - deklarasi -> let sumArray = numbers.reduce((result, bil) => result += bil);
Perulangan dan manipulasi object
32. Object For In
    - Melakukan perulangan properti dalam suatu object
    - deklarasi -> for(let key in person){
                     doSomething();
                   }
33. Object Assign
    - Mengembalikan array baru dengan menggabungkan/menyalin object lain
    - deklarasi -> let newPerson = Object.assign({newObject_optional}, person);
34. Object Keys
    - Mengembalikan array baru yang berisi key (string) dari suatu object
    - deklarasi -> let personKeys = Object.keys(person);
35. Object Values
    - Mengembalikan array baru yang berisi value dari suatu object
    - deklarasi -> let personValues = Object.values(person);
36. Object Entries
    - Mengembalikan array 2 dimensi yang berisi key dan value suatu object
    - deklarasi -> let personEntries = Object.entries(person);
37. Function Declaration
    - Prosedure untuk melakukan sebuah tugas
    - Berfungsi untuk mengurangi penulisan code yang sama berulang-ulang
    - Bisa juga disebut function statement/ function definition
    - Save for later use
    - deklarasi -> function namaFuction(parameter){
                     statement;
                   }
38. Function Expression
    - Function dengan menggunakan nama variabel sebagai nama functionnya
    - Function ini terdiri dari variabel dengan value anonymous function
    - Urutan penulisan sangat penting, Karna tidak bisa dipakai sebelum dideklarasi
    - Mendefinisikan scope ulang sehingga saat eksekusi berada di scope global
    - deklarasi -> let myFunction = function(parameter){
                     statement;
                   }
39. Arrow Function
    - Versi lebih pendek dari pada function expression
    - Tidak mendefinisikan scope ulang
    - Sangat dianjurkan selalu memakai arrow function untuk menghindari ambiguitas
    - deklarasi -> let myArrow = (parameter) => {
                     statement;
                   }
                -> let my1ParameterArrow = parameter => statement; (biasanya untuk function dengan 1 parameter & 1 line statement)
    - Tetap pakai cara deklarasi pertama!!
Note tambahan: https://www.youtube.com/watch?v=h33Srr5J9nY
40. Parameter Function
    - Secara harfiah kita bisa memasukkan apa saja ke dalam parameter function
      > Single value
      > function lain
      > parameter array -> tambahkan ... (titik 3x) -> ...number
41. Try Catch Finaly
    - Mengelola error agar program tetap berjalan
    - Minimal harus ada Try-Catch / Try-Finaly / ketiganya
    - Jika ada error maka akan masuk ke catch
    - Finaly akan otomatis berjalan pada akhir eksekusi, baik saat kode berhasil dijalankan ataupun terjadi error
    - deklarasi -> try{ 
                     doSomething();
                   } catch (exception){
                     doSomethingIfError();
                   } finaly {
                     finalyDoSomething();
                   }
42. Throw
    - Berfungsi untuk mengeluarkan error pada waktu yang diinginkan
    - Ketika dieksekusi akan mengeluarkan error
    - Bisa dicustome
    - deklarasi -> throw new Error(message);
43. Console Time & TimeEnd
    - Mengembalikan berapa lama suatu function dijalankan
    - Waktu yang dihasilkan dalam bentuk ms (mili second)
    - deklarasi -> console.time(namaString);
                   function
                   console.timeEnd(namaString);
44. Console Group & GroupEnd
    - Berfungsi untuk mencetak inline group
    - Selama belum ketemu groupEnd() maka code yang dijalankan akan berada di dalam indentasi yang sama
    - deklarasi -> console.group();
                   function
                   console.groupEnd();
45. Function Callback
    - Function yang dimasukkan ke dalam function lain sebagai sebuah argumen
    - deklarasi -> function someFunction(() => console.log("this is callback"));
Note: function someFuction memiliki callback yang berupa anonymous function yang mencetak "this is callback"