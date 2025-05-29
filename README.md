
https://github.com/user-attachments/assets/6fc295e3-79e3-4dc3-b984-3e204e4bdaa1

import 'package:flutter/material.dart';

void main() {
  runApp(CounterApp());
}

class CounterApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Button Counter',
      home: CounterHomePage(),
    );
  }
}

class CounterHomePage extends StatefulWidget {
  @override
  _CounterHomePageState createState() => _CounterHomePageState();
}

class _CounterHomePageState extends State<CounterHomePage> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      _counter += 1;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Button Counter'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text('You have pressed the button this many times:'),
            SizedBox(height: 10),
            Text(
              '$_counter',
              style: TextStyle(fontSize: 32, fontWeight: FontWeight.bold),
            ),
            SizedBox(height: 20),
            ElevatedButton(
              onPressed: _incrementCounter,
              child: Text('Press Me'),
            ),
          ],
        ),
      ),
    );
  }
}
