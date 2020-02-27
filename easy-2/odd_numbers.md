# Odd Numbers

**Print all odd numbers from 1 to 99, inclusive. All numbers should be printed on separate lines.**

---

*(Understanding the) Problem:*

*Input/Output:*

Input: No input.

Output: Strings output to screen.

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

None.

*Mental Model:*

Create a counter and a loop, and start the counter at 1. Print the counter whenever `counter.odd?`. Break the loop when counter equals 100.

*Examples/Test Cases/Edge Cases:*

```
1
3
5
7
9
etc...
```

*Data Structures:*

Just strings.

*Algorithm:*

1. Define a variable, `counter`, and set it equal to `1`. Begin a `loop`.
2. `puts counter if counter.odd?`.
3. `counter += 1`
4. `break if counter == 100`.

*Code:*

```ruby
counter = 1
loop do
  puts counter if counter.odd?
  counter += 1
  break if counter == 100
end
```



