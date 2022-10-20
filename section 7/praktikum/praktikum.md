import 'dart:io';

void main() {
  int faktorial = 1;
  print("Masukkan bilangan bulat : ");
  int? n = int.parse(stdin.readLineSync()!);
  if (n < 0) {
    print("Angka yang dimasukkan bukan bilangan bulat");
  } else {
    for (int i = 1; i <= n; i++) {
      faktorial *= i;
    }
    print("Hasil faktorial dari " +
        n.toString() +
        " adalah " +
        faktorial.toString());
  }
}

import 'dart:io';

void main() {
  int nilai;

  stdout.write('masukkan nilai anda: ');
  nilai = int.parse(stdin.readLineSync().toString());
  print('\n anda mendapatkan nilai: ${nilai1(nilai)}');
}

String nilai1(int nilai) {
  if (nilai > 70) {
    return 'A';
  }
  if (nilai > 40) {
    return ' B';
  }
  if (nilai > 0) {
    return 'C ';
  } else {
    return '';
  }
}