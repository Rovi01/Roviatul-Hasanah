1.AlertDialog
- untuk tampilan android, dari material design
- menginformasikan pengguna tentang situasi tertentu
- bisa digunakan untuk mendapatkan input dari user
- membutuhkan helper method showdialog

2.cara membuat alertdialog
- menambahkan alert dialog
- memanggil fungsi showDialog di dalam fungsi onPressed pada iconButton
- showDialog membuthkan context dan builder
- di buildernya akan me-return AlertDialog
- AlertDialog meyediakan properti seperti content dan actions
- content bisa dimasukkan widget text, gambar dan animasi gamber
- actions bisa di tambahkan button untuk menerima respon dari user

3.bottom sheet
-  seperti dialog tetapi muncul dari bawah layar aplikasi
- menggunakan fungsi bawaan flutter showModalBottomSheet
- membutuhkan dua properti, yaitu context dan builder