1. Declarative UI
-Flutter memiliki sifat declarative yang artinya flutter membangun UI nya pada screen untuk mencerminkan keadaan state saat ini

2. State
-State adalah ketika sebuah widget sedang aktif dan widget tersebut menyimpan data di memori
Flutter akan membangun ulang UI nya ketika ada state atau data yang berubah
Ada 2 jenis state dalam flutter, ephemeral state dan app state

3. Ephemeral State
-Digunakan ketika tidak ada bagian lain pada widget tree yang membutuhkan untuk mengakses data widget nya, contohnya: 
- PageView
- BottomNavigationBar
- Switch Button.
Tidak perlu state management yang kompleks
Hanya membutuhkan StatefulWidget dengan menggunakan fungsi setState()

4. Pendekatan State Management
-setState
	Lebih cocok penggunaan nya pada ephemeral state
Provider
Penggunaan untuk state management yang lebih kompleks seperti app state, pendekatan ini direkomendasikan oleh tim flutter karena mudah dipelajari
Bloc
Menggunakan pola stream/observable, untuk memisahkan UI dengan bisnis logic nya

Class yang perlu diperhatikan dalam penggunaan provider, yaitu: 
-Dari Package Provider
ChangeNotifierProvider
MultiProvider
Consumer

-Built In class dari Flutter SDK
ChangeNotifier

5. ChangeNotifier
-Class yang menambah dan menghapus listeners
Digunakan dengan cara meng-extends
Memanggil notifyListeners(), fungsi yang memberitahu widget yang menggunakan state bahwa terjadi perubahan data sehingga UI nya harus dibangun ulang


