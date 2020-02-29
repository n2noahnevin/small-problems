# Palindromic Numbers

**Write a method that returns true if its integer argument is palindromic, false otherwise. A palindromic number reads the same forwards and backwards.**

**Examples:**

```ruby
palindromic_number?(34543) == true
palindromic_number?(123210) == false
palindromic_number?(22) == true
palindromic_number?(5) == true
```

---

*Algorithm:*

1. Define a new method, `palindromic_number?`, that takes in an integer and returns a boolean.
2. Turn the integer into a string, and see if the string is equal to string.reverse.

*Code:*

```ruby
def palindromic_number?(num)
  str = num.to_s
  str == str.reverse
end

palindromic_number?(34543) == true
palindromic_number?(123210) == false
palindromic_number?(22) == true
palindromic_number?(5) == true
```

