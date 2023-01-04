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
# ListView
```dart
ListView(
{Key? key,
Axis scrollDirection = Axis.vertical,
bool reverse = false,
ScrollController? controller,
bool? primary,
ScrollPhysics? physics,
bool shrinkWrap = false,
EdgeInsetsGeometry? padding,
double? itemExtent,
Widget? prototypeItem,
bool addAutomaticKeepAlives = true,
bool addRepaintBoundaries = true,
bool addSemanticIndexes = true,
double? cacheExtent,
List<Widget> children = const <Widget>[],
int? semanticChildCount,
DragStartBehavior dragStartBehavior = DragStartBehavior.start,
ScrollViewKeyboardDismissBehavior keyboardDismissBehavior = ScrollViewKeyboardDismissBehavior.manual,
String? restorationId,
Clip clipBehavior = Clip.hardEdge}
)
```
Here is a table of the parameters for the `ListView` widget:

| Parameter | Description | Example |
| --- | --- | --- |
| `key` | A key to identify the widget | `key: Key('my-list-view')` |
| `scrollDirection` | The direction in which the list scrolls. Can be either `Axis.horizontal` or `Axis.vertical`. | `scrollDirection: Axis.horizontal` |
| `reverse` | Whether the list should scroll in the opposite direction of the `scrollDirection`. | `reverse: true` |
| `controller` | A scroll controller to use for the list. This can be used to control the scroll position of the list, and to listen for scroll events. | `controller: _scrollController` |
| `primary` | Whether this is the primary scroll view associated with the parent \`PrimaryScrollController |  |
| `physics` | The physics to use for the scroll view. This controls the way the list scrolls. | `physics: BouncingScrollPhysics()` |
| `shrinkWrap` | Whether the list should shrink its size to only the size of its children. If this is true, the `itemExtent` parameter will be ignored. | `shrinkWrap: true` |
| `padding` | The padding to add around the list. | `padding: EdgeInsets.all(8.0)` |
| `itemExtent` | The height of each list item. This can be used to create a more efficient scrolling experience by specifying a fixed item size. | `itemExtent: 50.0` |
| `prototypeItem` | A prototype widget to use for creating list items. This can be used to create a more efficient scrolling experience by creating list items with a fixed size and shape. | `prototypeItem: Text('Hello World')` |
| `addAutomaticKeepAlives` | Whether to wrap each child in an `AutomaticKeepAlive` widget. This can be used |
| `addRepaintBoundaries` | Whether to wrap each child in a `RepaintBoundary` widget. This can help improve the performance of scrolling by reducing the number of widgets that need to be repainted. | `addRepaintBoundaries: true` |
| `addSemanticIndexes` | Whether to assign semantic indexes to each child. This can be used to improve the accessibility of the list. | \`addSemanticIndexes` |
| `cacheExtent` | The amount of the list to cache. This can be used to improve the performance of scrolling by keeping more list items in memory. | `cacheExtent: 100.0` |
| `children` | The widgets to display in the list. | `children: <Widget>[Text('Item 1'), Text('Item 2')]` |
| `semanticChildCount` | The number of children that have semantic meaning. This can be used to improve the accessibility of the list. | `semanticChildCount: 2` |
| `dragStartBehavior` | The behavior when a drag starts. Can be either `DragStartBehavior.start` or `DragStartBehavior.down`. | `dragStartBehavior: DragStartBehavior.down` |
| `keyboardDismissBehavior` | The behavior when the user dismisses the keyboard. Can be either `ScrollViewKeyboardDismissBehavior.manual` or `ScrollViewKeyboardDismissBehavior.onDrag`. | `keyboardDismissBehavior: ScrollViewKeyboardDismissBehavior.onDrag` |
| `restorationId` | An ID that can be used to restore the scroll position when the app is restored. | `restorationId: 'my-list-view'` |
| `clipBehavior` | How to clip the widgets that overflow the parent widget. Can be either `Clip.none`, `Clip.hardEdge`, or `Clip.antiAlias`. | `clipBehavior: Clip.antiAlias` |
  
  ```dart
  ListView(
  scrollDirection: Axis.vertical,
  reverse: true,
  controller: _scrollController,
  primary: true,
  physics: BouncingScrollPhysics(),
  shrinkWrap: true,
  padding: EdgeInsets.all(8.0),
  itemExtent: 50.0,
  prototypeItem: Text('Hello World'),
  addAutomaticKeepAlives: true,
  addRepaintBoundaries: true,
  addSemanticIndexes: true,
  cacheExtent: 100.0,
  children: <Widget>[
    Text('Item 1'),
    Text('Item 2'),
    Text('Item 3'),
  ],
  semanticChildCount: 3,
  dragStartBehavior: DragStartBehavior.down,
  keyboardDismissBehavior: ScrollViewKeyboardDismissBehavior.onDrag,
  restorationId: 'my-list-view',
  clipBehavior: Clip.hardEdge,
)
```
