## Dart Basic Note

- The same syntax like Java. OOP Language
- Everything in dart is object
- Although Dart is strongly typed, type annotations are optional because Dart can infer types
- Unlike Java, Dart doesn’t have the keywords **public**, **protected**, and **private**.
- If an identifier starts with an underscore (_), it’s private to its library
- Uninitialized variables have an initial value of null. Even variables with numeric types are initially null, because numbers—like everything else in Dart—are objects.
- Variables store references
- If an object isn’t restricted to a single type, specify the **Object** or **dynamic** type
- **@override** provided by Dart
- In Dart we have **Map** (same with **object** in **javascript**)
- Same with Java, Dart also has constructor for class which is the special function (method) has the same name with class name.
- **null** value in Dart - used in uninitialized state
- Dart **doesn’t allow** constant variable at **class level**, but it can be if variable is a **static variable**

```dart
dynamic name ='Bob';
String name = 'Bob';
```

- **final** and **const** are used to declare constant variables
  - **final** variable can be set only once
  - **const** is used with **compile-time constant**
  - **const** is implicitly **final**

## Asynchrony support
- Attention to **Future** object
- A Future is used to represent a potential value, or error, that will be available at some time in the future. Receivers of a Future can register callbacks that handle the value or error once it is available (the same with promise in javascript)

```dart
Future<int> future = getFuture();
future.then((value) => handleValue(value))
      .catchError((error) => handleError(error));
```

**Future.then(() {});** the function that we passed to **then()** will be stored in memory until Future value is available

- Have **async**, **await** to write **asynchronous code** just like **synchronous code**

## Anonymous functions

- Same with javascript
- Can be assigned to a variable
- NO NAMED

## Lexical scope

- Scope is defined statically
- We can *follow the curly braces outwards*

## Lexical closures

- A closure is a function object that has access to variables in its lexical scope, even when the function is used outside of its original scope.

```dart
Function makeAdder(num addBy) {
  return (num i) => addBy + i;
}
```

## Functions

- Functions in dart are objects too, so it can be returned or passed as arguments to the another functions.
- type: **Function*
