**Lesson 1: Introduction to Ruby**

**1. What is Ruby?**
Ruby is a dynamic, object-oriented programming language known for its elegant syntax and focus on programmer happiness. It's widely used for web development, scripting, and more.

**2. Getting Started**
To start coding in Ruby, you'll need to have Ruby installed on your computer. Visit the [official Ruby website](https://www.ruby-lang.org/en/documentation/installation/) for installation instructions.

**3. Hello, Ruby!**
Let's write your first Ruby program. Create a file named `hello.rb` with the following content:

```ruby
puts "Hello, Ruby!"
```

Open your terminal, navigate to the folder containing `hello.rb`, and run the program with the command:

```bash
ruby hello.rb
```

You should see the output: `Hello, Ruby!`

**Lesson 2: Variables and Data Types**

**1. Variables**
Variables allow you to store and manipulate data. In Ruby, you don't need to declare their types explicitly. Here's an example:

```ruby
name = "Alice"
age = 30
```

**2. Data Types**
Ruby has various data types:

- Integers: Whole numbers (e.g., `5`, `-23`).
- Floats: Numbers with decimal points (e.g., `3.14`, `-0.5`).
- Strings: Text (e.g., `"hello"`, `'Ruby'`).
- Booleans: `true` or `false`.
- Symbols: Immutable identifiers (e.g., `:apple`, `:banana`).
- Arrays: Ordered lists (e.g., `[1, 2, 3]`).
- Hashes: Key-value pairs (e.g., `{ "name" => "Alice", "age" => 30 }`).

**3. Variable Interpolation**
You can insert variable values into strings using string interpolation:

```ruby
name = "Bob"
puts "Hello, #{name}!"
```

**4. Type Conversion**
You can convert between data types using methods like `to_i`, `to_f`, `to_s`.

**Code Sample: variables.rb**
Here's a simple code sample to experiment with variables and data types:

```ruby
# Variable assignment
name = "Alice"
age = 30

# Variable interpolation
greeting = "Hello, #{name}!"
puts greeting

# Type conversion
number_string = "42"
number = number_string.to_i
puts number * 2
```
