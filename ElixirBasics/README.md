## Elixir Basic

### Data types in Elixir

- tuple: Elixir uses curly brackets to define tuple, just like a list, tuple can hold any value

```elixir
{:ok, "hello"}
# :ok - the atom data type, same as the symbol of ruby
```

- list: List is stored in memory like a linked list, each element of list holds its value and points to the following element until reaches the end of the list

```elixir
list = [1, 2, 3]
```

- map: In elixir **map** is same with hash in ruby

```elixir
map = %{a: 1, b: 2}
```

- struct: Struct is extension of map, with struct we can define default value for each properties

```elixir
defmodule User do
    defstruct name: "John", age: 27
end
```

### Everything is module

- Below is the syntax is used to define module

```elixir

```