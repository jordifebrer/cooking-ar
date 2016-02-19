###sort
Returns the enum sorted

###sort_by
Sorts an enum mapping values with the given block

```ruby
# Sort alphabetically ASC
%w(Dundee Aberdeen Glasgow Edinburgh).sort
=> ["Aberdeen", "Dundee", "Edinburgh", "Glasgow"]

# Sort alphabetically DESC
%w(Dundee Aberdeen Glasgow Edinburgh).sort { |a, b| b <=> a }
=> ["Glasgow", "Edinburgh", "Dundee", "Aberdeen"]

# Sort by word length ASC
%w(Dundee Aberdeen Glasgow Edinburgh).sort_by { |word| word.length }
=> ["Dundee", "Glasgow", "Aberdeen", "Edinburgh"]

# Sort by word length DESC
%w(Dundee Aberdeen Glasgow Edinburgh).sort { |a, b| b.length <=> a.length }
=> ["Edinburgh", "Aberdeen", "Glasgow", "Dundee"]
```
