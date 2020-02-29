# Searching 101

**Write a program that solicits 6 numbers from the user, then prints a message that describes whether or not the 6th number appears amongst the first 5 numbers.**

**Examples:**

```plaintext
==> Enter the 1st number:
25
==> Enter the 2nd number:
15
==> Enter the 3rd number:
20
==> Enter the 4th number:
17
==> Enter the 5th number:
23
==> Enter the last number:
17
The number 17 appears in [25, 15, 20, 17, 23].


==> Enter the 1st number:
25
==> Enter the 2nd number:
15
==> Enter the 3rd number:
20
==> Enter the 4th number:
17
==> Enter the 5th number:
23
==> Enter the last number:
18
The number 18 does not appear in [25, 15, 20, 17, 23].
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: 6 Strings (all numbers)

Output: String (printed to screen), with integer and array interpolated.

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

Enter the first five values gotten into an array.

*Clarifying Questions:*

None.

*Mental Model:*

Using a loop, get 5 numbers from the user, and use `<<` to put them into an array. Then get one more number, and use `Array#include?` to see if that number is in the array.

*Examples/Test Cases/Edge Cases:*

```
==> Enter the 1st number:
25
==> Enter the 2nd number:
15
==> Enter the 3rd number:
20
==> Enter the 4th number:
17
==> Enter the 5th number:
23
==> Enter the last number:
17
The number 17 appears in [25, 15, 20, 17, 23].


==> Enter the 1st number:
25
==> Enter the 2nd number:
15
==> Enter the 3rd number:
20
==> Enter the 4th number:
17
==> Enter the 5th number:
23
==> Enter the last number:
18
The number 18 does not appear in [25, 15, 20, 17, 23].
```

*Data Structures:*

Strings, and data will be entered into an array.

*Algorithm:*

1. Create a `loop` that will use `gets.chomp` to get 5 numbers from the user. Enter these numbers into an `arr`. 
2. Get one last value from the user, and see if it is in the `arr` by using `arr.include?(last_value)`.
3. Print to the screen whether it appears or not.

*Code:*

```ruby
place_arr = ['1st', '2nd', '3rd', '4th', '5th', 'last']
counter = 0
arr = []
included = false
num = 0

loop do
  puts "Enter the #{place_arr[counter]} number:"
  num = gets.chomp
  if counter < 4
    arr << num
  else
    included = arr.include?(num)
  end
  counter += 1
  break if counter > 5
end

if included
  puts "The number #{num} appears in #{arr}."
else
  puts "The number #{num} does not appear in #{arr}."
end
```

It is also possible to complete this problem without using a loop:

```ruby
numbers = []

puts "Enter the 1st number:"
numbers << gets.chomp.to_i
puts "Enter the 2nd number:"
numbers << gets.chomp.to_i
puts "Enter the 3rd number:"
numbers << gets.chomp.to_i
puts "Enter the 4th number:"
numbers << gets.chomp.to_i
puts "Enter the 5th number:"
numbers << gets.chomp.to_i
puts "Enter the last number:"
last_number = gets.chomp.to_i

if numbers.include? last_number
  puts "The number #{last_number} appears in #{numbers}."
else
  puts "The number #{last_number} does not appear in #{numbers}."
end
```



