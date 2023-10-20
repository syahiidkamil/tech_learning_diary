
# Learning Diary: Dart Programming Language

## Date: October 20, 2023

## Author: Syahiid Nur Kamil

---

### What I Learned Today

Today, I focused on an essential paradigm in Dart: Object-Oriented Programming (OOP). OOP is crucial for writing clean, modular, and maintainable code. Below are the topics I explored:

#### Class Definitions and Constructors

In Dart, a class serves as a blueprint for creating objects. A class encapsulates data and methods that manipulate the data.

```dart
class Dog {
  String name;
  int age;
  
  // Constructor
  Dog(this.name, this.age);
}
```

#### Inheritance

Inheritance allows a class (subclass) to use properties and methods of another class (superclass).

```dart
class Animal {
  void breathe() {
    print('Breathing...');
  }
}

class Dog extends Animal {
  void bark() {
    print('Woof Woof');
  }
}
```

#### Polymorphism

Polymorphism in Dart allows a subclass to provide a specific implementation of a function that is already provided by its superclass.

```dart
class Animal {
  void makeSound() {
    print('Making animal sounds');
  }
}

class Dog extends Animal {
  @override
  void makeSound() {
    print('Woof Woof');
  }
}
```

#### Encapsulation

Encapsulation is used to restrict access to certain variables and methods, increasing the flexibility and maintainability of code.

```dart
class Rectangle {
  double _width; // private variable
  double _height; // private variable

  // Setter method
  setWidth(double w) {
    _width = w;
  }

  // Getter method
  double getWidth() {
    return _width;
  }
}
```

#### Getters and Setters

In Dart, you can use getters and setters to control the access and modification of an object's properties.

```dart
class Circle {
  double _radius;

  // Getter
  double get radius => _radius;

  // Setter
  set radius(double value) => _radius = value;
}
```

Today's learning journey has given me a deep understanding of Object-Oriented Programming in Dart. These OOP concepts are critical for building complex, scalable applications.

#### More on Constructors

Dart offers various types of constructors to initialize your objects.

##### Default Constructor

A default constructor has no arguments and serves to initialize variables to their default values.

```dart
class Student {
  String name;
  int age;
  
  Student() {
    name = "Unnamed";
    age = 0;
  }
}
```

##### Parameterized Constructor

A constructor that accepts parameters to initialize the object.

```dart
class Student {
  String name;
  int age;
  
  Student(this.name, this.age);
}
```

##### Named Constructors

Dart allows named constructors to enable multiple constructors for a single class.

```dart
class Point {
  double x, y;
  
  Point(this.x, this.y);
  
  // Named constructor
  Point.origin() {
    x = 0;
    y = 0;
  }
}
```

##### Constant Constructors

If you never intend to change an object, make it a constant with a const constructor.

```dart
class ImmutablePoint {
  final double x, y;
  const ImmutablePoint(this.x, this.y);
}

var origin = const ImmutablePoint(0, 0);
```

##### Factory Constructors

Factory constructors allow you to return an object from a constructor.

```dart
class Logger {
  final String name;
  static final Map<String, Logger> _cache = <String, Logger>{};
  
  factory Logger(String name) {
    return _cache.putIfAbsent(name, () => Logger._internal(name));
  }
  
  Logger._internal(this.name);
}
```

With these constructor types, Dart provides a flexible way to initialize objects according to different requirements.
