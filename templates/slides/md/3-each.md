###each
Simple way to loop an enum

```ruby
(1..3).each { |i| puts ">> #{i}" }
>> 1
>> 2
>> 3
=> 1..3

without block you'll get an Enumerator
e = (1..3).each

e.next
=> 1

e.next
=> 2

e.next
=> 3
```
