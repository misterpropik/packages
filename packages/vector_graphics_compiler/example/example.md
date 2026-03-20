`vector_graphics_compiler` compiles SVG files into an optimized binary format
at build time using Flutter's [asset transformer](https://docs.flutter.dev/ui/assets/asset-transformation) system.

## Setup

Declare your SVG asset with the transformer in `pubspec.yaml`:

```yaml
flutter:
  assets:
    - path: assets/my_icon.svg
      transformers:
        - package: vector_graphics_compiler
```

## Usage

Load the pre-compiled asset with `AssetBytesLoader` from
[`package:vector_graphics`](https://pub.dev/packages/vector_graphics):

```dart
import 'package:vector_graphics/vector_graphics.dart';

final Widget icon = VectorGraphic(
  loader: AssetBytesLoader('assets/my_icon.svg'),
);
```

See the [example app](https://github.com/flutter/packages/tree/main/packages/vector_graphics_compiler/example)
for a complete runnable demo.
