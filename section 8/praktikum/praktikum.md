import 'dart:async';

Future<List> calc(l1, p1) {
  var isi = [];
  return Future.delayed(Duration(seconds: 1), () {
    for (var el in l1) {
      isi.add(el * p1);
    }
    return isi;
  });
}

void main(List<String> args) async {
  var list1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  var pengali = 2;
  print('nilai list sebelum di kali dengan pengali ');
  print(list1);
  print('setiap elemen dalam list dikalikan dengan nilai pengali:');
  var new_list = await calc(list1, pengali);
  print(new_list);
}