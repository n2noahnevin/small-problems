# Mandatory Blocks

**The `Array#bsearch` method is used to search ordered `Array`s more quickly than `#find` and `#select` can. Assume you have the following code:**

```ruby
a = [1, 4, 8, 11, 15, 19]
```

**How would you search this `Array` to find the first element whose value exceeds `8`?**

---

`Array#bsearch` is a method that utilizes the quicker binary search in order to search an ordered array. Looking at the Ruby Docs, in order to find the first element whose value exceeds `8`, this instance method can be invocated as such:

`arr.bsearch { |num| num > 8 }`

This will return `11`, since it is the first value in the array greater than 8. 

