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