send request data from one page to another and catch the processed data back to the page

- pageone:

```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondPage()),
).then((result) {
  if (result != null) {
    setState(() {
      Map data = result;
      _location = data['location'];
    });
  }
});
```
- page two 

  ```dart
   Navigator.pop(context, {
   "location": snapshot.data[index].location,
    //flag": snapshot.data[index].flag,
    "time": snapshot.data[index].time,
    "isDaytime":
        snapshot.data[index].isDaytime,
    "url": snapshot.data[index].url,
    "weatherData":
        snapshot.data[index].weatherData,
    "dateconverted":
        snapshot.data[index].dateconverted,
  });
  ```
  
