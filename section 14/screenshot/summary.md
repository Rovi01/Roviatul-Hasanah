1.flutter cli 
adalah command line interface yaitu alat yang digunakan untuk berinteraksi dengan Flutter SDK dan merupakan suatu perintah yang di jalankan di dalam terminal ctor

2.important cli commands
- flutter doctor
- flutter create
- flutter run
- flutter emulator
- flutter channel
- flutter pub
- flutter build
- flutter clean

flutter doctor
perintah untuk menampilkan informasi software yang dibutuhkan flutter

flutter create
perintah untuk membuat project aplikasi flutter baru di directory
```
flutter create <nama_file>
flutter run
perintah untuk menjalankan project aplikasi di device yang tersedia
```
flutter run <dart_file>
```
##### flutter emulator
perintah untuk menampilkan daftar emulator yang terinstall dan maenmpilkan option untuk membuka emulator baru
```
flutter emulator
flutter emulator -- launch<emulator_id>
flutter emulator --create [--nama xyz]
```
##### flutter channel
perintah untuk menampilkan daftar flutter channel yang tersedia dan menunjukkan channel yang digunakan saat ini
```
flutter channel
```

##### flutter pub
ada dua syntax yang bisa kita gunakan , yaitu:
- flutter pub add, untuk menambahkan packages ke dependencies yang ada di pubspec.yaml
```
flutter pub add <package_name>
```
- flutter pub get,untuk ,mendownload semua packages atau dependencies yang ada di pubspec.yaml
```
flutter pub get
```
##### flutter build
perintah untuk memproduksi sebuah file aplikasi untuk keperluan deploy atau publish ke appstore,playstore dan lain-lain
```
fluttr build <directory>
```

##### flutter clean
- perintah untuk menghapus folder build serta file lainnya yang di hasilkan saat kita menjalankan aplikasi di emulator
- perintah ini akan memperkecil ukuran project tersebut
```
flutter clean
```

3.packages management
- flutter mendukung sharing packages
- packages dibuat developers lain
- mempercepat  pengembangan aplikasi karena tidak perlu membuat semuanya dari awal atau from scratch
- mendapatkan packages di website pub.dev

4.cara menambahkan packages
- cari package di pub.dev
- copy baris dependencies yang ada di bagian installing 
- buka punspec.yaml
- paste barisnya di bawah dependencies pubspec.yaml
- run flutter pub get di terminal
- import package di file dart agar bisa di gunakan
- stop atau restart aplikasi jika dibutuhkan
 