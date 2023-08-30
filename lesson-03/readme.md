**Lesson 3: Control Flow and Loops**

**1. Conditional Statements**
Conditional statements allow you to make decisions in your code. The most common type is the `if` statement:

```ruby
age = 18

if age >= 18
  puts "You're an adult."
else
  puts "You're a minor."
end
```

You can also use `elsif` for multiple conditions.

**2. Comparison Operators**
Comparison operators help in making comparisons:

- `==`: Equal to
- `!=`: Not equal to
- `<`: Less than
- `>`: Greater than
- `<=`: Less than or equal to
- `>=`: Greater than or equal to

**3. Logical Operators**
Logical operators allow you to combine conditions:

- `&&` (AND)
- `||` (OR)
- `!` (NOT)

**4. Loops**
Loops help you repeat code. The `while` loop runs while a condition is true:

```ruby
count = 1

while count <= 5
  puts "Count: #{count}"
  count += 1
end
```

The `for` loop iterates over a range:

```ruby
for num in 1..5
  puts "Number: #{num}"
end
```

**5. Arrays and Iteration**
Arrays are lists of items. You can iterate over them using loops:

```ruby
fruits = ["apple", "banana", "orange"]

fruits.each do |fruit|
  puts "I like #{fruit}s!"
end
```

**6. Case Statement**
A `case` statement is used for multi-way conditionals:

```ruby
grade = "B"

case grade
when "A"
  puts "Excellent!"
when "B"
  puts "Good!"
when "C"
  puts "Average."
else
  puts "Needs Improvement."
end
```

**Code Sample: control_flow_and_loops.rb**
Here's a simple code sample to experiment with control flow and loops:

```ruby
# Conditional statements
temperature = 25

if temperature > 30
  puts "It's hot outside."
elsif temperature > 20
  puts "It's warm outside."
else
  puts "It's cool outside."
end

# Loop with each
numbers = [1, 2, 3, 4, 5]

numbers.each do |number|
  puts "Squared: #{number * number}"
end

# Case statement
role = "admin"

case role
when "admin"
  puts "Welcome, Admin!"
when "user"
  puts "Hello, User!"
else
  puts "Access Denied."
end
```

