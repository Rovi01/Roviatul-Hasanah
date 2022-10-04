1. anonymous function
 >kita dapat mendeklarasikan function yang tidak memiliki nama yaitu anonymousfunction  dan berfungsi sebagai data  parameter contoh penulisan nya sebagai berikut :
 ```
 (){
    //perintah yang di jalankan saat fungsi di panggil
 }
```
2. Arrow Function
>>Arrow Function merupakan fungsi yang dapat memiliki nama ataupun tidak. Fungsi ini berisi satu data baik dari proses maupun data statis. Nilai return fungsi ini diambil dari data tersebut. 
dapat di tulis dengan :
```
()=> proses_yang _dijalankan_saat_fungsi_dipanggil();
```
berikut cara menggunakan arrow function.
```
var hello =() => print ('hello');
var jumlah = (int a, int b) => return a+b;


void main (){
   hello ();
   print (jumlah(1,3));
}
```
dengan fungsi ini maka penulisan akan membuat penulisan lebih singkat di banding penulisan yang biasanya.
3. async-await
-dengan menjalankan perintah async-await ini dapat menjalankan beberapa proses tanpa perlu menunggu
-proses di tulis dalam bentuk fungsi
- await akan menunggu hingga proses async selesai

fungsi dapat di tulis dengan:
```
void P1() {
	Future.delayed(Duration(seconds: 1), () {
		print('Hello dari p1');
	});
}

void P1() {
	print('Hello dari p1');
}

void main() {
	p1();
	p2();
}
```
pada fungsi di atas fungsi p1 akan di pending 1 detik setelah p2 telah di eksekusi.objek future berfungsi untuk menunda proses eksekusi suatu fungsi.

berikut merupakan source code dengan menambahkan perintah *await*
```
Future<void> P1() async {
	await Future.delayed(Duration(seconds: 1), () {
		print('Hello dari p1');
	});
}

void P1() {
	print('Hello dari p1');
}

void main() async {
	await p1();
	p2();
}
```
>ada source code ini, fungsi dengan keyword Await akan menunggu hingga proses asyncronus selesai. Dengan kata lain, fungsi p2() tidak akan dieksekusi hingga fungsi p1() selesai tereksekusi.