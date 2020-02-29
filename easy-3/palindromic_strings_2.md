# Palindromic Strings (Part 2)

**Write another method that returns true if the string passed as an argument is a palindrome, false otherwise. This time, however, your method should be case-insensitive, and it should ignore all non-alphanumeric characters. If you wish, you may simplify things by calling the `palindrome?` method you wrote in the previous exercise.**

**Examples:**

```ruby
real_palindrome?('madam') == true
real_palindrome?('Madam') == true           # (case does not matter)
real_palindrome?("Madam, I'm Adam") == true # (only alphanumerics matter)
real_palindrome?('356653') == true
real_palindrome?('356a653') == true
real_palindrome?('123ab321') == false
```

---

*Algorithm:*

1. Define a new method, `real_palindrome?`, that takes in a string as an argument and will return a boolean.
2. Create a new string variable, and set it equal to the argument string, except completely downcased, and only alphanumerics.
3. See if this new string is equal to the new string reversed. True if yes, False if no.

*Code:*

```ruby
ALPHANUMERICS = %w(a b c d e f g h i j k l m n o p q r s t u v w x y z 1 2 3 4 5 6 7 8 9 0)

def real_palindrome?(str)
  new_str = ''
  arr = str.downcase.chars
  arr.each do |char|
    if ALPHANUMERICS.include?(char) 
      new_str << char
    end
  end
  new_str == new_str.reverse
end
  
real_palindrome?('madam') == true
real_palindrome?('Madam') == true           # (case does not matter)
real_palindrome?("Madam, I'm Adam") == true # (only alphanumerics matter)
real_palindrome?('356653') == true
real_palindrome?('356a653') == true
real_palindrome?('123ab321') == false
```

A cleaner implementation involves utilizing the method `String#delete`:

```ruby
def real_palindrome?(string)
  string = string.downcase.delete('^a-z0-9')
  string == string.reverse
end
```

