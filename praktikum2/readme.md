soal 1:
Modifikasilah kode pada baris 3 di VS Code atau Editor Code favorit Anda berikut ini agar mendapatkan keluaran (output) sesuai yang diminta!

Jawaban:
kode: 
void main() { 
   for (int i = 19; i > 9; i--) {
    print('Nama saya adalah Rifqi, sekarang berumur ${i - 1}');
   }
}

soal 2:
Mengapa sangat penting untuk memahami bahasa pemrograman Dart sebelum kita menggunakan framework Flutter ? Jelaskan!

Jawaban:
Karena framework flutter memerlukan bahasa tingkat tinggi untuk memberikan pengalaman terbaik kepada pengembang, dan memungkinkan membuat aplikasi seluler yang luar biasa, maka dari itu flutter memilih dart yang merupakan bahasa tingkat tinggi, serta lebih efisien daripada bahasa pemrograman biasanya. 
maka dari itu, memahami dart merupakan akar fundamental sebelum memulai menggunakan framework flutter. 

soal 3:
Rangkumlah materi dari codelab ini menjadi poin-poin penting yang dapat Anda gunakan untuk membantu proses pengembangan aplikasi mobile menggunakan framework Flutter.

Jawaban: 
poin-poin penting yang saya dapatkan dari materi ini adalah:
- flutter memerlukan bahasa tingkat tinggi supaya memberikan pengalaman terbaik kepada pengembang, serta supaya dapat mengembangkan aplikasi seluler yang luar biasa. maka dari itu, memahami dart merupakan langkah awal yang diperlukan untuk dapat mengaplikasikan framework flutter.
- mempelajari operator bawaan dart serta bagaimana dart bekerja dengan OOP. 
- fitur-fitur dart antara lain adalah productive tooling yang merupakan tool untuk menganalisis kode, plugin, IDE, dan ekosistem paket yang besar. fitur garbage collection untuk mengefisiensi penyimpanan dengan mengoptimalisasi memori yang ditempati dengan mengelola atau dealokasi memori. fitur type annotations untuk keamanan dalam mengontrol semua data dalam memori. statically typed, dan portability karena dart tidak hanya dapat dikompilasi di web, tapi juga dapat secara native ke kode ARM dan x86.
- evolusi dan sejarah dart, diluncurkan pertama kali pada tahun 2011 dan meriilis versi stabilnya pada tahun 2013, serta terdapat perubahan besar pada akhir 2018. bermula fokus pada pengembangan web, kemudian mencoba memecahkan masalah pada javascript yang tidak menyediakan ketahanan seperti mayoritas bahasa pemrograman lainnya, sehingga dart ingin menjadi penerus dari js. kemudian menawarkan performa terbaik dan alat yang lebih baik untuk proyek berskala besar, dengan tool yang lebih modern dan stabil untuk mendapatkan performa terbaik dengan tetap menjaga nuansa bahasa pemrograman yang dinamis. kemudian dibentuk agar kuat dan fleksibel, dart dapat menyeimbangkan dua fitur utama, yakni fleksibilitas dan ketangguhan.
- cara kerja dart Perlu dicatat bahwa kode dan dependensi bisa jadi tidak sesuai dengan cara mengeksekusikan aplikasi; namun tidak perlu melakukan banyak perubahan pada kode untuk dapat mendukung cross-platform.
- pengenalan struktur bahasa dart adalah Dart menyediakan sebagian besar operator standar untuk memanipulasi variabel; built-in types adalah yang paling umum ditemukan dalam bahasa pemrograman tingkat tinggi. Control flow dan function sangat mirip dengan bahasa pemrograman lainnya. dengan object orientation, dart operators, arithmetic operators, operator increment dan decrement, operator equality dan relational, serta opereator logical. 
- kemudian praktik dengan dart, menggunakan dartpad. 

soal 4:
Buatlah penjelasan dan contoh eksekusi kode tentang perbedaan Null Safety dan Late variabel !

Jawaban:
null safety adalah sebuah fitur dari dart untuk mengamankan supaya dalam penulisan kode, variabel tidak boleh bernilai null jika tanpa diizinkan, karena bisa menyebabkan NoSuchMethodError. dengan non-lullable variable, jika mengisikan nilai variable bernilai null, maka akan muncul error saat dicompile A value of type 'Null' can't be assigned to a variable of type 'String'.
jika ingin boleh null, maka menuliskan "String? nama;"
contoh: void main() {
  String? nama;
  print(nama); // Output: null
}

jika dengan null assertion operator atau negasi, (!)
maka variable tidak boleh null. 
contoh:
void main() {
  String? nama = "Hilmi";
  print(nama!.length);
}

jika nama ternyata null, 
String? nama = null;
print(nama!.length);

akan error saat runtime
Null check operator used on a null value
jadi ! beresiko jika tidak hati hati.

Late Variable, late digunakan ketika variabel non-lullable akan diinisiasi nanti ketika belum dipakai. 
tanpa late, maka akan error:
String nama;
error:
Non-nullable variable 'nama' must be assigned before it can be used.

dengan late:
late String nama;

void main() {
  nama = "Hilmi";
  print(nama);
}

outputnya:
Hilmi

nah maka dart mengizinkan karena berjanji mengisi sebelum digunakan. 
jika tidak diisi:
late String nama;

void main() {
  print(nama);
}

runtime error:
LateInitializationError: Field 'nama' has not been initialized.

Null Safety:
Mengontrol apakah variabel boleh null atau tidak.
Late:
Menunda inisialisasi variabel non-nullable.
Operator !:
Memaksa Dart menganggap variabel tidak null.

