# Dart Class Wrapper

Wrapper for a simplified partial mocking in Unit Tests.


## Getting started

Initialization
```dart
// Support a list of classes
@GenerateWithMethodSetters([AppData])
import 'file_test_name.wrapper.dart';

void main() {
  group('Validate ....', () {
    setUp(() => mock = WrapperAppData());

    test('If ... Then ...', () {
      // Original method `getStateDelta`
      mock.mockGetStateDelta = (a, b) => 123.0;
      // .... 
    });
  });
}
```

Execution
```console
# Cleanup autogenerated files
dart run build_runner clean
# Generate wrappers
dart run build_runner build --delete-conflicting-outputs
# Run tests
flutter test
```

In addition to thanking, you may [treat us to :coffee:](https://www.buymeacoffee.com/lyskouski).
