1.assets 
- file yang di bundle dan di deployed bersamaan dengan aplikasi
- tipe-tipe assets , seperti : static data (JSON files),icons images, dan font file (tff)

2.menentukan assets 
- flutter menggunakan pubspec.yaml
- pubspec.yaml terletak pada root project , ntuk mengidentifikasi assets yang  dibutuhkan aplikasi
- gunakan karakter "/" untuk memasukkan semua assets dibawah satu directory name
```
assets:
- assets/my_icon.png
- assets/background.jpg
```

dan 
```
assets:
- assets/
```

 3.image
-  image atau gambar akan membuat tampilan aplikasi menjadi lebih menarik
- flutter mendukung format gambar seperti JPEG, WebP, GIF, Animated Web/GIF,PNG,BMP dan WBMP.
- menampilkan gambar dari project assets dan internet

 4.loading image versi 1
- gunakan widget image 
- membuthkan properti image dengan class AssetImage()
```
body :Column(
children : conts [
image(
image:assetimage('assets/backround.jpg'),
),
image(
image:assetimage('assets/my_icon.png'),
),
```
 5. loading images versi 2
- menggunakan method images.asset, mendapatkan image yang sudah ditambahkan dalam project
- menggunakan method image.network, mendapatkan data image melalui internet dengan menggunakan string url nya
```
body: Column (
children :
image.asset('assets/background.jpg'),
image.asset('https://picsum.photos/id/1'),
)
```