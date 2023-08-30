
**Lesson 9: Regular Expressions**

**1. Introduction to Regular Expressions**
Regular expressions (regex or regexp) are powerful patterns used for string matching and manipulation. They're widely used for tasks like validation, searching, and text manipulation.

**2. Creating Regular Expressions**
Regular expressions are defined using a combination of characters that define a specific pattern. For example:

```ruby
pattern = /ruby/
```

**3. Matching Patterns**
You can use the `=~` operator to check if a string matches a pattern:

```ruby
text = "Hello, Ruby programming is fun!"
pattern = /Ruby/

if text =~ pattern
  puts "Pattern found!"
else
  puts "Pattern not found."
end
```

**4. Character Classes**
Character classes match specific sets of characters:

- `[aeiou]`: Matches any vowel.
- `[0-9]`: Matches any digit.

**5. Anchors**
Anchors match positions within a string:

- `^`: Matches the start of a line.
- `$`: Matches the end of a line.

**6. Quantifiers**
Quantifiers define how many times a pattern should occur:

- `*`: Matches zero or more occurrences.
- `+`: Matches one or more occurrences.
- `?`: Matches zero or one occurrence.

**7. Groups and Capture**
Groups allow you to capture and manipulate parts of a matched string:

```ruby
text = "My phone number is 555-1234."
pattern = /(\d{3})-(\d{4})/

if match = text.match(pattern)
  puts "Area code: #{match[1]}"
  puts "Local number: #{match[2]}"
end
```

**8. Substitution**
You can use regular expressions for text substitution:

```ruby
text = "Hello, world!"
pattern = /world/
replacement = "Ruby"

new_text = text.gsub(pattern, replacement)
puts new_text  # Output: Hello, Ruby!
```

**Code Sample: regular_expressions.rb**
Here's a code sample to practice regular expressions:

```ruby
text = "Email me at john@example.com or jane@example.com."

# Match email addresses
pattern = /\w+@\w+\.\w+/
matches = text.scan(pattern)
puts matches.inspect

# Substitute email addresses
masked_text = text.gsub(pattern, "[email]")
puts masked_text
```
