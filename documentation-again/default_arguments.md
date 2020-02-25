# Default Arguments in the Middle

**Consider the following method and a call to that method:**

```ruby
def my_method(a, b = 2, c = 3, d)
  p [a, b, c, d]
end

my_method(4, 5, 6)
```

**Use the ruby documentation to determine what this code will print.**

---

In this code, my_method is a method definition that takes in four arguments, with arguments b and c having default values. when my_method is invocated, three arguments are given to it. The method will see the variables as such:

1. `a = 4`, first argument given
2. `b = 5`, given argument overrides default
3. `c = 3`, because only three arguments are given, c stays as its default value
4. `d = 6`, the last argument given

Therefore, the program will print:

`[4, 5, 3, 6]`

