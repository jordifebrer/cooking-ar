###select

returns all the elements from the enum that returns true to the given block

###reject

returns all the elements from the enum that returns false to the given block

```ruby
(1..3).select { |i| i<3  }
=> [1, 2]

(1..3).reject { |i| i<3  }
=> [3]
```
