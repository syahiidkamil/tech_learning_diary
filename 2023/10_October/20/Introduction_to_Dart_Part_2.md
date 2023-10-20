
# Learning Diary: Dart Programming Language
## Date: October 20, 2023
## Author: Syahiid Nur Kamil

---

### Variables and Data Types

#### What is Dart?

Dart is a modern programming language designed for both server and browser. It's statically typed and object-oriented, and it's the language behind Flutter, Google's UI toolkit for building natively compiled applications for mobile, web, and desktop from a single codebase.

#### Variables

In Dart, you declare variables using the `var` keyword, but you can also specify the type.

```dart
var name = 'John';  // Inferred as String
String surname = 'Doe';
```

#### Data Types

Dart has several built-in data types:

- `int` for integers
- `double` for floating-point numbers
- `String` for strings
- `bool` for Boolean values
- `List` for lists (arrays)
- `Map` for key-value pairs
- `Set` for unique collections

```dart
int age = 30;
double pi = 3.14159;
bool isTrue = false;
List<int> numbers = [1, 2, 3];
Map<String, int> data = {'apple': 1, 'banana': 2};
Set<int> uniqueNumbers = {1, 2, 3};
```

#### Const and Final

You can use `const` and `final` to declare variables that can't be changed.

- `final`: Can't be changed once assigned.
- `const`: Can't be changed and must be assigned a compile-time constant.

```dart
final name = 'John';
const pi = 3.14159;
```

const and final serve different purposes even though both imply immutability. The const keyword signifies that the variable's value is a compile-time constant. It's not just immutable; it's eternally unchangeable. On the other hand, final means the variable can't be reassigned once it has been initialized, but its value can be determined at runtime. This distinction becomes crucial when optimizing code, especially in the context of Flutter, where using const for widgets can enhance performance by avoiding unnecessary rebuilds. In essence, const can make your code more efficient, while final offers flexibility with immutability.

in official documentation it's stated that `Use const constructors on widgets as much as possible, since they allow Flutter to short-circuit most of the rebuild work. To be automatically reminded to use const when possible, enable the recommended lints from the flutter_lints package` (https://docs.flutter.dev/perf/best-practices)

---

### Basic Control Flow

#### If-Else Statements

Use `if`, `else if`, and `else` to make decisions in your code.

```dart
if (age > 18) {
  print('Adult');
} else if (age > 12) {
  print('Teenager');
} else {
  print('Child');
}
```

#### Switch-Case

For multiple conditions, you can use `switch-case`.

```dart
switch (grade) {
  case 'A':
    print('Excellent');
    break;
  case 'B':
    print('Good');
    break;
  default:
    print('Invalid grade');
}
```

#### Loops

For repetitive tasks, you can use loops like `for`, `while`, and `do-while`.

```dart
for (var i = 0; i < 3; i++) {
  print('Hello');
}

while (condition) {
  // code
}

do {
  // code
} while (condition);
```

---

### Functions and Scope

#### Defining Functions

In Dart, you can define functions using the `void` keyword if the function doesn't return anything, or specify the return type.

```dart
void greet() {
  print('Hello, world');
}

String greetWithName(String name) {
  return 'Hello, $name';
}
```

#### Anonymous Functions

You can also define anonymous functions (also called lambda functions).

```dart
var add = (a, b) => a + b;
```

#### Optional and Named Parameters

Dart allows functions to have optional positional, optional named, and optional default parameters.

```dart
void displayInfo(String name, [int age]) {
  // age is optional
}

void displayData({String name, int age}) {
  // Both are optional and named
}

void display(String name, {int age = 18}) {
  // age is optional and has a default value
}
```

---

### Reflections

Today, I've covered the basics of Dart, including variables, data types, control flow, and functions. These are the building blocks of any Dart application. My understanding of these concepts is solid, and I'm looking forward to diving deeper into more advanced topics.

### Next Steps

- Explore collections like List, Set, and Map.
- Dive into Object-Oriented Programming concepts.

---

