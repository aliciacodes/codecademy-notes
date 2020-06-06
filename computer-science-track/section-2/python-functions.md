# Introduction

*Function* is a collection of several lines of code. 

When calling a function, we can call all of these lines of code at once and avoid repetition. 

One function is print. We call print using this syntax

```python
print("Hello World")
```

This lesson will go into building functions, call them with or without inputs, and return values from them. 

# What is a function?

You want to create a program that will display on the big screen in the reception area that greets everyone every time they enter the building. 

```python
Hello!
It is sunny today.
Have a great day!
```

We use print statements for this purpose.

```
print("Hello!")
print("It is sunny today.")
print("Have a great day!")
```

Every time a person enters, we will call these three lines of code which can result in many lines of code.

In Python, this process can become easier by assigning lines of code to a *function*. This function will be named `greet`.  In order to call the function, we need to use the syntax `function_name()` . The parenthesis are important and make the code inside the function run. Here's what the function will look like

```
greet()
```

Every time `greet()` is called, we see:

```
Hello!
It is sunny today.
Have a great day!
```

Having this code inside of `greet()` is better form as it isolates this behavior from the rest of the code. Once this code works the way it is intended, it can be reused anywhere and are confident it'll work without reimplementation. You get the same output with less repeated code. 

NOTE: Repeated code is error prone and harder to understand so it's good to reduce the amount of it.



<u>Activity</u>

1. In `script.py`,  there is a function called sing_song. Call this function once to see what it prints

   Given:

```
def sing_song():
  print("You may say I'm a dreamer")
  print("But I'm not the only one")
  print("I hope some day you'll join us")
  print("And the world will be as one")
```

​		Solution: 

```
sing_song()
```

2. Now call `sing_song` a second time

   ```
   sing_song()
   ```



# Write A Function

Writing a function = heading + indented block of code. 

The heading starts with the word `def` and the name of the function, followed by parenthesis and a colon. The code beneath this must be indented. This is what the syntax looks like:

```
def function_name():
	some code
```

For the `greet()` example it will look like this:

```
def greet():
	print("Hello!")
	print("It is sunny today.")
	print("Have a great day!")
```

The keyword `def` tells Python a function is being defined. This function is called `greet`. Everything that is indented after the colon ( `:`  ) is run when `greet` is called, so in this case 3 print statements will be run. 



<u>Activity</u>

1. Write a function called `loading_screen` that prints `"This page is loading..."` to the console.
2. Outside the function body call `loading_screen()`

```
def loading_screen():
	print("This page is loading...")
loading_screen()
```



# Whitespace

```
def greet():
	print("Hello!")
	print("It is sunny today.")
	print("Have a great day!")
```

These print statements are all executed together when the `greet()`  function is called due to having the same amount of indentation. Whitespace tells the computer what is part of a function and what is not apart of the function. When ending a function, you want to unindent the line so it isn't identified as being part of the function.

```
def greet():
	print("Hello!")
	print("It is sunny today.")
	print("Have a great day!")
print("Printer paper needed")
```

When calling `greet()` it will not print the "Printer paper needed" message as it isn't part of the function since it's not indented. 

People use tabs or four spaces mostly for funtion indentation. It doesn't matter, just be consistent.

<u>Activity</u>

Given:

```
def about_this_computer():
  print("This computer is running on version Everest Puma")
  print("This is your desktop")

about_this_computer()
```



1. Run script.py. Look at what is printed out!
2. Remove the indent on the second print statement. Run the file. Now what's printed?



# Parameters 

Let's go back to the office display. The weather will be changing daily, but how do we change it? With a weather variable! We can make a variable that will hold the daily weather value. Then we can use *parameters* which are variables that can to be passed into a function when it's called.

```
def greet (weather):
print("Hello!")
print("It is " + weather + " today.")
print("Have a great day!")
```

In the definition (`def`) header, the `weather` is referred to as a *formal parameter*. The variable name is a placeholder for the daily weather. Now when we call `greet`, we must provide the `weather`.

```
greet("rainy")
```

The value between the parenthesis when we call a function (ex. `"rainy"`) is referred to as an *argument* of the function call. The argument is the information used in execution of the function. When the function is called, Python assigns the formal parameter name `weather` with the argument `weather`. It's like if this line were included at the top of the function:

```
weather = "rainy"
```

Every time `greet()` is called with a different value in the parenthesis, `weather` is assigned to it. 



<u>Activity</u>

Given 

```
def mult_two_add_three():
  number = 5
  print(number*2 + 3)
  
# Call mult_two_add_three() here:
```



1. The function `mult_two_add_three()` prints a number multiplied by `2` and added to `3`. As it is written right now, the `number` that it operates on is always `5`. Call the function and see what it prints to the console.

```
mult_two_add_three()
```

2. Now, modify the function definition so that it has a parameter called `number`. Then delete the `number = 5` assignment on the first line of the function. Pass the number `1` into your function call.

```
def mult_two_add_three(number):
  print(number*2 + 3)
  
# Call mult_two_add_three() here:
mult_two_add_three(1)
```

3. Call the function with the value `5` as the argument.

```
mult_two_add_three(5)
```

4. Call the function with the value `-1` as the argument.

```
mult_two_add_three(-1)
```

5. Call the function with the value `0` as the argument.

```
mult_two_add_three(0)
```



# Multiple Parameters

People in the office are working into the evenings now and want to see the time of day and the weather at the reception desk. 

We can make the function take more than one parameter by using commas:

```
def greet (weather, time_of_day):
print("Hello!")
print("It is " + weather + " today.")
print("Have a great "+ time_of_day + ""!")
```

The variables `weather` and `time_of_day` must now be provided when the function is called.



<u>Activity</u>

Given 

```
def mult_two_add_three(number):
  print(number*2 + 3)
```



1. The function `mult_two_add_three` takes a number, multiplies it by two and adds three. We want to make this more flexible. First, change the name of the function to `mult_x_add_y`.

```
def mult_x_add_y(number):
	print(number*2 + 3)
```

2. Now, add `x` and `y` as parameters of the function, after `number`.

```
def mult_x_add_y(number,x,y):
	print(number*2 + 3)
```

3. Inside the function, replace `2` in the print statement with `x`, and replace `3` in the print statement with `y`.

```
def mult_x_add_y(number,x,y):
  print(number*x + y)
```

4. Call the function with these values:

   number: 5

   x:  2

   y:  3

   ```
   mult_x_add_y(5,2,3)
   ```

5. Call the function with these values: number: 1, x: 3, y: 1

   ```
   mult_x_add_y(1,3,1)
   ```



# Keyword Arguments

We used two arguments in last exercise:

```
def greet (weather, time_of_day):
print("Hello!")
print("It is " + weather + " today.")
print("Have a great "+ time_of_day + ""!")
```

Whichever value is put into `greet()` first will be assigned to `weather` and the second value will be `time_of_day`. These are called *positional arguments*

because assignment depends on their position in the function call. 



Arguments can also be passed where they explicitly refer to what each argument is assigned to in the function. These are called *keyword arguments*.

```
greet(weather="sunny", time_of_day="evening")
```



We can use keyword arguments to make it explicit what each of our arguments to a function should refer to in the body itself. 



We can also define default arguments for a function using syntax very similar to our keyword-argument syntax, but used during the function definition. If the function is called without an argument for that parameter, it relies on the default. 

```
def greet (weather, time_of_day = "evening"):
print("Hello!")
print("It is " + weather + " today.")
print("Have a great "+ time_of_day + ""!")
```

In this case `time_of_day` has a default argument of "evening". If we call the function with only one argument, the value of "evening" is used for time_of_day and is the default.

```
greet("sunny")
```

Once you give an argument a default value (making it a keyword argument), no arguments that follow can be used positionally. Here is an example:

```
def greet(weather = "rainy", time_of_day) #not valid

def greet(weather, time_of_day = "day")
```



<u>Activity</u>

```
# Define create_spreadsheet():
def create_spreadsheet(title):
  print("Creating a spreadsheet called "+title)

# Call create_spreadsheet() below with the required arguments:
create_spreadsheet("Downloads")
```

1. We have defined a function `create_spreadsheet`, which just takes in a `title`, and prints that it is creating a spreadsheet.

   Run the code to see the function work on an input of `"Downloads"`.

2. Add the parameter `row_count` to the function definition. Set the default value to be `1000`.

```
def create_spreadsheet(title, row_count = 1000):
  print("Creating a spreadsheet called "+title)
```

3. Change the print statement in the function to print “Creating a spreadsheet called `title` with `row_count` rows”, where `title` and `row_count` are replaced with their respective values.

   **Remember, to concatenate a number to a string object, you’ll first have to cast `row_count` to a string using `str()`.** Otherwise, you’ll get a `TypeError`.

```
# Define create_spreadsheet():
def create_spreadsheet(title, row_count = 1000):
  print("Creating a spreadsheet called "+title + " with " + str(row_count) + " rows")
```

4. Call `call_spreadsheet` with `title` set to `"Applications"` and `row_count` set to `10`.

```
create_spreadsheet("Applications", 10)
```



# Returns

We've only been printing out some result to the console with the functions we've seen so far. 

Functions can return a value to the user so this can be used later or modified.  

When there is a result from a function that can be stored in a variable, it is called a *returned* function value. 

Use the keyword `return` to do this.

An example of a function `divide_by_four` that takes an integer argument, divides it by 4, and `return`s the result.

```
def divide_by_four(input_number):
	return input_number/4
```

The program that calls divide_by_four can be used later.

```
result = divide_by_four(16) #result holds 4
print("16 divided by 4 is " + str(result) + "!")
result2 = divide_by_four(result) #result holds 1
print(str(result) + " divided by 4 is " + str(result2) + "!")
```

You can also return strings:

```
def create_special_string(special_item):
  return "Our special is " + special_item + "."

special_string = create_special_string("banana yogurt")

print(special_string)
```

```
Our special is banana yogurt.
```



<u>Activity:</u>

Given:

```
def calculate_age(current_year, birth_year):
  age = current_year - birth_year
```



1. The function `calculate_age` in **script.py** creates a variable called `age` that is the difference between the current year, and a birth year, both of which are inputs of the function. Add a line to return `age`.

```
def calculate_age(current_year, birth_year):
  age = current_year - birth_year
  return age
```

2. Outside of the function, call `calculate_age` with values `2049` (`current_year`) and `1993` (`birth_year`) and save the value to a variable called `my_age`.

   ```
   my_age = calculate_age(2049, 1993)
   ```

3. Call `calculate_age` with values `2049` (`current_year`) and `1953` (`birth_year`) and save the value to a variable called `dads_age`.

   Print the string `"I am X years old and my dad is Y years old"` to the console, with `my_age` where the `X` is and `dads_age` where the `Y` is.

   ```
   dads_age = calculate_age(2049, 1953)
   print("I am " + str(my_age) + " years old and my dad is " + str(dads_age) + " years old")
   ```

   

# Multiple Return Values

You can return more than one value from a function.

```
#surface area of rectangular prism
def rectangle_prism(length, width, height):
	 lw = 2 * length * width
	 wh = 2 * width * height
	 lh = 2 * length * height
	 return lw, wh, lh
#When storing return values, you can store multiple.
lw, wh, lh = rectangle_prism(1,4,5)
print(lw)
print(wh)
print(lh)
```

<u>Activity</u>

1.Write a function called `get_boundaries()` that takes in two parameters, a number called `target` and a number called `margin`.

It should create two variables:

- `low_limit`: `target` minus the `margin`
- `high_limit`: `margin` added to `target`

```
def get_boundaries(target, margin):
  low_limit = target - margin
  high_limit = margin + target
```

2.  Return both `low_limit` and `high_limit` from the function, in that order.

```
def get_boundaries(target, margin):
  low_limit = target - margin
  high_limit = margin + target
  return low_limit, high_limit
```

3. Call the function on the target `100` with a margin of `20`. Save the returned values to variables called `low` and `high`.

```
low, high = get_boundaries(100,20)
```



# Scope

```
def get_the_weather(weather):
	return "The weather is " + weather + "."
print("The forecast is" + weather)
```

Can we access the weather outside of the function? No, if we run the code a `NameError` will be triggered saying `'weather' is not defined`. This variable was defined in the body of function and doesn't exist outside of it. Where the weather is defined is it's *scope* of the function and that's where the variable can be accessed.  

Variables defined outside scope of a function may be accessed inside the body of the function:

```
today = "June 7th"

def get_the_weather(weather):
	return "Today is " + today + "." + "The weather is " + weather + "."
print(get_weather("rainy"))
	#prints Today is June 7th. The weather is rainy.
```

<u>Activity</u>

Given:

```
def calculate_age(current_year, birth_year):
  age = current_year - birth_year
  return age
```



1. Outside of the function `calculate_age()`, try to print `current_year`. Does it work?

   No, it produces `NameError: name 'current_year' is not defined`

2. What about `age`? Outside of `calculate_age()`, try to print `age`. Does it work?

   No, it produces `NameError: name 'age' is not defined`

3. No! Even though we return `age` at the end of the function, the variable `age` still only exists within the context of the function.

   Remove both print statements.

4. Let’s try something different. Remove the parameter `current_year` so that it is no longer a parameter of `calculate_age()`.

5. It’s the year 2048.

   Define `current_year` as a variable BEFORE defining the function and give it the value `2048`. Now, every time `calculate_age()` is called, it should only take `birth_year`.

   ```
   current_year = 2048
   def calculate_age(birth_year):
     age = current_year - birth_year
     return age
   ```

   

6. Try to print `current_year` one last time. Does it work finally?

   Yes, it does since it is in a global scope. 

7. Hooray! Now we have `current_year` globally defined. Great work!

   Let’s make sure our function still works: print the value of `calculate_age()` with `1970` as the argument.

   ```
   current_year = 2048
   def calculate_age(birth_year):
     age = current_year - birth_year
     return age
   
   print(calculate_age(1970))
   ```

   

# Review

In this section, we learned

- How to write a function
- How to give a function inputs
- How to return values from a function
- What scope means

<u>Activity</u>

1. Define a function called `repeat_stuff` that takes in two inputs, `stuff`, and `num_repeats`.

   We will want to make this function print a string with `stuff` repeated `num_repeats` amount of times. For now, only put an empty `print` statement inside the function.

```
def repeat_stuff(stuff, num_repeats):
  print()
```

2. Outside of the function, call `repeat_stuff`.

   You can use the value `"Row "` for `stuff` and `3` for `num_repeats`.

```
repeat_stuff("Row ", 3)
```

3. Change the `print` statement inside `repeat_stuff` to a `return` statement instead.

   It should return `stuff*num_repeats`.

   **Note:** Multiplying a string just makes a new string with the old one repeated! For example:

   ```
   "na"*6
   ```

   results in the string `"nananananana"`.

```
def repeat_stuff(stuff, num_repeats):
  return stuff * num_repeats
```

4. Give the parameter `num_repeats` a default value of `10`.

```
def repeat_stuff(stuff, num_repeats = 10):
  return stuff * num_repeats
```

5. Add `repeat_stuff("Row ", 3)` and the string `"Your Boat. "` together and save the result to a variable called `lyrics`.

```
lyrics = repeat_stuff("Row ", 3) + "Your Boat. "
```

6. Create a variable called `song` and assign it the value of `repeat_stuff` called with the singular input `lyrics`.

```
song = repeat_stuff(lyrics)
```

7. Print song

```
print(song)
```

