# Included Modules

**Use irb to run the following code:**

```ruby
a = [5, 9, 3, 11]
puts a.min
```

**Find the documentation for the `#min` method and change the above code to print the two smallest values in the `Array`.**

---

`Array#min` can take an argument `n` that will return the minimum `n` elements as a new array. To print these two values, just `puts` out the members of this new array.

```ruby
a = [5, 9, 3, 11]
puts a.min(2)
```

This will print out:

```ruby
3
5
```

