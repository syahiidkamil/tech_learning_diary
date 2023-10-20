# Learning Diary: Dart Programming Language

## Date: October 20, 2023

## Author: Syahiid Nur Kamil

---

### What I Learned Today

Today, I delved deep into Dart, focusing on three main areas: Collections and Iterable Methods, Operators and Expressions

## Collections and Iterable Methods

### Collections

Dart offers robust built-in types for collections, such as List, Set, and Map.

#### List

A List is an ordered collection of items. It can be defined as follows:

```dart
var myList = [1, 2, 3];
```

#### Set

A Set is an unordered collection of unique items:

```dart
var mySet = Set.from([1, 2, 3, 4, 5]);
```

#### Map

A Map is an unordered collection of key-value pairs:

```dart
var myMap = {
  'name': 'John',
  'age': 30
};
```

### Iterable Methods

Dart collections come with a variety of methods for traversing, manipulating, and transforming the data.

- `forEach`: Apply a function to each element in the collection.
- `map`: Transform each element and create a new Iterable.
- `where`: Filter elements based on a condition.

```dart
var numbers = [1, 2, 3, 4];
var evenNumbers = numbers.where((n) => n % 2 == 0);
```

## Operators and Expressions

### Equality and Relational Operators

- `==`: Checks if two objects are equal.
- `!=`: Checks if two objects are not equal.
- `<`, `>`, `<=`, `>=`: Compare two values.

### Logical Operators

- `&&`: Logical AND
- `||`: Logical OR
- `!`: Logical NOT

```dart
if (a > b && b > c) {
  print("a is the largest number");
}
```

### Expressions

Expressions are combinations of variables, operators, and values that can be evaluated.

```dart
var sum = a + b;
var difference = a - b;
```
