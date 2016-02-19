###group_by

Groups the collection by result of the block

Examples:

```ruby
(1..10).group_by { |i| i % 5 }
=> {1=>[1, 6], 2=>[2, 7], 3=>[3, 8], 4=>[4, 9], 0=>[5, 10]}
```

```ruby
reviews = [
  {id: 1, name: "sushi", stars: 4.0},
  {id: 2, name: "ramen", stars: 5.0},
  {id: 3, name: "takoyaki", stars: 3.5},
  {id: 1, name: "sushi", stars: 5.0},
]

grouped_reviews = reviews.group_by { |review| review[:name] }
grouped_reviews.fetch("sushi")
=> [
  {:id=>1, :name=>"sushi", :stars=>4.0},
  {:id=>1, :name=>"sushi", :stars=>5.0}
]
```
