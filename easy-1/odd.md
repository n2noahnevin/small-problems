# Odd

**Write a method that takes one integer argument, which may be positive, negative, or zero. This method returns `true` if the number's absolute value is odd. You may assume that the argument is a valid integer value.**

**Examples:**

```ruby
puts is_odd?(2)    # => false
puts is_odd?(5)    # => true
puts is_odd?(-17)  # => true
puts is_odd?(-8)   # => false
puts is_odd?(0)    # => false
puts is_odd?(7)    # => true
```

**Keep in mind that you're not allowed to use `#odd?` or `#even?` in your solution.**

---

*(Understanding the) Problem:*

*Inputs/Outputs:*

Input to the `is_odd?` method: An integer

Output from the `is_odd?` method: A boolean

*Problem Domain:*

Odd number: A number that, when divided by `2`, has a remainder.

Absolute value: The positive equivalent to a number. For example: |-2| == 2, and |2| == 2.

*Implicit Requirements*:

Since the integer can be assumed to be valid input, no implicit requirements.

*Clarifying Questions:*

1. (For example) Is the `odd?` method off of the table for this exercise? (Answer would be "yes.")

*Mental Model*:

We are to write a method definition for the method `is_odd?`, which will return `true` if the absolute value of the number given is an odd number. 

*Examples/Test Cases/Edge Cases:*

```ruby
puts is_odd?(2)    # => false
puts is_odd?(5)    # => true
puts is_odd?(-17)  # => true
puts is_odd?(-8)   # => false
puts is_odd?(0)    # => false
puts is_odd?(7)    # => true
```

*Data Structure*:

No explicit data structure needed.

*Algorithm:*

1. Define new method, `is_odd?`, that takes a singular integer argument, `num`.
2. Check if `num` is odd with the logic `num % 2 != 0`. Leave as the last line of the method to be implicitly returned.
3. Invocate `is_odd?` Below the method definition.

*Code:*

```ruby
def is_odd?(num)
  num % 2 != 0
end

puts is_odd?(2)    # => false
puts is_odd?(5)    # => true
puts is_odd?(-17)  # => true
puts is_odd?(-8)   # => false
puts is_odd?(0)    # => false
puts is_odd?(7)    # => true
```















