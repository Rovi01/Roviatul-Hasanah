1.apa itu flutter 
fluter adalah alat pengembangan antarmuka pengguna dari google yang digunakan untuk membuat aplikasi mobile , desktop,  dan web.
2.keunggulan flutter
- mudah di gunakan 
- produktivitas tinggi
- dokumnetasi lengkap dapat di akses di website flutter.dev
- komunitas yang berkembang
3.bagian dari flutter
sdk(software development kit) yang merupakan alat-alat untuk membantu proses pengembangan aplikasi dan didalam sdk sudah termasuk dengan framework yaitu perlengkapan untuk membentuk aplikasi yang dapat di kustomisasi, dan framework sendiri digunakN untuk membangun aplikasi yang cantik dan multiplatform hanya dengan single code base

4.membuat project flutter
- project flutter dapat di buat dengan cara menuliskan cara flutter create <nama_project>
contoh
```
flutter create phonebookapp
```
5.menjalankan project flutter
- masuk ke direktori project
- lalu jalankan perintah 
```
flutter run
```
6.struktur direktori flutter
1.direktori platform:
- android
- ios
- web
2.direktori project:
- lib-ruang kerja utama
- test- aktivitas pengujian
7.file utama 
- file yang partama kali dibaca dan di jalankan adalah main.dart
- main.dart berada didalam direktori lib
- didalam main.dart kita dapat menuliskan fungsi main yang merupakan entry point saat kita menjalankan aplikasi
- di dalam fungsi main terdapat fungsi runapp yang berfungsi untuk memberitahukan flutter dan merupakan top level widget dari aplikasi yang di buat.

 8.widget
- digunakan untuk membentuk antarmuka(UI)
- widget juga berupa class
- dan dapat terdiri dari beberapa widget

9.jenis direktori
1.stateless
- tidak bergantung pada perubahan data
- hanya fokus pada tampilan
- dibuat dengan extends pada class stateless widget
dibuat dengan:
```
class MyWiidget extends  statelessWidget {
conts MyWidget({Key?key}): super(key:key);

@override
Widget build (BuildContext){
return conts MaterialApp(
home: Scaffold(
body: Text('selamat datang di flutter.'),
),
);
}
}
```
2.stateful
- mementingkan pada perubahan data
- dibuat dengan extends pada class stateful widget
- 1 widget menggunakan 2 class (widget dan state)
class widget
```
class MyWiidget extends  statelessWidget {
conts MyWidget({Key?key}): super(key:key);
@override
createState()=> MyWidgetState();
}
```
class state
```
class MyWidgetState extends State <MyWidget>{
@override
Widget build (BuildContext context){
return const Materiaapp(
home:scafforl(
body: Text ('selamat datang di flutter.'),
),
);
}
}
```
10.Built in Widget
- widget yang dapat langsung digunakan
- sudah ter-install bersama flutter
#### MaterialApp
membangun aplikasi dengan desain material
```
conts MaterialApp(
    home: Text('selamat datang di flutter.'),
);
```
#### Scaffold
membentuk sebuah halaman 
```
conts Scaffold(
    body:Text('selamat datang di flutter'),
);
```
#### AppBar

digunakan untuk membentuk application bar yang terletak pada bagian atas halaman
```
AppBar(
    title:  conts Text ('Home'),
);
```
#### Text
berfungsi untuk menampilkan teks
```
conts Text ('haloo');
```

 11.MaterialApp
- widget dasar yang mengemas seluruh widget dalam aplikasi
- widget yang digunakan pada sistem android
- di import  dari package:flutter/material.dart

 12. CupertinoApp
- widget dasar yang mengemas seluruh widget dalam aplikasi 
- widget yang digunakan pada sistem ios
- di import dari package:flutter/cupertino.dart

13.row dan column
- row meletakkan widget childrennya secara horizontal
```
body: row(
children : conts[
BlueBox(),
BlueBox(),
BlueBox(),
],
),
```
- column meletakkan widget childrennya secara  vertikal
```
body: column(
children : conts[
BlueBox(),
BlueBox(),
BlueBox(),
],
),
```

14.MainAxisSize properti
- menentukan seberapa banyak space menempati main axis
- main axis dari row adalah horizontal
- main axis dari column adalah vertikal
- properti mainaxissize memiliki  dua values, mainaxissize.max dan MainAxisSize.min
- MainAxisSize.max menempati semua space dari main axis
- MainAxisSize.min tidak memiliki extra space, hanya untuk childrennya saja

15. MainAxisAlignment properti
- propertiini digunakan row dan column untuk memposisikan children mereka di extra space yang ada
- memniliki 6 values:
1.MainAxisAlignment.start
2.MainAxisAlignment.end
3.MainAxisAlignment.center
4.MainAxisAlignment.spaceBetween
5.MainAxisAlignment.spaceEvenly
6.MainAxisAlignment.spaceAround