**Lesson 12: Advanced Topics**

**1. Metaprogramming**
Metaprogramming is the practice of writing code that manipulates code itself. In Ruby, you can dynamically create classes, methods, and modify behavior at runtime. While powerful, metaprogramming can make code harder to understand and maintain if used excessively.

**2. Dynamic Method Definitions**
You can define methods dynamically using the `define_method` method:

```ruby
class MyClass
  define_method :dynamic_method do
    puts "This method was defined dynamically."
  end
end

my_instance = MyClass.new
my_instance.dynamic_method  # Output: This method was defined dynamically.
```

**3. Open Classes and Monkey Patching**
In Ruby, you can modify existing classes and add methods to them. This practice is known as "monkey patching." While it offers flexibility, it can also lead to unexpected behavior and conflicts.

```ruby
class String
  def reverse_and_upcase
    self.reverse.upcase
  end
end

puts "hello".reverse_and_upcase  # Output: OLLEH
```

**4. Reflection**
Reflection allows you to examine and modify the structure of classes and objects at runtime. Ruby provides methods like `class`, `methods`, and `instance_variables` for introspection.

```ruby
class MyClass
  attr_accessor :name

  def initialize
    @name = "Alice"
  end
end

obj = MyClass.new
puts obj.class  # Output: MyClass
puts obj.methods  # Output: List of methods
puts obj.instance_variables  # Output: List of instance variables
```

**5. Multithreading and Concurrency**
Ruby supports multithreading, which allows multiple threads to run concurrently. However, due to the Global Interpreter Lock (GIL), Ruby threads are limited in their ability to take full advantage of multiple processor cores. For CPU-bound tasks, consider using multiprocessing or other languages.

**6. Performance Optimization**
Ruby offers several techniques for optimizing code performance:
- Using built-in methods (e.g., `map`, `reduce`) for efficiency.
- Avoiding unnecessary method calls and object creation.
- Using the `Benchmark` module to measure execution time.

**7. Code Profiling**
Code profiling helps identify bottlenecks and performance issues in your code. The `ruby-prof` gem provides a tool for profiling Ruby code.

**8. Garbage Collection**
Ruby's garbage collector automatically reclaims memory used by objects that are no longer accessible. Understanding how the garbage collector works can help optimize memory usage in your applications.

**9. Error Handling and Exceptions**
In addition to the basics of exception handling covered earlier, advanced topics include structured error handling using the `begin...ensure...else...ensure` construct, custom exception classes, and exception chaining.

**Code Sample: Dynamic Method Definitions and Metaprogramming**
Here's an example of using dynamic method definitions and metaprogramming:

```ruby
class DynamicMethodsExample
  METHODS = ['foo', 'bar', 'baz']

  METHODS.each do |method_name|
    define_method method_name do
      puts "Dynamic method: #{method_name}"
    end
  end
end

instance = DynamicMethodsExample.new
instance.foo  # Output: Dynamic method: foo
instance.bar  # Output: Dynamic method: bar
```

**Next Steps**
Advanced topics in Ruby open up opportunities for powerful and flexible programming. However, they also come with greater complexity and potential pitfalls. As you continue learning, you can explore more advanced topics like building domain-specific languages (DSLs), exploring low-level Ruby implementation details, and diving deeper into specific performance optimization strategies.
