**Lesson 7: File Input and Output (File I/O)**

**1. Reading Files**
File I/O is the process of reading from and writing to files. Ruby provides simple and powerful methods to interact with files. Let's start with reading from a file:

```ruby
# Create a file named 'example.txt' with some text content.
File.open("example.txt", "w") do |file|
  file.puts "Hello, Ruby!"
  file.puts "File I/O is fun!"
end

# Read from the file
File.open("example.txt", "r") do |file|
  content = file.read
  puts content
end
```

**2. Writing to Files**
You can write data to a file using the `puts` method or other methods like `write`:

```ruby
File.open("output.txt", "w") do |file|
  file.puts "This is a line of text."
  file.puts "Writing to files is easy!"
end
```

**3. File Modes**
When opening files, you can specify different modes:
- `"r"`: Read (default)
- `"w"`: Write (creates a new file or truncates an existing file)
- `"a"`: Append (creates a new file or appends to an existing file)

**4. Handling File Exceptions**
Always handle potential exceptions when working with files. You can use `begin` and `rescue` blocks to catch exceptions and provide fallback behavior.

**5. File Manipulation with `File` Class**
The `File` class provides various methods to manipulate files, including renaming, deleting, and checking for existence.

**Code Sample: file_io.rb**
Here's a code sample to practice file input and output:

```ruby
# Writing to a file
File.open("my_file.txt", "w") do |file|
  file.puts "Line 1"
  file.puts "Line 2"
end

# Reading from a file
File.open("my_file.txt", "r") do |file|
  content = file.read
  puts content
end
```

**Next Steps**
File I/O is a crucial skill for working with external data and storing program outputs. As you continue learning, you can explore more advanced topics like error handling, working with different file formats (e.g., CSV, JSON), and managing larger data sets.
