# Array Average

**Write a method that takes one argument, an array containing integers, and returns the average of all numbers in the array. The array will never be empty and the numbers will always be positive integers.**

**Examples:**

```ruby
puts average([1, 5, 87, 45, 8, 8]) == 25
puts average([9, 47, 23, 95, 16, 52]) == 40
```

**The tests above should print `true`.**

---

*(Understanding the) Problem:*

*Input/Output:*

Input: An array of integers

Output: Integer

*Problem Domain:*

Average: To find the average, add all the qualifying numbers together and divide by how many numbers there are total.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Increment through the array, adding up all of the values inside of it into one variable. Then divide that integer by array.size. Return this value.

*Examples/Test cases/Edge Cases:*

```ruby
puts average([1, 5, 87, 45, 8, 8]) == 25
puts average([9, 47, 23, 95, 16, 52]) == 40
```

*Data Structures:*

An array contains the initial data.

*Algorithm:*

1. Define a new method, `average`, and take in an array of integers, `arr`, as an argument.
2. Define a local variable, `total`, and set it equal to 0.
3. Using `arr.each`, increment through the array, adding every value to `total`.
4. Calculate `total / arr.size'. This is your average. Return this value.

*Code:*

```ruby
def average(arr)
  total = 0
  arr.each { |num| total += num }
  total / arr.size
end

puts average([1, 5, 87, 45, 8, 8]) == 25
puts average([9, 47, 23, 95, 16, 52]) == 40
```

Another implementation using the methods `Enumerable#reduce` and `Array#count` is shown below:

```ruby
def average(numbers)
  sum = numbers.reduce { |sum, number| sum + number }
  sum / numbers.count
end
```



