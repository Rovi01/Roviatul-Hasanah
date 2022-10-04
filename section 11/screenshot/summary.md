1.constructur adalah 
- method yang di jalankan saat pembuatan objoct
- dapat menerima parameter
- tidak memiliki return
- nama sama dengan kelas
contoh 
``` class Hewan {
var mata;
var kaki;

Hewan (){
mata = 0;
kaki = 0;
}
}
```
2. inheritence
- membuat class baru dengan memanfaatkan class yang sudah ada
- bertujuan agar kemampuan classyang sudah ada dapat dimiliki oleh class baru
- dapat dianalogikan dengan seorang anak yang mewarisi sifat dari orang tua nya dimana yang mewarisi sifat tersebut diberi nama kelas anak dan yang mewariskan sifat tersebut di beri nama kelas induk.
- untuk melakukan inheritance kita dapat menambahkan extends saat pembuatan class baru
```
import 'nama fileclass.dart';
class kambing extends Hewan {
kambing(){
mata = 2;
kaki =4;
}
}
```
dan dapat di panggil dengan
```
void main (){
var k1 =kambing();
print(k1.mata);
print (k1.kaki);

var h1 = Hewan();
print(h1.mata);
print(h1.kaki);
}
```

3. method overridding
- menulis ulang method yang ada pada super-class
- bertujuan agar class memiliki method yang sama , dengan proses yang berbeda
melakukan overriding 
- dilakukan pada class yang melakukan inheritance
- method sudah ada pada class induk
- method di tulis ulang seperti membuat method baru pada class anak
- ditambahkan tanda @override di baris sebelum method di buat
 dapat ditulis dengan
```
import 'constructor.dart';

class Kambing extends Hewan {
@override
reproduksi (){
print('melahirkan');
}
@override
bernapas (){
print('paru-paru');
}
}

void main (){
var k1 =Kambing();
k1.reproduksi();// telah melakukan method override
k1.bernapa();

var h1= hewan();
h1.reproduksi();// sebelum melakukan method override
h1.bernapas();
}
```

4.interface
- berupa clas
- menunjukkan methid apa saja yang ada pada suatu class
- seluruh method wajib di override
- di gunakan dengan menggunakan kata kunci implements

cara menggunakan interface
- sekilas mirip inheritance
- pada class yang melakukan implements wajib melakukan override semua method yang ada pada class induk

cara penggunaan 
```
//membuat class hewan terlebih dahulu
class Hewan {
reproduksi (){
print ('tidak di ketahui');
}

bernafas (){
print ('tidak di ketahui');
}
}


//lalu kita langsung dapat menggunakan interface
class Kambing implements Hewan {
@override
reproduksi(){
print('melahirkan');
}

@overrride
bernafas (){
print ('paru-paru');
}
}
```