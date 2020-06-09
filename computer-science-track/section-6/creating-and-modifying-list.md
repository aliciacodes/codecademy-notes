# What is a list?

A *list* is an ordered set of objects. This is specific to Python, not all languages have the same definition.

Think about ordering people by oldest to youngest in a college classroom.

- Paige is 28 years old.
- Cristine is 20 years old.
- Ben is 25 years old.
- James is 18 years old.

In Python, you create the variable `ages` to store the numbers:

```
ages = [28, 20, 25, 18]
```

How to Form A List:

1. It begins with an opening bracket `[`and ends with a square bracket `]`.
2. Each item is separated by a comma (`,`)
3.  To make it more readable, a (` `) should be inserted after the comma. You don't have to, but it does make it easier.

<u>Activity</u>

1. A new student added the class:

   - Arizona is 23

   Add Arizona's age to the end of the list `ages`

   ```
   # broken_ages = [28 20 25 18]
   ages = [28, 20, 25, 18, 23]
   ```

2. Remove the `#` in front of the definition of the list `broken_heights`. If you run this code, you’ll get an error:

   ```
   SyntaxError: invalid syntax
   ```

   Add commas (`,`) to `broken_ages` so that it runs without errors.

```
broken_ages = [28, 20, 25, 18]
```

# List II

Lists can contain more than numbers, there can be strings, floats, ints, and more. 

We can make a list of strings that have all the student's names who are in the class

```
names = ['Paige', 'Cristine', 'Ben', 'James', 'Arizona']
```

There can be multiple data types on one list.

```
list_mixed = ['James', 18]
```



<u>Activity</u>

1. Add any string to the list `ints_and_strings`.

   ```
   ints_and_strings = [1, 2, 3, 'four', 'five', 'six']
   ```

2. Create a new list called `sam_height` that contains:

   - The string `'Sam'`
   - The number `67`

   ```
   sam_height = ['Sam', 67]
   ```

   

# Lists of Lists

Lists can have strings and ints, but they can also contain lists as well. 

Age Example:

- Paige is 28 years old.
- Cristine is 20 years old.
- Ben is 25 years old.
- James is 18 years old.

We can create a list that has just James' age in it:

```
james = ['James', 18]
```

We can put several of the lists into one list to represent the student's name and age.

```
age = [['Paige',28], ['Ben', 25], ['James', 18], ['Cristine', 20]]
```

<u>Activity</u>

1. A new student named `'Nessa'` has added the class. Nessa is `21` years old. Add a sublist to `age` that represents Nessa and her age.

   ```
   age = [['Paige',28], ['Ben', 25], ['James', 18], ['Cristine', 20], ['Nessa', 21]]
   ```

2. Create a list of lists called `eye color` where each sublist contains a student’s name and their eye color. Use the following data:

   - `'Alex'` has `hazel eyes`
   - `'Sai'` has `brown eyes`

   ```
   eye_color = [['Alex', 'hazel'], ['Sai', 'brown']]
   ```

   

# Zip

Age Example:

- Paige is 28 years old.
- Cristine is 20 years old.
- Ben is 25 years old.
- James is 18 years old.

We only have a list of names and ages:

```
names = ['Paige', 'Cristine', 'Ben', 'James']
ages = [28, 20, 25, 18]
```

If we want to create a list of lists pairing the respective names with their ages, we can use the command `zip`. 

`zip` can take two (or more) lists as inputs and returns an object that contains a list of pairs. Each pair contains one element from each input. 

You can't print this, it will return a location in memory

```
names_and_heights = zip(names, heights)
print(names_and_heights)
<zip object at 0x7f1631e86b48>
```

To see nested lists, convert the zip object to a list first.

```
print(list(names_and_heights))
```

returns:

```
[('Paige', 28), ('Cristine', 20), ('Ben', 25), ('James', 18)]
```

<u>Activity:</u>

1. Use `zip` to create a new variable called `names_and_dogs_names` that combines `names` and `dogs_names` into a `zip` object.

   Make sure to run the code for this step before proceeding to the next instruction!

   ```
   names = ['Jenny', 'Alexus', 'Sam', 'Grace']
   dogs_names = ['Elphonse', 'Dr. Doggy DDS', 'Carter', 'Ralph']
   
   names_and_dogs_names = zip(names, dogs_names)
   ```

2. Create a new variable named `list_of_names_and_dogs_names` by calling `list()` on `names_and_dogs_names`. Print this new variable .

   ```
   list_of_names_and_dogs_names = list(names_and_dogs_names)
   print(list_of_names_and_dogs_names)
   ```

   

# Empty Lists

A list doesn't have to contain anything. Initialize an empty list like this:

```
empty_list = []
```

We create empty lists when we plan on filling it later based on other input. 

<u>Activity</u>

1. Create an empty list and call it `my_empty_list`.

```
my_empty_list = []
```



# Growing a List: Append

We can add to a list using `.append()`. Let's look at the `empty_list`.

```
empty_list = []
```

Add the element `1` using the following commands:

```
empty_list.append(1)
```

If we print the `empty_list`, it now contains `1`.

```
>>> print(empty_list)
[1]
```

When a list has items, new elements are added to the **end** of the list.

```
empty_list.append(4)
empty_list.append(2)
print(empty_list)
```

The output is:

```
[1, 4, 2]
```

The function `.append()` comes **after** the name of the list. It's different from functions like `print` that come before. 

<u>Activity</u>

1. Jiho works for a gardening store called Petal Power. He keeps a record of orders in a list called `orders`.

   Use `print` to inspect the orders he has received today.

   ```
   orders = ['daisies', 'periwinkle']
   print(orders)
   ```

2. Jiho just received a new order for `'tulips'`. Use `append` to add this string to `orders`.

   ```
   orders.append('tulips')
   ```

3. Another order has come in! Use `append` to add `'roses'` to `orders`.

   ```
   orders.append('roses')
   ```

4. Use `print` to inspect the `orders` Jiho has received today.

   ```
   print(orders)
   ```

   

# Growing a List: Plus (+)

When there are multiple items to be added to a list, use `+` to combine two lists. 

Below, there are a list of `cats` that are in a rescue shelter.

```
cat = ['Oreo', 'Peanuts', 'Rocky']
```

Two new kittens arrive into the shelter and they are named `Sunny` and `Shadow`.

```
>>> cats_in_shelter = cat + ['Sunny', 'Shadow']
>>> print(cats_in_shelter)
['Oreo', 'Peanuts', 'Rocky', 'Sunny', 'Shadow']
```

 A new variable `cats_in_shelter` which contains the original items sold and new ones. It does not change the original `cat` array.  

```
print(cat)
```

We can only use `+` with already created lists.

```
my_list = [1, 2, 3]
my_list + 4
```

We will get the following error:

```
TypeError: can only concatenate list (not "int") to list
```

We want to add a single element using `+` , we have to put it into a list with brackets (`[]`):

```
my_list + [4]
```

<u>Activity</u>

1. Jiho is still updating his list of `orders`. He just received orders for `'lilac'` and `'iris'`.

   Use `+` to create a new list called `new_orders` that combines `orders` with the two new orders.

   ```
   new_orders = orders + ['lilac','iris']
   ```

   

2. Remove the `#` in front of the list `broken_prices`. If you run this code, you’ll get an error:

   ```
   TypeError: can only concatenate list (not "int") to list
   ```

   Fix the command by inserting brackets (`[` and `]`) so that it will run without errors.

   ```
   # broken_prices = [5, 3, 4, 5, 4] + 4
   broken_prices =  [5, 3, 4, 5, 4] + [4]
   ```

   

# Range I

Sometimes, we need a list of consecutive numbers. (ex. Need a list between numbers 0-9)

```
a_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Typing this all out takes times and more numbers that are written, the more likely there is a typo.

Python gives an easy way of creating lists using a function called `range`. 

`Range` takes a single input and generates numbers starting at `0` and ending at the number inputted subtracted by 1. 

```
up_to_9 = range(10)
```

The range function returns an object that can be turned into a list.

```
>>> print(up_to_9)
range(0, 10)
>>> print(list(up_to_9))
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

<u>Activity</u>

```
list1 = range(3)
```

1. Modify `list1` so that it is a range containing numbers starting at 0 and up to, but not including, 9.

   ```
   list1 = range(9)
   ```

2. Create a range called `list2` with the numbers 0 through 7.

   ```
   list2 = range(8)
   ```

   

# Range II

Range creates lists that start at `0` when there is only a single argument.

With two arguments, you can decide where the list starts and where it ends. If there are two numbers, there will be a list of consecutive numbers between the two. 

```
>>> a_list = range(-1, 8)
>>> print(list(a_list))
[-1, 0, 1, 2, 3, 4, 5, 6, 7]
```

With three arguments, we get a list that "skips" every nth number.

```
>>> a_range = range(1, 10, 3)
>>> print(list(a_range))
[1, 4, 7]
```

 We can skip as many numbers as we want.

<u>Activity</u>

```
list1 = range(5, 15, 2)
```



1. Modify the `range` function that created `list1` such that it:
   - Starts at `5`
   - Has a difference of `3` between each item
   - Ends **before** `15`

```
list1 = range(5, 15, 3)
```

2. Create a range object called `list2` that:
   - Starts at `0`
   - Has a difference of `5` between each item
   - Ends **before** `40`

```
list2 = range(0, 40, 5)
```



# Review

This section was about

- instantiating lists with data and empty lists.
- create a list of list using `zip`
- Adding to a list with `.append()` or `+`
- Use `range` to create  a list of integers



<u>Activity</u>

1. Maria is entering customer data for her web design business. You’re going to help her organize her data.

   Start by turning this list of customer first names into a list called `first_names`. Make sure to enter the names in this order:

   - Ainsley
   - Ben
   - Chani
   - Depak

```
first_names = ['Ainsley', 'Ben', 'Chani', 'Depak']
```

2. Create an empty list called `age`.

```
age = []
```

3. Depak’s age is `42`. Use `.append()` to add `42` to `age`.

```
age.append(42)
```

4. Maria needs a list of the ages for all customers. Create a new list called `all_ages` that adds `age` with the following list, containing the ages for Ainsley, Ben, and Chani:

```
[32, 41, 29]
```

Make sure `all_ages` begins with the ages for Ainsley, Ben, and Chani and ends with Depak’s age (stored in `age`).

```
all_ages = [32, 41, 29] + age
```

5. Create a new variable called `name_and_age` that combines `first_names` and `all_ages` using `zip`.

```
name_and_age = zip(first_names, all_ages)
```

6. Create a range object called `ids` with an id number for each customer. Since there are 4 customers, so id values should go from `0` to `3`.

```
ids = range(0,4)
```



Python Lists:

Which of these commands would create a list of numbers starting at `0` and up to (but not including) `9`?

```
list(range(9))
```



Which of the following would create a range object that starts at `3`, goes up to but not including `15` where each number is `4` greater than the previous number?

```
range(3, 15, 4)
```



How could we add `['Hawaii', 'Alaska']` to the list `states`?

```
states = states + ['Hawaii', 'Alaska']
```



What list would be created by this command: `list(range(2, 14, 4))`?

```
[2, 6, 10]
```



What would be the output of the following code snippet?

```
string1 = "The quick brown" 
string2 = "fox jumps over" 
string3 = string1+string2 
print(string3 +" the lazy dog.")
```

```
The quick brownfox jumps over the lazy dog.
```



Which of the following is the correct way to create the following list of names: `'Tom'`, `'Jerry'`, `'Tweetie'`, `'Sylvester'`?

```
names = ['Tom', 'Jerry', 'Tweetie', 'Sylvester']
```



Which of the following is the correct way to add the number `4` to `mylist`?

```
mylist.append(4)
```



Is the following list a valid Python list?

`mylist = ['Mount Everest', 29029]`

Yes, lists can contain multiple data types.



Which of the following is the correct way to create an empty list?

empty_list = []
