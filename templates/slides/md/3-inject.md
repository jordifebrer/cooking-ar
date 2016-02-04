###inject

Runs a block once for each element of the list.

Examples:

```ruby
(1..5).inject { |sum, n| sum + n }
(1..5).inject(:+)
=> 15

(1..5).inject { |prod, n| prod * n }
(1..5).inject(:*)
=> 120
```

```ruby
def count_vowels(str)
  str.scan(/[aeoui]/i).count
end

%w{ Edinburgh Glasgow Aberdeen Dundee }.inject do |memo, word|
  count_vowels(memo) > count_vowels(word) ? memo : word
end
=> Aberdeen
```
