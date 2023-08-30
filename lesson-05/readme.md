**Lesson 5: c**

**1. Introduction to Methods**
Methods (also known as functions) allow you to group code into reusable blocks. They help keep your code organized and promote the "Don't Repeat Yourself" (DRY) principle.

**2. Defining and Calling Methods**
Here's how you define and call a method in Ruby:

```ruby
# Method definition
def greet(name)
  puts "Hello, #{name}!"
end

# Method call
greet("Alice")  # Output: Hello, Alice!
```

**3. Return Values**
Methods can also return values:

```ruby
def add(a, b)
  return a + b
end

result = add(3, 5)
puts result  # Output: 8
```

**4. Default Parameters**
You can set default values for method parameters:

```ruby
def greet(name = "Guest")
  puts "Hello, #{name}!"
end

greet  # Output: Hello, Guest!
greet("Bob")  # Output: Hello, Bob!
```

**5. Variable Scope**
Variables defined within a method are local to that method. They can't be accessed from outside.

**6. The `return` Keyword**
Methods automatically return the result of the last expression evaluated. You can also use the `return` keyword explicitly.

**7. Built-in Methods**
Ruby comes with a variety of built-in methods. For example:

```ruby
text = "Hello, Ruby!"

puts text.upcase       # Output: HELLO, RUBY!
puts text.length       # Output: 12
puts text.include?("Ruby")  # Output: true
```

**8. Method Naming Conventions**
Use snake_case for method names (e.g., `calculate_tax`) and question marks for methods that return boolean values (e.g., `valid?`).

**Code Sample: methods_and_functions.rb**
Here's a code sample to practice methods and functions:

```ruby
# Method definition
def square(x)
  return x * x
end

# Method call
result = square(4)
puts result  # Output: 16

# Default parameters
def greet(name = "User")
  puts "Hello, #{name}!"
end

greet  # Output: Hello, User!
greet("Charlie")  # Output: Hello, Charlie!

# Built-in methods
text = "Ruby is fun!"
puts text.upcase     # Output: RUBY IS FUN!
puts text.length     # Output: 13
puts text.include?("fun")  # Output: true
```
