# Squaring an Argument

**Using the `multiply` method from the "Multiplying Two Numbers" problem, write a method that computes the square of its argument (the square is the result of multiplying a number by itself).**

**Example:**

```ruby
square(5) == 25
square(-8) == 64
```

---

Note: For the sake of time, the PEDAC process will be skipped over for this example.

*Code:*

```ruby
def multiply(num1, num2)
  num1 * num2
end

def square(num)
  multiply(num, num)
end

square(5) == 25
square(-8) == 64
```

