# Class and Instance Methods

### Locate the ruby documentation for methods File::path and File#path. How are they different? ###

File::path returns the string representation of the path. This is a class method, so it is called on the class:

```ruby
File.path('str')
```

File#path is an instance function, so it is called on an instance of File.

```ruby
f = File.new('file.txt')
puts f.path
```



