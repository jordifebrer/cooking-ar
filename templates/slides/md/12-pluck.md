###pluck
Select attribute/s returning the result to an array

```sh
rails generate model FootballTeam name: string
rake db:migrate
rails c
```

```ruby
> FootballTeam.create(name: "Hibernian F.C.")
> FootballTeam.create(name: "Heart of Midlothian F.C.")
> FootballTeam.create(name: "F.C. Barcelona")

> FootballTeam.all.pluck(:name)
=> ["Hibernian F.C.", "Heart of Midlothian F.C.", "F.C. Barcelona"]

> FootballTeam.all.pluck(:id)
=> [1, 2, 3]

> FootballTeam.all.pluck(:id, :name)
=> [[1, "Hibernian F.C."], [2, "Heart of Midlothian F.C."], [3, "F.C. Barcelona"]]
```
