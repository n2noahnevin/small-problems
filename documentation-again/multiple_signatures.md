# Multiple Signatures

**What do each of these `puts` statements output?**

```ruby
a = %w(a b c d e)
puts a.fetch(7)
puts a.fetch(7, 'beats me')
puts a.fetch(7) { |index| index**2 }
```

---

`Array#fetch`, as seen in the Ruby Docs, is a method that takes returns the element at position `index`, its first argument. A second argument given signifies a default value to give in the `index` is outside array bounds. A block can also be given as an argument, but it will only be executed when an invalid `index` is given.

1. ```ruby
   puts a.fetch(7)
   #=> IndexError exception
   ```

2. ```ruby
   puts a.fetch(7, 'beats me')
   #=> beats me
   ```

3. ```ruby
   puts a.fetch(7) { |index| index**2 }
   #=> 49
   ```

