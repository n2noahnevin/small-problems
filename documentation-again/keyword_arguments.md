# Keyword Arguments

**What does this code print?**

```ruby
5.step(to: 10, by: 3) { |value| puts value }
```

---

The `Numeric#step` method will invoke the given block with the sequence of numbers starting at in this case 5, each time increasing by 3, until 10 has been reached. This code will print:

```ruby
5
8
```

