# How old is Teddy?

**Build a program that randomly generates and prints Teddy's age. To get the age, you should generate a random number between 20 and 200.**

**Example Output:**

```plaintext
Teddy is 69 years old!
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: None

Output: A String (method returns nil)

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Define a new method that puts a random number between 20 and 200 into a variable. Print that variable in a string, and return this string.

*Examples/Test Cases/Edge Cases:*

```ruby
Teddy is 69 years old!
```

*Data Structures:*

Will use a string, no other data structures needed.

*Algorithm:*

1. Define a new method, `teddy_age`, that takes in no arguments.
2. Define a new local variable `age`, and set it equal to `rand(20..200)`.
3. `puts` the string `Teddy is #{age} years old!`.

*Code:*

```ruby
def teddy_age
  age = rand(20..200)
puts "Teddy is #{age} years old!"
end

teddy_age
```

---

#### Further Exploration

**Modify this program to ask for a name, and then print the age for that person. For an extra challenge, use "Teddy" as the name if no name is entered.**

---

*Algorithm:*

1. Define a new method, `age`, that takes in one String argument: `name`. Define the default value for `name` to be `'Teddy'`.
2. Repeat above algorithm's instructions, except also interpolating `name` into the string to return.

```ruby
def age(name='Teddy')
  age = rand(20..200)
  puts "#{name} is #{age} years old!"
end

puts "What is your name?"
name = gets.chomp
age(name)
```







