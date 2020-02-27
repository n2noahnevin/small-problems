# Greeting a user

**Write a program that will ask for user's name. The program will then greet the user. If the user writes "name!" then the computer yells back to the user.**

**Examples:**

```plaintext
What is your name? Bob
Hello Bob.
What is your name? Bob!
HELLO BOB. WHY ARE WE SCREAMING?
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: String (name from user)

Output: String (printed to screen)

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

1. Any verification needed?
2. Does the program need to loop?

*Mental Model:*

Get the user's name. Get an array of the chars of the name. Check if `arr[-1] == '!'`. If it doesn't just return a hello. If it does, return the "yelling" answer.

*Examples/Test Cases/Edge Cases:*

```plaintext
What is your name? Bob
Hello Bob.
What is your name? Bob!
HELLO BOB. WHY ARE WE SCREAMING?
```

*Data Structures:*

Strings and an array.

*Algorithm:*

1. Use `gets.chomp` to get the user's `name`.
2. Define a new variable, `arr`, and set it equal to `name.chars`.
3. Use an `if` statement to check what `arr[-1]` equals. If it equal `!`, then take off the `!` with `chop`, and "yell" back. If it doesn't, then `puts` a normal greeting.

*Code:*

```ruby
puts "What is your name?"
name = gets.chomp

arr = name.chars

if arr[-1] == '!'
  name = name.chop
  puts "HELLO #{name}. WHY ARE WE SCREAMING?"
else
  puts "Hello #{name}."
end
```