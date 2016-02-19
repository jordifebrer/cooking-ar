###grep
Returns an array with every element of the enum that matches with the pattern

```ruby
(1..5).grep 1..100
=> [1, 2, 3, 4, 5]

(1..5).grep 3..4
=> [3, 4]

["one", "two", "three", "four"].grep(/o/)
=> ["one", "two", "four"]

["one", "two", "three", "four"].grep(/o/) do |num|
  num.upcase
end
=> ["ONE", "TWO", "FOUR"]
```
