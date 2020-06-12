# Introduction

What if we wanted to `print()` each item from a list of items from a coffee shop called `shop_items` we would need to use this:

```
shop_items = ['latte', 'coffee', 'americano', 'bagel', 'muffin']
print(coffee[0])
print(coffee[1])
print(coffee[2])
print(coffee[3])
print(coffee[4])
```

This is incredibly inefficient and will make our code a mess. Luckily, in Python and most other programming languages, there is an easier way of using or *iterating* items in a list called *loops*. These repeat a set of code many times. There are many kinds of loops. Loops that move through each item (*for loops*), ones that keep going until we tell them to stop (*while loops*)m and create new lists through loops (*list comprehensions*).

<u>Activity</u>

1. Paste the following code into **script.py**:

   ```
   dog_breeds = ['french_bulldog', 'dalmatian', 'shihtzu', 'poodle', 'collie']
   for breed in dog_breeds:
       print(breed)
   ```

   This will print each `breed` in `dog_breeds`.

   

# Create a For Loop

*for loops* - They let us perform an action on each item in the list.

*iteration* - using/modifying each element in a list. An *iterable* is an object like a list, a string, or a range that contains multiple items you can loop through

```
shop_items = ['latte', 'coffee', 'americano', 'bagel', 'muffin']
for item in shop_items:
	print(item)
```

Here is how to write it:

```
for <temp variable> in <iterable>:
	<action>
```

`item` is a temporary variable, `shop_items` is the list (iterable), and `print(item)` was the action performed on the list. 

The temporary variable can be named whatever we want and doesn't need to be initialized beforehand. In all the examples, the action needs to be indented and every argument you want to include needs to be indented. If you forgot to indent, then you get an `IndentationError`. 

<u>Activity</u>

1. Run the code. You should get an `IndentationError` because the `print(game)` line is not indented.

```
board_games = ['Settlers of Catan', 'Carcassone', 'Power Grid', 'Agricola', 'Scrabble']

sport_games = ['football', 'football - American', 'hockey', 'baseball', 'cricket']

for game in board_games:
print(game)
```

2. Indent line 6 so that you don’t get an `IndentationError` when you run the code.

```
for game in board_games:
	print(game)
```

3. Write a loop that prints each `sport` in `sport_games`.

```
for sport in sport_games:
	print(sport)
```



# Using Range in Loops

Sometimes, when iterating through a list we may want to do an action a certain number of times. 

```
for i in <list of length 5>:
	print("This message will print 5 times")
```

To do this, we can use the `range` function to create a list of `n` length to enable us to iterate through a list a given number of times. 

Remember, `range` returns a list from 0 to `n-1`.

```
zero_through_five = range(6)

zero_through_one = range(2)
```



<u>Activity</u>

1. Use the `range` function in a for loop to print out `promise` 5 times.

```
for i in range(6):
	print("promise")
```



# Infinite Loops

What if we have code like this?

```
divide_two = [4, 2, 1]

for num in divide_two:
	divide_two.append(num/2)
```

Every time we enter the loop, we're adding the previous number (`num` ) divided by `2` so the list will keep on growing. 

This is called an infinite loop, it never terminates. This is dangerous since the code will run forever and taking up memory.

If this accidentally happens, you can hit `control` + `c` on your keyboard to terminate the program.

<u>Activity</u>

1. Suppose we have two lists of students, `students_period_A` and `students_period_B`. We want to combine all students into `students_period_B`.

   Write a for loop that goes through each `student` in `students_period_A` and adds it to the end of `students_period_B`.

```
students_period_A = ["Alex", "Briana", "Cheri", "Daniele"]
students_period_B = ["Dora", "Minerva", "Alexa", "Obie"]

for student in students_period_A:
	students_period_B.append(student)
```

2. Inside the for loop, after appending `student` to `students_period_B`, print `student`.

   ```
   for student in students_period_A:
   	students_period_B.append(student)
   	print(student)
   ```

   

3. Let’s suppose you made a typo in the body of your for loop. Oh no! We will go through a few steps to see what happens when you end up with an infinite loop and how you fix it:

1. Inside the for loop, change the object of the append statement from `students_period_B` to `students_period_A`.
2. Run this code. What do you notice happens? Over the run button, notice the loading circle is continuing without anything happening. This is an infinite loop! To end this program we must **refresh the page**. (Note: The reason this loop is infinite is that we’re adding each student in `students_period_A` to `students_period_A` which would create a never-ending list of all the student names.)
3. After refreshing your page, you should see that the run button is back. Now get rid of the change we made that caused an infinite loop by changing the object of the append statement back to `student_period_B`.

```
for student in students_period_A:
	students_period_A.append(student)
	print(student)
```



# Break

Sometimes, we want a loop to search through a list of values.

```
starbucks_menu = ["vanilla_latte", "caffe_mocha", "flat_white", "chai_latte", "cold_brew", "smores_frap"]

#We want to order a chai latte
for drink in starbucks_menu:
  if drink == "chai_latte":
    print("Chai latte added to your order!")
```

The code goes through each `drink` in `starbucks_menu` and finds a match. After finding the chai latte, we don't need to continue on in the list. 

So, we found it. How can you stop the for loop so it doesn't continue? You can use a `break` statement which goes to the code outside the loop. 

```
starbucks_menu = ["vanilla_latte", "caffe_mocha", "flat_white", "chai_latte", "cold_brew", "smores_frap"]

#We want to order a chai latte
for drink in starbucks_menu:
  print(drink)
  if drink == "chai_latte":
  break
print("Chai latte added to your order!")
```

We would get this output, proving the break statement works!

```
vanilla_latte
caffe_mocha
flat_white
chai_latte
Chai latte added to your order!
```



<u>Activity:</u>

1. You have a list of dog breeds you can adopt, `dog_breeds_available_for_adoption`. Using a for loop, iterate through the `dog_breeds_available_for_adoption` list and print out each dog breed.

```
dog_breeds_available_for_adoption = ['french_bulldog', 'dalmatian', 'shihtzu', 'poodle', 'collie']
dog_breed_I_want = 'dalmatian'

for dog in dog_breeds_available_for_adoption:
  print(dog)
```

2. Inside your for loop, after you print each dog breed, check if it is equal to `dog_breed_I_want`. If so, print `"They have the dog I want!"`

```
for dog in dog_breeds_available_for_adoption:
  print(dog)
  if dog == dog_breed_I_want:
  	print("They have the dog I want!")
```

3. Add a break statement when your loop has found `dog_breed_I_want`, so that the rest of the list does not need to be checked.

```
for dog in dog_breeds_available_for_adoption:
  print(dog)
  if dog == dog_breed_I_want:
  	break
print("They have the dog I want!")
```



# Continue

What if we want to skip values while iterating? We want to print out all numbers that aren't multiple of two. In Python, we can do this with the `continue` statement to move onto the next element without breaking out of the loop.

```
num_list = range(10)

for i in num_list:
  if i % 2 == 0:
   	 continue
  print(i)
```

```
1
3
5
7
9
```

When we find a multiple of 2, the `continue` moves the index to the next value in the list without printing the value.



<u>Activity</u>

1. Your computer is the doorman at a bar in a country where the drinking age is 21.

   Loop through the `ages` list. If an entry is less than `21`, skip it and move to the next entry. Otherwise, print the age.

```
ages = [12, 38, 34, 26, 21, 19, 67, 41, 17]

for age in ages:
	if age < 21:
		continue
	print(age)
```



# While Loops

The `while` loop performs a code until a condition is reached.

While loops are used to iterate through lists, like loops:

```
legendary_pokemon = ["Articuno", "Zapdos", "Moltres", "Mew, Mewtwo"]

index = 0
while index < len(legendary_pokemon):
	print(legendary_pokemon[index])
	index += 1
```

When the condition (`index < len(legendary_pokemon)`) is satisfied, the code inside the `while` loop runs.

While loops are useful when you don't know how many iterations it will take to satisfy a condition

<u>Activity</u>

1. You are adding students to a Poetry class, the size of which is capped at 6. While the length of the `students_in_poetry` list is less than `6`, use `.pop()` to take a student off the `all_students` list and add it to the `students_in_poetry` list.
2. Print the `students_in_poetry` list .

```
all_students = ["Alex", "Briana", "Cheri", "Daniele", "Dora", "Minerva", "Alexa", "Obie", "Arius", "Loki"]
students_in_poetry = []

while len(students_in_poetry) < 6:
  student = all_students.pop()
  students_in_poetry.append(student)
  
print(students_in_poetry)
```



# Nested Loops

What we have a list of lists? How can we loop through all the individual elements contained?

```
sinnoh_gym_pokemon = [["Geodude", "Onix", "Cranidos"], ["Turtwig", "Cherubi", "Roserade"], ["Meditite", "Machoke", "Lucario"]]
for team in sinnoh_gym_pokemon:
	for pokemon in team:
		print(pokemon)
```

This is the output:

```
Geodude
Onix
Cranidos
Turtwig
Cherubi
Roserade
Meditite
Machoke
Lucario
```

<u>Activity</u>

1. We have provided the list `sales_data` that shows the numbers of different flavors of ice cream sold at three different locations of the fictional shop, Gilbert and Ilbert’s Scoop Shop. We want to sum up the total number of scoops sold. Start by defining a variable `scoops_sold` and set it to zero.

```
sales_data = [[12, 17, 22], [2, 10, 3], [5, 12, 13]]
scoops_sold = 0
```

2. Go through the `sales_data` list. Call each inner list `location`, and print out each `location` list.

```
for location in sales_data:
	print(location)
```

3. Within the `sales_data` loop, go through each `location` list and add the element to your `scoops_sold` variable.

   By the end, you should have the sum of every number in the `sales_data` nested list.

```
for location in sales_data:
	for scoop in location:
		scoops_sold += scoop
print(scoops_sold)
```



# List Comprehension

A list comprehension is a precise way to create lists that takes less lines of code. We want only elements that are divisible by 5. 

```
nums = range(20)
divi_by_5 = []
for num in nums:
	if num % 5 == 0:
		divi_by_5.append(num)
print(divi_by_5)
```

This is the output

```
[0, 5, 10, 15]
```



```
divi_by_5 = [num for num in nums if num % 5 == 0]
```

This list comprehension

1. Takes an element in `words`
2. Assigns the element to a variable called `num`.
3. Checks if `num % 5 == 0`, if it is it adds it to `divi_by_5`. If not, nothing happens.

If there isn't any `if` statements, then there will just be a copy of `divi_by_5`. 

<u>Activity</u>

1. We have defined a list `heights` of visitors to a theme park. In order to ride the Topsy Turvy Tumbletron roller coaster, you need to be above 161 centimeters. Using a list comprehension, create a new list called `can_ride_coaster` that has every element from `heights` that is greater than `161`.
2. Print `can_ride_coaster`.

```
heights = [161, 164, 156, 144, 158, 170, 163, 163, 157]

can_ride_coaster = [height for height in heights if height > 161]
print(can_ride_coaster)
```



# More List Comprehensions

Now, we want to add a string saying  " `num` is a multiple of 5!"

```
nums = [num + " is a multiple of 5!" for num in divi_by_5]
```

This takes a num in `divi_by_5` , assigns the integer to a variable `num`, concatenates the num with "is a multiple of 5! ", and finally appends to a new list called `nums`. This will repeat for the remainder of the list. You can also do this with numbers to add, subtract, divide, or multiplying values. 

<u>Activity</u>

1. We have provided a list of temperatures in celsius. Using a list comprehension, create a new list called `fahrenheit` that converts each element in the `celsius` list to fahrenheit.
2. Print `fahrenheit`.

**Note: ** To convert, use the formula:

```
temperature_in_fahrenheit = temperature_in_celsius * 9/5 + 32
```

```
celsius = [0, 10, 15, 32, -5, 27, 3]
fahrenheit = [celi * 9/5 + 32 for celi in celsius]
print(fahrenheit)
```



# Review

Good job! In this lesson, you learned

- how to write a for loop
- how to use `range` in a loop
- what infinite loops are and how to avoid them
- how to skip values in a loop
- how to write a while loop
- how to make lists with one line

Let’s get some more practice with these concepts!

<u>Activity</u>

1. Create a list called `single_digits` that consists of the numbers 0-9 (inclusive).

```
single_digits = range(10)
```

2. Create a for loop that goes through `single_digits` and prints out each one.

```
for digit in single_digits
	print(digit)
```

3. Before the loop, create a list called `squares`. Assign it to be an empty list to begin with.

```
squares = []
```

4. Inside the loop that iterates through `single_digits`, append the squared value of each element of `single_digits` to the list `squares`. You can do this before or after printing the element.

```
single_digits = range(10)
squares = []
for digit in single_digits:
  print(digit)
  squares.append(digit ** 2)
```

5. After the for loop, print out `squares`.

```
print(squares)
```

6. Create the list `cubes` using a list comprehension on the `single_digits` list. Each element of `cubes` should be an element of `single_digits` taken to the third power

```
cubes = [digit ** 3 for digit in single_digits]
```



# The Quiz



Fill in the blank with the appropriate `while` condition in order to print the numbers 1 through 10 in order:

```
i = 1
____________
    print(i)
    i += 1
```

```
Answer: while i <= 10
```

What would be the output of the following code:

```
numbers = [1, 1, 2, 3]
for number in numbers:
  if number % 2 == 0:
    continue
  print(number)
```

```
1, 1, 3
```

What would be the output of the following code:

```
drink_choices = ["coffee", "tea", "water", "juice", "soda"]
for drink in drink_choices:
  print(drink)
```

```
coffee
tea
water
juice 
soda
```

Which of these list comprehensions will create a list equal to `desired_list`? 

```
desired_list = [-1, 0, 1, 2, 3]
```

```
[i-1 for i in range(5)]
```

What would be the output of the following code:

```
for i in range(3):
	print(i)
```

```
0 1 2
```

Which of these list comprehensions will create a list equal to `desired_list`?

```
my_list = [5, 10, -2, 8, 20]
desired_list = [10, 8, 20]
```

```
[i for i in my_list if i > 5]
```

What would be the output of the following code:

```
numbers = [2, 4, 6, 8]
for number in numbers:
  print("hello!")
```

```
hello!hello!hello!hello!
```

What would be the output of the following code:

```
for i in range(3):
  print(5)
```

```
5 5 5
```

What would be the output of the following code:

```
numbers = [1, 1, 2, 3]
for number in numbers:
  if number % 2 == 0:
    break
  print(number) 
```

```
1
1
```