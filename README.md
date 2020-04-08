# mediaquery
flutter
/// media query
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: MainPage(),
    );
  }
}

class MainPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("latihan query"),
      ),
      body: (MediaQuery.of(context).orientation == Orientation.portrait)
          ? Column(
              children: generatecontainer(),
            )
          : Row(children: generatecontainer()),
    );
  }

  List<Widget> generatecontainer() {
    return <Widget>[
      Container(
        color: Colors.black,
        width: 100,
        height: 100,
      ),
      Container(
        color: Colors.red,
        width: 100,
        height: 100,
      ),
      Container(
        color: Colors.blue,
        width: 100,
        height: 100,
      ),
    ];
  }
}
