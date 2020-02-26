# Sum of Digits

**Write a method that takes one argument, a positive integer, and returns the sum of its digits.**

**Examples:**

```ruby
puts sum(23) == 5
puts sum(496) == 19
puts sum(123_456_789) == 45
```

**The tests above should print `true`.**

**For a challenge, try writing this without any basic looping constructs (`while`, `until`, `loop`, and `each`).**

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Positive Integer

Output: Integer

*Problem Domain:*

Sum: Addition of all digits.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Take in an integer as an argument. Separate the integer's digits individually, and then add them all up. Return this value.

*Examples/Test Cases/Edge Cases:*

```ruby
puts sum(23) == 5
puts sum(496) == 19
puts sum(123_456_789) == 45
```

*Data Strucutures:*

The data will be transformed into an array.

*Algorithm:*

1. Define a new method, `sum`, that takes a positive integer, `num`, as an argument.
2. Use `num.digits` to create an array of all the digits of `num`. Store this in a new local variable, `arr`.
3. Return `arr.reduce(:+)` , which will add up all the members of `arr`.

```ruby
def sum(num)
  arr = num.digits
  arr.reduce(:+)
end

puts sum(23) == 5
puts sum(496) == 19
puts sum(123_456_789) == 45
```

Another implementation that converts to a string is shown below:

```ruby
def sum(number)
  number.to_s.chars.map(&:to_i).reduce(:+)
end
```

