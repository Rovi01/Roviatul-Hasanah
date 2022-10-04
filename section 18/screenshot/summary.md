1.Row dan Column
- row meletakkan widget childrennya secara horizontal
- column meletakkan widget childrennya secara vertikal

2. MainAxisSize properti
- menentukkan seberapa banyak space menempati main axis 
- main axis dari row adalah horizontal
- main axis dari column adalah vertikal
- properti mainAxisSize memiliki dua values, MainAxisSize.max dan MainAxisSize.min
- MainAxisSize.max menempati semua space dari main axis
- MainAxisSize.min tidak memiliki extra space, hanya untuk childrennya saja

3.MainAxisAligment properti
- properti digunakan column dan row untuk memposisikan children mereka di extra space yang ada
- memiliki 6 values 
1.MainAxisAligment.start
2.MainAxisAligment.end
3.MainAxisAligment.center
4.MainAxisAligment.spaceBetween
5.MainAxisAligment.spaceEvenly
6.MainAxisAligment.space.Around

4.CrossAxisAligment
- properti digunakan column dan row untuk memposisikan children mereka pada cross axis
- cross axis dari row adalah vertikal dan cross axis dari column
- memiliki 5 values
1. CrossAxisAligment.start
2. CrossAxisAligment.end
3. CrossAxisAligment.center
4. CrossAxisAligment.stretch
5.CrossAxisAligment.baseline

 5.flexible widget
- membungkus widget lain sehingga child dari flexible widget menjadi flexible atau resizable
- sangat berguna untuk membuat aplikasi  yang responsif
- harus berada dalam turunan parent widget row atau column 
- perubahan ukuran di tentukan dengan properti fit dan flex


6.fit properti
- menentukan apakah flexible widget memenuhi extra space yang tersedia di main axis nya
- meneriama nilai value berupa FlexFit.loose atau FlexFit.tight
- flexFit.loose akan memiliki ukuran minimum
- FlexFit.tight akan memiliki ukuran maximum

 7.Flex properti
- menentukan perbandingan ukuran dari child widget nya
- menerima niai values berupa integer
- membandingkan nilainya dengan flex properti lain
