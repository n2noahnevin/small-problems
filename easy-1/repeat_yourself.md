# Repeat Yourself

**Write a method that takes two arguments, a string and a positive integer, and prints the string as many times as the integer indicates.**

**Example:**

```ruby
repeat('Hello', 3)
```

**Output:**

```terminal
Hello
Hello
Hello
```

---

(Understanding the ) Problem:

This problem is asking for the definition of a method called `repeat`, which will take two arguments as input:

1. A string
2. A number

And will `puts` the string argument as many times as the number argument.

```ruby 
def repeat(str, num)
  num.times { |_| puts str }
end

repeat('Hello', 3)
```

Note: This implementation uses the `times` method, which will return `num` from the `repeat` block. A question to ask the interviewer is: "What should be returned by the method?"