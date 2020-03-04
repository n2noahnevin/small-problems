# Short Long Short

**Write a method that takes two strings as arguments, determines the longest of the two strings, and then returns the result of concatenating the shorter string, the longer string, and the shorter string once again. You may assume that the strings are of different lengths.**

**Examples:**

```ruby
short_long_short('abc', 'defgh') == "abcdefghabc"
short_long_short('abcde', 'fgh') == "fghabcdefgh"
short_long_short('', 'xyz') == "xyz"
```

---

*Algorithm:*

1. Define a new method, `short_long_short`, that takes two strings as arguments, and returns a new string.
2. Use a ternary operator to return the result of `str1 + str2 + str` or `str2 + str1 + str2` depending on which is shorter.

*Code:*

```ruby
def short_long_short(str1, str2)
  str2.length > str1.length 
              ? str1+str2+str1 : 
                str2+str1+str2
end

short_long_short('abc', 'defgh') == "abcdefghabc"
short_long_short('abcde', 'fgh') == "fghabcdefgh"
short_long_short('', 'xyz') == "xyz"
```

