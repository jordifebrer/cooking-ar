###max_by

returns max value from enum

###min_by

returns min value from enum

```ruby
reviews = [
  {id: 1, name: "sushi", stars: 4.0},
  {id: 2, name: "ramen", stars: 5.0},
  {id: 3, name: "takoyaki", stars: 3.5},
  {id: 1, name: "sushi", stars: 5.0},
]

reviews.max_by {|review| review[:stars]}
=> {:id=>2, :name=>"ramen", :stars=>5.0}

# ruby >= 2.2.0
# reviews.max_by(2) {|review| review[:stars]}
#=> [{:id=>2, :name=>"ramen", :stars=>5.0}, {:id=>2, :name=>"ramen", :stars=>5.0}, {:id=>3, :name=>"takoyaki", :stars=>3.5}, {:id=>1, :name=>"sushi", :stars=>5.0}]

grouped_reviews.fetch("sushi").max_by {|r| r[:stars]}
=> {:id=>1, :name=>"sushi", :stars=>5.0}

reviews.min_by {|review| review[:stars]}
=> {id: 3, name: "takoyaki", stars: 3.5}

```




