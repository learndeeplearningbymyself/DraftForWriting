**FittedBox** forces its childs to available space

In **Flexible Widget** we have **fit** property and **FlexFit** enum
**FlexFit** enum has two values:
- **loose** - take as much space as fit it childs
- **tight** - it only takes as much space as fits in there without squeezing any items off the screen, so we will not see black/ yellow warning marker. If we use **flex** property (default value is 1), the value of flex notices us that this Widget will take ~ part amongs **tight** elements

We also have **Expanded** Widget, it sames with **Flexible** that has **fit: FlexFit.tight**

**ListTile** widget often is used in conjunction with lists but you don't have to use it in conjuction
- ListTile - leading: first widget

In state class of **StatefulWidget** we have **global context object**

In **Theme** we have default **errorColor is red**

## Responsive & Adaptive UIs

Adaptive means you adapting your UI with different OS(s)

<img src="https://user-images.githubusercontent.com/43769314/62917624-ef2f8d00-bdd7-11e9-8f1f-45a44a8121e4.png" width="720">

By One Codebase, One Widget Tree, depending on platform, we create different Sub-Trees / Widget (for iOS and Android)

## Constraints

Define how a widget is rendered on the screen, set by height, width
If you don't set it, default values will be used by Flutter

<img src="https://user-images.githubusercontent.com/43769314/62920860-e8a61300-bde1-11e9-9d29-f0f92ed2453e.png" width="720">

Don't use **{}** in *if inside of a list* syntax

```dart
if (condition) handle
```