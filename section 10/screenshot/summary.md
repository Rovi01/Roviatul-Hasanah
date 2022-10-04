1.apa itu object oriented programing
> object oriented programing  adalah konsep paradigma yang berkonsep objek kita dapat memvisualisaikan objek dari dunia nyata kedalam program komputer.

>object oriented program bisa di sebut juga oop dalam oop kita dapat menyusun program dalam bentuk abstrak objek di mana kita bisa menampilkan atribut atau properti yang relevan saja dan menyembunyikan detailnya, data dan proses juga dapat diletakkan pada abstraksi tersebut 

 2.keuntungan OOP
 - pertama yaitu mudah di troubleshoot ketika terjadi error pada program, kita bisa mengetahui letak error tanpa memeriksa baris-berbaris Setiap kode kita.
 - kedua yaitu mudah digunakan ulang, beberapa objek memiliki kesamaan ciri-ciri dan perilaku sehingga kita tidak perlu membangun ulang ciri-ciri dan perilaku tersebut di setiap objek yang ada di program kita.

 3.penggunaan OOP 
 penggunaan OOP juga bisa kita dapatkan pada bahasa program seperti C++, Java, Javascript, dan  Phyton 

 4.Komponen OOP 
 OOP memiliki beberapa bagian, diantaranya :
 1. class

    class merupakan abstraksi dari sebuah benda atau objek dan memiliki ciri- yang di sebut property dan di dalam class juga memiliki sifat atau kemampuan yang disebut method

    > membuat class

    >kita dapat membuat class dengan menggunakan kata kunci *class*  di ikuti dengan nama kelasnya dan harus di tuliskan dengan pascal case atau di awali dengan huruf besar. Selain itu setiap properti harus ditulis dalam kurung kurawal ({})

    >Dari kelas yang kita buat kita dapat membuat objek berdasarkan kelas tersebut kita dapat menyimpan objek dalam sebuah variabel yang bisa kita sebut sebagai Instance of class object . object akan diperlakukan sebagai data.

    seperti contohh di bawah ini:
```
void main (){
    var h1 = Hewan ();
    var h2 = Hewan ();
    var h3 = Hewan ();

    print(h1);
    print(h2);
    print(h3);

} 
```

 2. Property

 properti merupakan ciri-ciri suatu class atau hal-hal yang dimiliki oleh suatu class untuk menggambarkan suatu objek contohnya seperti nama usia dan berat badan dll.
 properti juga memiliki sifat yang sama dengan variabel dimana saat kita membuat properti kita harus menentukan tipe data terlebih dahulu dan menginisialisasikan nilainya secara eksplisit atau kita juga dapt membuat nilai nya menadi null label dengan cara menambahkan tanda tanya setelah tipe datanya 

>Membuat properti 

 properti harus diletakkan di dalam sebuah   kelas, kita tidak bisa meletakkan properti di luar kelas, dan  seperti variabel properti harus diawali dengan tipe datanya lalu nama propertinya.
 dapat di tuliskan dengan
 ```
 class Hewan {
    var mata =1;
    var kaki = 2;
 }
```
dan dapat di akses dengan source code berikut:
``` 
void main (){
    var h1 = Hewan ();
    print (h1.mata);
    print (h1.kaki);
}
```
3. method

method  merupakan sifat atau perilaku Suatu kelas kita bisa membayangkan method itu seperti aktivitas yang dapat dikerjakan Suatu kelas Contohnya seperti hewan yang bisa bersuara, makan tidur dan lain-lain. metode merupakan sebuah function yang terdapat dalam sebuah kelas kita membuat funtion  atau method sama seperti  function yang sudah kita pelajari di dart  dasar yang bisa kita tambahkan parameter Kita juga bisa tambahkan return valuenya 

Dalam OOP  untuk membuat objek kita bisa tambahka function  atau methodnya di dalam sebuah kelas,  seperti contoh dibawah ini kita membuat absen yang bernama makan yang kita buat di dalam kelas sapi.
dituliskan dengan source code berikut
``` 
class Sapi {
    void makan (){
        print('makan');
    }
}
void main () {
var h1 = Sapi ();
h1.makan();
}
```

