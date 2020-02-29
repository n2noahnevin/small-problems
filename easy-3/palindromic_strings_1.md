# Palindromic Strings (Part 1)

**Write a method that returns true if the string passed as an argument is a palindrome, false otherwise. A palindrome reads the same forward and backward. For this exercise, case matters as does punctuation and spaces.**

**Examples:**

```ruby
palindrome?('madam') == true
palindrome?('Madam') == false          # (case matters)
palindrome?("madam i'm adam") == false # (all characters matter)
palindrome?('356653') == true
```

---

*Algorithm:*

1. Define a new method, `palindrome?`, that takes in a string as an argument and returns a boolean.
2. Reverse the string, and see if the original string is equal to the reversed string.
3. Return true if it is, false if it isn't.

*Code:*

```ruby
def palindrome?(str)
  str == str.reverse
end

palindrome?('madam') == true
palindrome?('Madam') == false          # (case matters)
palindrome?("madam i'm adam") == false # (all characters matter)
palindrome?('356653') == true
```

