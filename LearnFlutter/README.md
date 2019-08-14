**setState()** is called when theme or **MediaQuery** has changed, **MediaQuery** also holds the information about **viewInset**

We use **builder** when we want to build Widget dynamically

## const constructor & const widget

**const constructor** - if a class have this type of constructor, the instance that is created from class will be unchangeable, use to notice that all properties of this instance is **final** (means can not change it)

We do not use Widget objects like normal objects, we use them to pass onto the **Widget Tree**

When the **build()** method runs, all the widgets of Widget tree are placed, not be changed

If we know data pass to Widget will never be changed, we can use **const** before that Widget in **WidgetTree Code**, we use that to tell Flutter **doesn't need to rebuild this Widget anymore**

By this way, we can improve the performance of our apps with tiny changes

## Good Code

Has two types
- **Readability / Understandability**
- **Performace** 

If MediaQuery content usually changes, you should put it into separate Widget to **prevent recall build()** method as much as possible

Attention that **MediaQuery** 's **type** is **MediaQueryData**

## Widget Lifecycle

With **Stateful Widget** **initState** is implemented by **State Class**

**didUpdateWidget** method have **oldWidget** argument - it's a previous Widget, this method is called when Widget changes

**dispose()** is called when Widget is destroyed, so we use it to clean up data, listener, life connection

Image for **Widget lifecycle**

<img src="https://user-images.githubusercontent.com/43769314/62992786-d4205400-be8f-11e9-8b60-c9e2ab434e25.png" width="720">

**initState()** is often used for fetching some initial data you need in your app, is called before **build()** so do not use **setState** in **initState**

**didUpdateWidget()** is not usually used, we use it if we know something changed in parent widget and we need to refetch data in our state

## App lifecycle

<img src="https://user-images.githubusercontent.com/43769314/62996237-ea81dc00-be9e-11e9-88ff-846fb44d7b10.png" width="720">

**Mix-in** not the same as extends, you can use some methods or properties from another class (not all) - the other way for **multiple inherrit** (same with **ruby**)

**didChangeAppLifecycleState** is called when lifecycle state changes

## Understanding context

**MediaQuery** and **Theme** use **InheritedWidget** behind the scenes
context knows about the general structure of widget tree, so it can directly access any other widget without passing data through arguments

Flutter uses **InheritedWidget** to get data of **MediaQuery** and **Theme** it useful for Flutter establish behind the scenes channel to exchange data between widgets in **Widget Tree**

## About key in Flutter

Every Widget in Flutter has a key

We need key when this is **topmost** - **stateful** item of list

We use **super()** to instantiating the parent class if we want to pass extra data to parent class
Key makes Flutter identify widget easier

With **StatefulWidget** state object is attached to Element **not Widget**

## GridView

Sliver in Flutter are really just scrollable areas on the screen
**gridDelagate** takes care about structuring, layouting the grid

## Navigation in Flutter Apps

Pages are managed as a Stack, Top-most Page is visible. So we can **pushing** or **poping** page
- Push: when navigate to new page
- Pop: when get out of page

<img src="https://user-images.githubusercontent.com/43769314/63011230-dfd93e00-bec2-11e9-9b81-0a3e5f453228.png" width="720">