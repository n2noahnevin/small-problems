# How Many?

**Write a method that counts the number of occurrences of each element in a given array.**

```ruby
vehicles = [
  'car', 'car', 'truck', 'car', 'SUV', 'truck',
  'motorcycle', 'motorcycle', 'car', 'truck'
]

count_occurrences(vehicles)
```

**The words in the array are case-sensitive: `'suv' != 'SUV'`. ` Once counted, print each element alongside the number of occurrences.**

**Expected output:**

```terminal
car => 4
truck => 3
SUV => 1
motorcycle => 2
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Array of Strings

Output: Hash

*Problem Domain:*

No definitions needed.

*Implicit Requirements*

Method input verification.

*Clarifying Questions:*

1. Will the array given to the method always be a `char` array?
2. What is expected when an empty array is passed into the method?

*Mental Model*

Given an array of strings, take each string and try to pass the string into a `hash`. If the string is already a key in the `hash`, then increment the value of that key by `1`. If not, make it a key, and set the value to `1`. 

*Examples, Test Cases, Edge Cases*

```ruby
vehicles = [
  'car', 'car', 'truck', 'car', 'SUV', 'truck',
  'motorcycle', 'motorcycle', 'car', 'truck'
]

count_occurrences(vehicles)

=begin
car => 4
truck => 3
SUV => 1
motorcycle => 2
=end
```

*Data Structure*

We will create a `Hash` in order to store the different words and number of occurences.

*Algorithm*

1. Define a new method, `count_occurences`, that takes a `char` array named `arr` in as an argument.
2. Define a new hash, called `h`, and initialize it to an empty hash. 
3. Define a new local variable, `counter`, and initialize it to `0`.
4. Start a `loop`. Break out of this loop when `counter == arr.size`.
5. Check if arr[counter] is a key in `h`. If yes, increment the attached value. If no, make it a key and set value to 1.
6. Print the keys and values of the hash.

*Code:*

```ruby
def count_occurrences(arr)
  h = {}
  counter = 0
  loop do
    break if counter == arr.size
    if h.has_key?(arr[counter])
      h[arr[counter]] += 1
    else
      h[arr[counter]] = 1
    end
    counter += 1
  end
  h.each { |key, value| puts "#{key} => #{value}" }
end

vehicles = [
  'car', 'car', 'truck', 'car', 'SUV', 'truck',
  'motorcycle', 'motorcycle', 'car', 'truck'
]

count_occurrences(vehicles)
```

Here's another implementation making good use of `Array#uniq`: 

```ruby
def count_occurrences(array)
  occurrences = {}

  array.uniq.each do |element|
    occurrences[element] = array.count(element)
  end

  occurrences.each do |element, count|
    puts "#{element} => #{count}"
  end
end
```

