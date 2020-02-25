# Optional Arguments Redux

**Assume you have the following code:**

```ruby
require 'date'

puts Date.new
puts Date.new(2016)
puts Date.new(2016, 5)
puts Date.new(2016, 5, 13)
```

**What will each of the 4 `puts` statements print?**

---

The first statement, `puts Date.new`, will print a new Date object to the screen with the first date of the Julian calendar. 

```ruby
puts Date.new
#=> #<Date: -4712-01-01>
```

The second statement, `puts Date.new(2016)`, will print a new Date object with the year 2016, and the month and day the default values.

```ruby
puts Date.new(2016)
#=> #<Date: 2016-01-01>
```

The third statement, `puts Date.new(2016, 5)`, will print a new Date object with the year 2016 and the month 5, and the day being the default value.

```ruby
puts Date.new(2016, 5)
#=> #<Date: 2016-05-01>
```

The final statement, `puts Date.new(2016, 5, 13)`, prints a new Date object with the year 2016, the month 5, and the day 13.

```ruby
puts Date.new(2016, 5, 13)
#=> #<Date: 2016-05-13>
```



