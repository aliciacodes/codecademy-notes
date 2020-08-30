# Modules

### Modules Python Introduction

When programming, you should reuse as much code as you can whether that be for ourselves or even for other programmers. 

Python makes this easy by allowing developers to easily share code that the community can use as a tool. These tools are called **modules** which are sometimes also referred to as "libraries" or "packages". Packages are typically a directory to hold a collection of modules. 

This is the basic syntax you need to import a module.

```
from module_name import object_name
```

Modules can include a lot of code that may slow down your program or conflict with existing code so you must import only what you need. 

The `datetime` module is a popular module that lets you work with dates and times. This comes  with the Python Standard Library.



Instructions:

1. In *script.py* import the `datetime` type from the `datetime` library.

```
from datetime import datetime
```

2. Create a variable `current_time` and set it equal to `datetime.now()`.

```
current_time = datetime.now()
```

3. Print out `current_time`.

```
print(current_time)
```

#### Modules Python Random

Another commonly used Python module is `random` which can generate numbers or select items at random. 

To use more than one module, you can syntactically write it like this:

```
import random
```

Two common random functions are:

`random.choice()` takes a list of arguments and returns a number from the list

`random.randint()` takes two numbers as arguments and generates a random number inclusively between the two numbers passed in. 

Instructions:

1.  In **script.py** import the `random` library.

```
import random
```

2. Create a variable `random_list` and set it equal to an empty list

```
random_list = []
```

3. Turn the empty list into a list comprehension that uses `random.randint()` to generate a random integer between 1 and 100 (inclusive) for each number in `range(101)`.

```
random_list = [random.randint(1,101) for i in range(101)]
```

4. Create a new variable `randomer_number` and set it equal to `random.choice()` with `random_list` as an argument.

```
randomer_number = random.choice(random_list)
```

5. Print `randomer_number` out to see what number was picked!

```
print(randomer_number)
```

#### Modules Python Namespaces

When we invoke the `randint()` function why do we need to invoke `random`? This is a default behavior where Python gives a default name to a module called a *namespace*. This namespace isolates functions, classes, and variables defined in the module from the rest of the code. 

This name can be altered by *aliasing* using the `as` keyword. Aliasing is mostly done when the library's name is long.

```
import module_name as name_you_pick_for_the_module
```

When you encounter an `import *` this is a wildcard and matches anything and everything. This is considered to be dangerous since it can pollute the namespace which is when the same name applies to two possible things. ex. You happen to have a `floor()` function focused on floor tiles using `from math import *` would also import a function `floor()` that rounds down floats. 

In the following exercises, you will use a function from the random library called `random.sample`. It takes a range and a number as input, and as output produces a specified number of random numbers from that range. 

Instructions

1. Below `import codecademylib3_seaborn`, import `pyplot` from the module `matplotlib` with the alias `plt`.

```
import codecademylib3_seaborn
from matplotlib import pyplot as plt
```

2. Import `random` below the other import statements. It’s best to keep all imports at the top of your file.

```
import random
```

3. Create a variable `numbers_a` and set it equal to the range of numbers 1 through 12 (inclusive).

```
numbers_a =  range(1, 13)
```

4. Create a variable `numbers_b` and set it equal to a random sample of twelve numbers within `range(1000)`.

```
numbers_b = random.sample(range(1000), 12)
```

5. Now let’s plot these number sets against each other using `plt`. Call `plt.plot()` with your two variables as its arguments.

```
plt.plot(numbers_a, numbers_b)
```

6. Now call `plt.show()` and run your code!

   You should see a graph of random numbers displayed. You’ve used two Python modules to accomplish this (`random` and `matplotlib`).

```
plt.show()
```



**Modules Python Decimals**

What do you do when you are writing software that handles decimal values. When you use the built-in Python library for [floating-point arithmetic](https://en.wikipedia.org/wiki/Floating-point_arithmetic) to calculate sums, it is oddly formatted.

```
pen_cost = 0.35
pencil_cost = 0.10

amazon_cost = pen_cost + pencil_cost
#Returns 0.44999999999999996
```

In Python, there can be rounding errors when you use a data type that performs decimal arithmetic accurately. You can use the decimal module to do this!

```
from decimal import Decimal
pen_cost = Decimal('0.35')
pencil_cost = Decimal('0.10')

amazon_cost = pen_cost + pencil_cost
#Returns 0.45 instead of 0.44999999999999996
```

The `decimal` module's `Decimal` data type adds 0.10 with 0.35 and this data type deals with the accuracy errors.



Modules can provide functions or data types we can use to solve a general problem so we can focus on specific problems in our software!

<u>Activity</u>

1. Run your code to see the weird floating point math that occurs.

```
# Import Decimal below:

# Fix the floating point math below:
two_decimal_points = 0.2 + 0.69
print(two_decimal_points) #Returns 0.8899999999999999

four_decimal_points = 0.53 * 0.65
print(four_decimal_points) #Returns 0.34450000000000003
```

2. Import `Decimal` from the `decimal` module.

```
from decimal import Decimal
```

3. Use `Decimal` to make `two_decimal_points` only have two decimals points and `four_decimal_points` to only have four decimal points.

```
# Import Decimal below:
from decimal import Decimal

# Fix the floating point math below:
two_decimal_points = Decimal('0.2') + Decimal('0.69')
print(two_decimal_points)

four_decimal_points = Decimal('0.53') * Decimal('0.65')
print(four_decimal_points)
```



**Modules Python Files and Scope**

Scope: If variables are defined *inside* a function, it will not be accessible *outside* of it. This also applies to classes and files. Even files inside the same directory cannot reference each other's function, classes, or anything else. So how do you access these methods.

**Files are modules** so you can give a file access to everything in another using the `import` statement. An example of this is using the import statement: `from fruit_names import fruit_names` at the top of **fruit.py** to get the names of every fruit. 

Activity

1. Tab over to **library.py** and define a function `always_three()` with no parameters that returns 3.

```
#library.py
def always_three():
	return 3
```

2. Call your `always_three()` function in script.py. Check out that error message you get in the output terminal and the consequences of file scope.

```
#script.py

always_three()
#Error in terminal:   File "script.py", line 4, in <module>
    always_three()
NameError: name 'always_three' is not defined
```

3. Resolve the error with an import statement at the top of **script.py** that imports your function from `library`. Run your code and watch `import` do its magic!

```
#script.py
from library import always_three

always_three()
```



**Modules Python Review**

What was learned: 

- what modules are and how they can be useful
- how to use a few of the most commonly used Python libraries
- what namespaces are and how to avoid polluting your local namespace
- how scope works for files in Python

As a programmer, you should no reinvent the wheel and modules allow you to use code that's already been created. This lesson used some of the Python Standard Library, but there are many more that come packaged with Python. 

Using a package manager like (pip3 or conda) you can install any module available on the Python Package index. 

