# Control Flow Introduction (Poor)

In your everyday life, you have many questions and decisions to make. Is it a workday? Then you better be up by 6 A.M. If not, you can sleep in some. Do you have a big meeting today? Well, you better pull out your best attire. If not, normal work clothes are okay

![control flow diagram](/home/alicia/Downloads/Untitled Diagram.jpg)

The questions and decisions you make in the mornings, each step you make and result that occur is due to the conditions of the day and surroundings. 

Computers go through a similar flow when code is executing. A program runs (wake up) and move through a checklist like this. They determine if the conditions are met and if they are they will execute code and return a value. 

This is called the *Control Flow* of a program. In Python, scripts execute from top to bottom until it reaches the end. It is the programmer's job to include gateways (in this case the diamond shape with the questions inside) which are called conditional statements, to tell the computer to run certain blocks of code. 



# Boolean Functions

In order to build control flow, you need to see if something is true or false. In code, there is a type of data called a boolean that can **only** be `True` or `False`. 

An example of this is asking if "Is today is a Tuesday?" If today is Tuesday, it will be `true`. If today is Saturday, it will be `false`.

A boolean expression is a statement that can be objectively true or false like "Today is Tuesday". The phrase "Red is the worst color" is not a boolean expression since it is an opinion, someone else might think that red is the best color. 

How about this phrase?

```
Saturday starts with the letter 'C'
```

This is a boolean statement since it can only be `True` or `False` even though this statement is `False`.

<u>Activity</u>

Determine if the following statements are boolean expressions or not. If they are, set the matching variable to the right to `"Yes"` and if not set the variable to `"No"`. Here’s an example of what to do:

Example statement:

```
My dog is the cutest dog in the world.
```

```
example_statement = "No"
```

This is an opinion and not a boolean expression, so you would set `example_statement` to `"No"` in the editor to the right. Okay, now it’s your turn:

Statement one:

```
Dogs are mammals.
```

```
statement_one = "Yes"
```

Statement two:

```
My dog is named Pavel.
```

```
statement_two = "Yes"
```

Statement three:

```
Dogs make the best pets.
```

```
statement_three = "No"
```

Statement four:

```
Cats are female dogs.
```

```
statement_four = "Yes"
```



# Relational Operators: Equals and Not Equals

How do we create boolean expressions in Python?

- Relational Operators: Compares two items and return either `True` or `False`. Sometimes called *comparators*.

Here are two boolean operators

- Equals: `==`
- Not equals: `!=`

These operators will compare two values and return `True` and `False` if they are equal or not.

```
>>> 5 == 5
True
>>> 5 != 5
False
>>> -1 == 1
False
>>> '10' == 10
False
```

`>>>` is the prompt to run Python in the terminal and you can enter simple expressions like these into the terminal. 

The last statement is false due to the `' '` making `'10'` into a string. This is different from the int value `7` so they aren't equal. Always be mindful of types!

<u>Activity</u> 

1. Determine if the following boolean expressions are `True` or `False`. Input your answer as `True` or `False` in the appropriate variable to the right.

   Statement one:

   ```
   (5 * 2) - 1 == 8 + 1
   ```

   ```
   statement_one = True
   ```

   Statement two:

   ```
   13 - 6 != (3 * 2) + 1
   ```

   ```
   statement_two = False
   ```

   Statement three:

   ```
   3 * (2 - 1) == 4 - 1
   ```

   ```
   statement_three = True
   ```

   

# Boolean Variables

`True` and `False` (always capitalized) have their own types: `bool`. They are the only values of `bool` and any variable that has one of these values is a *boolean variable*.

Boolean variables can be made by 

- Setting a variable equal to  `True` or `False`.

```
set_to_true = True
set_to_false = False
```

- Set variables equal to a boolean expression

```
bool_one = 5 == 7
bool_two = 1 * 1 == 2
bool_three = 4 + 6 != 10
```

Now these variables will return `True` or `False ` when referenced since they were assigned a boolean value. 

```
>>> bool_one
False
>>> bool_two
True
>>> bool_three
False
```

<u>Activity</u>

1. Create a variable named `my_baby_bool` and set it equal to `"true"`.

   ```
   my_baby_bool = "true"
   ```

2. Check the type of `my_baby_bool` using `type(my_baby_bool)`.

   You’ll have to print it to get the results to display in the terminal.

   ```
   print(type(my_baby_bool)) #It's a string
   ```

3. It’s not a boolean variable! Boolean values `True` and `False` always need to be capitalized and do not have quotation marks.

   Create a variable named `my_baby_bool_two` and set it equal to `True`.

   ```
   my_baby_bool_two = True
   ```

4. Check the type of `my_baby_bool_two` and make sure you successfully created a boolean variable.

   You’ll have to print it to get the results to display in the terminal.

   ```
   print(type(my_baby_bool_two))
   ```

   

# If Statements

Understanding boolean variables and expressions are  because the are the building blocks of *conditional statements*. 

The decision making process of "Is it a workday? If so, wake up at 6AM." is a conditional. In programming, we phrase it as an "if-then" statement where the boolean statement is the *if* part and beginning of the conditional statement and the *then* part is the conclusion of the conditional statement that will be executed. 

```
If it is a workday then wake up at 6AM
```

In this case, the boolean expression is `it is a workday` and the conditional statement is checking if this is true. 

If "`it is a workday == True"` then the rest of the conditional statement will be executed and you will wake up at 6AM the next day.

The form of a conditional statement

```
If [it is a workday] then [wake up at 6AM]
```

In Python, it looks like this:

```
if is_workday:
	wake_up_6AM()
```

Instead of `then`, there is a colon, `:`. This tells the computer what is coming next should the condition be met. 

Some conditionals can be equations, like this:

```
if 4 == 13-9:
	print('red')
```

This code will print `'red'` to the terminal because this statement is `True`.

<u>Activity</u>

1. In the workspace **script.py** there is a function with an `if` statement. I wrote this function because my coworker Dave kept using my computer without permission and he is a real doofus. It takes `user_name` as an input and if the user is Dave it tells him to stay off my computer.

   Enter a user name in the field for `user_name` and try running the function.

   ```
   def dave_check(user_name):
     if user_name = "Dave":
       return "Get off my computer Dave!"
   
     
   # Enter a user name here, make sure to make it a string
   user_name = "Alicia"
   print(dave_check(user_name))
   ```

2. Oh no! We got a `SyntaxError`! This happens when we make a small error in the syntax of the conditional statement.

   Read through the error message carefully and see if you can find the error. Then, fix it, and run the code again.

   ```
   def dave_check(user_name):
     if user_name == "Dave":
       return "Get off my computer Dave!"
   ```

3. Ugh! Dave got around my security and has been logging onto my computer using our coworker Angela’s user name, `angela_catlady_87`.

   Update the function with a second `if` statement so it checks for this user name as well and returns

   ```
    "I know it is you Dave! Go away!"
   ```

   in response. That’ll teach him!

   ```
   def dave_check(user_name):
     if user_name == "Dave":
       return "Get off my computer Dave!"
     if user_name == "angela_catlady_87":
     	return "I know it is you Dave! Go away!"
   ```

   

# Relational Operators II

So, far we know two relational operators, `=` and `!=` , but there are four more you can use to create boolean expression.

- Greater than: `>`

- Less than: `<`
- Greater than or equal to: `>=`
- Less than or equal to: `<=`

Ex. You are a movie usher and want to make sure everyone who sees R-rated movies are over the age of 17. 

```
def r_check(age):
	if age >= 17:
		return True
```

The function takes the inputted `age` and compare it to the `int` 17. If the `age` is greater or equal to 17, it will return `True`.

<u>Activity</u>

1. Write a function called `greater_than` that takes two integer inputs, `x` and `y` and returns the value that is greater. If `x` and `y` are equal, return the string

   ```
   "These numbers are the same"
   ```

```
def greater_than(x,y):
	if x > y:
		return x
	if y > x:
		return y
	if x == y:
		return "These numbers are the same"
```

2. The nearby college, *Calvin Coolidge’s Cool College* (or 4C, as the locals call it) requires students to earn 120 credits to graduate. Write a function called `graduation_reqs` that takes an input `credits` and checks if the student has enough credits to graduate. If they do, return the string

   ```
   "You have enough credits to graduate!"
   ```

```
def graduation_reqs(credits):
	if credits >= 120:
		return "You have enough credits to graduate!"
```



3. Call `graduation_reqs` with an input of 120 `credits` and print the result to the terminal. Can a student with 120 `credits` graduate from *Calvin Coolidge’s Cool College*?

   ```
   print(graduation_reqs(120))
   ```

   

# Boolean Operators: and

The conditions you want to check in conditional statement will require more than one boolean expression. 

You can build larger boolean expressions using *boolean operators*. These operators known as *logical operators* combine smaller boolean expressions into larger one. 



Three boolean operators:

- `and`
- `or`
- `not`

`and` combines two boolean expressions and evaluates as `True` if both boolean expressions are `True`, `False` if they aren't.



An example of this:

```
Harry Potter is a book and water is a liquid
```

This boolean expression comprises of two smaller expressions `Harry Potter is a book` and `water is a liquid`. Both of these are `True` and connected by the `and` operator so the entire expression is `True`.

Let's look at other examples:

```
>>> (2 - 1 == 1) and (5 + 2 == 7)
True
>>> (6 - 1 == 5) and (4 < 2)
False #2 is not greater than 4.
>>> (7 != 7) and (8 > 7)
False #7 does equal 7
>>> (9 == 10) and (6+7 == 13)
False #9 does not equal 10
```

<u>Activity</u>

1. Set the variables `statement_one` and `statement_two` equal to the results of the following boolean expressions:

   Statement one:

   ```
   (2 + 2 + 2 >= 6) and (-1 * -1 < 0)
   ```

   ```
   statement_one = False
   ```

   Statement two:

   ```
   (4 * 2 <= 8) and (7 - 1 == 6)
   ```

   ```
   statement_two = True
   ```

   

2. Let’s return to *Calvin Coolidge’s Cool College*. 120 credits aren’t the only graduation requirement, you also need to have a GPA of 2.0 or higher. Rewrite the `graduation_reqs` function so it takes two inputs, `gpa` and `credits`, and checks to see if a student meets both requirements using an `and` statement.

   If they do, return the string

   ```
   "You meet the requirements to graduate!"
   ```

   ```
   def graduation_reqs(credits,gpa):
     if credits >= 120 and gpa >= 2.0:
       return "You meet the requirements to graduate!"
   ```



# Boolean Operators: or

 `or`  - combines two expressions into larger expression that is `True` if either component is `True`.

```
Apples are a fruit or lightning is thunder
```

The statement is composed of two expressions: `apples are fruit` which is `True` and `lightning is thunder` is `False`. Due to the `or` operator, the entire statement is `True`. Only one expression needs to be `True` for the entire statement to be `True`.

Python doesn't work like English which implies with an `or` statement that one component is `True` then the other is `False`.  If an `or  ` statement has two `True` components, the entire expression is  `True`.  If both statements are `False`, then the whole expression is `False`.

```
>>> True or (3 + 13 == 8)
True
>>> (4 + 8 == 12) or True
True
>>> (7 < 2) or True
True
>>> (4 == 5) or (-1 > 9)
False
```



<u>Activity</u>

1. Set the variables `statement_one` and `statement_two` equal to the results of the following boolean expressions:

   Statement one:

   ```
   (2 - 1 > 3) or (-5 * 2 == -10)
   ```

   ```
   statement_one = True
   ```

   Statement two:

   ```
   (9 + 5 <= 15) or (7 != 4 + 3)
   ```

   ```
   statement_two = True
   ```

   

2. The registrars office at *Calvin Coolidge’s Cool College* has another request. They want to send out a mailer with information on the commencement ceremonies to students who have met at least one requirement for graduation (120 credits and 2.0 GPA).

   Write a function called `graduation_mailer` that takes two inputs, `gpa` and `credits` and checks if a student either has 120 or more credits or a GPA 2.0 or higher and if so returns `True`.

   ```
   def graduation_mailer(gpa, credits):
     if gpa >= 2.0 or credits >= 120:
       return True
   ```

   

# Boolean Operators: not

`not` - If applied to any boolean expression, it reverses the boolean value. Ex. If we have a `True` statement and apply a `not` operator it produces a `False` statement.

```
not False == True
not True == False
```

Consider the following:

```
Apples are not a fruit.
```

Took the statements `Apples are a fruit` and added a `not` operator to make `False` statement `apples are not a fruit`.

The main difference from English is that the `not` operator is at the beginning of the statement.

```
>>> not 3 - 2 == 1
False
>>> not 9 < 8
True
```

<u>Activity</u>

1. Set the variables `statement_one` and `statement_two` equal to the results of the following boolean expressions:

   Statement one:

   ```
   not (4 + 5 <= 9)
   ```

   ```
   statement_one = False
   ```

   Statement two:

   ```
   not (8 * 2) != 20 - 4
   ```

   ```
   statement_two = True
   ```

   The registrar’s office at *Calvin Coolidge’s Cool College* has been so impressed with your work so far that they have another task for you. They want you to return to the first function you wrote, `graduation_reqs`, and add in several checks using `and` and `not` statements.

   - If a student meets both requirements the function should return

     ```
     "You meet the requirements to graduate!"
     ```

   - If a student’s GPA is greater or equal to 2.0 but they don’t have enough credits the function should return

     ```
     "You do not have enough credits to graduate."
     ```

   - If they have enough credits but their GPA is less than 2.0 the function should return

     ```
     "Your GPA is not high enough to graduate."
     ```

   - If they do not have enough credits and their GPA is less than 2.0, the function should return

     ```
     "You do not meet either requirement to graduate!"
     ```

   Make sure your return value matches those strings exactly. Capitalization, punctuation, and spaces matter!

   ```
   def graduation_reqs(gpa, credits):
     if (gpa >= 2.0) and (credits >= 120):
       return "You meet the requirements to graduate!"
     if (gpa >= 2.0) and not (credits >= 120):
     	return "You do not have enough credits to graduate."
     if not (gpa >= 2.0) and (credits >= 120):
     	return "Your GPA is not high enough to graduate."
     if not (gpa >= 2.0) or not (credits >= 120):
     	return "You do not meet either requirement to graduate!"
   ```

   

# Else Statements

When you start adding a lot of `if` statements in a function the code becomes cluttered. 

We have other tools to help build control flow. 

`else` statements describe what the code should do when defined conditions are **not** met.

`else` statements need a preceding `if` statement(s) to appear.

```
if weekday:
	wake_up(6AM)
else:
	sleep_in()
```

We can build `if` statements that execute different code if conditions are or aren't met. We no longer need to write `if` statements to cover each condition, a blanket `else` statement for each time the condition isn't met.

In the R-rated movie example, we can now add an else statement to return a message if they person is younger than 17.

```
def r_check(age):
	if age >= 17:
		return True
	else:
	return "This person is not old enough to see the movie."
```

<u>Activity</u>

1. *Calvin Coolidge’s Cool College* has **another** request for you. They want you to add an additional check to the `graduation_reqs` function. If a student is failing to meet both graduation requirements, they want the function to return:

   ```
   "You do not meet the GPA or the credit requirement for graduation."
   ```

   Use an `else` statement to add this to your function.

   ```
   def graduation_reqs(gpa, credits):
     if (gpa >= 2.0) and (credits >= 120):
       return "You meet the requirements to graduate!"
     if (gpa >= 2.0) and not (credits >= 120):
       return "You do not have enough credits to graduate."
     if not (gpa >= 2.0) and (credits >= 120):
       return "Your GPA is not high enough to graduate."
     else:
     	return "You do not meet the GPA or the credit requirement for graduation."
   ```

   

# Else If Statement

`elif` - This statement checks another condition after the previous `if` statement isn't met. This controls the order the program to check each of the conditional statements. First, the `if` statement is checked, then  each`elif` is checked from top to bottom, and the `else` statement is executed at the end if no conditions are checked. 

```
def makeup_rewards(money_spent)
if money_spent >= 1000:
	print("Congrats! You have platinum status.")
elif money_spent >= 750:
	print("Congrats! You have gold status.")
elif money_spent >= 350:
	print("Congrats! You have silver status.")
else:
	print("Congrats! You have bronze status")
```

What happens if the `elif` statements were turned to `if` statements? If you spent $1,000, then the first 3 messages would all print because each `if` condition is met. 

Since `elif` statements are used, it checks conditions in sequence and only prints one message. If $400.00 is spent, it first checks if over $1,000 is spent, if not, then it checks over $750, then it will check $350 and the message is printed. 

<u>Activity</u>

1. *Calvin Coolidge’s Cool College* has noticed that students prefer to get letter grades over GPA numbers. They want you to write a function called `grade_converter` that converts an inputted GPA into the appropriate letter grade. Your function should be named `grade_converter`, take the input `gpa`, and convert the following GPAs:

- 4.0 or higher should return `"A"`
- 3.0 or higher should return `"B"`
- 2.0 or higher should return `"C"`
- 1.0 or higher should return `"D"`
- 0.0 or higher should return `"F"`

You can do this by creating a variable called `grade`.

Then, you should use `elif` statements to set `grade` to the appropriate letter grade for the `gpa` entered.

At the end of the function, return `grade`.

```
def grade_converter(gpa):
  if gpa >= 4.0:
    grade = "A"
  elif gpa >= 3.0:
    grade = "B"
  elif gpa >= 2.0:
    grade = "C"
  elif gpa >= 1.0:
    grade = "D"
  else:
    grade = "F"
  return grade
```



# Try and Except Statements

Use `try` and `except` statements to check for possible errors a user might encounter.

```
try:
	#a statement
except ErrorName:
	#a statement
```

Workflow

1. The `try` will be executed. If an exception isn't raised, then the `try` will terminate.
2. If an `exception` like a `NameError` or `ValueError` is raised then the except will execute.



```
def divides(a,b):
	try:
		result = a/b
		print(result)
	except ZeroDivisionError:
		print("Can't divide by zero!")
```

This function takes two numbers, `a` and `b` as input and returns `a` divided by `b`. There is a chance `b` could be zero and cause a error so we want to catch this error. 



<u>Activity</u>

1. The function in the editor is very simple and serves one purpose: it raises a `ValueError`.

   Try running it by entering `raises_value_error()` into the code editor and hitting run.

   Remember, unindent this function call so it isn’t included in the function itself.

   ```
   def raises_value_error():
       raise ValueError
   
   raises_value_error()
   ```

   

2. Great! Nice error raising! Now let’s make that error message a little more palatable.

   Write a `try` statement and an `except` statement around the line of code that executes the function to catch a ValueError and make the error message print `You raised a ValueError!`

   ```
   def raises_value_error():
       try:
         raise ValueError
       except ValueError:
         print("You raised a ValueError!")
   ```

   

# Review

- Boolean expressions are statements that are either `True` or `False`.
- Boolean variables is a variable that set to either `True` or `False`.
- Create boolean expressions using relational operators:
  - Equals: `=`
  - Not equals: `!=`
  - Greater than: `>`
  - Greater than or equal to: `>=`
  - Less than: `<`
  - Less than or equal to: `<=`
- `if` statements are used to contorl flow in code
- `else` statements used to execute code if no other conditions are met
- `elif` statements used to build additional checks after the `if` statements so all `if` statements don't get triggered
- `try` and `except` statements build error control into code.

<u>Activity:</u>

1. The admissions office at *Calvin Coolidge’s Cool College* has heard about your programming prowess and wants to get a piece of it for themselves. They’ve been inundated with applications and need a way to automate the filtering process. They collect three pieces of information for each applicant:

   1. Their high school GPA, on a 0.0 - 4.0 scale.
   2. Their personal statement, which is given a score on a 1 - 100 scale.
   3. The number of extracurricular activities they participate in.

   The admissions office has a cutoff point for each category. They want students that have a GPA of 3.0 or higher, a personal statement with a score of 90 or higher, and who participated in 3 or more extracurricular activities.

   Write a function called `applicant_selector` which takes three inputs, `gpa`, `ps_score`, and `ec_count`. If the applicant meets the cutoff point for all three categories, have the function return the string:

   ```
   "This applicant should be accepted."
   ```

   ```
   def applicant_selector(gpa, ps_score, ec_count):
   	if gpa >= 3.0 and ps_score >= 90 and ec_count >= 3:
   		return "This applicant should be accepted."
   ```

   

   **2.** Great! The admissions office also wants to give students who have a high GPA and a strong personal statement a chance even if they don’t participate in enough extracurricular activities.

   If an applicant meets the cutoff point for GPA and personal statement score, but not the extracurricular activity count, the function should return the string:

   ```
   "This applicant should be given an in-person interview."
   ```

   ```
   def applicant_selector(gpa, ps_score, ec_count):
   	if gpa >= 3.0 and ps_score >= 90 and ec_count >= 3:
   		return "This applicant should be accepted."
   	elif gpa >= 3.0 and ps_score >= 90 and ec_count < 3:
   		return "This applicant should be given an in-person interview."
   ```

3. Finally, for all other cases, the function should return the string:

   ```
   "This applicant should be rejected."
   ```

   ```
   def applicant_selector(gpa, ps_score, ec_count):
   	if gpa >= 3.0 and ps_score >= 90 and ec_count >= 3:
   		return "This applicant should be accepted."
   	elif gpa >= 3.0 and ps_score >= 90 and ec_count < 3:
   		return "This applicant should be given an in-person interview."
   	else:
   		return "This applicant should be rejected."
   ```
