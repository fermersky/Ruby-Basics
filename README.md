# Ruby-Basics

* Variables and Data Types
```ruby
a = 5 # int
b = 5.34 # float
name = "Daniel" # string
isMale = true # boolean
a_symbol = :itsasymbol # symbol
```
* conditional statement
```ruby
if a > b
  puts "yeap"
elsif a < b
  # puts "nope"
else
  puts "equal"
end
```

* loops
```ruby
# while loop
num = 0
while num < 10
  num += 1
  #puts num
end

# for loop
for num in 1...10
  # puts num
end

# each lopp
[23, 1, 7, 62, 12].each do |num|
  # print "#{num} "
end
```
* Arrays and hash table
```ruby
# Arrays
array = [1,2,3,4,5]
names = [
  "Daniel",
  "Alina",
  "Nastya"
]
names.push("Yarik");
names << "Serega" # equal to names.<<("Serega")

# Key-Value
simple_hash = {
  "name" => "Daniel",
  "about" => "is a handsome fellow"
}
simple_hash["age"] = 18 # dynamicly add new key-value ^-^
puts "#{simple_hash["name"]} #{simple_hash["about"]} #{simple_hash["age"]}"

# each loop for hash table
simple_hash.each do |key, value|
  # puts "key - #{key}; value - #{value}"
end

```
* Classes
```ruby
class Vehicle
  attr_reader :mark # only for read
  attr_writer :model # only for write
  attr_accessor :count # both

  def initialize(mark, model, count) # constructor
    @mark = mark
    @model = model
    @count = count
  end
end

veh = Vehicle.new("Audi", "RS8", 4) # creat instance of class
veh.model = "Bmw"
# puts veh.mark

module Skills
  def speedUp
    puts "Fastest man in the World"
  end

  # A module can have no instances.
  # A module can have no subclasses.
end

class Person
  include Skills # using module

  def initialize(name, age)
    @name = name
    @age = age
  end

  def name # getter
    @name
  end

  def age # getter
    @age
  end

  def isDaniel # method of class
    if @name == "Daniel"
      true # return true ^-^
    else
      false
    end
  end

  def to_s
    "#{name} #{age}"
  end
end

per = Person.new("Daniel", 18)
per.speedUp
puts per.to_s
```
