# Reverse It (Part 2)

**Write a method that takes one argument, a string containing one or more words, and returns the given string with words that contain five or more characters reversed. Each string will consist of only letters and spaces. Spaces should be included only when more than one word is present.**

**Examples:**

```ruby
puts reverse_words('Professional')          # => lanoisseforP
puts reverse_words('Walk around the block') # => Walk dnuora the kcolb
puts reverse_words('Launch School')         # => hcnuaL loohcS
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: String

Output: String

*Problem Domain:*

No definitions needed.

*Implicit Requirements*

None.

*Clarifying Questions:*

None.

*Mental Model*:

Take a string into the method, and split the string into an array of words. Check if the word contains more than 5 chracters, and if it does, reverse it. Turn the array back into a string and return it.

*Examples/Test Cases/Edge Cases:*

```ruby
puts reverse_words('Professional')          # => lanoisseforP
puts reverse_words('Walk around the block') # => Walk dnuora the kcolb
puts reverse_words('Launch School')         # => hcnuaL loohcS
```

*Data Structures:*

The input string will be transferred into an array, then back into a string.

*Algorithm:*

1. Define a new method, `reverse_words`, that takes in a string as an argument, called `str`.
2. Use `str.split(' ')` to split the input string into an array of words, called `word_arr`.
3. Increment through `word_arr`, and write an `if` statement to check if `word_arr[counter].length >= 5`. If it is, then reverse the word.
4. Use `str.join(' ')` to create the new array, and return it.

*Code:*

```ruby
def reverse_words(str)
  word_arr = str.split(' ')
  word_arr.each do |word| 
    word.reverse! if word.length >= 5
  end
  word_arr.join(' ')
end

puts reverse_words('Professional')          # => lanoisseforP
puts reverse_words('Walk around the block') # => Walk dnuora the kcolb
puts reverse_words('Launch School')         # => hcnuaL loohcS
```



