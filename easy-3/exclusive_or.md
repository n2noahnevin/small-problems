# Exclusive Or

**The `||` operator returns a truthy value if either or both of its operands are truthy, a falsey value if both operands are falsey. The `&&` operator returns a truthy value if both of its operands are truthy, and a falsey value if either operand is falsey. This works great until you need only one of two conditions to be truthy, the so-called *exclusive or*.**

**In this exercise, you will write a method named `xor` that takes two arguments, and returns `true` if exactly one of its arguments is truthy, `false` otherwise.**

**Examples:**

```ruby
xor?(5.even?, 4.even?) == true
xor?(5.odd?, 4.odd?) == true
xor?(5.odd?, 4.even?) == false
xor?(5.even?, 4.odd?) == false
```

---

Note: For the sake of time, the PEDAC process will be skipped over for this example.

*Code:*

```ruby
def xor?(num1, num2)
  (num1 && !num2) || (!num1 && num2)
end

xor?(5.even?, 4.even?) == true
xor?(5.odd?, 4.odd?) == true
xor?(5.odd?, 4.even?) == false
xor?(5.even?, 4.odd?) == false
```

