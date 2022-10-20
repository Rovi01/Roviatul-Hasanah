void main(List<String> args) {
  List<List<int>> nilai = [
    [21, 32],
    [33, 43],
    [22, 44],
    [55, 65]
  ];

  var nilaiMap = nilai.asMap();
  print(nilaiMap);
  for (int i = 0; i < nilaiMap.length; i++) {
    print('nilai yang ada di key $i di map: ${nilaiMap[i]}');
  }
}
