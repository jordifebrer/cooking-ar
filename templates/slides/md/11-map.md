###map
Returns a new array as a result of aplying the block to every element.

```ruby
> cities = %w(Dundee Aberdeen Glasgow Edinburgh)
=> ["Dundee", "Aberdeen", "Glasgow", "Edinburgh"]

> cities.map { |word| word.length }
=> [6, 8, 7, 9]

# Doesn't change the original object
> cities.map { |word| word.upcase }
=> ["DUNDEE", "ABERDEEN", "GLASGOW", "EDINBURGH"]

> cities
=> ["Dundee", "Aberdeen", "Glasgow", "Edinburgh"]

# Changes the original object
> cities.map! { |word| word.upcase }
=> ["DUNDEE", "ABERDEEN", "GLASGOW", "EDINBURGH"]

> cities
=> ["DUNDEE", "ABERDEEN", "GLASGOW", "EDINBURGH"]
```
