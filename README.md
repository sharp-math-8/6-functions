# 6-functions

Because computers are so good at following instructions, one of the ways we can use them most effectively is to write the instructions in a way that they can be repeated.

A block of code that can be run over and over again to perform a specific task is called a function. By organising the repetitive parts of our program into functions, we can make the program smaller, more efficient, and easier to maintain.

Think of functions like little machines or factories within your program. They each need to do one little generic thing.

A simple function in Python looks like this:
```
# This function will print a greeting

def greetingPrinter():
  print("-------------------------")
  print("|        Hello!         |")
  print("-------------------------")

# use it by calling the function by name
greetingPrinter()
```

Functions can accept variables from the main program too. We call these arguments. They let us put information into the function, like this:
```
# This function will print a personalized greeting

def personalGreetingPrinter( name ):
  print("-------------------------")
  print("        Hello {}!         ".format(name) )
  print("-------------------------")


userName = input("What's your name? >>>")
personalGreetingPrinter( userName )
```

More than one argument looks like this:
```
# This function will work out your dog's age

def inDogYears( name, age ):
  dogAge = float( age ) * 7
  print("Your dog {} is {} in dog-years.".format(name, dogAge))


dogName = input("What is your dog's name? >>>")
humanAge = input("How old is your dog in people years? >>>")
inDogYears( dogName, humanAge )
```

Very importantly, functions can also return values to the main program, like this:
```
# This function will find the hypotenuse
# a^2 + b^2 = c^2 right?

def hypoFrom( a, b ):
  cSquared = float(a)**2 + float(b)**2
  c = cSquared**0.5
  return c


sideA = input("What is the shortest side of your right-angle triangle? >>>")
sideB = input("What is the second-shortest side of your right-angle triangle? >>>")
sideC = hypoFrom( sideA, sideB )
print("The hypotenuse of your triangle is {}".format( sideC ))
```

## Your Task:
1.  Write a functions to draw three different shapes on the screen: triangle, square, hexagon, etc. Now write a main program which asks the user for a shape, and runs the correct function using an if-statement.

## Bonus
*Write a function which check to see if what the user enters is one of the possible inputs and only allow correct inputs to continue (i.e. prevent the user crashing the program with an invalid input)*
