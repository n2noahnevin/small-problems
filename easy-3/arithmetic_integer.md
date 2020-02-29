# Arithmetic Integer

**Write a program that prompts the user for two positive integers, and then prints the results of the following operations on those two numbers: addition, subtraction, product, quotient, remainder, and power. Do not worry about validating the input.**

**Example:**

```plaintext
==> Enter the first number:
23
==> Enter the second number:
17
==> 23 + 17 = 40
==> 23 - 17 = 6
==> 23 * 17 = 391
==> 23 / 17 = 1
==> 23 % 17 = 6
==> 23 ** 17 = 141050039560662968926103
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Two strings (number choices) from user

Output: 6 strings printed to the screen.

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

1. Is a `prompt` method needed in order to print with a proper `==>` before the string?
2. Do we need to take into account the sheer size that the exponential total can come to?

*Mental Model:*

Get the two numbers from the user. Print out each operation to the screen, using string interpolation to enter the appropriate values.

*Examples/Test Cases/Edge Cases:*

```
==> Enter the first number:
23
==> Enter the second number:
17
==> 23 + 17 = 40
==> 23 - 17 = 6
==> 23 * 17 = 391
==> 23 / 17 = 1
==> 23 % 17 = 6
==> 23 ** 17 = 141050039560662968926103
```

 *Data Structures:*

None needed.

*Algorithm:*

1. Get the two numbers from the user and place them into variables.
2. Using string interpolation, output the appropriate operation to the screen with said operation being performed.
3. What should be done if input is `0`?

*Code:*

```ruby
def prompt(message)
  puts "==> #{message}"
end

prompt "Enter the first number:"
num1 = gets.chomp.to_i
prompt "Enter the second number:"
num2 = gets.chomp.to_i

prompt "#{num1} + #{num2} = #{num1+num2}"
prompt "#{num1} - #{num2} = #{num1-num2}"
prompt "#{num1} * #{num2} = #{num1*num2}"
prompt "#{num1} / #{num2} = #{num1/num2}"
prompt "#{num1} % #{num2} = #{num1%num2}"
prompt "#{num1} ** #{num2} = #{num1**num2}"
```

