**Lesson 10: Working with JSON**

**1. Introduction to JSON**
JSON (JavaScript Object Notation) is a lightweight data interchange format used to store and exchange data between systems. Ruby provides built-in support for working with JSON.

**2. JSON Basics**
JSON data consists of key-value pairs enclosed in curly braces `{}`. Keys are strings, and values can be strings, numbers, booleans, arrays, or other objects.

```json
{
  "name": "Alice",
  "age": 30,
  "is_student": false,
  "hobbies": ["reading", "painting"],
  "address": {
    "city": "New York",
    "zip": "10001"
  }
}
```

**3. Converting JSON**
You can convert Ruby objects to JSON using the `JSON` module:

```ruby
require 'json'

data = {
  "name" => "Bob",
  "age" => 25,
  "is_student" => true
}

json_data = data.to_json
puts json_data
```

**4. Parsing JSON**
You can parse JSON strings into Ruby objects:

```ruby
json_string = '{"title": "Book", "price": 10}'
parsed_data = JSON.parse(json_string)
puts parsed_data["title"]  # Output: Book
```

**5. Nested JSON**
JSON can represent complex nested structures:

```ruby
json_string = '{
  "name": "Eve",
  "address": {
    "city": "San Francisco",
    "zip": "94101"
  }
}'
parsed_data = JSON.parse(json_string)
puts parsed_data["address"]["city"]  # Output: San Francisco
```

**6. Reading and Writing JSON Files**
You can read JSON data from files and write JSON data to files:

```ruby
require 'json'

# Reading JSON from a file
file_content = File.read('data.json')
parsed_data = JSON.parse(file_content)

# Writing JSON to a file
data_to_write = { "name" => "Charlie", "age" => 28 }
File.open('output.json', 'w') do |file|
  file.write(data_to_write.to_json)
end
```

**Code Sample: json_handling.rb**
Here's a code sample to practice working with JSON:

```ruby
require 'json'

# Convert Ruby object to JSON
data = {
  "name" => "Alice",
  "age" => 30,
  "hobbies" => ["reading", "painting"]
}

json_data = data.to_json
puts json_data

# Parse JSON to Ruby object
json_string = '{"title": "Movie", "genre": "Drama"}'
parsed_data = JSON.parse(json_string)
puts parsed_data["title"]

# Read and write JSON files
file_content = File.read('data.json')
parsed_data = JSON.parse(file_content)

data_to_write = { "name" => "Bob", "age" => 25 }
File.open('output.json', 'w') do |file|
  file.write(data_to_write.to_json)
end
```
