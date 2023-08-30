**Lesson 4: Arrays and Hashes**

**1. Arrays**
Arrays are ordered collections of items. They can hold any data type, including other arrays or hashes. Here's how you create and work with arrays:

```ruby
fruits = ["apple", "banana", "orange"]

# Accessing elements
puts fruits[0]  # Output: apple

# Adding elements
fruits.push("grape")
fruits << "kiwi"

# Iterating over an array
fruits.each do |fruit|
  puts "I love #{fruit}s!"
end
```

**2. Hashes**
Hashes are collections of key-value pairs. They're often used to represent structured data. Here's how you create and work with hashes:

```ruby
person = {
  "name" => "Alice",
  "age" => 30,
  "occupation" => "developer"
}

# Accessing values
puts person["name"]  # Output: Alice

# Adding or updating key-value pairs
person["location"] = "New York"
person["age"] = 31

# Iterating over a hash
person.each do |key, value|
  puts "#{key}: #{value}"
end
```

**3. Array Methods**
Arrays have useful methods like `length`, `first`, `last`, and `include?`:

```ruby
numbers = [2, 4, 6, 8, 10]

puts numbers.length    # Output: 5
puts numbers.first     # Output: 2
puts numbers.last      # Output: 10
puts numbers.include?(5)  # Output: false
```

**4. Hash Methods**
Hashes also have helpful methods like `keys`, `values`, and `has_key?`:

```ruby
grades = {
  "Math" => "A",
  "Science" => "B",
  "History" => "C"
}

puts grades.keys     # Output: ["Math", "Science", "History"]
puts grades.values   # Output: ["A", "B", "C"]
puts grades.has_key?("English")  # Output: false
```

**5. Nested Structures**
You can have arrays of hashes or hashes of arrays for more complex data structures:

```ruby
students = [
  { "name" => "Alice", "age" => 25 },
  { "name" => "Bob", "age" => 30 }
]

book = {
  "title" => "Ruby Programming",
  "authors" => ["Alice", "Bob"],
  "chapters" => 10
}
```

**Code Sample: arrays_and_hashes.rb**
Here's a code sample to practice arrays and hashes:

```ruby
# Arrays
colors = ["red", "green", "blue"]
colors.push("yellow")
puts colors.length   # Output: 4

# Hashes
person = {
  "name" => "Eve",
  "age" => 28
}
person["location"] = "San Francisco"
puts person["age"]  # Output: 28

# Nested structures
students = [
  { "name" => "Charlie", "age" => 22 },
  { "name" => "Diana", "age" => 27 }
]
puts students[1]["name"]  # Output: Diana
```

**Next Steps**
Arrays and hashes are fundamental for storing and organizing data. Practice creating and manipulating arrays and hashes to build your understanding. In the next lesson, we'll dive into methods and functions, which will allow you to organize and reuse your code more effectively.
