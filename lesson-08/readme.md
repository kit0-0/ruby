**Lesson 8: Exception Handling**

**1. Introduction to Exceptions**
Exceptions are errors that occur during program execution. Exception handling allows you to gracefully handle these errors, preventing your program from crashing.

**2. `begin`, `rescue`, and `end`**
You can use a `begin` block to wrap the code that might raise an exception. The `rescue` block catches the exception and provides a way to handle it:

```ruby
begin
  result = 10 / 0
rescue ZeroDivisionError
  puts "Division by zero error!"
end
```

**3. Handling Multiple Exceptions**
You can handle different exceptions in separate `rescue` blocks or use a single `rescue` block with multiple exception types:

```ruby
begin
  # Code that might raise an exception
rescue ZeroDivisionError
  # Handle division by zero error
rescue TypeError, ArgumentError
  # Handle other specific errors
end
```

**4. `ensure`**
The `ensure` block is used to specify code that will run regardless of whether an exception was raised:

```ruby
begin
  # Code that might raise an exception
rescue SomeException
  # Handle the exception
ensure
  # Code that will run regardless
end
```

**5. `raise`**
You can use the `raise` keyword to manually raise an exception:

```ruby
def sqrt(number)
  raise "Negative number not allowed" if number < 0
  Math.sqrt(number)
end

puts sqrt(16)  # Output: 4.0
puts sqrt(-9)   # Raises an exception
```

**6. Custom Exceptions**
You can define custom exception classes by subclassing `StandardError`:

```ruby
class CustomError < StandardError
  def initialize(message = "A custom error occurred")
    super(message)
  end
end

begin
  raise CustomError.new("This is a custom error message.")
rescue CustomError => e
  puts "Caught exception: #{e.message}"
end
```

**Code Sample: exception_handling.rb**
Here's a code sample to practice exception handling:

```ruby
def divide(a, b)
  begin
    result = a / b
  rescue ZeroDivisionError
    puts "Division by zero error!"
  else
    puts "Result: #{result}"
  end
end

divide(10, 2)   # Output: Result: 5
divide(8, 0)    # Output: Division by zero error!
```

**Next Steps**
Exception handling is crucial for building robust and reliable programs. As you continue learning, you can explore more advanced topics like creating custom exception classes, logging errors, and handling exceptions in different parts of your code.
