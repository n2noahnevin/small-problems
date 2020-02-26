# What's my Bonus?

**Write a method that takes two arguments, a positive integer and a boolean, and calculates the bonus for a given salary. If the boolean is `true`, the bonus should be half of the salary. If the boolean is `false`, the bonus should be `0`.**

**Examples:**

```ruby
puts calculate_bonus(2800, true) == 1400
puts calculate_bonus(1000, false) == 0
puts calculate_bonus(50000, true) == 25000
```

**The tests above should print `true`.**

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Positive Integer, and Boolean

Output: Integer

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Take in a number and boolean as arguments. If the boolean equals false, automatically return 0. If it equals true, then return num / 2. 

*Examples/Test Cases/Edge Cases:*

```ruby
puts calculate_bonus(2800, true) == 1400
puts calculate_bonus(1000, false) == 0
puts calculate_bonus(50000, true) == 25000
```

*Data Structures:*

No explicit data structure needed.

*Algorithm:*

1. Define a new method, `calculate_bonus`, that takes in two arguments: `num`, a positive integer, and `status`, a boolean.
2. Define an `if` block that will return `num / 2` if `status == true`, and `0` if `status == false`.

*Code:*

```ruby
def calculate_bonus(num, status)
  if status
    num / 2
  else
    0
  end
end

puts calculate_bonus(2800, true) == 1400
puts calculate_bonus(1000, false) == 0
puts calculate_bonus(50000, true) == 25000
```

Another implementation using the ternary operator is shown below:

```ruby
def calculate_bonus(salary, bonus)
  bonus ? (salary / 2) : 0
end
```

