**Lesson 11: Working with Databases**

**1. Introduction to Databases**
Databases are crucial for storing and managing structured data in applications. Ruby provides various libraries and frameworks for interacting with databases.

**2. SQLite Database**
SQLite is a lightweight and self-contained database engine. You can use it with Ruby through the `sqlite3` gem.

**3. Connecting to a Database**
Here's how you can connect to an SQLite database and execute SQL queries:

```ruby
require 'sqlite3'

db = SQLite3::Database.new("mydatabase.db")

# Create a table
db.execute("CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)")

# Insert data
db.execute("INSERT INTO users (name, age) VALUES (?, ?)", ["Alice", 30])

# Query data
users = db.execute("SELECT * FROM users")
puts users.inspect
```

**4. ORM: ActiveRecord**
ActiveRecord is a popular Object-Relational Mapping (ORM) library that simplifies database interaction. It's commonly used with the Ruby on Rails framework.

**5. Connecting with ActiveRecord**
To use ActiveRecord, you need to define models that correspond to database tables:

```ruby
require 'active_record'

# Configure database connection
ActiveRecord::Base.establish_connection(
  adapter: 'sqlite3',
  database: 'mydatabase.db'
)

# Define a model
class User < ActiveRecord::Base
end

# Create a new user
User.create(name: "Bob", age: 25)

# Query users
users = User.all
puts users.inspect
```

**6. Migrations**
Migrations allow you to manage changes to your database schema over time:

```ruby
class CreatePosts < ActiveRecord::Migration[6.0]
  def change
    create_table :posts do |t|
      t.string :title
      t.text :content
      t.timestamps
    end
  end
end
```

**Code Sample: working_with_databases.rb**
Here's a code sample to practice working with databases using SQLite and ActiveRecord:

```ruby
require 'sqlite3'
require 'active_record'

# SQLite database
db = SQLite3::Database.new("mydatabase.db")
db.execute("CREATE TABLE IF NOT EXISTS students (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)")

db.execute("INSERT INTO students (name, age) VALUES (?, ?)", ["Alice", 20])
db.execute("INSERT INTO students (name, age) VALUES (?, ?)", ["Bob", 22])

students = db.execute("SELECT * FROM students")
puts students.inspect

# ActiveRecord
ActiveRecord::Base.establish_connection(
  adapter: 'sqlite3',
  database: 'mydatabase.db'
)

class Student < ActiveRecord::Base
end

Student.create(name: "Charlie", age: 23)
Student.create(name: "Diana", age: 21)

students = Student.all
puts students.inspect
```

