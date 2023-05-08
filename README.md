# Flutter We Slide

The inspiration behind the package was actually a need for a slide transition like spotify (iOS) Unfortunately, I couldn’t find any efficient package, so I literally banged my fist on the table, rolled up my sleeves and created my own solution. Through this package I could better understand some principles of flutter animation :)

## Installation

Add this to your package's pubspec.yaml file:

   ```
   dependencies:
  we_slide: ^2.4.0
   ```

## Basic Example

   ```
   import 'package:we_slide/we_slide.dart';

final _colorScheme = Theme.of(context).colorScheme;
final double _panelMinSize = 70.0;
final double _panelMaxSize = MediaQuery.of(context).size.height / 2;
return Scaffold(
  backgroundColor: Colors.black,
  body: WeSlide(
    panelMinSize: _panelMinSize,
    panelMaxSize: _panelMaxSize,
    body: Container(
      color: _colorScheme.background,
      child: Center(child: Text("This is the body 💪")),
    ),
    panel: Container(
      color: _colorScheme.primary,
      child: Center(child: Text("This is the panel 😊")),
    ),
    panelHeader: Container(
      height: _panelMinSize,
      color: _colorScheme.secondary,
      child: Center(child: Text("Slide to Up ☝️")),
    ),
  ),
);
   ```
