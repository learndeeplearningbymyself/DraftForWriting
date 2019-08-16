## Named Routes

- Just like a route system in web app
- In a bigger app, it can be easier to manage because you have a list of available routes
- Make your app become more cleaner
- We will use **pushNamed** instead of **push** in this case

home (in MaterialApp) **always also has an automatically named route** which is just slash **(/)**
- **onGenerateRoute** is reached if you are going to a named route with **pushNamed**, that is not registered in the routes table, usually used in highly dynamic application, the function that you pass to it should return a **Route**
- **onUnknownRoute** is reached when Flutter failed to build a screen with all other measures so if you don't use **onGenerateRoute**, before throwing an error, Flutter will try to use **onUnknownRoute** to show something on the screen (same as 404 page of website)

## ClipRRect

Use other widget as a child and force it into a certain form

## Tab Screen

**DefaultTabController** and **TabBar** here are automatically connected by Flutter behind the scenes, so **DefaultTabController** will automatically detect which tab you selected and then show the right content for that tab. Content is passed to **TabBarView** - this is used for **Default Tab Bar**

The way you add **Tab** is the **same** with you add **Screen**

But if you want to use **Bottom Tab Bar**, don't need to use **DefaultTabController** or **TabBarView**, just using **bottomNavigationBar** property of **Scaffold**, very easy

## Drawer

Backdrop is behind Drawer

**context** is globally in **State class** but not in **initState**, because it is runned before **build**, too early

**didChangeDependencies** is called when state change in here we can tap into context

## Tips & Tricks

Passing data via constructors can be **cumbersome** and **dificult**

## State & State Management

State = Data which affects the UI. We have two kinds of state
- App-wide State: affect entire app, authenticated
- Widget (local) State - affects only a widget on its own, Form Input

<img src="https://user-images.githubusercontent.com/43769314/63145818-ce637380-c033-11e9-8488-1fc76d6f74ab.png" width="720">

We can do this

```dart
Provider.of(context)
```

to set up a direct communication channel behind the scenes