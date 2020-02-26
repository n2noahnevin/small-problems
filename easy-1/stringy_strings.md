# Stringy Strings

**Write a method that takes one argument, a positive integer, and returns a string of alternating 1s and 0s, always starting with 1. The length of the string should match the given integer.**

**Examples:**

```ruby
puts stringy(6) == '101010'
puts stringy(9) == '101010101'
puts stringy(4) == '1010'
puts stringy(7) == '1010101'
```

**The tests above should print `true`.**

---

*(Understanding the) Problem*

*Input/Output:*

Input: Positive integer

Output: A string

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Take in the integer from the argument, and create a loop. Adds a `1` to the string, and then swaps the value to add to a `0`, repeating until the counter equals the argument integer.

*Examples/Test Cases/Edge Cases:*

```ruby
puts stringy(6) == '101010'
puts stringy(9) == '101010101'
puts stringy(4) == '1010'
puts stringy(7) == '1010101'

# All should be true
```

*Data Structures:*

Will use strings, and convert values into array format as well.

*Algorithm:*

1. Define a new method, `stringy`, that takes in a positive integer, `num`, as an argument.
2. Define new local variables `str` ,`counter`, and `value`. Set `value` to `'1'`.
3. Create a `loop`. Break the loop when `counter == num`. In the loop, do `str << value`. Change `value` to `'0'` for next iteration.
4. Return `str`.

*Code:*

```ruby
def stringy(num)
  str = ''
  counter = 0
  value = '1'
  loop do 
    break if counter == num
    str << value
    counter += 1
    if value == '1'
      value = '0'
    else
      value = '1'
    end
  end
  str
end

puts stringy(6) == '101010'
puts stringy(9) == '101010101'
puts stringy(4) == '1010'
puts stringy(7) == '1010101'
```

Below is another implementation that uses the `Integer#times` method and the `?` operator:

```ruby
def stringy(size)
  numbers = []

  size.times do |index|
    number = index.even? ? 1 : 0
    numbers << number
  end

  numbers.join
end
```



