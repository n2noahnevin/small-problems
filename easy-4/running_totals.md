# Running Totals

**Write a method that takes an Array of numbers, and returns an Array with the same number of elements, and each element has the running total from the original Array.**

**Examples:**

```ruby
running_total([2, 5, 13]) == [2, 7, 20]
running_total([14, 11, 7, 15, 20]) == [14, 25, 32, 47, 67]
running_total([3]) == [3]
running_total([]) == []
```

---

*Algorithm:*

1. Define a new method, `running_total`, that takes in an array as an argument.
2. Iterate through the array, and define a variable that will keep a running tab of the array total. For every iteration, add the newest array total to the running tab, and then insert the running tab into the new array.
3. Return the new array.

*Code:*

```ruby
def running_total(arr)
  running_tab = 0
  counter = 0
  arr.map do |num|
    running_tab += arr[counter]
    counter += 1
    running_tab
  end
end

running_total([2, 5, 13]) == [2, 7, 20]
running_total([14, 11, 7, 15, 20]) == [14, 25, 32, 47, 67]
running_total([3]) == [3]
running_total([]) == []
```

An easier solution using `map` more efficiently is shown below:

```ruby
def running_total(array)
  sum = 0
  array.map { |value| sum += value }
end
```

---

#### Further Exploration

**Try solving this problem using `Enumerable#each_with_object` or `Enumerable#inject` (note that `Enumerable` methods can be applied to Arrays).**

---

`Enumerable#each_with_object`:

```ruby
def running_total(arr)
  total = 0
  arr.each_with_object([]) do |num, array|
    total += num
    array << total
  end
end

running_total([2, 5, 13]) == [2, 7, 20]
running_total([14, 11, 7, 15, 20]) == [14, 25, 32, 47, 67]
running_total([3]) == [3]
running_total([]) == []
```



