Generic Dart Utilities, made specifically to support multiple Moontree repos.

## Example

```dart
//import 'package:moontree_utils/moontree_utils.dart'; // everything
//import 'package:moontree_utils/extensions/extensions.dart'; // all extensions
import 'package:moontree_utils/extensions/int.dart'; 
import 'package:moontree_utils/src/mixins.dart' show ToStringMixin;
import 'package:moontree_utils/src/list.dart' show range;

class Example with ToStringMixin {
  final String symbol;

  Example(this.symbol);

  @override
  List<Object?> get props => <Object?>[symbol];

  @override
  List<String> get propNames => ['symbol'];

  void example() {
    for (var i in range(100, start: 999)) {
      print(i.toCommaString()); // 999 1,000 1,001 ... 1,099 
    }
  }
}
```
