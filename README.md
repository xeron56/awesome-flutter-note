# awesome-flutter-note

```dart
(new) Visibility Visibility({
  Key? key,
  required Widget child,
  Widget replacement = const SizedBox.shrink(),
  bool visible = true,
  bool maintainState = false,
  bool maintainAnimation = false,
  bool maintainSize = false,
  bool maintainSemantics = false,
  bool maintainInteractivity = false,
})
package:flutter/src/widgets/visibility.dart   
```

Here is a table of the parameters for the `Visibility` widget:

| Parameter | Description | Example |
| --- | --- | --- |
| `key` | A key to identify the widget | `key: Key('my-visibility-widget')` |
| `child` | The widget to show or hide | `child: Text('Hello World')` |
| `replacement` | The widget to show when `child` is hidden | `replacement: Text('This text is hidden')` |
| `visible` | Determines whether the `child` widget should be visible or not. If `false`, the `replacement` widget will be shown in its place. | `visible: true` |
| `maintainState` | If `true`, the `child` widget's state will be preserved when it is hidden. If `false`, the `child` widget's state will be discarded when it is hidden. | `maintainState: false` |
| `maintainAnimation` | If `true`, the `child` widget's animation will be preserved when it is hidden. If `false`, the `child` widget's animation will be stopped when it is hidden. | `maintainAnimation: true` |
| `maintainSize` | If `true`, the `child` widget's size will be preserved when it is hidden. If `false`, the `child` widget will be shrunk to a size of 0 when it is hidden. | `maintainSize: true` |
| `maintainSemantics` | If `true`, the `child` widget's semantics will be preserved when it is hidden. If `false`, the `child` widget's semantics will be discarded when it is hidden. | `maintainSemantics: true` |
| `maintainInteractivity` | If `true`, the `child` widget's interactivity will be preserved when it is hidden. If `false`, the `child` widget will not be interactive when it is hidden. | `maintainInteractivity: true` |

Here is an example of using the `Visibility` widget:
```dart
Visibility(
  child: Text('Hello World'),
  replacement: Text('This text is hidden'),
  visible: true,
  maintainState: false,
  maintainAnimation: true,
  maintainSize: true,
  maintainSemantics: true,
  maintainInteractivity: true,
)
```
