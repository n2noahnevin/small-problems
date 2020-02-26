# List of Digits

**Write a method that takes one argument, a positive integer, and returns a list of the digits in the number.**

Examples:

```ruby
puts digit_list(12345) == [1, 2, 3, 4, 5]     # => true
puts digit_list(7) == [7]                     # => true
puts digit_list(375290) == [3, 7, 5, 2, 9, 0] # => true
puts digit_list(444) == [4, 4, 4]             # => true
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Positive Integer

Output: Array

*Problem Domain:*

List: In this case, an array of integers.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Examples/Test Cases/Edge Cases:*

```ruby
puts digit_list(12345) == [1, 2, 3, 4, 5]     # => true
puts digit_list(7) == [7]                     # => true
puts digit_list(375290) == [3, 7, 5, 2, 9, 0] # => true
puts digit_list(444) == [4, 4, 4]             # => true
```

*Data Structure:*

The easiest way to get all of the digits by themselves will be by conversion to a `String`.

*Algorithm:*

1. Define a new method, `digit_list`, which takes in a positive integer, `num`, as an argument. 
2. In the method, change `num` into a `String` using `to_s`, and then change it into an array of its characters using `chars`.
3. Finally, `map` these into a new array, changing each `char` back into an `integer` using `to_i`. 

*Code:*

```ruby
def digit_list(num)
  num.to_s.chars.map { |char| char.to_i }
end

puts digit_list(12345) == [1, 2, 3, 4, 5]     # => true
puts digit_list(7) == [7]                     # => true
puts digit_list(375290) == [3, 7, 5, 2, 9, 0] # => true
puts digit_list(444) == [4, 4, 4]             # => true
```

