Arsitektur MVVM

1. MVVM ( Model View Model View Model)
-memisahkan logic dengan tampilan view ke dalam view model

A. keuntungan 1 Reusability
-jika ada beberapa tampilan yang memerlukan alur logic yang sama, mereka bisa menggunakan view model yang sama.
B. keuntungan 2 maintainability
-mudah dirawat karena pekerjaan terkait tampilan tidak tertumpuk bersama logic.
C. keuntungan 3 testability
-pengujian menjadi terpisah antara pengujian tampilan dengan pengujian logic sehingga dapat meningkatakan produktifitas pada pengujian.

2. melakukan MVVM 
-model memiliki 2 bagian, yaitu bentuk data yang akan digunakan dan sumber dari data tersebut.
-tiap screen diletakkan dalam sebuah direktori yang didalamnya terdapat view dan view model