# Tip calculator

**Create a simple tip calculator. The program should prompt for a bill amount and a tip rate. The program must compute the tip and then display both the tip and the total amount of the bill.**

**Example:**

```plaintext
What is the bill? 200
What is the tip percentage? 15

The tip is $30.0
The total is $230.0
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: Bill amount and tip rate

Output: Tip (float) and total bill (float) (both rounded to one decimal place)

*Problem Domain:*

No definitions needed.

*Implicit Requirements:*

None.

*Clarifying Questions:*

1. Is input validation needed?
2. Is it required to round both to one decimal place?

*Mental Model:*

Ask the user for the bill and the tip percentage. Multiply the bill by the tip percentage / 100. Save this total, and add it to the bill total. Return both values interpolated in strings.

*Examples/Test Cases/Edge Cases:*

```
What is the bill? 200
What is the tip percentage? 15

The tip is $30.0
The total is $230.0
```

*Data Structures:*

None other than strings needed.

*Algorithm:*

1. Using `gets.chomp.to_f`, ask for and save the `bill` and `tip_percent`.
2. Define a new variable named `tip`, and set it equal to `(bill *  (tip_percent / 100)).round(1)`.
3. `puts` this tip using string interpolation.
4. Define another local variable, `total`, and set it equal to `(bill + tip).round(1)`.
5. `puts` this using string interpolation also.

*Code:*

```ruby
puts "What is the bill?"
bill = gets.chomp.to_f
puts "What is the tip percentage?"
tip_percent = gets.chomp.to_f

tip = (bill * (tip_percent/100)).round(1)
total = (bill + tip).round(1)

puts "The tip is $#{tip}"
puts "The total is $#{total}"
```

---

#### Further Exploration

**Our solution prints the results as `$30.0` and `$230.0` instead of the more usual `$30.00` and `$230.00`. Modify your solution so it always prints the results with 2 decimal places.**

**Hint: You will likely need `Kernel#format` for this.**

---

Note: The original solution had the rounding set to two decimal places. That will be reflected here as well.

```ruby
puts "What is the bill?"
bill = gets.chomp.to_f
puts "What is the tip percentage?"
tip_percent = gets.chomp.to_f

tip = (bill * (tip_percent/100)).round(2)
total = (bill + tip).round(2)

puts "The tip is #{sprintf("%.2f", tip)}"
puts "The total is #{sprintf("%.2f", total)}"
```

