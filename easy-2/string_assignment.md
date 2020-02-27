# String Assignment

**Take a look at the following code:**

```ruby
name = 'Bob'
save_name = name
name = 'Alice'
puts name, save_name
```

**What does this code print out? Think about it for a moment before continuing.**

**If you said that code printed**

```ruby
Alice
Bob
```

**you are 100% correct, and the answer should come as no surprise. Now, let's look at something a bit different:**

```ruby
name = 'Bob'
save_name = name
name.upcase!
puts name, save_name
```

**What does this print out? Can you explain these results?**

---

The variable `name` is set equal to the string `'Bob'`, and then the variable `save_name` is set equal to `name`. This means they both reference the same memory location. `name.upcase!` is a destructive method that will alter `name`, and any other variables that point to `name`. Therefore, `save_name` will *also* be altered, and both variables will `puts` BOB.