###all?
Returns true if it's never false or nil

###any?
Return true if at least one returns true

Example:

```ruby
reviews = [
  {id: 1, name: "sushi", stars: 4.0},
  {id: 2, name: "ramen", stars: 5.0},
  {id: 3, name: "takoyaki", stars: 3.5},
  {id: 1, name: "sushi", stars: 5.0},
]

reviews.all? { |review| review[:stars] >= 4 }
=> false

reviews.any? { |review| review[:stars] > 4 }
=> true
```
