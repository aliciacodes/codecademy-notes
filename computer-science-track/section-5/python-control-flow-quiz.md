1. Determine the truth value of the following expressions:
    ```
    #A: 
    4 * 5 <= 21 - 1
				
    #B: 
    18 + 6 > 9 * 3
    ```
    Answer:
    A: True
    B: False
2. Read the following code carefully. What will happen when the code is executed?
```
def simple_conditional(x):
  if x = 0:
    print("x is equal to zero.")
  elif x >= 0:
    print("x is greater than zero.")
  else:
    print("x is less than zero.")

simple_conditional(0)
```
There will be a SyntaxError since `=` is not relational operator. 

3. Determine the truth value of the following expressions:
    ```
    #A: 
    (4 <= 2 * 3) and (7 + 1 == 8)
				
    #B: 
    (12 > 6 * 2) or ( 7 >= 3 + 4) #First is False, second is True
    ```
    Answer:
    A: True
    B: True

4. What will the code below print when it is executed?
    ```
    def divide_two_numbers(x, y):
        result = x / y
        return result

    try:
        result = divide_two_numbers(2,0)
        print(result)
    except NameError:
        print("A NameError occurred.")
    except ValueError:
        print("A ValueError occurred.") 
    except ZeroDivisionError:
        print("A ZeroDivisionError occurred.")
    ```
    Answer:
    A ZeroDivisionError Occured.

5. Consider the code below. What would this print to the terminal?
    ```
    def print_something(x):
        if x <= 2:
            print("This is printed")
        if x <= 4:
            print("This is also printed")
        if x <= 6:
            print("Is this printed?")
        if x <= 8:
            print("This might be printed.")

    print_something(5)
    ```
    Answer: 
    Is this printed?
    This might be printed.

6. Which of the following is a Boolean expression?
    Answer: My name is Angelo
    Not Boolean: The quiz is hard, Three is most elegant number, NY Yankees are the classiest baseball team.

7. Which of the following variables contains a Boolean value?
    Answer: `my_cool_variable` = 7 + 8 != 13
    Not Correct: 
    `my_fun_variable = 2 + 9`
    `my_super_variable = "True" + "False"`
    `my_chill_variable = "This is True."`

8.  Determine the truth value of the following expressions:
    ```
    # A: 
    3 ** 2 + 1 != 30 / 3

    # B: 
    (9 - 4) * 2 == 77 / 7 - 1
    ```
    Answer: 
    A: False
    B: True