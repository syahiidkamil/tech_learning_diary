
# Learning Diary: Dart Programming Language

## Date: October 20, 2023

## Author: Syahiid Nur Kamil

---

### What I Learned Today

Today, I delved deep into Dart, focusing on Handling Exceptions and Asynchronous Programming.

#### Handling Exceptions

Understanding how to handle exceptions is crucial for writing robust software. Dart provides multiple ways to catch and handle errors that might occur during execution.

##### Try-Catch Block

The `try-catch` block is the most straightforward way to handle exceptions. Here's a simple example:

```dart
try {
  // Code that might throw an exception
} catch (e) {
  // Handle the exception
}
```

##### Throw

You can also throw exceptions manually using the `throw` keyword.

```dart
throw FormatException('This is a custom exception');
```

##### Finally

The `finally` clause is executed whether an exception is thrown or not.

```dart
try {
  // Code that might throw an exception
} catch (e) {
  // Handle the exception
} finally {
  // This block will always execute
}
```

#### Asynchronous Programming in Dart

Asynchronous programming is essential for performing time-consuming computations without freezing the application. Dart uses `Future` and `async-await` for this.

##### Future

A `Future` represents a potential value that will be available at some time in the future.

```dart
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  return 'Data fetched';
}
```

##### Async-Await

The `async` and `await` modifiers are used often with `Future`. The `await` keyword will pause code execution until the `Future` is resolved.

```dart
void main() async {
  String data = await fetchData();
  print(data);  // Output: Data fetched
}
```

##### Streams

A `Stream` is a sequence of asynchronous events. Streams are similar to `Future`, but instead of returning a single value, a `Stream` can yield multiple values over time.

```dart
Stream<int> countStream(int to) async* {
  for (int i = 1; i <= to; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i;
  }
}
```

### Final Thoughts

Understanding how to properly handle exceptions and utilize asynchronous programming constructs in Dart is fundamental for building resilient and responsive applications. The language provides multiple tools for error-handling and async operations, making it highly flexible for different kinds of projects.

---

