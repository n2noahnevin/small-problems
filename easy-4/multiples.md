# Multiples of 3 and 5

**Write a method that searches for all multiples of 3 or 5 that lie between 1 and some other number, and then computes the sum of those multiples. For instance, if the supplied number is `20`, the result should be `98` (3 + 5 + 6 + 9 + 10 + 12 + 15 + 18 + 20).**

**You may assume that the number passed in is an integer greater than 1.**

**Examples:**

```ruby
multisum(3) == 3
multisum(5) == 8
multisum(10) == 33
multisum(1000) == 234168
```

---

*Algorithm:*

1. Define a new method, `multisum`, that takes in one integer as an argument.
2. Define a counter variable, and loop until `counter == num`. Every iteration, check if the counter is divisible by 3 or 5. If yes, add it to a `total` variable.
3. Return the total variable.

*Code:*

```ruby
def multisum(num)
  counter = 1
  total = 0
  while counter <= num
    if counter % 3 == 0 || counter % 5 == 0
      total += counter
    end
    counter += 1
  end
  total
end

multisum(3) == 3
multisum(5) == 8
multisum(10) == 33
multisum(1000) == 234168
```

