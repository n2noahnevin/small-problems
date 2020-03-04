# Leap Years (Part 1)

**In the modern era under the Gregorian Calendar, leap years occur in every year that is evenly divisible by 4, unless the year is also divisible by 100. If the year is evenly divisible by 100, then it is not a leap year unless the year is evenly divisible by 400.**

**Assume this rule is good for any year greater than year 0. Write a method that takes any year greater than 0 as input, and returns true if the year is a leap year, or false if it is not a leap year.**

```ruby
leap_year?(2016) == true
leap_year?(2015) == false
leap_year?(2100) == false
leap_year?(2400) == true
leap_year?(240000) == true
leap_year?(240001) == false
leap_year?(2000) == true
leap_year?(1900) == false
leap_year?(1752) == true
leap_year?(1700) == false
leap_year?(1) == false
leap_year?(100) == false
leap_year?(400) == true
```

---

*Algorithm:*

1. Define a new method, `leap_year?`, that takes in an integer greater than `0`, and that'll return a boolean.
2. Check if the `num % 4 == 0`. If yes, then also check if `num % 100 == 0`. If yes, then check if `num % 400 == 0`. If only divisible by 4, return true. If only divisible by 4 and 100, return false. If divisible by all three, return true. All other cases, return false.

*Code:*

```ruby
def leap_year?(num)
  by_4 = num % 4 == 0
  by_100 = num % 100 == 0
  by_400 = num % 400 == 0
  
  case
    when by_4 && by_100 && by_400
    return true
    when by_4 && by_100
    return false
    when by_4
    return true
  else
    return false
  end
end

leap_year?(2016) == true
leap_year?(2015) == false
leap_year?(2100) == false
leap_year?(2400) == true
leap_year?(240000) == true
leap_year?(240001) == false
leap_year?(2000) == true
leap_year?(1900) == false
leap_year?(1752) == true
leap_year?(1700) == false
leap_year?(1) == false
leap_year?(100) == false
leap_year?(400) == true
```

