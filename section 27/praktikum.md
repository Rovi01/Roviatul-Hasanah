import 'package:dio/dio.dart';
import 'package:flutter/material.dart';
import 'package:flutter_testing/models/foods.dart';

class FoodService {
  final Dio dio = Dio();

  Future<List<Foods>?> fetchFood() async {
    try {
      final Response response = await dio.get(
          'https://my-json-server.typicode.com/hadihammurabi/flutter-webservice/foods');

      debugPrint(response.data.toString());

      List<Foods> foods =
          (response.data as List).map((e) => Foods.fromJson(e)).toList();

      return foods;
    } catch (e) {
      rethrow;
    }
  }
}

class Foods {
  int? id;
  String? name;

  Foods({this.id, this.name});

  Foods.fromJson(Map<String, dynamic> json) {
    id = json['id'];
    name = json['name'];
  }

  Map<String, dynamic> toJson() {
    final Map<String, dynamic> data = <String, dynamic>{};
    data['id'] = id;
    data['name'] = name;
    return data;
  }
}

import 'package:flutter/material.dart';
import 'package:flutter_testing/models/foods.dart';
import 'package:flutter_testing/service/services.dart';

enum HomeViewState {
  none,
  loading,
  error,
}

class HomeViewModel extends ChangeNotifier {
  HomeViewState _state = HomeViewState.none;
  HomeViewState get state => _state;

  List<Foods> _foods = [];
  List<Foods> get foods => _foods;

  changeState(HomeViewState s) {
    _state = s;
    notifyListeners();
  }

  getFoods() async {
    changeState(HomeViewState.loading);

    try {
      FoodService services = FoodService();
      final response = await services.fetchFood();
      _foods = response!;
      notifyListeners();
      changeState(HomeViewState.none);
    } catch (e) {
      changeState(HomeViewState.error);
    }
  }
}
