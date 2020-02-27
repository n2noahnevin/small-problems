# When will I Retire?

**Build a program that displays when the user will retire and how many years she has to work till retirement.**

**Example:**

```plaintext
What is your age? 30
At what age would you like to retire? 70

It's 2016. You will retire in 2056.
You have only 40 years of work to go!
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Strings (age from user and their retiring age)

Output: Strings (`puts` to screen)

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Get the user's age and retirement age. Find the difference, and add this to the current year. Use string interpolation to print out current year, retiring year, and the difference in strings.

*Examples/Test Cases/Edge Cases:*

```
What is your age? 30
At what age would you like to retire? 70

It's 2016. You will retire in 2056.
You have only 40 years of work to go!
```

*Data Structures:*

Just strings.

*Algorithm:*

1. Use `gets.chomp.to_i` to get `age` and `retiring_age`.
2. Define a variable, `diff`, and set it equal to `retiring_age - age`.
3. Define a constant and set it equal to the current year (2020).
4. Define another variable, `retiring_year`, and set it equal to `CURRENT_YEAR + diff`.
5. Use `puts` to return needed information to the screen.

*Code:*

```ruby
CURRENT_YEAR = 2020

puts "What is your age?"
age = gets.chomp.to_i
puts "At what age would you like to retire?"
retiring_age = gets.chomp.to_i

diff = retiring_age - age
retiring_year = CURRENT_YEAR + diff

puts "It's #{CURRENT_YEAR}. You will retire in #{retiring_year}."
puts "You have only #{diff} years of work to go!"
```

Note: It's also possible to use `Time.now.year` to get the current year.