# Reverse It (Part 1)

**Write a method that takes one argument, a string, and returns a new string with the words in reverse order.**

**Examples:**

```ruby
puts reverse_sentence('') == ''
puts reverse_sentence('Hello World') == 'World Hello'
puts reverse_sentence('Reverse these words') == 'words these Reverse'
```

**The tests above should print `true`.**

---

*(Understanding the) Problem:*

*Input/Output:*

Input: A string

Output: A (new) string

*Problem Domain:*

Reverse order: The new string will have a reverse order, meaning the actual words aren't to be altered, just their place in the string.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Create a method that will take in the string, split it into an array of words, and then feed that array into a new string, except reversed.

*Examples/Test Cases/Edge Cases*

```ruby
puts reverse_sentence('') == ''
puts reverse_sentence('Hello World') == 'World Hello'
puts reverse_sentence('Reverse these words') == 'words these Reverse'

# All should evaluate to true
```

*Data Structures:*

We are dealing with Strings both as input and output of this method, but because of `String#split`, we will also be morphing our data into an array.

*Algorithm:*

1. Define a new method, `reverse_sentence`, That takes in a String, `str`, as an argument. 
2. Create a new local variable, `new_str`, and set it equal to `str.split(' ').reverse.join(' ')`.
3. Return this new string.

*Code:*

```ruby
def reverse_sentence(str)
  new_str = str.split(' ').reverse.join(' ')
end

puts reverse_sentence('') == ''
puts reverse_sentence('Hello World') == 'World Hello'
puts reverse_sentence('Reverse these words') == 'words these Reverse'
```



