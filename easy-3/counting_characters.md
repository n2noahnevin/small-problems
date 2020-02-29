# Counting the Number of Characters

**Write a program that will ask a user for an input of a word or multiple words and give back the number of characters. Spaces should not be counted as a character.**

**Input:**

```plaintext
Please write word or multiple words: walk
```

**Output:**

```plaintext
There are 4 characters in "walk".
```

**Input:**

```plaintext
Please write word or multiple words: walk, don't run
```

**Output:**

```plaintext
There are 13 characters in "walk, don't run".
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: String (from user)

Output: String (to screen)

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

1. Should `print` be used, since the example has the request and the user string on the same line?

*Mental Model:*

Ask the user for a word or multiple words. Split this word into characters. If the character is a space, ignore it, if not, increment a total.

*Examples/Test Cases/Edge Cases:*

```plaintext
Please write word or multiple words: walk
```

```plaintext
There are 4 characters in "walk".
```

```plaintext
Please write word or multiple words: walk, don't run
```

```plaintext
There are 13 characters in "walk, don't run".
```

*Data Structures:*

An array will be used to store every character.

*Algorithm:*

1. Get the string from the user.
2. Separate the string into chars.
3. Go through the entire array, and for every char, if  the char is a space, next, if not, increment a variabe `total`.
4. Print the result to the screen.

*Code:*

```ruby
print "Please write word or multiple words: "
str = gets.chomp

char_arr = str.chars
total = 0
char_arr.each do |char|
  if char == ' '
    next
  else
    total += 1
  end
end

puts "There are #{total} characters in \"#{str}\"."
```

Another implementation is to use `String#delete` to delete all of the spaces out of the user string, and then use `String#size` to get the total:

```ruby
print 'Please write word or multiple words: '
input = gets.chomp
number_of_characters = input.delete(' ').size
puts "There are #{number_of_characters} characters in \"#{input}\"."
```

