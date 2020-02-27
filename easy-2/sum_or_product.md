# Sum or Product of Consecutive Integers

**Write a program that asks the user to enter an integer greater than 0, then asks if the user wants to determine the sum or product of all numbers between 1 and the entered integer.**

**Examples:**

```plaintext
>> Please enter an integer greater than 0:
5
>> Enter 's' to compute the sum, 'p' to compute the product.
s
The sum of the integers between 1 and 5 is 15.


>> Please enter an integer greater than 0:
6
>> Enter 's' to compute the sum, 'p' to compute the product.
p
The product of the integers between 1 and 6 is 720.
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Strings (number and answer from user)

Output: String (with variables interpolated)

*Problem Domain:*

Product: Multiplication

Sum: Addition

*Implicit Requirements:*

Input verification.

*Clarifying Questions:*

1. Will verification of the user input need to be checked?

*Mental Model:*

Ask the user for an integer greater than 0, and then 's' or 'p'. Run a loop that breaks off then it reaches the integer + 1. Each time, either add or multiply the number into a total, and return it to the screen with string interpolation.

*Examples/Test Cases/Edge Cases:*

```
>> Please enter an integer greater than 0:
5
>> Enter 's' to compute the sum, 'p' to compute the product.
s
The sum of the integers between 1 and 5 is 15.


>> Please enter an integer greater than 0:
6
>> Enter 's' to compute the sum, 'p' to compute the product.
p
The product of the integers between 1 and 6 is 720.
```

*Data Structures:*

Just strings.

*Algorithm:*

1. Use `gets.chomp.to_i` to get an integer greater than 0 from the user. Verify that it's an integer greater than 0, if not, ask for another.
2. Use `gets.chomp` to get either 's' or 'p' from the user. If neither, ask again.
3. Start a `loop` and create a `counter`. Increment the `counter` and every time, either add or multiply depending on the user's input. Break the `loop` when `counter > num`.
4. Return the values needed using string interpolation.

*Code:*

```ruby
def prompt(message)
  puts ">> #{message}"
end

num = 0
loop do
  prompt "Please enter an integer greater than 0:"
  num = gets.chomp.to_i
  break if num > 0 && num.integer?
  prompt "Invalid input, please try again."
end

answer = ''
loop do
  prompt "Enter 's' to compute the sum, 'p' to compute the product."
  answer = gets.chomp
  break if answer.downcase == 's' || answer.downcase == 'p'
  prompt "Invalid input, please try again."
end

word = answer == 's' ? 'sum' : 'product'

total = answer == 's' ? 0 : 1

counter = 1
loop do
  if answer == 's'
    total += counter
  else
    total *= counter
  end
  counter += 1
  break if counter > num
end

puts "The #{word} of the integers between 1 and #{num} is #{total}."
```

Note: Some unexpected issues with this code were:

1. Setting `total` to `0` initially made it impossible to get a correct answer for `product`, because anything times `0` is still `0`. To fix this, I made a ternary call to set total to either `0` for sum, or `1` for product.
2. I overlooked having to also change wording in the final statment to either `'product'` or `'sum'` depending on user input. I also solved this with a ternary operator.
3. `Enumerable#inject` would be perfect for a simpler implementation of this method. Also defining a method for each choice would look neater.