class ContactModel {
  String name;
  String phone;
  ContactModel({
    required this.name,
    required this.phone,
  });

  Map<String, dynamic> toMap() {
    return {'name': name, 'phone': phone};
  }
}

import 'package:flutter/material.dart';
import 'package:setstate_contact/pages/home_page.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: HomePage(),
    );
  }
}
