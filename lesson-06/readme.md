**Lesson 6: Object-Oriented Programming (OOP)**

**1. Introduction to Object-Oriented Programming**
Object-Oriented Programming (OOP) is a programming paradigm that revolves around the concept of objects, which are instances of classes. OOP promotes code organization, modularity, and reusability.

**2. Classes and Objects**
A class is a blueprint for creating objects. An object is an instance of a class. Let's create a simple class:

```ruby
class Dog
  def initialize(name, age)
    @name = name
    @age = age
  end

  def bark
    puts "#{@name} says Woof!"
  end
end

# Creating objects
dog1 = Dog.new("Buddy", 3)
dog2 = Dog.new("Charlie", 5)

# Calling methods
dog1.bark  # Output: Buddy says Woof!
dog2.bark  # Output: Charlie says Woof!
```

**3. Instance Variables**
Instance variables (prefixed with `@`) store object-specific data. They're accessible within methods of the class.

**4. Accessors and Getters/Setters**
Accessors (`attr_reader`, `attr_writer`, `attr_accessor`) simplify working with instance variables by generating getter and setter methods.

**5. Inheritance**
Inheritance allows a class to inherit attributes and methods from another class. The subclass can override or extend inherited methods:

```ruby
class Puppy < Dog
  def bark
    puts "#{@name} says Yip!"
  end
end

puppy = Puppy.new("Max", 1)
puppy.bark  # Output: Max says Yip!
```

**6. Polymorphism**
Polymorphism allows objects of different classes to be treated as objects of a common superclass:

```ruby
class Cat
  def make_sound
    puts "Meow!"
  end
end

class Cow
  def make_sound
    puts "Moo!"
  end
end

def animal_sound(animal)
  animal.make_sound
end

cat = Cat.new
cow = Cow.new

animal_sound(cat)  # Output: Meow!
animal_sound(cow)  # Output: Moo!
```

**Code Sample: object_oriented_programming.rb**
Here's a code sample to practice object-oriented programming:

```ruby
class Car
  def initialize(make, model)
    @make = make
    @model = model
  end

  def info
    puts "#{@make} #{@model}"
  end
end

car1 = Car.new("Toyota", "Corolla")
car2 = Car.new("Honda", "Civic")

car1.info  # Output: Toyota Corolla
car2.info  # Output: Honda Civic
```
