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

Do not confuse between **Map** and **Object** in Dart. In Dart **Object** is the instance of the class

## Mixin and Class

With **mixin** you can share properties or methods but less of a strong connection, just like utility functions provider

```dart
mixin Agility {
   var speed = 10;
  
  void sitDown() {
    print('Sitting down...');
  }
}

class Mammal {
  void breathe() {
    print('Breathe in ... Breathe out ...');
  }
}

class Person extends Mammal with Agility {
  String name;
  int age;
  
  Person(this.name, this.age);
}

void main() {
  final pers = Person('Max', 30);
  print(pers.name);
  
  pers.breathe();
  pers.sitDown();
  print(pers.speed);
}
```

## Deep Dive With Future

Basically in Dart **Future is a generic type**

```dart
Future<Type>
```

**catchError** will catch all errors **before it not after it**

```dart
void main() {
  var result = 1 + 1; // this is available immediately

  var myFuture = Future(() {
     return 'Hello';
  }); // not stop dart code executing until this Future job done
  
  print('This runs first!');
  myFuture
    .then((result) => print(result))
    .then((_) {
      print('After first then!');
    })
    .catchError((err) {
      print(err);
    });
  print('This also runs before the future is done!');
}
```

If we use **async** key word, all the code inside a function will be automatically wrapped by the **Future**

```dart
Future<void> functionName(params) async {
  // code inside here are automatically wrapped by Future object, so we do not need to use return keyword here
}
```

**..** notation will not return result the of method is used with it, it will return the result of method before

```dart
Matrix4.rotationZ(-8 * pi / 180)
  ..translate(-10.0), // return the result of rotationZ not translate
```

**try**, **catch**, **on** - with **on** we can specify exactly **what type of error**

```dart
try {
  // code
} on HttpException catch (error) {
  // handle error
}
```
