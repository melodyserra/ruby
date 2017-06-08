# Intro to Ruby

## Install Software

#### Install RVM

`\curl -sSL https://get.rvm.io | bash -s stable`

#### Install Ruby

`rvm install ruby --disable-binary`

#### Check Installation

`ruby -v`

#### Install Rails

`gem install rails`

## The Ruby Language

- To practice using Ruby we can use the Interactive Ruby (IRB) tool.
- Everything is an object.
- Everything that is manipulated is an object, and the results of those manipulations are objects.
- In Ruby everything is an object and you'll be able to use object methods on it all.

Let's take a look at some examples:

```
puts "Melody Serra".length
puts "Melody".index("M")
puts 35.even?
```

- We can tell that everything is an object, because everything has a "class":

```
"Melody Serra".class #String
4.class #Fixnum
[].class #Array
Object.class #Class
```

- Something like this `message = "Hello World"` is essentially the equivalent of `message = String.new("Hello World")`.

- There is little conversion of type:

#### JS

console.log("Hello " + 4 + 2); //Hello 42

#### Ruby
```
puts "Hello " + 4 + 2 #no implicit conversion of Fixnum into String
```

## Modules Versus Objects

#### Modules
- Modules are like libraries.
- Usually used for containing a bunch of "helper" functions that you can call throughout your program.
- Great example is the [Math module](http://www.ruby-doc.org/core-2.1.4/Math.html) built into Ruby:

```
Math.sqrt(9) #3.0
```

#### Objects
- Ruby is a proper object-oriented language.
- "Classes" wrap methods that are related to that object.
- Instead of prototypes in JS that relate to some object, we have classes that encapsulate methods.
- Classes can also inherit from other classes - this is called extension.

## Control Flow in Ruby
- Controlling the flow of your application is crucial because it allows you to perform actions only under certain conditions.
- Control flow often involves the use of "conditional" statements such as `if` - `else` blocks and the use of loops such as `for` and `while`.

#### `if` statements

```ruby
yes =  true

if yes
	puts "Indeed!"
end
```

#### `if` - `else` blocks:

```ruby
name = "Melody"
if name == "Bob"
	puts "Hello Bob"
elsif name == "John"
	puts "Hello John"
else
	puts "Hello Someone"
end
```

- Code inside a block is only executed when the condition is met.
- By condition being met, we mean that the statement returns `true`.

## Getting User Data in IRB
- Ruby has a method called `gets` that allows you to retrieve data from the user typing into the console.
- In order to prevent the input from receiving a new line each time you must call the `.chomp` method:

```
message = gets.chomp

num = gets.chomp.to_i
```

## In-Class Lab 1

We will create a simple string conversion tool that takes in a string and alters it using our string class methods.
First, write one gets statement that will take a string from our user.
Create a class called ConvertString that will wrap our methods.
Create an initializer that will set the given string to an instance variable.
Create 4 different methods that will apply 4 string class methods to the inputted string. You can reference them here.
Output the resulting string to the console using puts.
Instantiate the class using each of these methods.

## In-Class Lab 2

Create a class called Car. Inside of that class, define a method called initialize and pass in color, make, and model as parameters. Define another method called drive where you print a statement that says "We are now driving." Define a third method called paint that takes in new_color as a parameter and then prints out the new color. Lastly define a method called describe_car that will print out: "We are driving in the color make model."

## Take Home Lab 1
- Let's create a simple calculator using the Ruby Math module.
- First, write two `gets` statements that will take 2 numbers from our user.
- Create a class called `Calculator` that will wrap all of our methods.
- Create an `initializer` method that takes in the 2 numbers and sets them as instance variables.
- Write at least 4 methods that perform different math operations and output the result using `puts`. You can reference them [here](http://www.ruby-doc.org/core-2.1.4/Math.html).
- Instantiate your class using each of these 4 methods.
- Bonus 1: Create a simple `if else` statement that will choose which method to pick based on a third `gets` input.
- Bonus 2: Create another method that uses one of the Math constants in your operation.
