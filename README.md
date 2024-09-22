# fading_edge_scrollview

Package providing FadingEdgeScrollView which allows you to build scrollable views with fading edges

## Usage

Create scrollable view with fading edges by wrapping yout widget in `FadingEdgeScrollView`

```dart
FadingEdgeScrollView(
  child: yourWidget,
)
```

additional constructor parameters are:
* `gradientFractionOnStart` and `gradientFractionOnEnd` - double values from 0 to 1, telling how big fade should be on start and end parts of child widget. Default values are 0.1
* `parametersIfChildTypeUnknown` should be set if child does not extend ScrollView, SingleChildScrollView, AnimatedList, PageView or ListWheelScrollView. Otherwise, it is ignored

View passed as child **MUST** have `controller` set. 

See documentation and example folder for more information

## Migration to version 5

Change all calls to `FadingEdgeScrollView.fromSomeWidget` to `FadingEdgeScrollView`

## Breaking change in version 4.0.0

Field `shouldDisposeScrollController` was removed. I was not realizing how widgets should work when I added it.
If you were using it - move `scrollController` creation and disposal to some `StatefulWidget`.

## Demo

Click to see on Youtube:  
[![ListView with images demo](https://img.youtube.com/vi/71pDlfC9pxU/0.jpg)](https://www.youtube.com/watch?v=71pDlfC9pxU "ListView with images demo")
[![ListView demo](https://img.youtube.com/vi/2kNr3fW0nP8/0.jpg)](https://www.youtube.com/watch?v=2kNr3fW0nP8 "ListView demo")
[![PageView demo](https://img.youtube.com/vi/6nZhJXVwkvU/0.jpg)](https://www.youtube.com/watch?v=6nZhJXVwkvU "PageView demo")
[![SingleChildScrollView demo](https://img.youtube.com/vi/0CJKyvr7fT4/0.jpg)](https://www.youtube.com/watch?v=0CJKyvr7fT4 "SingleChildScrollView demo")
