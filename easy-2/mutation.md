# Mutation

**What will the following code print, and why? Don't run the code until you have tried to answer.**

```ruby
array1 = %w(Moe Larry Curly Shemp Harpo Chico Groucho Zeppo)
array2 = []
array1.each { |value| array2 << value }
array1.each { |value| value.upcase! if value.start_with?('C', 'S') }
puts array2
```

---

In this code, `array2` will be altered to include every element of `array1`, because `<<` is a destructive method that, when combined with `Array#each`, will add each element of `array1` into `array2`. 

Then, `array1` will be run through again using `Array#each`, this time destructively changing each value that starts with a `'C'` or `'S'` to be entirely upcase. The values in both arrays are, in fact, the exact same String objects, so a destructive change to one will be reflected in both arrays. Therefore, `puts array2` will output:

```
Moe
Larry
CURLY
SHEMP
Harpo
CHICO
Groucho
Zeppo
```

