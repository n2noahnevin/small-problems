# How big is the room?

**Build a program that asks a user for the length and width of a room in meters and then displays the area of the room in both square meters and square feet.**

**Note: 1 square meter == 10.7639 square feet**

**Do not worry about validating the input at this time.**

**Example Run:**

```plaintext
Enter the length of the room in meters:
10
Enter the width of the room in meters:
7
The area of the room is 70.0 square meters (753.47 square feet).
```

---

*(Understanding the) Problem:*

*Input/Output:*

Input: length and width from user

Output: area in square methers and square feet

*Problem Domain:*

1 Square Meter: Equal to 10.7639 square feet.

Area: Length * Width

*Implicit Requirements:*

None.

*Clarifying Questions:*

1. Do the totals need to be rounded to 2 decimal places?

*Mental Model:*

Ask the user for the length and the width of the room in meters. Save these into variables. Multiply these together to get the square meters and save this into a variable. Convert this into square meters and save into another variable. Output the two square results into a `puts` statement.

*Examples/Test Cases/Edge Cases:*

```
Enter the length of the room in meters:
10
Enter the width of the room in meters:
7
The area of the room is 70.0 square meters (753.47 square feet).
```

*Data Structures:*

None needed other than strings.

*Algorithm:*

1. Ask the user to input length in meters. Save it using `gets.chomp`. Do the same for width. Set the variables to be floats with `to_f`.
2. Define a new local variable `meter_area` and set it equal to `length * width`.
3. Define another local variable `feet_area`, and set it equal to `meter_area * 10.7639`.
4. `puts` out the values.

*Code:*

```ruby
METERS_TO_FEET = 10.7639

puts "Enter the length of the room in meters:"
length = gets.chomp.to_f
puts "Enter the width of the room in meters:"
width = gets.chomp.to_f

meter_area = (length * width).round(2)
feet_area = (meter_area * METERS_TO_FEET).round(2)

puts "The area of the room is #{meter_area} square meters (#{feet_area} square feet)."
```

Note: It is good practice to store the conversion number into a constant.

---

#### Further Exploration

**Modify this program to ask for the input measurements in feet, and display the results in square feet, square inches, and square centimeters.**

---

```ruby
FEET_TO_INCH = 144
INCH_TO_CM = 6.4516

puts "Enter the length of the room in feet:"
length = gets.chomp.to_f
puts "Enter the width of the room in feet:"
width = gets.chomp.to_f

feet_area = (length * width).round(2)
inch_area = (feet_area * FEET_TO_INCH).round(2)
cm_area = (inch_area * INCH_TO_CM).round(2)

puts "The area of the room is #{feet_area} square feet (#{inch_area} square inches, or #{cm_area} square centimeters)."
```

